# Galaxy A505f In-Display Fingerprint on Android 16 GSI (LineageOS 23.2)

**Status:** Investigation closed. FOD UI works. Enrollment does NOT work.
**Device:** Samsung Galaxy A50 (SM-A505F/DS, codename `a50dd`, Exynos 9610)
**Sensor:** Egis ET713 (optical, in-display)
**Author:** ibralyam (Telegram: t.me/ibralyam)

---

## 1. Summary

- The FOD icon and FOD screen can be made to show up with a vendor overlay.
- Touching the sensor area is detected as a FOD touch.
- Fingerprint enrollment fails. The Samsung HAL returns error `38`.
- Sensor power, reset and TrustZone communication are all fine.
- Swapping the vendor to `f4vendor.img` did not help. It also broke Hotspot and Bluetooth.
- Final decision: stay on `A505f-vendor.img` and stop working on FOD for AOSP.
- This matches what the A50 community has seen for years: no AOSP-based ROM has working fingerprint on this phone.

---

## 2. Test Setup

| Item | Value |
|---|---|
| ROM | LineageOS 23.2 GSI (Android 16, SDK 36) |
| Vendor (final) | `A505f-vendor.img` (A505FDDS9CUK1, Android 11 base, SDK 30) |
| Vendor (tested) | `f4vendor.img` (A505FDDS9CVA4, SDK 31) |
| Kernel | Mint Beta 1413 (4.14.194, AOSP A12 permissive, KSU variant) |
| Patch (system) | 2026-08-01 |
| SELinux | Permissive |
| Verified boot | green |
| Tools | Termux (root), TWRP 3.7.0_9-0 |

---

## 3. What Works

1. System boots normally.
2. Settings shows a normal fingerprint menu (after the overlay fix).
3. FOD icon area is detected on touch.
4. Fingerprint HAL starts and stays alive.
5. Sensor power rail and reset pin behave correctly.

## 4. What Does Not Work

1. Enrollment. It stays stuck and never completes.
2. Unlock with fingerprint (nothing can be enrolled).

---

## 5. Fix That Worked: FOD UI Overlay

**Problem:** Settings showed "rear sensor" text. No FOD icon. No enroll screen.

**Cause:** The framework value `config_udfps_sensor_props` is empty in `framework-res.apk`. Android does not know where the in-display sensor is.

**Fix:** A static overlay APK in `/vendor/overlay`.

- Target package: `android`
- Static: `android:isStatic="true"`, priority 999
- Value: `config_udfps_sensor_props` = `x, y, radius`
- Values used (guess, not calibrated): `540, 1950, 95`

**Result:** The FOD UI appears. Touch on the sensor area is seen as FOD.

**Install steps (root):**
```
mount -o rw,remount /vendor
mkdir -p /vendor/overlay
cp A50Udfps.apk /vendor/overlay/
chmod 644 /vendor/overlay/A50Udfps.apk
chcon u:object_r:vendor_file:s0 /vendor/overlay/A50Udfps.apk
```

**Note:** This only fixes the UI. It does not fix enrollment. It was NOT added to the flashable ROM zip.

---

## 6. Architecture of the Fingerprint Stack

```
Settings / SystemUI
        |
Android 16 framework (HIDL 2.1 -> AIDL adapter)
        |
vendor.samsung.hardware.biometrics.fingerprint@2.1-service.a50
  (libbauthserver.so, libbauthtzcommon.so, libteecl.so)
        |
/dev/tzdev  (tzdaemon, tzts_daemon)
        |
TEEGRIS Trusted App
  /vendor/tee/00000000-0000-0000-0000-46494e474502
        |
Egis ET713 sensor (secure access through TrustZone)
```

Extra service for FOD:
`vendor.lineage.biometrics.fingerprint.inscreen@1.0-service.a50`
(uses `/sys/class/sec/tsp/cmd fod_enable`).

Kernel driver: `egis_fingerprint` (`etspi,et7xx`, device `/dev/esfp0`).

---

## 7. The Error

Key log lines:

```
setEnrollSession BAuth_Control_OP fail : 38
common_prepare Fail : 38
recovery_mode fail : 38
m_active_group -1
enroll gid != m_active_group -1, 0
```

Also:

- `type_check.dat` contains `Fail`. It comes back after deletion.
- Driver prints `etspi_work_func_debug ... type: failed`.
- Expected HIDL messages (harmless): `onUiReady unsupported in HIDL`, `setIgnoreDisplayTouches unsupported in HIDL`.

Meaning: the HAL talks to the Trusted App. The call succeeds. The Trusted App itself returns result `38`. Then the HAL has no active group and rejects enrollment.

---

## 8. What Was Checked (and Ruled Out)

| Check | Result |
|---|---|
| Sensor regulator `VDD_BTP_3P3` (3.3V) | OK |
| Reset GPIO (gpio-160) timing | OK |
| Pinctrl states | OK |
| Kernel SPI events | None (sensor is behind TrustZone) |
| `tlc_communicate` return codes | All `TEEC_SUCCESS` |
| Trusted App present in vendor | Yes |
| SELinux | Permissive. Not the cause |
| `/data/vendor/biometrics` permissions | OK |
| Delete `type_check.dat`, `calib.dat`, `switch` | No effect |
| System properties | HAL reads almost none |
| Different vendor (`f4vendor.img`) | No fix. Broke Hotspot and Bluetooth |

---

## 9. Open Hypothesis (Not Proven)

Mint 1413 kernel config has:

```
CONFIG_PROCA=y
CONFIG_FIVE=y
CONFIG_FIVE_TEE_DRIVER=y
CONFIG_FIVE_USE_TZDEV=y
CONFIG_TZDEV=y
CONFIG_TEEGRIS_VERSION=2
```

Idea: Samsung PROCA/FIVE may check the caller binary signature (xattr `security.pa` / `security.five`). The HAL in the vendor images has only `security.selinux`. The Trusted App may then refuse the HAL, giving error `38`.

Status: **not confirmed and not refuted.** A test needs a kernel build with PROCA/FIVE disabled. No build environment was available (phone and Termux only).

---

## 10. Vendor Comparison

| | A505f-vendor.img | f4vendor.img |
|---|---|---|
| Fingerprint HAL | `...@2.1-service.a50` | `...@3.0-service` |
| TA label | `vendor_file` | `tee_file` |
| Build | A505FDDS9CUK1 | A505FDDS9CVA4 |
| SDK | 30 | 31 |
| Enroll | Fails (38) | Not tested (side effects) |
| Hotspot | Works | Broken |
| Bluetooth | Works | Crashes |

Decision: use `A505f-vendor.img`.

---

## 11. Useful Facts

- Sensor position sysfs: `13.77,0.00,7.29,7.29,14.80,14.80,12.00,12.00,5.00`
- DT chip ID: ET713. Model info: A505.
- Stock Samsung ROM + stock kernel: fingerprint works.
- Stock Samsung vendor + Quantum Kernel on GSI is listed as working on the Treble wiki. Not reproduced here.

---

## 12. Termux / Toybox Notes

- `getfattr` has no `-m` option.
- `pkill -f` inside `su -c` kills its own shell. Use `kill $(pidof name)`.
- Kernel logs: `logcat -b kernel -d`. The ring buffer rolls fast. Capture right after boot.
- Tracefs is at `/sys/kernel/tracing`.
- For long root scripts: `su -c 'sh /data/data/com.termux/files/home/script.sh'`.
- `aapt2` in Termux may need `pkg upgrade -y`.

---

## 13. Conclusion

- FOD UI: fixed with the overlay.
- Enrollment: blocked by TrustZone error `38`.
- Not caused by hardware, power, SELinux, cache files, or the vendor image.
- Only open lead: PROCA/FIVE in the kernel. It needs a custom kernel build.
- Project decision: stay on `A505f-vendor.img`. Stop FOD work on AOSP ROMs. Ship the ROM without fingerprint support.

## 14. Known Issue Text (for ROM post)

> Fingerprint (in-display) does not work. This is a known A50 limitation on AOSP-based ROMs.
> Use PIN, pattern or password.

---

## 15. Credits

- ibralyam: testing, vendor, kernel and GSI supply
- Mint Kernel developers
- Samsung et7xx driver authors
- LineageOS team
