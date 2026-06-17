# gaming-setup-WIN

Personal source of truth for the metadata, configurations, presets, inventories, and recovery notes that define my Windows gaming environment.

This repository records how the environment is organized and configured. It does not store game media, emulator distributions, firmware, or other large runtime assets.

## Purpose

My development environment is divided between two existing repositories:

* `BashScripts-WIN` provides bootstrap, installation, maintenance, and command-line automation.
* `dotfiles-WIN` stores managed development-environment configuration.

`gaming-setup-WIN` applies the same source-of-truth principle to gaming software without expanding either existing repository beyond its intended responsibility.

The repository is intended to answer questions such as:

* Which emulators are installed?
* Where are their live installations located?
* Which configuration files are worth preserving?
* Which games use per-title emulator settings?
* Which games use ReShade?
* Which ReShade preset belongs to each installation?
* Which files are required to reconstruct the setup?
* Which generated or copyrighted files must remain outside Git?
* Where should local recovery archives be written?

## Scope

This repository may contain:

* Emulator configuration files
* Per-title emulator overrides
* Title metadata
* File hashes for personally managed media
* Emulator and game compatibility notes
* ReShade presets
* ReShade installation records
* Path and inventory manifests
* Recovery procedures
* Configuration templates
* Future metadata-management and backup helpers

This repository must not contain:

* ISO, XISO, ROM, XBE, XEX, CHD, or other game media
* BIOS, firmware, encryption keys, or proprietary system files
* Emulator executables or DLLs
* Virtual hard disks
* Save files
* Shader caches
* Screenshots or captured video
* Download archives
* Generated backup archives
* Credentials, tokens, or private keys

## Repository Relationships

### BashScripts-WIN

`BashScripts-WIN` remains responsible for general-purpose commands, bootstrap operations, and reusable shell automation.

A future command such as `gamebackup`, `gameinventory`, or `genconfigs` may be exposed through `BashScripts-WIN`, but gaming-specific metadata and templates belong here.

### dotfiles-WIN

`dotfiles-WIN` remains responsible for the development environment:

* Git Bash
* Git
* WSL
* VS Code
* Windows Terminal

Gaming configuration is intentionally kept separate.

## Source of Truth and Live State

The repository is the source of truth for small, durable, human-maintained records.

The live gaming environment remains under locations such as:

* `E:/Video_Games`
* `E:/Video_Games/Emulators`
* Individual native-game installation directories

Generated local recovery archives may later be written to:

* `E:/!BACKUP/gaming-setup-WIN`

Because the live files and that backup directory may reside on the same physical drive, those archives provide local recovery rather than protection against complete drive failure.

GitHub provides an additional off-machine copy of the metadata and configuration stored in this repository.

## Directory Layout

### `docs/`

Architecture notes, naming conventions, recovery procedures, and decisions affecting the repository as a whole.

### `emulators/`

Configuration and metadata organized by emulator.

Each emulator directory may contain:

* A README describing the live installation
* Preserved global or per-title configurations
* Per-title metadata
* Recovery notes

It must not contain emulator binaries, game media, BIOS files, or virtual disks.

### `manifests/`

Tab-separated inventories describing emulators, games, ReShade installations, paths, and backup targets.

Machine-specific records should use filenames ending in `.local.tsv` and remain untracked.

### `reshade/`

ReShade presets and records showing which games, executables, rendering APIs, and presets belong together.

ReShade binaries, downloaded shader packages, and game executables are excluded.

### `templates/`

Reusable starting points for title metadata, emulator notes, and future structured records.

## Data Model

The repository distinguishes between four kinds of information:

1. **Configuration**
   Files consumed directly by an emulator or graphics tool.

2. **Metadata**
   Structured records describing titles, formats, hashes, status, and relationships.

3. **Inventory**
   Tables describing what is installed and where it lives.

4. **Recovery knowledge**
   Human-readable instructions required to reconstruct or repair the setup.

These categories should remain separate even when they describe the same game or emulator.

## Naming

Repository filenames should prefer stable names over display names containing excessive region and language tags.

A title record may preserve the exact media filename internally while using a shorter stable identifier for configuration and metadata filenames.

Example:

* Display title: `Halo - Combat Evolved`
* Media filename: `Halo - Combat Evolved (USA) (Rev 2).xiso.iso`
* Metadata file: `halo-combat-evolved.json`
* Config file: `halo-combat-evolved.toml`

## Workflow

The initial workflow is deliberately manual:

1. Add an emulator README when an emulator becomes part of the managed setup.
2. Record it in `manifests/emulators.tsv`.
3. Add title metadata only when it provides useful information.
4. Preserve a per-title config only when the title genuinely requires an override.
5. Record ReShade installations when they are deliberately configured.
6. Commit meaningful changes with descriptive messages.

Automation should be added only after repeated manual work exposes a stable operation worth scripting.

## Public Repository Hygiene

This repository may be public.

Before committing:

* Review files for usernames, credentials, tokens, and personal identifiers.
* Do not commit proprietary game or system content.
* Keep machine-specific path records in ignored `.local.*` files where appropriate.
* Confirm that archives and large generated files remain excluded.
* Review `git diff --staged` before every push.

## Current Status

Initial structure only.

The first managed target is expected to be the xemu installation under the Xbox emulator directory. Xenia and ReShade records will be added as those setups become active.
