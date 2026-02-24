# RC Translation Automation Guide

## Purpose
- `Sample/WorldEditor.rc` is the source of truth for the latest English resources.
- Language folders (`AE`, `CZ`, `DE`, `ES`, `FR`, `HU`, `IT`, `PL`, `PT`, `RO`, `TR`, etc.) are generated from `Sample` and then translated in place.
- Preserve language DLL naming from each language `.vcxproj` (`WorldEditorRemix_XX`).

## CHARSETS (ANSI)
- ae 1256
- cz 1250
- de 1252
- dk 1252
- en 1252
- es 1252
- fr 1252
- gr 1253
- hu 1250
- it 1252
- nl 1252
- pl 1250
- pt 1252
- ro 1250 (two accents may require a conversion to proper ansi)
- ru koi8-ru
- tr 1254

## Conversion Rules
Start from `Sample/WorldEditor.rc`.

In each language `.rc`:
1. Replace:
   - `#include "resource.h"`
   - with `#include "../Sample/resource.h"`
2. Replace resource string paths:
   - `"res\\..."`
   - with `"..\\Sample\\res\\..."`
3. Replace TEXTINCLUDE `WorldEditor.rc2` path with double backslashes:
   - `"..\\Sample\\res\\WorldEditor.rc2"`
4. Replace final tail include using single backslashes (RC include syntax):
   - `#include "..\Sample\res\WorldEditor.rc2"`

Warnings:
- Do not produce mixed forms like `"..\Sample\res\\..."`.
- Resource string paths must stay fully escaped with double backslashes.

## Safe Translation Rules
- Translate in situ for the target language, with terminology suitable for a 3D map creator/editor for an online game.
- Reuse only safe mappings when automating:
  - `STRINGTABLE` by string ID.
  - `MENUITEM` by `(menu resource ID, command ID)`.
  - dialog `CAPTION` by dialog resource ID.
- Never bulk-map control labels by shared IDs like `IDC_STATIC` (prevents repeated-string corruption).

## Preserved Blocks
- Keep Korean bootstrap block intact:
  - `LANGUAGE LANG_KOREAN, SUBLANG_DEFAULT`
  - `#pragma code_page(949)`
- Keep target language block with correct charset/code page.
- Preserve placeholders and escapes exactly:
  - `%d`, `%s`, `\n`, `\t`, doubled quotes `""`.

## Validation Checklist
- ANSI / no BOM output.
- No mixed slash escaping.
- Resource ID parity with `Sample/WorldEditor.rc`.
- No mass repeated labels in dialogs.
- Project target names unchanged (`WorldEditorRemix_XX`).

## Common Pitfalls
- Mixed path escaping (`"..\Sample\res\\..."`) causing RC/path errors.
- Over-aggressive control text reuse by non-unique IDs (`IDC_STATIC`) causing repeated labels.
- Encoding drift (UTF-8 BOM or wrong codepage) corrupting accents or compile behavior.

## Quick Recipe
1. Copy `Sample/WorldEditor.rc` to target language folder.
2. Apply path transforms (`../Sample/resource.h`, `..\\Sample\\res\\...`, rc2 include rules).
3. Set target language and correct code page.
4. Apply safe translation pass (STRINGTABLE, MENUITEM, dialog CAPTION only).
5. Run validation checks (encoding, escaping, ID parity, repeated-label scan, target names).
