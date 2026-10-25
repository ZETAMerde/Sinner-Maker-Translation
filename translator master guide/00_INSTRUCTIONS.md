# Translator master guide

You are translating Sinner Maker from English into your language. The reader of your output is a person who will import `translation` back into the game. Write for that import.

`spanish` and `chinese` are finished official translations. They show the meaning, the tone, and the terms. They are not drafts. Your worksheet is `languages/<code>/`. Fill or revise `translation` there. Leave every other field unchanged.

## Where your language lives

- `languages/zh/`: 简体中文. `translation` already holds the current official Chinese. Revise it. Read `languages/zh/README.md`.
- `languages/ru/`: Русский. `translation` is empty on every row.
- `languages/de/`: Deutsch. `translation` is empty on every row.
- `languages/it/`: Italiano. `translation` is empty on every row.
- `languages/ko/`: 한국어. `translation` is empty on every row.
- `languages/ja/`: 日本語. `translation` is empty on every row.
- `languages/pl/`: Polski. `translation` is empty on every row.
- `languages/ar/`: العربية. `translation` is empty on every row.

The root `units/` folder is the shared English source. Do not edit it. Do not put your work in `translated/`.

## What to do

1. Read `01_STYLE.md`, `02_GLOSSARY.md`, `03_OFFICIAL_CHOICES.md`, and the README in your language folder before any string.
2. Walk every JSON file under `languages/<code>/units/`. `manifest.json` lists the same relative paths. Do not skip a file.
3. Fill or revise `translation` on every object inside `strings`. Leave every other field unchanged.
4. Save the file where it is. Example: `languages/ko/units/dialogue/door/sinners/Angela.json`.
5. Do not reorder strings. Do not drop ids. Do not add strings.

## Work in this order

Inside your language folder, in this order:

1. `units/ui_core/`
2. `units/ui_scenes/` and `units/ui_scripts/`
3. `units/dialogue/` one conversation file at a time, so a later line still fits the earlier one
4. `units/dialogue_library/`
5. `units/talk_about/` including `pronouns.json`
6. `units/gdscript_spoken/` and `units/localize_gaps/`
7. `units/resources/`
8. `units/unwired.json` and `units/ui_scripts/display_tables.json`

Translate a whole conversation file before the next one.

## Do not translate

- `id`, `source`, file names, JSON keys
- `[#tags]` such as `[#serious]` and `[#head_shake]`. Copy the tags from `english`.
- `[[[` `]]]` and the `|` between variants
- `{{placeholders}}`, `{name}` `{subj}` `{obj}` `{poss}` `{ref}` `{friend}` `{sinner_name}` and any other `{word}` token
- `%s` `%d` `%%` in the same order
- `[if ...]` conditions if one appears in `notes`
- Proper names listed in the glossary

`lookup_english` is metadata for the later import. Do not edit it. `spanish` and `chinese` stay as shipped.

## Empty translation

Every row whose `english` has words needs a non-empty `translation`. `copy_exactly` rows must set `translation` equal to `english`.
