# OSE Advanced Fantasy — Owlbear Rodeo Extension

A full character sheet extension for **Old-School Essentials Advanced Fantasy** with an integrated dice roller.

## Features

- **Stats Tab** — All 6 ability scores with auto-calculated OSE modifiers, combat stats (HP, AC, THAC0, saves), languages, and notes
- **Abilities Tab** — Class abilities, thief/specialist skills, racial abilities, weapons table
- **Inventory Tab** — Item tracker with weight/value, encumbrance calculator, coin purse
- **Spells Tab** — Spell slots per level (levels 1–9) with usage pips, spell list
- **Dice Roller** — Always-visible dock with one-click preset rolls; results appear in an animated overlay on top of the sheet
- **Auto-save** — All data saved to localStorage and persists between sessions

## Installation (Owlbear Rodeo)

### Method 1: Local Dev Server (recommended for testing)
1. Extract this folder somewhere on your machine
2. Serve it with any static file server, e.g.:
   ```
   npx serve .
   ```
   or
   ```
   python3 -m http.server 8080
   ```
3. In Owlbear Rodeo, open **Settings → Extensions**
4. Click **Add Extension** and enter: `http://localhost:8080/manifest.json`

### Method 2: Host Online (for permanent use)
1. Deploy this folder to any static host (Netlify, Vercel, GitHub Pages, etc.)
2. In Owlbear Rodeo, go to **Settings → Extensions → Add Extension**
3. Enter the URL to your hosted `manifest.json`

## Usage

- Click the **⚔** action button in the Owlbear toolbar to open the character sheet popover
- Fill in your character details — everything auto-saves
- Use the **Dice Roller** dock at the bottom to roll presets with one click
- Click **+ New Preset** to build and save custom roll formulas
- Click any preset chip to roll — the result appears as an animated overlay on the sheet

## Dice Roller

**Quick Rolls** (on the Stats tab): One-click ability checks and saving throws  
**Preset Chips**: Saved rolls in the dock — click the name to roll, hover for the × to delete  
**Builder**: Enter a name, count, die type, and modifier — roll once or save as a preset

## File Structure

```
ose-extension/
├── manifest.json       # Owlbear extension manifest
├── icon.svg            # Extension icon
└── src/
    └── sheet.html      # The full character sheet + dice roller
```
