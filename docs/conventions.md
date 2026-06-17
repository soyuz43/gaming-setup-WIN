# Conventions

## Filenames

Use lowercase, stable, hyphen-separated identifiers where practical.

Examples:

- `halo-combat-evolved.json`
- `burnout-3-takedown.toml`
- `max-payne-3.ini`

Exact media filenames should be recorded inside metadata rather than copied
into every repository filename.

## Status Values

Suggested title statuses:

- `untested`
- `testing`
- `playable`
- `imperfect`
- `blocked`
- `retired`

## Local Files

Machine-specific records should end in `.local.*` and remain outside Git.

## Structured Data

- TSV files use one header row and literal tab separators.
- JSON files must remain valid JSON.
- Unknown values remain empty or `null`.
- Detailed prose belongs in Markdown rather than table cells.
