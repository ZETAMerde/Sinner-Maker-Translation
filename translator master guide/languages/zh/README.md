# 简体中文

This is the Chinese worksheet. `translation` already holds the current official Simplified Chinese from the game. Revise that text. The other language folders start empty. This one does not.

## What to do

1. Read `00_INSTRUCTIONS.md`, `01_STYLE.md`, `02_GLOSSARY.md`, and `03_OFFICIAL_CHOICES.md` in the parent folder before any string.
2. Edit the JSON files under `units/` in this folder. The paths match the parent `units/` folder.
3. Change `translation` only.
4. `chinese` on the same row is the original official line. After you edit `translation`, `chinese` still shows what shipped.
5. Where `chinese` is empty, `translation` is empty. Write that line.
6. Where the line is already right, leave `translation` as it is.
7. Do not reorder strings. Do not drop ids. Do not add strings.

## How to revise

- Keep the sense of `english`, the speaker in `voice_hint`, and the neighbours `prev_english` and `next_english`.
- Keep `[#tags]` from `english`. If `reference_note` says the current Chinese tags differ, fix the tags on `translation` so they match `english`.
- Keep placeholders, pools, and the same variant count.
- Colloquial Simplified Chinese, full-width punctuation. No long dash. Use `，`, `……`, or `～`.
- `copy_exactly` rows must set `translation` equal to `english`.

Every row whose `english` has words needs a non-empty `translation` when you are done.
