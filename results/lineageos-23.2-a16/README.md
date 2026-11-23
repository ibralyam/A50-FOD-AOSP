# LineageOS 23.2 (Android 16 GSI)

Tester: ibralyam
Date: 2026-11-09 to 2026-11-10

**Result:** Closed. The FOD UI works. Enrollment fails with Trusted App error `38`.

Full report: [docs/INVESTIGATION.md](../../docs/INVESTIGATION.md)

## Setup

| Item | Value |
| --- | --- |
| ROM | LineageOS 23.2 GSI |
| Android / SDK | 16 / 36 |
| Vendor (final) | `A505f-vendor.img`, A505FDDS9CUK1, Android 11 base, SDK 30 |
| Vendor (tested) | `f4vendor.img`, A505FDDS9CVA4, SDK 31 |
| Kernel | Mint Beta 1413 (4.14.194, AOSP A12, KSU variant), SELinux permissive |
| Security patch | 2026-08-01 |
| Verified boot state | green |
| Tools | Termux (root), TWRP 3.7.0_9-0 |

## What was changed

- A static overlay in `/vendor/overlay` that sets `config_udfps_sensor_props` to `540, 1950, 95`.
  The values are a guess, not calibrated. See [overlay/README.md](../../overlay/README.md).
- Vendor tested: `f4vendor.img`. It did not help and it broke Hotspot and Bluetooth.

## What works

- The system boots.
- Settings shows a normal fingerprint menu (after the overlay).
- The FOD area is detected on touch.
- The fingerprint HAL starts and stays alive.
- Sensor power and reset behave correctly.

## What does not work

- Enrollment never completes.
- Unlock by fingerprint, because nothing can be enrolled.

## Key log lines

```
setEnrollSession BAuth_Control_OP fail : 38
common_prepare Fail : 38
recovery_mode fail : 38
m_active_group -1
```

## Checks

| Check | Result |
| --- | --- |
| Fingerprint menu in Settings | Works, after the overlay |
| FOD icon and enroll screen | Appear, after the overlay |
| Touch on the sensor | Detected |
| HAL starts and stays alive | Yes |
| Enrollment completes | No |
| Error code | 38, from the Trusted App |

## Files

- Cleaned logs: [logs/](logs/README.md)
- Big logs: release asset `fp-logs-filtered.zip`
- Device overlays for comparison: release asset `device-overlays.zip`
- `framework-res.apk` from the GSI: not uploaded. Path `/system/framework/framework-res.apk`, SHA-256 `be508796a106a9af9fe78e49239ad023c6cadfebdd6585d17635fa1f69042a37` on the test device.

## Conclusion

The HAL talks to the Trusted App, and the Trusted App returns `38`. Power, reset, SELinux, cache files, and the vendor swap were ruled out.
The open lead is PROCA and FIVE in the kernel. See [docs/PROCA_FIVE_TEST_PLAN.md](../../docs/PROCA_FIVE_TEST_PLAN.md).
