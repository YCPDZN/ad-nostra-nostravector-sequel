# Ad-Nostra

A 3D browser RPG and the sequel to NOSTRAVECTOR. It is 2137 AD, ten years after the defeat of the Catharsis, and the mining town of Ad-Nostra has become a super-city under Governor Croxian Mascar.

## Play

The game is a single page, `index.html`, with no build step. It loads its character models with `fetch`, so it has to be served over HTTP; opening the file directly from disk will not load the models.

```
python3 -m http.server 8000
```

Then open http://localhost:8000. It also runs as-is on GitHub Pages (Settings → Pages → deploy from the branch root).

Controls: `W A S D` move, drag to look, scroll to zoom, `Tab` or click to target, `1`–`4` abilities, `R` stim, `E` talk, `Space` jump.

## What is in the game

- The city: Governor's Plaza with the golden statue of Orion Mascar, the Governor's Spire, the Shaft One memorial and the Salt Lantern Cantina.
- Beyond the ring: Savanna Verge, Husk Flats and the Deep Cut, each with tougher enemies and a four-quest chain ending in a boss.
- Three classes, levelling, gear upgrades, and a character editor (body, hair, skin, hair colour, suit).
- Croxian Mascar, Orion Mascar, Human Federation of Sol infantry and citizens built from the NOSTRAVECTOR models.

## Files

- `index.html` — the whole game (uses three.js r128 from a CDN).
- `*.b64.txt` — the four character models, base64-encoded, as the page loads them.
- `models/` — the original `.glb` models.

## Multiplayer

Shared presence and chat only work when the page is published as a Claude artifact, where the hosting page provides the room connection. Served from anywhere else, the game runs as a solo session and progress is saved in the browser.
