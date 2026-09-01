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
- Clearing the entire board earns a Perfect Clear bonus — dealing quietly favors hands that can finish one off once the board is already close to empty
- Undo (↩️) reverts your last placement, as long as it didn't clear a line
- Reroll (🔀) swaps your current three pieces for new ones — one free use per game
- Settings menu (⚙️) with 15 selectable color themes (Peach, Lavender Dream, Minty Fresh, Sunset, Sunrise, Pink Lemonade, Beach, Bubblegum, Forest, Autumn, Frost, Galaxy, Cyberpunk, Volcano, Midnight) plus a fully custom theme you build from 4 picked colors, sound/haptics toggles, and a two-tap "reset all progress" option
- Piece colors automatically match whichever theme is active — pick a theme and the blocks follow, unless you've manually customized them
- Customizable block colors (🎨), with a reset-to-theme-defaults option
- Zen Mode (🧘, in Settings) removes the fail state — a hand with nowhere to go quietly reshuffles instead of ending the game
- Hard Mode (💀, in Settings) disables Undo and Reroll for a stricter, no-safety-net challenge
- Sprint Mode (⏱️, in Settings) caps a run at 30 placements — score as high as you can before time's up. Tracks its own best score, separate from the regular leaderboard
- Time Attack (⏰, in Settings) gives you a countdown — 1, 2, or 3 minutes, your pick — to score as high as possible, with a pause button (⏸️, or the P key) that freezes the clock mid-run. Tracks its own best score, separate from the regular leaderboard, with a toast + confetti the moment you beat it
- Survival Mode "Rising Tide" (🌊, in Settings) fills a few random cells with obstacles every 5 placements — see how long you can last before the board closes in. Tracks your longest survival streak, with a toast + confetti the moment you beat it
- Practice Mode (🧪, in Settings) plays a run without saving anything — no leaderboard entry, no stats, no badge progress. Good for messing around risk-free
- Lucky Pieces (✨) occasionally show up gold-glowing in the tray and score double when placed
- Colorblind-friendly Shape Marks (🔲, in Settings) overlay a distinct glyph on every piece color so you're never relying on hue alone
- Quit button (🏠) in the toolbar backs out to the title from any in-progress game, with a tap-again-to-confirm safety
- A clean title screen (Start Game, Daily Challenge) with a separate Menu page (☰) for High Scores, Settings, and How to Play (❓) — keeps the main screen from getting crowded
- Top-10 named high score leaderboard (🏆) with a separate board for each board size, plus session stats (games played, lines cleared, best combo, daily play streak, today's best score, total time played)
- Unlockable badges (🏅) for milestones — first clear, a x5 combo, a perfect clear, 100 lines total, a 7-day streak, a 500+ score, trying 5 themes, a Zen Mode game, a Hard Mode win, finishing a game without Undo, completing a Daily Challenge, a 7-day Daily Challenge streak, scoring 200+ on the Mini board, collecting Lucky Pieces, finishing a Sprint, beating a Time Attack clock, and surviving 50 placements in Survival Mode — each worth points toward an overall rank (Rookie through Legend), shown with a live "X / Y unlocked" count and an All/Done/To‑do filter in the Badges screen, plus a "RANK UP" toast the moment your total points cross into the next rank
- A small sparkline of your last 10 scores (per board size) in the High Scores screen
- A live fill meter shows how full the board is, shifting from green to red as things get risky, with a pulsing board outline once it's critically full
- Daily Challenge (📅, on the title screen) is a numbered puzzle (like #142) with the same seeded piece sequence for everyone that day, plus a rotating daily twist — Classic, No Reroll, Double Bonus, Head Start (a pre-filled board), or Combo Frenzy — previewed on the title screen before you start. Tracks its own best score and a daily completion streak
- Board Size (Settings) switches between Classic 8×8 and a faster Mini 6×6 board — locked while a game is in progress, and each size keeps its own leaderboard and "BEST" score
- A bigger celebration — toast + confetti — every 5 combo tier (x5, x10, x15…)
- Backup / Restore (💾, in Settings) exports all your progress as a copyable text code, and can restore it back in on any device that code is pasted into
- Sound effects and haptic feedback on mobile, with a mute toggle (🔊/🔇)
- A little confetti celebration when you set a new #1 high score or unlock a badge
- Keyboard shortcuts: Esc closes menus (and resumes if paused), M mutes, U undoes, R rerolls, P pauses/resumes during Time Attack
- Share Score copies a shareable result to your clipboard from the game-over screen
- Home button on the game-over screen (or the toolbar Quit button, mid-game) to return to the title without restarting
- Warm pastel visual theme by default, with chunky, blocky display type, 15 alternate preset themes (including an Accessible theme built on the colorblind-safe Okabe-Ito palette), and a build-your-own custom theme
- All game data (high scores, stats, preferences) saved locally per-browser (`localStorage`) — nothing leaves your device
- Fully responsive, single-file, no external dependencies beyond Google Fonts
