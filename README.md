# Sprite Alive

**See your animation the way it will feel in-game — before you touch an engine.**

Sprite Alive is a free, browser-based sprite sheet animation tester for pixel artists and game developers. Drop in a sprite sheet, slice it, and watch it play with placeholder game-feel effects like beams, hit flashes, and glow — in under 30 seconds.

**[▶ Try it live]https://cupcakechan.github.io/sprite-alive/**



## Why

Existing sprite previewers answer *"is my animation smooth?"* — but not *"will it feel like a game?"* The only way to see your attack animation with a synced beam or hit flash has been a full engine import: slice, animate, script, press Play. Sprite Alive gives you that feedback loop in seconds, with zero setup.

## Features

- **Drag & drop import** — PNG sprite sheets via drop, file picker, or Ctrl+V paste
- **Smart slicing** — auto-detects frames in horizontal strips, or manual frame count / grid cell size (empty grid cells are skipped automatically)
- **Playback controls** — FPS slider, loop, ping-pong, frame stepping
- **Onion skinning** — previous frame ghosted red, next frame green, for spotting jerky movement
- **Purpose presets** — Attack, Idle, Walk/Run, Hit — each pre-configures playback and effects
- **Placeholder effects** with live parameters:
  - **Beam** — mouse-aimed energy beam synced to a trigger frame
  - **Hit flash** — sprite blinks a tint color on impact frames
  - **Glow pulse** — breathing aura for idle/charge animations
  - **Afterimage** — ghost trail of previous frames
- **Stage options** — zoom (1x–4x), grid / dark / light backgrounds

## Privacy

**Your art never leaves your browser.** There is no server, no upload, no account. The entire tool is a single HTML file — file reading, slicing, and rendering all happen locally on your machine.

## Usage

1. Open the [live page](https://cupcakechan.github.io/sprite-alive/) (or download `index.html` and double-click it — it works offline).
2. Drop in a sprite sheet, or click **Try the demo sheet**.
3. Confirm the slicing grid lines up with your frames, then **Continue**.
4. Pick a **Purpose** preset, press **Space**, and tune the FPS and effects until it feels right.

Works best with PNG sheets that have transparency. Horizontal strips and uniform grids are both supported.

## Tech

Vanilla JavaScript + Canvas. One file, no frameworks, no build step, no dependencies.

Effects are small plug-in objects — each is a name, a parameter list, and a `draw()` function. Adding a new effect means adding one object to the `EFFECTS` array in `index.html`.

## Roadmap

- [ ] Screen shake effect
- [ ] GIF export
- [ ] Per-frame timing (hold frames)
- [ ] Loop seam indicator for walk cycles
- [ ] Mobile-friendly layout

## Status

Alpha 0.1 — feedback welcome via [issues](../../issues).# sprite-alive