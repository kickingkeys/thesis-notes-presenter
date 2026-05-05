# Thesis Notes Presenter

A minimal speaker-notes prompter for the ITP thesis presentation. Open it on your phone or iPad in landscape, tap **Play**, and tap right/left to advance through your notes while you drive the slides on another device.

## Features

- **Tap right** to advance, **tap left** to go back
- Keyboard arrows (← / →) work too on a laptop
- **Timer in the top-right** counts up from 00:00 — turns orange after 10:00 as a soft warning
- **Auto-resume**: if your screen sleeps or you reload mid-talk, it remembers which note you were on and keeps the timer running
- **Long-press the top-left corner** to reset
- **Goes fullscreen** on press Play (where supported)
- All notes live in a single editable `notes.json` file — no rebuild needed when you tweak them

## Hosting

Push to GitHub, enable GitHub Pages on the `main` branch root, and the URL is yours.

```sh
gh repo create thesis-notes-presenter --public --source . --remote origin --push
```

Then in the repo settings → Pages → Build from `main` / `(root)`.

## Editing notes

Open `notes.json`. Each entry in the `notes` array is one slide's notes. Use `\n\n` for paragraph breaks, and prefix lines with `·` for bullets:

```json
"notes": [
  "First slide notes here.",
  "Second slide.\n\nWith multiple paragraphs.\n\n· bullet\n· another bullet"
]
```

No build step. Save the file, refresh the page.
