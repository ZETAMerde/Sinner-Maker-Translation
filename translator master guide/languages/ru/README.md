# Русский

This worksheet is empty on purpose. The game has no Russian translation yet. `translation` is empty on every row. Fill it.

The current Chinese text is only in `languages/zh/`. Do not look for it here.

## What to do

1. Read `00_INSTRUCTIONS.md`, `01_STYLE.md`, `02_GLOSSARY.md`, and `03_OFFICIAL_CHOICES.md` in the parent folder before any string.
2. Edit the JSON files under `units/` in this folder. The paths match the parent `units/` folder.
3. Fill `translation` from `english`. `spanish` and `chinese` show how those languages handled the line. Write Russian.
4. Leave every other field unchanged.
5. Do not reorder strings. Do not drop ids. Do not add strings.

## How to write

- Use the normal orthography of Russian. Do not copy the English lowercase shape.
- Sinner speech is rough, spoken, and direct. The glossary lists the voices.
- Copy `[#tags]` from `english`.
- Keep placeholders, pools, and the same variant count.
- No long dash.
- `copy_exactly` rows must set `translation` equal to `english`.
- Every row whose `english` has words needs a non-empty `translation`.
