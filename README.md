# ABC 123 Hunt

A letters, numbers and sight words game for a kindergartner, packaged as a home-screen web app.

**Live:** https://mmanning997.github.io/abc-123-hunt/

The same game is also published as a private Claude artifact. Design notes, the word list and the change history are in the Obsidian vault at `Family/Kids Projects/ABC 123 Hunt.md`.

## Put it on an iPad

1. Open the live link in **Safari** on the iPad.
2. Tap **Share**, then **Add to Home Screen**, then **Add**.
3. Open it from the new icon once while online. After that it works offline.

Stickers and progress are saved on that iPad only.

## Update the game

The game is one file. It is edited in the vault as `ABC 123 Hunt - source.html`, and `build.py` pulls that copy into `src/game.html` when it differs.

```bash
python3 build.py
git add -A && git commit -m "Describe the change" && git push
```

GitHub Pages serves the `main` branch root, so the push is the deploy. An installed copy picks up the new version the next time it is opened online.

## What's here

| Path | What it is |
|---|---|
| `src/game.html` | The game source, the same file as the Claude artifact |
| `build.py` | Wraps the source into `index.html` and writes `sw.js` |
| `index.html`, `sw.js` | Built files (don't edit by hand) |
| `manifest.webmanifest`, `icons/` | App name and home-screen icon |
| `fonts/` | Andika and Grandstander, bundled so the app works offline |

## Fonts

Andika (SIL International) and Grandstander (The Grandstander Project Authors) are licensed under the SIL Open Font License 1.1. The license texts are in `fonts/`.
