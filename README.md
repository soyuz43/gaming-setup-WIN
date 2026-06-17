# gaming-setup-WIN

Windows gaming environment metadata, configuration records, inventories, and recovery documentation.

This repository preserves the configuration and organizational data required to maintain and reconstruct the gaming environment. It does not contain game media, emulator binaries, firmware, save data, or other large runtime assets.

## Related Repositories

- [BashScripts-WIN](https://github.com/soyuz43/BashScripts-Win)  
  Bootstrap scripts, automation, installation, and maintenance workflows.

- [dotfiles-WIN](https://github.com/soyuz43/dotfiles-WIN)  
  Development environment configuration for Git Bash, Git, WSL, VS Code, and Windows Terminal.

## Included

- Emulator configuration files
- Per-title emulator overrides
- Emulator and game metadata
- Compatibility and troubleshooting notes
- ReShade presets and installation records
- Inventory manifests
- Recovery documentation
- Configuration templates

## Excluded

- Game media (`ISO`, `XISO`, `ROM`, `XBE`, `XEX`, `CHD`, etc.)
- Emulator executables, libraries, BIOS, firmware, and virtual disks
- Save files, caches, screenshots, and recordings
- Download archives and generated backups
- Credentials, tokens, and private keys

## Repository Layout

```
docs/        Repository documentation, conventions, and recovery procedures
emulators/   Emulator-specific configuration and metadata
manifests/   Inventory and installation records
reshade/     ReShade presets and installation records
templates/   Structured record templates
```

## Managed Platforms

Current:
- Original Xbox (`xemu`)

Planned:
- Xbox 360 (`Xenia`)
- Additional emulators as required