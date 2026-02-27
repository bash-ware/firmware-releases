# Bashware Firmware Releases

Central repository for compiled firmware binaries used by the Bashware Updater app.

## Structure

```
firmware-releases/
├── manifest.json          # Device registry with latest versions
└── firmware/              # Compiled .hex files
    ├── MCKnob_v1.0.0.hex
    ├── MicroMidi_v2.0.1.hex
    └── ...
```

## manifest.json

The Electron updater app fetches this file to know which firmware versions are available.

Each device entry contains:
- `pid` — USB Product ID
- `latest` — Latest firmware version string
- `file` — Path to the .hex file
- `date` — Upload date
- `reportsVersion` — Whether the device can report its firmware version via serial

## Devices

| Device | PID | Status |
|--------|-----|--------|
| MCKnob | 9209 | Active |
| MicroMidi | 920a | Active |
| CKnob | 920b | Active |
| VAYU | 920c | Active |
