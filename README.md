# Arcade

Two browser-based arcade games, built with plain HTML5/CSS/JS — no build step, no dependencies.

## Play

Open a game's HTML file directly in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

### Neon Snake (`index.html`)

A neon arcade Snake game.

- **Arrow keys / WASD** — move
- **Space** — pause / resume
- **Enter** — start / restart
- Touch users get on-screen directional buttons
- High score saved locally (`localStorage`)

### Block Blast! (`block-blast.html`)

A drag-and-drop block puzzle in the style of *Block Blast* / *1010!*. Drag pieces from the tray onto the 8×8 grid — fill a full row or column to blast it away and score points. Chain clears back-to-back for a combo multiplier. The game ends when none of your three pieces fit anywhere on the board.

- Drag pieces with mouse, touch, or pen (pointer events)
- Row/column clears, combo multiplier, and score popups
- Top-10 high score leaderboard saved locally (`localStorage`), with name entry when you set a new record
- Fully responsive, single-file, no external dependencies

## Features

- Smooth rendering with glow effects
- Fully responsive, single-file games, no external dependencies
