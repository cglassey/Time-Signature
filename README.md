# Tap Time Trainer

A tiny, mobile-friendly web app that **gamifies learning musical time signatures**. Pick a time signature and BPM, hit **Start**, and tap the big pad in time with the beat. You’ll get instant feedback (Perfect / Close / Miss), streaks, levels, and an accuracy meter.

- 🎯 **Tight timing** via Web Audio API with a scheduler
- 🟢 **Downbeats highlighted**; LEDs for beats in the measure
- 🧠 **Training & Challenge** modes (Challenge hides the click to test your inner clock)
- 🥁 **Tap Tempo** to set BPM by tapping

## Quick start

1. Download this repo (or just `index.html`).
2. Open `index.html` in any modern browser.

## Deploy to GitHub Pages

1. Create a new GitHub repo, e.g. `tap-time-trainer`.
2. Upload `index.html` to the root of the repo.
3. In **Settings → Pages**, set **Source** to **Deploy from a branch**, select `main` (or `master`) and the root (`/`).
4. Wait a moment; your site will appear at: `https://<your-username>.github.io/<repo-name>/`

## Files

- `index.html` — all HTML/CSS/JS in one file
- `LICENSE` — MIT License
- `README.md` — this file

## Tech notes

- Uses a **lookahead scheduler** (`setInterval` every ~25ms) to schedule clicks slightly ahead of audio time for stability.
- Click sound is a short square-wave blip with an envelope; **downbeats are louder** for orientation.
- Accuracy scoring thresholds (tweak in JS):
  - Perfect ≤ **40 ms**
  - Close ≤ **90 ms**
  - Miss  > **90 ms**
- Challenge mode pattern: after 2 measures visible, **hide click for 4 measures**, then **show for 1** to re-sync (repeats).

## License

MIT © 2025
