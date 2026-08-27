# Arcade

Two browser-based arcade games sharing one warm pastel theme, built with plain HTML5/CSS/JS — no build step, no dependencies.

## Play

Open a game's HTML file directly in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

### Amber Snake (`index.html`)

A classic Snake game.

- **Arrow keys / WASD** — move
- **Space** or the on-screen ⏸ button — pause / resume
- **Enter** — start / restart
- Touch users get on-screen directional buttons
- Top-10 named high score leaderboard (🏆), plus session stats (games played, food eaten, best length)
- Sound effects with a mute toggle (🔊/🔇)
- A little confetti celebration when you set a new #1 high score
- Home button on the game-over screen to return to the title without restarting

### Jumble (`jumble.html`)

A drag-and-drop block puzzle in the style of *Block Blast* / *1010!*. Drag pieces from the tray onto the 8×8 grid — fill a full row or column to blast it away and score points. Chain clears back-to-back for a combo multiplier. The game ends when none of your three pieces fit anywhere on the board.

- Drag pieces with mouse, touch, or pen (pointer events)
- Row/column clears, combo multiplier, and score popups
- Undo (↩️) reverts your last placement, as long as it didn't clear a line
- Customizable block colors (🎨), with a reset-to-defaults option
- Top-10 named high score leaderboard (🏆), plus session stats (games played, lines cleared, best combo)
- Sound effects with a mute toggle (🔊/🔇)
- A little confetti celebration when you set a new #1 high score
- Home button on the game-over screen to return to the title without restarting

## Features

- Shared warm pastel visual theme with chunky, blocky display type
- All game data (high scores, stats, preferences) saved locally per-browser (`localStorage`) — nothing leaves your device
- Fully responsive, single-file games, no external dependencies beyond Google Fonts
