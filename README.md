# Start Reactor — Among Us Mini-Game

A browser recreation of the **Start Reactor** task from Among Us: a Simon-style memory game built with plain HTML, CSS, and JavaScript — no frameworks, no build step.

![Among Us](svg/among-us-space.svg)

## How to Play

1. Open `index.html` in your browser (or serve the folder with any static file server).
2. Click **PLAY**.
3. Watch the left panel: it flashes a sequence on the 3×3 grid, one step longer each round.
4. Repeat the sequence by clicking the matching squares on the right panel.
5. Complete all 5 rounds to start the reactor. Miss a step and... **you are the impostor** — the game restarts automatically.

The LEDs on top of each panel track your progress through the current round.

## Running Locally

No dependencies are required. Either open the file directly:

```
index.html
```

or serve it (recommended, so audio loads reliably):

```bash
npx serve .
# or
python -m http.server
```

Then visit the printed local URL.

## Project Structure

```
├── index.html      # Page markup and game bootstrap
├── js/
│   └── reactor.js  # Game logic (sequence generation, playback, input checking)
├── styles/
│   ├── styles.css  # Main layout and panel styling
│   ├── rules.css   # Responsive breakpoints
│   └── among.css   # Floating crewmate animation
├── audio/          # Sound effects for each square, start, fail, and complete
└── svg/            # Background, panel frame, and LED graphics
```

## Features

- Sequence-memory gameplay faithful to the original Among Us task
- Sound effects for every square, plus start / fail / complete jingles
- LED progress indicators and animated feedback for success and failure
- Responsive layout that stacks the panels on narrow screens
- Animated crewmate drifting through space in the background
