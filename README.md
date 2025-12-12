# Anki Vocabulary Deck Template

A clean Anki card layout with automatic audio playback, colored level badges, and a ready-to-import vocabulary CSV. Use the snippets in `template/` to style your own note type and the CSV to jump-start your deck.

## Preview
| Light Front | Light Back | Dark Front | Dark Back |
| --- | --- | --- | --- |
| ![Light front](template/pics/light_front.png) | ![Light back](template/pics/light_back.png) | ![Dark front](template/pics/dark_front.png) | ![Dark back](template/pics/dark_back.png) |

## Vocabulary CSV Format
- Column order (9 total): Word, IPA, Level (A1–C2), Part of Speech, Definition, Meaning/Translation, Synonyms, Example, Example 2.
- Example sentences may include simple HTML like `<b>word</b>` to highlight the target term; keep other markup minimal.
- Sample row: `"revert","rɪˈvɜːt","C1","verb","to return to a previous state or subject","eski haline dönmek","return, regress","We should not <b>revert</b> to the old inefficient system.","Try not to <b>revert</b> to your bad habits when you get stressed."`

## Generate CSV with an LLM
- Use the curated prompt to turn text, word lists, or uploaded documents into an Anki-ready CSV with typo fixes, deduplication, CEFR filtering, batching over 50 items, and bolded targets in examples.
- Full prompt (TR): [docs/prompt.md](docs/prompt.md)

## Set Up in Anki (Desktop)
1) `Tools -> Manage Note Types -> Add`; clone a basic note type or create new.  
2) In `Cards...`, replace **Front Template** with `template/front.html`, **Back Template** with `template/back.html`, **Styling** with `template/style.css`.  
3) Set fields in this order: `Word`, `IPA`, `Level`, `Part of Speech`, `Definition`, `Meaning`, `Synonyms`, `Example`, `Example 2`, `wordAudio`, `exampleAudio`.  
4) `File -> Import` `vocabulary.csv`, choose the note type, map columns; mark `Synonyms` and `Example 2` optional if empty.  
5) Sync and review. Night mode colors adjust automatically.

## Field Notes
- `Level` colors the badge (A1–A2 green, B1–B2 orange, C1–C2 purple; defaults to gray otherwise).
- `Part of Speech` shows as a secondary badge.
- `wordAudio` and `exampleAudio` are optional fields; if present, playback starts automatically shortly after the card loads.
