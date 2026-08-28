# Amber Arcade

Two browser-based arcade games styled as a retro amber CRT cabinet, built with plain HTML5 canvas and JavaScript — no build step, no dependencies.

## Play

Open `index.html` (Snake) or `tetris.html` (Tetris) in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Amber Snake (`index.html`)

- **Arrow keys / WASD** — move
- **Space** — pause / resume
- **Enter** — start / restart
- Touch users get on-screen directional buttons

## Tetris (`tetris.html`)

- **Arrow left / right** — move
- **Arrow down** — soft drop
- **Arrow up** — rotate
- **Space** — hard drop
- **C / Shift** — hold piece
- **P / Esc** — pause / resume
- **Enter** — start / restart
- Touch users get on-screen move / rotate / drop / hold buttons

Gameplay:
- 7-bag piece randomizer, hold with swap, ghost piece, and a 3-piece next queue
- Combo scoring and back-to-back Tetris bonus, with score popups on the board
- Sound effects (movement, rotation, line clears, level-ups, game over) — muteable
- Level speed-up every 10 lines, elapsed-time display, and a local top-5 high-score list

Customizable theme (⚙ settings button, in-game or from the title screen):
- Seven built-in skins — Amber Arcade, Daylight (light), Pastel Dream, Synthwave, Arctic Mint, Retro Rainbow, Noir
- A custom-hue slider that generates its own palette and piece colors on the fly
- Toggles for sound, the ghost piece, and grid lines
- All choices are saved locally and persist between visits

## Features

- Both games share a retro CRT-cabinet look
- Smooth canvas rendering with glow effects and particle bursts
- High scores saved locally (`localStorage`)
- Fully responsive, single-file, no external dependencies
