# Anki Vocabulary Deck Template

A clean Anki card layout with automatic audio playback, colored level badges, and a ready-to-import vocabulary CSV. Use the snippets in `template/` to style your own note type and the CSV to jump-start your deck.

## Preview
Screenshots live in `template/pics`: `light_front.png` (light mode front), `light_back.png` (light mode back), `dark_front.png` (dark mode front), and `dark_back.png` (dark mode back).

| Light Mode — Card Front | Light Mode — Card Back |
| --- | --- |
| ![Light mode front](template/pics/light_front.png) | ![Light mode back](template/pics/light_back.png) |

| Dark Mode — Card Front | Dark Mode — Card Back |
| --- | --- |
| ![Dark mode front](template/pics/dark_front.png) | ![Dark mode back](template/pics/dark_back.png) |

## Files
- `template/front.html` – front template with level and part-of-speech badges plus word audio autostart.
- `template/back.html` – back template with definition, meaning, synonyms, examples, and example audio autostart.
- `template/style.css` – shared styling with light/dark support and refined typography.
- `vocabulary.csv` – sample deck data ready for import.

## Set Up in Anki (Desktop)
1) In Anki, go to `Tools -> Manage Note Types -> Add` and clone an existing basic note type (or create new).  
2) Open the new note type’s `Cards...` editor:  
   - Replace the **Front Template** with the contents of `template/front.html`.  
   - Replace the **Back Template** with `template/back.html`.  
   - Replace the **Styling** with `template/style.css`.  
3) Ensure the note type has these fields in order: `Word`, `IPA`, `Level`, `Part of Speech`, `Definition`, `Meaning`, `Synonyms`, `Example`, `Example 2`, `wordAudio`, `exampleAudio`.  
4) Import `vocabulary.csv` via `File -> Import`, choose your note type, and map the columns to the fields above (mark `Synonyms` and `Example 2` as optional if empty rows exist).  
5) Sync and review. Night mode colors adjust automatically.

## Field Notes
- `Level` colors the badge (A1–A2 green, B1–B2 orange, C1–C2 purple; defaults to gray otherwise).
- `Part of Speech` shows as a secondary badge.
- `wordAudio` and `exampleAudio` are optional fields; if present, playback starts automatically shortly after the card loads.

## Tips
- Use the light/dark screenshots as a reference when tweaking colors; CSS custom properties at the top of `template/style.css` keep changes centralized.
- Keep IPA text concise; the font size is tuned for typical IPA length.
- For additional example sentences, duplicate the `Example 2` block in `template/back.html` and add more fields to the note type as needed.
