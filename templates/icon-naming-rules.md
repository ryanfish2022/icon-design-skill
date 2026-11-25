# Icon naming and inventory rules

Use lowercase kebab-case and semantic names (use `download`, not `arrow-thing`).

Pattern: `name[-style][-state][-size].ext`

Examples:
- `download-outline-24.svg`
- `download-filled-24.svg`
- `sync-disabled-24.svg`
- `launcher-clay-1024.png`

Keep identifiers stable across revisions; use Git history for versioning. Separate distinct families into directories. Maintain a manifest with:
- id
- label
- category
- function and metaphor
- variant and size
- filename
- style-contract version
- QA status

Do not imply multiple sizes or variants exist unless they were actually exported.
