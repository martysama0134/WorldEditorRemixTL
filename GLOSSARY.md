# WorldEditor Multilingual Glossary

## Scope And Usage
- This file is the terminology source of truth for WorldEditor UI translations.
- Current rollout includes `en` and `it`; add new language columns over time (`de`, `fr`, etc.).
- Use this glossary together with `AGENTS.md` (process rules, encoding, path escaping, validation).
- If a term conflicts with older text, this glossary takes precedence unless explicitly overridden.

## Canonical Schema
- `term_id`: stable key for automation and reviews.
- `en`: canonical source text.
- `it`: canonical Italian translation.
- `it_compact`: compact Italian label for constrained controls.
- `domain`: UI context (`ui`, `tool`, `menu`, `dialog`, `status`).
- `notes`: constraints and edge-case guidance.
- `compact_rule`: when compact form is allowed.

## Style Rules
- Prefer tool/action wording in UI labels.
- Keep technical placeholders and symbols unchanged: `%d`, `%s`, `\n`, `\t`, `&`, `""`.
- Keep product/proper names unchanged: `WorldEditor`, `ReMIX`.
- Keep technical terms in English only when domain-standard in this project.

## Canonical Mappings
| term_id | en | it | it_compact | domain | notes | compact_rule |
| --- | --- | --- | --- | --- | --- | --- |
| eraser_tool | eraser | Cancella | Canc. | tool | Tool/action context; avoid `gomma` for this meaning. | Use compact only if control is constrained and EN is shorter. |
| reset | reset | Reimposta | Reimp. | ui | Use for reset actions across dialogs/buttons. | Use compact only if control is constrained and EN is shorter. |
| unselect | unselect | Deseleziona | Desel. | ui | Use for deselection actions. | Use compact only if control is constrained and EN is shorter. |
| hierarchy_current_area | Hierarchy (Current Area) | Gerarchia (area corrente) | Gerarchia (area corr.) | dialog | Keep area qualifier in parentheses. | Use compact only if control is constrained and EN is shorter. |
| rmouse_teleport_object | RMouseClick = Teleport to Object | Click destro = teletrasporta all'oggetto | Click dx = teletrasp. all'ogg. | dialog | Preserve equation-style hint format. | Use compact only if control is constrained and EN is shorter. |
| scan_new_obj | Scan New Obj | Scansiona nuovo oggetto | Scans. nuovo ogg. | tool | Expand `Obj` to `oggetto` in full form. | Use compact only if control is constrained and EN is shorter. |
| water_output | Water Output | Output acqua | Out. acqua | ui | Keep `Output` as accepted technical noun. | Use compact only if control is constrained and EN is shorter. |
| picking | picking | picking | picking | tool | Keep in English by default as domain term. | Compact not needed by default. |
| rotation | rotation | rotazione | rotaz. | ui | Use for rotation labels in controls and hints. | Use compact only if control is constrained and EN is shorter. |
| object | object | oggetto | ogg. | ui | Use for object labels and actions. | Use compact only if control is constrained and EN is shorter. |
| height | height | altezza | alt. | ui | Translate `Height` to `Altezza` as default. | Use compact only if control is constrained and EN is shorter. |

## Do / Don't Examples
- Do: `Reimposta rotazione`
- Do: `Reimposta altezza`
- Do: `Deseleziona picking`
- Don't: `Gomma` for the erase tool label
- Don't: mixed-language phrasing when a canonical mapping exists

## Extending To New Languages
- Add one column per language (for example `de`, `fr`, `es`) without changing existing `term_id`.
- Fill translations progressively; do not remove old mappings.
- Update `notes` when terminology decisions evolve.
