# What the official translations changed

The October 8 pack told translators to redo Spanish from scratch and to keep sinner speech lowercase with no final period. The official Spanish and Chinese shipped on October 11 replace that rule. This file records what those files actually did.

## Speech

Spanish uses sentence capitals and periods. 4,748 of 5,180 dialogue rows start with a capital or with `¿` / `¡`. 2,659 end with a period. Chinese uses `。？！，……～` and no long dash.

The Angela knock in Spanish is `[#anxious_hands]Oye, ehm, en realidad estaba buscando a alguien.` In Chinese it is `[#anxious_hands]嘿，嗯……其实我在找一个人。`

## Menus

Menu voice stays punchy where the author already set it.

- Start = EMPEZAR / 开始
- Back = ATRÁS
- Go BACK = VOLVER
- Metro Menu = Menú METRO

## Terms

Locked terms, used the same way every time:

- chief = jefe / 首领
- sinner = pecador / 罪人
- village = pueblo / 村庄
- plaza = plaza / 广场
- church = iglesia / 教堂
- faith = fe / 信仰
- candle = vela / 蜡烛
- sin orb = orbe de pecado / 罪孽宝珠
- The Fool = El Loco / 愚者
- The Hanged Man = El Ahorcado / 倒吊人
- The Lovers = El Enamorado / 恋人
- Strength = La Templanza in the Spanish card name, 力量 in Chinese

`La Templanza` is the Temperance name. Translate the English card Strength. Chinese `力量` is the match. The Spanish string stays in the unit so you can see what shipped.

## Tags

Copy `[#tags]` from the live English line. They drive the animation. Spanish changed the tag on 761 dialogue rows (`[#dislike]` became `[#head_shake]`, and similar). Chinese tag text matches its own English column. When `reference_note` is present, keep the tags on `english`.

## Coverage you can lean on

`script_lines` matches on all 2,650 English lines in both languages. Dialogue-library paths are 606/606/606. Talk-about paths are 121/121/121.

Dialogue text: 154 unique Spanish lines have no Chinese twin, and every unique Chinese dialogue line has a Spanish twin. Join dialogue on the words, after tags are stripped. Do not join on the CSV key. `Isaiah:4` is a different sentence in each file. About 835 shared keys disagree, mostly because Spanish retagged the line and Chinese kept the older tag.

`ui_scripts`: 341 Spanish rows have no Chinese. `ui_scenes`: 140. `resources`: match by key, then by English, because 160 Spanish English strings and 124 Chinese English strings do not line up.

An empty `spanish` or `chinese` means that official file has no line for this English. Translate from `english` and from whichever reference is present.

## New homes

These were not finished in the October 8 sheet. They ship now.

- `locale/official_<locale>/script_lines.csv` for lines spoken from GDScript
- `data/dialogue_library/lines_<locale>.json`
- `data/talk_about/lines_<locale>.json` and the locale block in `pronouns.json`
- `verbatim/` for credits whose English casing must stay exact

`manifest.json` in this folder counts how many live lines received each reference when the guide was built.
