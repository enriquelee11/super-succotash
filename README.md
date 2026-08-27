# Jumble

A browser-based drag-and-drop block puzzle, built with plain HTML5/CSS/JS — no build step, no dependencies.

## Play

Open `jumble.html` directly in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000/jumble.html
```

## How to play

Drag pieces from the tray onto the 8×8 grid — fill a full row or column to blast it away and score points. Chain clears back-to-back for a combo multiplier. The game ends when none of your three pieces fit anywhere on the board.

## Features

- Drag pieces with mouse, touch, or pen (pointer events)
- Row/column clears, combo multiplier, and score popups
- Undo (↩️) reverts your last placement, as long as it didn't clear a line
- Customizable block colors (🎨), with a reset-to-defaults option
- Top-10 named high score leaderboard (🏆), plus session stats (games played, lines cleared, best combo)
- Sound effects with a mute toggle (🔊/🔇)
- A little confetti celebration when you set a new #1 high score
- Home button on the game-over screen to return to the title without restarting
- Warm pastel visual theme with chunky, blocky display type
- All game data (high scores, stats, preferences) saved locally per-browser (`localStorage`) — nothing leaves your device
- Fully responsive, single-file, no external dependencies beyond Google Fonts
