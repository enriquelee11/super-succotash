# Chess Machine

A browser-based chess game with a bot opponent whose playing strength you control with a rating slider (0–2000). Built with plain HTML, CSS, and JavaScript — no build step, no dependencies.

## Play

Open `index.html` in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Features

- Full chess rules: castling, en passant, pawn promotion, check/checkmate/stalemate, and draw by insufficient material or the 50-move rule
- Bot opponent with an adjustable 0–2000 rating slider — lower ratings search less deeply and blunder more often, higher ratings search deeper (up to 3 plies) with tighter, more consistent play
- Click-to-move interface with legal move highlights, last-move and check highlighting, and a promotion piece picker
- Move list in simplified algebraic notation, captured-piece tray with material difference
- Play as White or Black, undo, and start a new game at any time
- Optional chess clock with selectable time controls (1, 3, 5, 10, 15, 30 minutes, or no limit) — the game ends immediately if a side's clock runs out
- Customizable appearance: six full theme presets (Midnight, Daylight, Wood Classic, Deep Ocean, Forest, Sunset), plus individual color pickers for light squares, dark squares, white pieces, and black pieces — choices are saved locally in the browser

## Notes

The bot is a lightweight negamax search with alpha-beta pruning and a material + centrality evaluation; rating is simulated via search depth, move-selection noise, and blunder probability rather than calibrated against real player data.
