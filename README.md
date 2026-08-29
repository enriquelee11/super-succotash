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

## Pigris (`tetris.html`)

A Tetris variant with its own mascot: **Blox**, a pixel-art blue pig who
greets new players on the title screen and cycles through short tips
(movement, rotation, hold, hard drop, line clears) — tap the speech bubble
to skip ahead.

- **Arrow left / right** — move
- **Arrow down** — soft drop
- **Arrow up** — rotate
- **Space** — hard drop
- **C / Shift** — hold piece
- **P / Esc** — pause / resume
- **Enter** — advance the title/mode screens, or start / restart
- Touch users get on-screen move / rotate / drop / hold buttons

Flow: title screen (PLAY) → choose Marathon / Sprint 40 / Zen and a
starting level (GO) → play. Every overlay scrolls if its content doesn't
fit the board.

Gameplay:
- Three modes: **Marathon** (endless), **Sprint 40** (race to clear 40
  lines, fastest times saved locally), and **Zen** (the stack clears
  itself instead of ending the game)
- Adjustable starting level (1–15)
- 7-bag piece randomizer, hold with swap, ghost piece, and a 3-piece next queue
- T-spin detection with its own bonus scoring (rotate a T-piece into a
  3-corner-blocked slot without sliding it afterward)
- Combo scoring and back-to-back bonus for Tetrises and T-spins, with score popups on the board
- A pulsing red glow and heartbeat cue when the stack gets dangerously tall, and a screen shake on big clears
- Per-run line-clear breakdown (singles/doubles/triples/Tetrises) shown on game over
- Sound effects and a looping background chiptune (each independently muteable), plus haptic vibration on supported devices
- Level speed-up every 10 lines, elapsed-time display, fullscreen toggle, and local leaderboards (high scores for Marathon, best times for Sprint)

Customizable theme (⚙ settings button, in-game or from the title screen):
- Eight built-in skins — Amber Arcade, Daylight (light), Pastel Dream, Sherbet (pink/green/yellow), Synthwave, Arctic Mint, Retro Rainbow, Noir
- A custom-hue slider that generates its own palette and piece colors on the fly
- Toggles for sound, music, the ghost piece, grid lines, and haptics
- All choices are saved locally and persist between visits

## Features

- Both games share a retro CRT-cabinet look
- Smooth canvas rendering with glow effects and particle bursts
- High scores saved locally (`localStorage`)
- Fully responsive, single-file, no external dependencies
