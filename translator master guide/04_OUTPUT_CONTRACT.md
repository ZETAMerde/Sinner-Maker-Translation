# Output contract

Each unit JSON has a `strings` array. The only field you write is `translation`, inside your folder under `languages/`.

Chinese starts filled: `languages/zh/` copies the current official Chinese into `translation` so you can revise it. Russian, German, Italian, Korean, Japanese, Polish, and Arabic start with `translation` empty.

```json
{
  "id": "door/sinners/Angela.dialogue#1",
  "english": "[#anxious_hands]hey, uhm, I was actually looking for someone",
  "spanish": "[#anxious_hands]Oye, ehm, en realidad estaba buscando a alguien.",
  "chinese": "[#anxious_hands]嘿，嗯……其实我在找一个人。",
  "translation": ""
}
```

Tags in that example stay with the line. Your `translation` keeps the tags from `english`. The sentence uses the normal writing of your language.

## Fields you must not change

`id`, `english`, `lookup_english`, `spanish`, `chinese`, `style`, `casing_rule`, `speaker`, `source`, `channel`, `voice_hint`, `prev_english`, `next_english`, `placeholders`, `import_target`, `wired`, `copy_exactly`, `notes`, `source_line`, `reference_note`.

`prev_english` and `next_english` are the neighbouring lines in that file. Use them. The whole file is the conversation.

`reference_note` appears only when the Spanish or Chinese tags differ from `english`.

## Where each unit is imported later

This pack does not change the game. A later import writes your `translation` into the per-language copies of:

- `locale/official_<locale>/dialogue.csv`
- `locale/official_<locale>/script_lines.csv`
- `locale/official_<locale>/ui_scenes.csv`
- `locale/official_<locale>/ui_scripts.csv`
- `locale/official_<locale>/ui_core.csv`
- `locale/official_<locale>/resources.csv`
- `data/dialogue_library/lines_<locale>.json`
- `data/talk_about/lines_<locale>.json` and the locale block in `pronouns.json`

`import_target` on each row names the file. `<locale>` is your language code.

Dialogue Manager looks lines up by the English text with `[#tags]` stripped. Keep the tags in `translation` anyway.

Rows with `wired` false are still required. They are spoken or shown, but a CSV may not be read for them yet.

## Checks

- Every id from this pack still exists in `languages/<code>/units/`.
- `translation` is non-empty when `english` has words.
- `copy_exactly` rows match `english` exactly.
- `[#tags]`, `{{}}`, `{name}`, `%s`, and `%d` from `placeholders` still appear in `translation`.
- Variant pools keep the same number of `|` separators.
- Tags come from `english`, including when the Spanish reference uses a different tag.
- `translation` contains no long dash.
