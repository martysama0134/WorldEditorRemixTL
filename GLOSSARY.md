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
- `domain`: UI context (`ui`, `tool`, `menu`, `dialog`, `status`).
- `notes`: constraints and edge-case guidance.

## Style Rules
- Prefer tool/action wording in UI labels.
- Keep technical placeholders and symbols unchanged: `%d`, `%s`, `\n`, `\t`, `&`, `""`.
- Keep product/proper names unchanged: `WorldEditor`, `ReMIX`.
- Keep technical terms in English only when domain-standard in this project.

## Canonical Mappings
| term_id | en | it | domain | notes |
| --- | --- | --- | --- | --- |
| eraser_tool | eraser | Cancella | tool | Tool/action context; avoid `gomma` for this meaning. |
| reset | reset | Reimposta | ui | Use for reset actions across dialogs/buttons. |
| unselect | unselect | Deseleziona | ui | Use for deselection actions. |
| hierarchy_current_area | Hierarchy (Current Area) | Gerarchia (area corrente) | dialog | Keep area qualifier in parentheses. |
| rmouse_teleport_object | RMouseClick = Teleport to Object | Click destro = teletrasporta all'oggetto | dialog | Preserve equation-style hint format. |
| scan_new_obj | Scan New Obj | Scansiona nuovo oggetto | tool | Expand `Obj` to `oggetto`. |
| water_output | Water Output | Output acqua | ui | Keep `Output` as accepted technical noun. |
| picking | picking | picking | tool | Keep in English by default as domain term. |

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
