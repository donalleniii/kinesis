# Kinesis

Procedural particle field demo. Single HTML file, no build step, no dependencies beyond two CDN modules. Open in Chrome and run.

[Live demo](https://donalleniii.github.io/kinesis/)

## Systems

- **Curl Noise** — divergence-free flow on a 2D simplex noise scalar potential
- **Clifford Attractor** — bounded strange attractor, parametric map
- **Physarum** — slime mold pheromone simulation with three-sensor agents
- **DLA** — diffusion-limited aggregation, dendritic crystalline growth
- **Reaction-Diffusion** — Gray-Scott two-chemical PDE on a downsampled grid
- **Flocking** — Reynolds boids with spatial hashing for O(n) neighbor lookup

## Hand control

Press `C` to enable the camera. MediaPipe Hands tracks up to two hands. Each hand's screen position selects a quadrant in the on-canvas grid; the pinch distance (thumb to index) controls that cell's parameter via soft takeover, so values are not snapped when you enter a cell. With both hands tracked, the distance between them drives the most visually impactful parameter for the active system. Bipolar parameters (Scale, Rotate) snap to zero near the middle of the pinch range.

## Hotkeys

- `1`–`6` switch systems directly. Arrow keys cycle.
- `Space` pause, `R` reseed, `S` screenshot, `F` fullscreen
- `H` hide menu, `C` toggle camera, `G` toggle quadrant grid

## Run

Open `index.html` in Chrome. No server, no install.

## Stack

- Canvas2D, vanilla JS (ES modules)
- [lil-gui](https://lil-gui.georgealways.com/) for the panel
- [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands.html) for landmark tracking

Built with [Claude Code](https://claude.com/claude-code).
