# Logs

Logs from the investigation. They are evidence for [the report](../README.md).

## Privacy

These files were cleaned before upload. Serial numbers, MAC addresses, Wi-Fi names, SIM IDs and private IP addresses were replaced with `XXXX`.
Large logs were filtered to fingerprint related lines. The full raw logs stay private.
Check your own logs before you upload them. See [CONTRIBUTING.md](../CONTRIBUTING.md).

## Bigger bundle

`fp-logs-filtered.zip` is on the Releases page. It holds the larger logs, filtered and cleaned.

## How to read the key lines

```
setEnrollSession BAuth_Control_OP fail : 38
common_prepare Fail : 38
recovery_mode fail : 38
m_active_group -1
enroll gid != m_active_group -1, 0
```

The HAL calls the Trusted App. The call succeeds. The Trusted App returns `38`.
Then the HAL has no active group and rejects enrollment.
The lines with `fail : 38` are in `fp21.txt` and `fp11_boot.txt`.

Harmless lines: `onUiReady unsupported in HIDL` and `setIgnoreDisplayTouches unsupported in HIDL`.

## Index

Dates are 2026-11-09 and 2026-11-10. The descriptions come from the file contents.

| File | What it holds |
| --- | --- |
| dump_fp.txt | Fingerprint service dump: provider, counters, HAL deaths |
| fp5_dmesg_touch.txt | Kernel log while touching the sensor (`fod_enable`, `etspi`) |
| fp7.txt | Init and service start log. Shows services that could not be found |
| fp8.txt | Logcat after boot, with `PHH-Enroll` lines |
| fp9_dmesg.txt | Kernel log, filtered |
| fp10_dmesg.txt | Kernel log from one test run |
| fp11_boot.txt | Boot log with the `fail : 38` lines |
| fp12.txt | `/dev/esfp0` and the fingerprint sysfs attributes |
| fp13.txt | Kernel messages around suspend and resume, with `etspi` |
| fp13_b.txt | Same kind of log in dmesg format |
| fp14.txt | `/efs` listing with SELinux labels |
| fp15.txt | Strings from the fingerprint HAL (Egis storage paths, error text) |
| fp16.txt | Kernel and logcat lines from one test run |
| fp17.txt | Device tree property names of the sensor node |
| fp18.txt | Regulator and `gpio-160` state |
| fp19.txt | Regulator summary. `VDD_BTP_3P3` is 3300 mV |
| fp20.txt | Trace event groups and trace setup |
| fp21.txt | Logcat during an enrollment attempt, with the `fail : 38` lines |
| fp22.txt | Build and boot properties |
| fp23.txt | Kernel config lines for TZDEV |
| fp24.txt, fp24_b.txt | Vendor properties and file attributes of the HAL files |

Related: [vendor structure](../docs/vendor_structure.md).
