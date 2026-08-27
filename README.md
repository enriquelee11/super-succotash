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

## Amber Tetris (`tetris.html`)

- **Arrow left / right** — move
- **Arrow down** — soft drop
- **Arrow up** — rotate
- **Space** — hard drop
- **P** — pause / resume
- **Enter** — start / restart
- Touch users get on-screen move / rotate / drop buttons
- Next-piece preview, level speed-up every 10 lines, and standard line-clear scoring

## Features

- Both games share the same amber-phosphor CRT cabinet look and color palette
- Smooth canvas rendering with glow effects and particle bursts
- High score saved locally (`localStorage`)
- Fully responsive, single-file, no external dependencies
