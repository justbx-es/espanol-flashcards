# Español Flashcards

A mobile-friendly flashcard app for French ↔ Spanish vocabulary.

## Adding or removing decks

All decks live in the `decks/` folder as simple CSV files.

### To add a deck
1. Create a CSV file with two columns: `french,spanish` (header row optional)
   ```
   french,spanish
   enceinte,embarazada
   faux,falso
   ```
2. Upload it to the `decks/` folder on GitHub
3. Open `manifest.json` and add an entry:
   ```json
   { "name": "My New Deck", "file": "decks/My_New_Deck.csv" }
   ```

### To remove a deck
1. Delete the CSV file from `decks/`
2. Remove its entry from `manifest.json`

### manifest.json format
```json
[
  { "name": "Basic 1", "file": "decks/Basic_1.csv" },
  { "name": "Basic 2", "file": "decks/Basic_2.csv" }
]
```
The `name` is what appears in the app's dropdown. The `file` is the path relative to the repo root.

## Features
- FR→ES or ES→FR direction toggle (resets current session)
- Type your answer, press Enter or tap Check
- End-of-deck score summary
- Retest only the cards you got wrong
- Works offline once visited (service worker cache)
- Colombian flag home screen icon on iPhone

## Deploying to GitHub Pages
1. Push all files to a public GitHub repo
2. Go to Settings → Pages → Branch: main → Save
3. Visit `https://yourusername.github.io/reponame` in Safari
4. Share → Add to Home Screen
