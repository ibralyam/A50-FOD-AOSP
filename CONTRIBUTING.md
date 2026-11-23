# Contributing

Any new test helps, even a failed one. The matrix in [README.md](README.md) grows with each result.

## What helps most

1. A test of the open lead. See [docs/PROCA_FIVE_TEST_PLAN.md](docs/PROCA_FIVE_TEST_PLAN.md).
2. The same vendor and kernel on a different ROM. This shows if the ROM matters.
3. A different vendor or kernel on the same ROM.
4. Calibrated overlay values. The current ones are a guess.
5. A log from a stock Samsung ROM where enrollment works.

## Add a test

1. Copy `results/TEMPLATE.md` to `results/<rom>-<version>-a<android>/README.md`.
   Example: `results/pixelos-16.2-a16/README.md`.
2. Fill in every section.
3. Put small cleaned logs in `results/<folder>/logs/`.
4. Put big logs on a release, named after the ROM, for example `logs-pixelos-16.2.zip`.
5. Add a row to the matrix in `README.md`.
6. Open a pull request, or open an issue with the Test report template.

One folder for each combination of ROM, Android version, vendor, and kernel. A change in any of them can change the result.

## Files from a ROM or a vendor

Do not upload framework-res, vendor binaries, or other ROM files again for each test.
Write the path on the device and the SHA-256. Upload only small files that you need to explain a result.

## Before you upload a log

Logs can hold private data. Check these first:

- Serial numbers (`ro.serialno`, `ro.boot.serialno`, `ap_serial`) and `ro.boot.em.did`
- IMEI, ICCID, IMSI and phone numbers
- MAC addresses and BSSID
- Wi-Fi names (SSID)
- Private IP addresses
- Account names and email addresses

Replace them with `XXXX`. Filter large logs to fingerprint lines.

## Rules

- Say clearly what is tested and what is a guess.
- Do not copy Samsung keys or private files. Link to where you got them.
- Be kind. This is a hobby project.

## Contact

Telegram: https://t.me/ibralyam
