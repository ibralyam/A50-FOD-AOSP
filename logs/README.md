# Logs

Raw logs from the investigation. They are here as evidence.

## Before you use them

- Check for private data before you upload new logs. See [CONTRIBUTING.md](../CONTRIBUTING.md).
- Large files are better as release assets than as repo files.

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

## Harmless lines

- `onUiReady unsupported in HIDL`
- `setIgnoreDisplayTouches unsupported in HIDL`

## Index

Add one line for each log you upload:

| File | What it shows |
| --- | --- |
| (add files here) | |
