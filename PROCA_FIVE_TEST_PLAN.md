# Test Plan: PROCA and FIVE

This is the one open lead. It is not confirmed and not refuted.

## The idea

The Mint 1413 kernel has these options:

```
CONFIG_PROCA=y
CONFIG_FIVE=y
CONFIG_FIVE_TEE_DRIVER=y
CONFIG_FIVE_USE_TZDEV=y
CONFIG_TZDEV=y
CONFIG_TEEGRIS_VERSION=2
```

Samsung PROCA and FIVE may check the signature of the calling binary. The check uses the extended attributes `security.pa` and `security.five`.
The fingerprint HAL in the vendor images only has `security.selinux`.
The Trusted App may then refuse the HAL and return error `38`.

## What a test needs

- A kernel build with PROCA and FIVE turned off.
- A build environment. The author only had a phone and Termux.

## Steps

1. Get the Mint kernel source for the A50.
2. Turn off `CONFIG_PROCA` and `CONFIG_FIVE`. Check what else depends on them.
3. Build and flash the kernel.
4. Boot the ROM with the overlay installed.
5. Try fingerprint enrollment.
6. Capture the log right after the attempt. The kernel ring buffer rolls fast.
7. Report the result.

## What to look for

- Does the phone still boot? The Trusted App or other services may depend on these options.
- Does error `38` change or go away?
- Does `type_check.dat` still say `Fail`?

## Useful commands

```
logcat -b kernel -d
getfattr -d /vendor/bin/hw/<fingerprint HAL binary>
```

`getfattr` in toybox has no `-m` option.
Use `kill $(pidof name)` and not `pkill -f` inside `su -c`.

## Report

Open an issue with the Test report template. Say that it is a PROCA/FIVE test.

## Risk

You can get a bootloop. Keep a working kernel and TWRP ready.
