# Fireworks Interactive Canvas Experience

A lightweight, festive front-end project built with vanilla JavaScript and HTML5 Canvas.  
Users can launch fireworks with mouse interaction and cycle through character avatars, all inside a fullscreen animated scene.

## Portfolio Summary

This project demonstrates:

- Canvas animation and particle effects without external libraries.
- Real-time mouse-driven interaction.
- Layered rendering with multiple canvases.
- Clean separation of concerns across small focused scripts.
- Visual styling and motion design using only CSS and native browser APIs.

## Live Preview

Add your deployed URL here once published:

- `https://hhok95.github.io/Fireworks`

## Project Goals

- Build an engaging, interactive browser animation from scratch.
- Practice object-based animation architecture (`Firework`, `Fleck` classes).
- Keep the stack minimal and dependency-free.
- Create a portfolio-ready artifact that is easy to run and easy to explain.

## Features

- Fullscreen gradient sky background.
- Starfield and layered foreground for depth.
- Mouse-aimed fireworks launch and explosion effects.
- Particle trails with friction, gravity, and fade-out decay.
- Clickable avatar cycling through themed character images.
- Animated heading text using CSS gradient movement.

## Tech Stack

- HTML5
- CSS3
- JavaScript (ES6)
- HTML Canvas 2D API

No framework and no build tooling required.

## Repository Structure

```text
Fireworks/
├── assets/
│   ├── bear.png
│   ├── cookie.png
│   ├── reindeer.png
│   ├── santa.png
│   └── snowman.png
├── index.html
├── styles.css
├── avatar-toggle.js
├── canvas-background.js
└── canvas-fireworks.js
```

## Architecture Overview

- `index.html`
  - Defines UI text, avatar image, and two stacked canvases.
  - Loads all scripts directly in the browser.
- `styles.css`
  - Handles layout, layering, typography, and title animation.
- `canvas-background.js`
  - Renders static scene elements (gradient sky, ground, stars).
- `canvas-fireworks.js`
  - Manages animation loop, user input, projectile paths, and particle systems.
- `avatar-toggle.js`
  - Cycles avatar images on click.

## How It Works

### 1. Scene Setup

On load, both canvases are sized to the viewport.  
The background canvas is painted once.  
The fireworks canvas runs a continuous animation loop (`requestAnimationFrame`).

### 2. User Interaction

- Mouse position becomes the target coordinate.
- Holding mouse click spawns fireworks from a bottom anchor point.
- Clicking the avatar switches to the next character image.

### 3. Firework Lifecycle

1. A `Firework` launches from the anchor toward the mouse target.
2. Once it reaches target distance, it spawns multiple `Fleck` particles.
3. Particles fade with alpha decay and are removed from arrays when finished.

## Running Locally

Because this is a static project, there are two simple options:

1. Open `index.html` directly in a browser.
2. Or run a local server from the project root:

```bash
python3 -m http.server 8080
```

Then visit `http://localhost:8080`.

## Deploying (GitHub Pages)

1. Create a new GitHub repository.
2. Push this project to `main`.
3. In repository settings, enable GitHub Pages from branch `main` (root).
4. Your site will be available at:
   `https://<your-username>.github.io/<repo-name>/`

## Suggested Portfolio Talking Points

If you include this project in your portfolio, emphasize:

- Implemented interactive particle physics using friction, gravity, and alpha decay.
- Structured animation logic into reusable classes.
- Balanced visual quality with performance via controlled particle counts.
- Delivered a polished experience with no framework overhead.

## Potential Improvements

- Add touch support for mobile fireworks launch.
- Make scene responsive to window resize after load.
- Add sound effects with optional mute toggle.
- Add keyboard accessibility and ARIA improvements.
- Add configurable color themes and firework presets.
- Include FPS/performance instrumentation for optimization analysis.

## Credits

- Fonts loaded from Google Fonts (`Pacifico`, `Work Sans`).
- Character image assets are stored in `assets/`.

## License

No license file is currently included.  
For public portfolio use, consider adding an MIT license.
