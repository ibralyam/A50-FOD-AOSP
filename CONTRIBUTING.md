# Contributing

This project looks for a way to make the in-display fingerprint (Egis ET713) work on AOSP ROMs for the Galaxy A50.
The investigation is closed, but one lead is still open. Any new test result helps, even a failed one.

## What helps most

1. A test of the open lead. See [docs/PROCA_FIVE_TEST_PLAN.md](docs/PROCA_FIVE_TEST_PLAN.md).
2. A result on another vendor, kernel or ROM. Say exactly what you used.
3. A check of the overlay values. The current values are a guess.
4. A log from a stock Samsung ROM that shows how the Trusted App is called when enrollment works.

## Send a test report

Open an issue with the "Test report" template. Include:

- Device and model (for example SM-A505F)
- ROM name, version and Android version
- Vendor image name and build (for example A505FDDS9CUK1)
- Kernel name and version, and whether SELinux is permissive
- What you changed
- What you expected
- What happened
- The key log lines (look for `BAuth_Control_OP fail`)

## Before you upload a log

Logs can hold private data. Check these first:

- Serial numbers (`ro.serialno`, `ro.boot.serialno`, `ap_serial`)
- IMEI and phone numbers
- Wi-Fi names and MAC addresses
- Account names and email addresses

Remove or replace them with `XXXX`.

## Rules

- Say clearly what is tested and what is a guess.
- Do not post copies of Samsung binaries or keys. Link to where you got them.
- Be kind. This is a hobby project.

## Contact

Telegram: https://t.me/ibralyam
