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
- While dragging, cells that would complete a line light up so you can plan ahead
- Clearing the entire board earns a Perfect Clear bonus
- Undo (↩️) reverts your last placement, as long as it didn't clear a line
- Reroll (🔀) swaps your current three pieces for new ones — one free use per game
- Settings menu (⚙️) with 5 selectable color themes (Peach, Lavender Dream, Minty Fresh, Sunset, Midnight), sound/haptics toggles, and a two-tap "reset all progress" option
- Customizable block colors (🎨), with a reset-to-defaults option
- Top-10 named high score leaderboard (🏆), plus session stats (games played, lines cleared, best combo, daily play streak)
- Unlockable badges (🏅) for milestones — first clear, a x5 combo, a perfect clear, 100 lines total, a 7-day streak, and a 500+ score
- A live fill meter shows how full the board is, shifting from green to red as things get risky
- Sound effects and haptic feedback on mobile, with a mute toggle (🔊/🔇)
- A little confetti celebration when you set a new #1 high score or unlock a badge
- Keyboard shortcuts: Esc closes menus, M mutes, U undoes, R rerolls
- Share Score copies a shareable result to your clipboard from the game-over screen
- Home button on the game-over screen to return to the title without restarting
- Warm pastel visual theme by default, with chunky, blocky display type and 4 alternate themes to pick from
- All game data (high scores, stats, preferences) saved locally per-browser (`localStorage`) — nothing leaves your device
- Fully responsive, single-file, no external dependencies beyond Google Fonts
