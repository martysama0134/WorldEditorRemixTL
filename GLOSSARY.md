# WorldEditor Multilingual Glossary

## Scope And Usage
- This file is the terminology source of truth for WorldEditor UI translations.
- Current rollout includes `en`, `it`, `de`; `fr` is now active and future columns can be added over time (`es`, `pt`, etc.).
- Use this glossary together with `AGENTS.md` (process rules, encoding, path escaping, validation).
- If a term conflicts with older text, this glossary takes precedence unless explicitly overridden.
- German (`de`/`de_compact`) entries must use canonical umlaut-bearing forms (cp1252-safe), not lossy placeholders like `?`.

## Canonical Schema
- `term_id`: stable key for automation and reviews.
- `en`: canonical source text.
- `it`: canonical Italian translation.
- `it_compact`: compact Italian label for constrained controls.
- `de`: canonical German translation.
- `de_compact`: compact German label for constrained controls.
- `fr`: canonical French translation.
- `fr_compact`: compact French label for constrained controls.
- `domain`: UI context (`ui`, `tool`, `menu`, `dialog`, `status`).
- `notes`: constraints and edge-case guidance.
- `compact_rule`: when compact form is allowed.

## Style Rules
- Prefer tool/action wording in UI labels.
- Keep technical placeholders and symbols unchanged: `%d`, `%s`, `\n`, `\t`, `&`, `""`.
- Keep product/proper names unchanged: `WorldEditor`, `ReMIX`.
- Keep technical terms in English only when domain-standard in this project.

## Canonical Mappings
| term_id | en | it | it_compact | de | de_compact | fr | fr_compact | domain | notes | compact_rule |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| eraser_tool | eraser | Cancella | Canc. | Löschen | Lösch. | Effacer | Eff. | tool | Tool/action context; avoid physical-eraser wording in both IT and DE. | Use compact only if control is constrained and EN is shorter. |
| reset | reset | Reimposta | Reimp. | Zurücksetzen | Zurücks. | Réinitialiser | Réinit. | ui | Use for reset actions across dialogs/buttons. | Use compact only if control is constrained and EN is shorter. |
| unselect | unselect | Deseleziona | Desel. | Abwählen | Abw. | Désélectionner | Désél. | ui | Use for deselection actions. | Use compact only if control is constrained and EN is shorter. |
| hierarchy_current_area | Hierarchy (Current Area) | Gerarchia (area corrente) | Gerarchia (area corr.) | Hierarchie (aktueller Bereich) | Hierarchie (akt. Bereich) | Hiérarchie (zone actuelle) | Hiérarchie (zone act.) | dialog | Keep area qualifier in parentheses. | Use compact only if control is constrained and EN is shorter. |
| rmouse_teleport_object | RMouseClick = Teleport to Object | Click destro = teletrasporta all'oggetto | Click dx = teletrasp. all'ogg. | Rechtsklick = Teleport zum Objekt | Rechtsklick = Teleport z. Obj. | Clic droit = téléport vers l'objet | Clic dr. = téléport obj. | dialog | Preserve equation-style hint format. | Use compact only if control is constrained and EN is shorter. |
| scan_new_obj | Scan New Obj | Scansiona nuovo oggetto | Scan nuovo ogg | Neues Objekt scannen | Obj. scan | Scanner nouvel objet | Scan nv obj. | tool | Expand `Obj` for full IT/DE forms; edge-case compact kept for narrow controls. | Use compact only if control is constrained and EN is shorter. |
| water_output | Water Output | Output acqua | Acqua Out. | Wasserausgabe | Wasser Out. | Sortie eau | Eau Out. | ui | Accepted output noun with compact override for narrow controls. | Use compact only if control is constrained and EN is shorter. |
| picking | picking | picking | picking | Picking | Picking | picking | picking | tool | Keep in English by default as domain term. | Compact not needed by default. |
| rotation | rotation | rotazione | rotaz. | Rotation | Rot. | rotation | rot. | ui | Use for rotation labels in controls and hints. | Use compact only if control is constrained and EN is shorter. |
| object | object | oggetto | ogg. | Objekt | Obj. | objet | obj. | ui | Use for object labels and actions. | Use compact only if control is constrained and EN is shorter. |
| height | height | altezza | altezza | Höhe | Höh. | hauteur | haut. | ui | Translate `Height` to local language by default; edge-case compact allowed in constrained controls. | Use compact only if control is constrained and EN is shorter. |
| add_texture | Add texture | Aggiungi texture | Agg. texture | Textur hinzufügen | Tex. hinzuf. | Ajouter texture | Ajout tex. | tool | Texture add action label. | Use compact only if control is constrained and EN is shorter. |
| terrain_output | Terrain Output | Output terreno | Terreno Out. | Terrainausgabe | Terrain Out. | Sortie terrain | Terrain Out. | ui | Future-facing mapping if `Terrain Output` appears in UI. | Use compact only if control is constrained and EN is shorter. |
| light_position_edit | Modif.LucePos | Modifica posizione luce | Mod. Luce Pos | Lichtposition bearbeiten | LichtPos. mod. | Modifier position lumière | Mod. pos. lumi. | tool | Legacy token preserved in EN source; edge-case compact DE spacing differs intentionally. | Use compact only if control is constrained and EN is shorter. |
| brush_shape | Brush Shape | Forma Pennello | Forma Penn. | Pinselform | Pinsel Form | Forme pinceau | Forme pinc. | ui | Brush form label; edge-case spaced compact kept for constrained UI readability. | Use compact only if control is constrained and EN is shorter. |
| meter | Meter | Metri | Metri | Meter | Meter | Mètre | Mètre | status | Unit label in coordinate/size panels. | Compact not needed. |
| brush_shape_circle | Brush Shape Circle | Forma Cerchio | Forma Cerch. | Pinselform Kreis | Pinsel Form Kreis | Forme pinceau cercle | Forme cercle | ui | Edge case from old DE wording where compound can exceed small control widths. | Use compact only if control is constrained and EN is shorter. |
| brush_shape_square | Brush Shape Square | Forma Quadrato | Forma Quad. | Pinselform Quadrat | Pinsel Form Quadrat | Forme pinceau carré | Forme carré | ui | Edge case from old DE wording where compound can exceed small control widths. | Use compact only if control is constrained and EN is shorter. |
| height_brush | Height Brush | Pennello Altezza | Penn. Alt. | Höhenpinsel | Höhenpins. | Pinceau hauteur | Pinc. haut. | ui | Panel title for height brush controls. | Use compact only if control is constrained and EN is shorter. |
| height_base | Height Base | Base Altezza | Base Alt. | Höhenbasis | Höh.basis | Base hauteur | Base haut. | ui | Short groupbox label in map object panel. | Use compact only if control is constrained and EN is shorter. |
| adjust_all_water_height | Adjust All Water Height | Regola tutta l'altezza acqua | Regola alt. acqua | Wasserhöhe anpassen | Wasserhöh. anp. | Ajuster hauteur eau | Ajust. haut. eau | ui | Prefer old-DE style concise verb phrase as edge-case accepted wording. | Use compact only if control is constrained and EN is shorter. |
| adjust_terrain_height | Adjust Terrain Height | Regola altezza terreno | Alt. terr. reg. | Terrainhöhe anpassen | Terrainhöh. anp. | Ajuster hauteur terrain | Ajust. haut. terr. | ui | Prefer old-DE style concise terrain wording for constrained controls. | Use compact only if control is constrained and EN is shorter. |
| align_texture_for_height | Align Texture for Height | Allinea texture per altezza | Allinea tex alt. | Textur an Höhe ausrichten | Textur an Höh. | Aligner texture à la hauteur | Aligner tex haut. | ui | Keep technical relation between texture and height explicit. | Use compact only if control is constrained and EN is shorter. |
| min_height | Min Height | Altezza Min | Alt. Min | Min Höhe | Min Höh. | Hauteur min | Haut. min | status | Coordinate/height range label. | Use compact only if control is constrained and EN is shorter. |
| max_height | Max Height | Altezza Max | Alt. Max | Max Höhe | Max Höh. | Hauteur max | Haut. max | status | Coordinate/height range label. | Use compact only if control is constrained and EN is shorter. |
| unselect_object | Unselect Object | Deseleziona oggetto | Desel. ogg. | Objekt abwählen | Obj. abw. | Désélectionner objet | Désél. obj. | ui | Edge-case short button uses compact by default in DE due width constraints. | Use compact only if control is constrained and EN is shorter. |
| new_directory | New Directory | Nuova directory | Nuova dir. | Neues Verzeichnis | Neues Verz. | Nouveau dossier | Nouv. dossier | ui | Directory action in object panel; old-DE specific preferred term `Verzeichnis`. | Use compact only if control is constrained and EN is shorter. |
| portal_information | Portal Information | Info Portale | Info Port. | Portalinfo | Portalinfo | Infos portail | Infos portail | ui | Old-DE edge-case keeps compact compound form used in editor contexts. | Compact not needed by default. |
| selected_object_info | Selected Object Info | Info oggetto selezionato | Info ogg. sel. | Ausgewählte Objektinfo | Obj.info | Infos objet sélectionné | Infos obj. sélect. | ui | Object panel information group title. | Use compact only if control is constrained and EN is shorter. |
| change_base_position | Change BasePosition | Cambia posizione base | Pos. base | Basispos. ändern | Basispos. | Changer position base | Pos. base | ui | Map file panel action; compact DE form preferred on narrow controls. | Use compact only if control is constrained and EN is shorter. |
| save_server_attr | Save ServerAttr | Salva ServerAttr | Salva SAttr | ServerAttr speichern | ServerAttr speich. | Enregistrer ServerAttr | Enreg. SAttr | ui | Keep `ServerAttr` token for compatibility and user recognition. | Use compact only if control is constrained and EN is shorter. |
| save_atlasmap_mini | Save Atlasmap/mini | Salva Atlasmap/mini | Salva Atl/Mini | Atlas/Mini speichern | Atlas/Mini speich. | Enregistrer Atlasmap/mini | Enreg. Atl/Mini | ui | Preserve `Atlasmap/mini` domain token, shorten action verb if constrained. | Use compact only if control is constrained and EN is shorter. |
| save_collision_data | Save collision Data | Salva dati collisione | Salva coll. | Kollisionsdaten speichern | Koll.-Daten sp. | Enregistrer données collision | Enreg. coll. | ui | Collision save action in map file panel. | Use compact only if control is constrained and EN is shorter. |
| starting_point | Starting Point | Punto di partenza | Punto part. | Startpunkt | Startpkt. | Point de départ | Pt départ | ui | Groupbox title for map starting position controls. | Use compact only if control is constrained and EN is shorter. |
| environment_variable | Environment Variable | Variabile ambiente | Var. amb. | Umgebungsvariable | Umgeb.-Var. | Variable d'environnement | Var. env. | ui | Groupbox title for environment variable controls. | Use compact only if control is constrained and EN is shorter. |
| set_environment_var | Set Environment var. | Imposta var. ambiente | Imp. var. amb. | Umgebungsvar. setzen | Umgeb.-Var. setz. | Définir var. env. | Var. env. déf. | ui | Action button for environment variable assignment. | Use compact only if control is constrained and EN is shorter. |
| new_map | New Map | Nuova mappa | Nuova mappa | Neue Karte | Neue Kart. | Nouvelle carte | Nv carte | dialog | Dialog caption for map creation. | Use compact only if control is constrained and EN is shorter. |
| new_event | New Event | Nuovo evento | Nuovo ev. | Neues Ereignis | Neues Ereign. | Nouvel événement | Nvl év. | dialog | Dialog caption for event creation. | Use compact only if control is constrained and EN is shorter. |
| new_generic | New | Nuovo | Nuovo | Neu | Neu | Nouveau | Nouv. | ui | Generic action label; use context-specific rows when available. | Compact not needed by default. |
| apply_action | Apply | Applica | Applica | Anwenden | Anw. | Appliquer | Appl. | ui | Generic apply action in effect/texture panels. | Use compact only if control is constrained and EN is shorter. |
| apply_to_whole | Apply to the whole | Applica a tutto | Applica tutto | Auf alles anwenden | Auf alles anw. | Appliquer partout | Appl. partout | ui | Bulk-apply action; DE compact form required on narrow buttons. | Use compact only if control is constrained and EN is shorter. |
| apply_without_texture_area | Apply to the area w/o texture | Applica a area senza texture | Applica area no tex | Nur auf Bereich ohne Textur | Nur Bereich ohne Tex | Appliquer zone sans texture | Appl. zone sans tex | ui | Tile/paint option; keep meaning explicit even in compact forms. | Use compact only if control is constrained and EN is shorter. |
| patch_grid | Patch Grid | Griglia patch | Griglia patch | Patch-Raster | Patch-Raster | Grille patch | Grille patch | ui | Option checkbox for patch overlay grid. | Compact not needed by default. |
| compass | Compass | Bussola | Bussola | Kompass | Kompass | Boussole | Boussole | ui | Option checkbox for compass overlay. | Compact not needed by default. |

## Do / Don't Examples
- Do: `Reimposta rotazione`
- Do: `Reimp. altezza` on constrained reset controls
- Do: `Deseleziona picking`
- Don't: `Gomma` for the erase tool label
- Don't: mixed-language phrasing when a canonical mapping exists

## Override Note
- Explicit per-term overrides can supersede generic compact style rules when requested for UI fit or product consistency.

## Extending To New Languages
- Add one column per language (for example `de`, `fr`, `es`) without changing existing `term_id`.
- Fill translations progressively; do not remove old mappings.
- Update `notes` when terminology decisions evolve.
