# How the game speaks

Write in the normal orthography of the target language. The English sinner lines are lowercase and often have no final period. That shape is the source text. It is not a spelling rule for your language.

Official Spanish uses normal written Spanish: a capital, opening `¿` or `¡` when the language wants them, and a final period. The Angela knock is `[#anxious_hands]Oye, ehm, en realidad estaba buscando a alguien.`

Official Chinese is colloquial Simplified Chinese with full-width punctuation. The same knock is `[#anxious_hands]嘿，嗯……其实我在找一个人。`

Use your language the same way. Do not copy the English lowercase shape. Do not copy the retired rule that forbade capitals and final periods.

## Tags, pools, placeholders

Copy every `[#tag]` from `english`. Tags choose the animation. If `reference_note` says the Spanish or Chinese tags differ, keep the tags on `english`. The reference strings stay verbatim so you can see the choice.

`[[[#tag]line one|#tag]line two]]]` is one random pool. Translate each variant. Keep every `[#tag]`, every `|`, and the same number of variants.

Keep `{{placeholders}}`, `{name}`, `%s`, `%d`, `%%`, and BBCode. Named placeholders may move to fit word order. Spell every token exactly. Percent placeholders stay in the same order.

Do not use a long dash. A comma, an ellipsis, or your language's normal pause is enough. Chinese uses `，`, `……`, or `～` where a long dash would have sat.

A line that is only `...` stays `...`. `copy_exactly` rows set `translation` equal to `english`.

## Menus and items

Buttons and short labels are short and direct. Spanish shouts some of them (`EMPEZAR`, `ATRÁS`, `VOLVER`, `Menú METRO`). Chinese uses ordinary simplified labels (`开始`). Follow the menu habit of the target language. Do not copy Spanish capitals into `translation`.

Item descriptions, studies, laws, and trait text are clear sentences. Periods are allowed. Forbidden Bible pages are a rough diary. Keep the swagger.

Scene button keys sometimes have padding spaces (`     OK     `). That padding is the lookup key. Do not change `english`.

## People and gender

Tarot lines are spoken by any sinner. Avoid wording that locks the speaker to one gender unless the line names a man or a woman.

Named women: Angela, Matilde, Lilith, Lizbeth, Marilou. Named men: Mario, Isaiah, Soren, Caesar, Gabriel. If the glossary does not state a gender, do not invent one.

Talk-about lines insert `{subj}`, `{obj}`, `{name}` after translation. Write so the line still works for every pronoun set. `pronouns.json` has the shipped sets, including Chinese 她 / 他 / TA. Add one block for the target language and use it everywhere.

## Voice

Post-rapture colony. Demons happened. Heaven took the rest. The player is the priest. Sinners call them chief. Faith is real, and so is swearing, lust, panic, and dark jokes. Do not turn a line into a sermon, and do not sand it into a joke that forgot the rapture.

Tarot is the voice, not a costume. The glossary lists each card and each named speaker. Enemy-tier lines are uglier. Friendship does not change the card. It changes how much they let the priest in.
