# Recovery

This document will describe how to reconstruct the managed gaming environment.

## Recovery Order

1. Restore the repository.
2. Recreate the expected directory structure.
3. Install emulator applications.
4. Restore permitted configuration files.
5. Restore ReShade presets and installation records.
6. Reconnect large assets stored outside Git.
7. Validate paths, controllers, renderers, and per-title overrides.

## Local Archive Location

Expected local recovery archive root:

`E:/!BACKUP/gaming-setup-WIN`

Archives on the same physical drive provide protection against accidental
changes, but not complete drive failure.
