# UDFPS Overlay

`A50Udfps.apk` is a small static overlay. It makes the FOD UI appear on Android 16.

## What it does

- Sets `config_udfps_sensor_props` in the `android` framework package.
- Without this value, Settings shows "rear sensor" text, and there is no FOD icon or enroll screen.
- With it, the FOD UI appears and a touch on the sensor area is seen as a FOD touch.

| Item | Value |
| --- | --- |
| Target package | `android` |
| Static | `android:isStatic="true"` |
| Priority | 999 |
| Value | `x, y, radius` = `540, 1950, 95` |

The values are a guess. They are not calibrated.

## What it does not do

It does not fix enrollment. Enrollment still fails with TrustZone error `38`.
The overlay is not part of the flashable ROM zips.

## Install (root)

```
mount -o rw,remount /vendor
mkdir -p /vendor/overlay
cp A50Udfps.apk /vendor/overlay/
chmod 644 /vendor/overlay/A50Udfps.apk
chcon u:object_r:vendor_file:s0 /vendor/overlay/A50Udfps.apk
```

Reboot after you copy it.

## Test environment

LineageOS 23.2 GSI (Android 16), vendor `A505f-vendor.img`, Mint Beta 1413 kernel, SELinux permissive.
Other ROMs are not tested.

## Remove it

```
mount -o rw,remount /vendor
rm /vendor/overlay/A50Udfps.apk
```

## Help calibrate

Try other `x, y, radius` values and report what changes. See [CONTRIBUTING.md](../CONTRIBUTING.md).

## SHA-256

Add the checksum of the APK here:

```
sha256sum A50Udfps.apk
```
