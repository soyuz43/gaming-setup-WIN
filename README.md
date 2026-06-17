# gaming-setup-WIN

Windows gaming environment metadata, configuration, inventory, and recovery records.

This repository documents the gaming environment and preserves small, durable configuration files. It does not store game media, emulator binaries, firmware, or other large runtime assets.

## Related Repositories

- `BashScripts-WIN` — bootstrap, installation, maintenance, and automation scripts.
- `dotfiles-WIN` — development environment configuration.

`gaming-setup-WIN` stores gaming-specific metadata and configuration.

## Scope

### Included

- Emulator configuration files
- Per-title configuration overrides
- Game and emulator metadata
- Compatibility and troubleshooting notes
- ReShade presets and installation records
- Inventory manifests
- Recovery documentation
- Configuration templates

### Excluded

- Game media (`ISO`, `XISO`, `ROM`, `XBE`, `XEX`, `CHD`, etc.)
- Emulator executables and libraries
- BIOS, firmware, encryption keys, and virtual disks
- Save data and runtime caches
- Screenshots, recordings, and generated archives
- Credentials, tokens, and private keys

## Repository Layout

```
docs/        Documentation, conventions, and recovery procedures
emulators/   Emulator-specific configuration and metadata
manifests/   Inventory and installation records
reshade/     ReShade presets and installation records
templates/   Structured record templates
```

## Data Categories

| Category | Purpose |
|---|---|
| Configuration | Files consumed by emulators or graphics tools |
| Metadata | Structured information about games and installations |
| Inventory | Records of what is installed and where it exists |
| Recovery | Procedures required to rebuild or repair the environment |

## Current Status

Managed environments:

- xemu (Original Xbox)

Planned support:

- Xenia (Xbox 360)
- Additional emulators as required