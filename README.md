# Picnic Monster 🌭

A Flappy Bird–style browser game starring a fuzzy googly-eyed monster who has to dodge his way through a world of hot dogs, ketchup bottles, and mustard bottles. Built entirely in a single `index.html` file with plain HTML5 Canvas and vanilla JavaScript — no build step, no dependencies, no libraries.

## How to play

Open `index.html` in any modern browser (or visit the GitHub Pages link if this repo has one enabled).

- **Jump:** press `Space` or click/tap the canvas
- **Goal:** fly through the gaps in the oncoming obstacles without hitting the floor, the ceiling, or an obstacle
- **Score:** +1 every time you clear an obstacle
- **Restart:** click or press `Space` on the Game Over screen

## Features

- **Three obstacle patterns** that mix it up as you fly:
  - a gap between a top and bottom obstacle (the classic)
  - a single obstacle rising from the ground — fly over it
  - a single obstacle hanging from the ceiling — fly under it
- **Three obstacle skins**, picked at random for each gate: hot dog, ketchup bottle, mustard bottle
- **Ramping difficulty** — gaps get tighter, obstacles get closer together, and the scroll speed increases as your score climbs
- **A hard ceiling** so you can't just fly off the top of the screen
- **A scrolling fry bed** along the floor, moving in sync with the obstacles
- **Cosmetic streaks that level up with your score:**
  - a rainbow trail kicks in at score 10
  - it upgrades to a fire trail + a flickering flame aura on the monster at score 20
- **Top 3 high scores**, saved locally in the browser (`localStorage`) so they persist between visits
- **Fireworks** when you beat your all-time best score

## Running it

No installation needed — it's a static HTML file.

```bash
# just open it directly
open index.html          # macOS
start index.html         # Windows
```

Or serve it locally for a browser-friendlier experience:

```bash
python3 -m http.server
```

then visit `http://localhost:8000`.

### Hosting on GitHub Pages

Since the game lives in `index.html` at the repo root, GitHub Pages will serve it as-is — just enable Pages for this repo (Settings → Pages → Deploy from branch) and point it at the root of the `main` branch.

## Tech notes

- Single self-contained HTML file — all rendering is done with the 2D Canvas API, all art (the monster, obstacles, fries, trail/fire effects) is drawn procedurally in code, nothing is loaded from external images or fonts.
- Physics are frame-rate independent (delta-time based), so gameplay feels the same regardless of display refresh rate.
- No copyrighted or trademarked characters/logos are used — the monster and all obstacle designs are original.
