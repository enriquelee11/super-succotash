# Arcade Cabinet

Two browser games with a retro arcade cabinet look, built with plain HTML5 canvas and JavaScript — no build step, no dependencies.

## Play

Open `index.html` (Amber Snake) or `dash.html` (Pulse Dash) in any modern browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Amber Snake (`index.html`)

A neon-amber take on classic Snake.

- **Arrow keys / WASD** — move
- **Space** — pause / resume
- **Enter** — start / restart
- Touch users get on-screen directional buttons
- Smooth canvas rendering with glow effects and particle bursts
- Increasing speed as your score climbs
- High score saved locally (`localStorage`)

## Pulse Dash (`dash.html`)

A one-button, music-synced rhythm platformer inspired by Geometry Dash.

- **Tap, click, or press Space** — jump / fly / flip (hold for ship, wave, and robot modes)
- A Geometry Dash-style home screen greets you first, with a big PLAY button (opens the level-select menu) and an ICONS button (opens icon customization) side by side
- Level select (scrollable) — choose from seven levels of increasing difficulty:
  - **Warm Up** (Easy, 120 BPM) — a gentle intro using only the simplest modes
  - **Pulse Dash** (Medium, 150 BPM) — a full tour through all seven vehicle modes
  - **Overdrive** (Hard, 170 BPM) — the same pattern run twice at a faster tempo
  - **Redline** (Insane, 190 BPM) — pushed further still
  - **Nightmare** (180 BPM) — introduces **dual mode**: two synchronized cubes in stacked split lanes, controlled by the same single tap
  - **Apocalypse** (205 BPM) — the nightmare pattern, dual sections included, run twice at a faster tempo
  - **Extreme Demon** (225 BPM) — the true final gauntlet: the nightmare pattern run twice at the highest tempo in the game, capped with an all-new dual-mode finale storm found nowhere else — the longest, densest level, ending in a stretch of back-to-back dual-mode sections with zero room for a mistake
- Every obstacle, jump pad, and portal is timed to a procedurally generated soundtrack (Web Audio API), so the whole level plays in lockstep with the beat
- Speed portals push the scroll pace faster or slower around the middle of each level (the music keeps its own tempo — only the gameplay pace changes, like Geometry Dash's speed portals)
- UFO mode has real hazards on the ceiling as well as the floor, so camping at max altitude is no longer a free pass — you have to genuinely navigate
- Hitting an obstacle is instant failure — you restart the current level from the beginning
- Portals shift you between eight vehicle modes as you progress: cube, ship, ball, UFO, wave, robot, spider, and dual — each with its own movement physics
- An ICONS button in the menu opens an icon customization screen — pick a color (presets or a full color picker) and a finish (Neon glow or flat Matte) for each vehicle mode independently, with a live preview; saved locally (`localStorage`) and applied to your own icon in-game while portals and other mode indicators keep their signature colors for clarity
- An account chip on the home screen lets you create or switch between named local profiles, each with its own saved best % and cleared-level record per level, plus its own icon customization — handy for multiple players sharing one device. These are local profiles only (no password, no server): the game is a static file with no backend, so "logging in" just repoints your save data at a different `localStorage` namespace on this browser, not a real cross-device account
- Level cards show a green **✓ CLEAR** once you've reached 100% on that level (per active profile, or globally if playing as guest)
- A MENU button lets you back out to level select at any time; best completion percentage is saved per level (`localStorage`)

## General

- Fully responsive, single-file games, no external dependencies (fonts load from Google Fonts, everything else is inline)
