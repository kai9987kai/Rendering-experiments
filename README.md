
# Rendering Experiments

A collection of browser-based rendering experiments exploring neural-style deformation, procedural texture generation, physics-driven visuals, particle systems, animated mesh distortion, audio-reactive rendering, and interactive 3D visual labs.

Everything runs client-side in standalone HTML files. No build step, no backend, and no package installation are required.

![HTML](https://img.shields.io/badge/HTML-100%25-orange)
![Three.js](https://img.shields.io/badge/Three.js-r128-black)
![TensorFlow.js](https://img.shields.io/badge/TensorFlow.js-browser_AI-ff6f00)
![License](https://img.shields.io/badge/License-MIT-green)

---

## Overview

**Rendering Experiments** is a creative WebGL playground for testing advanced browser graphics ideas. The repo mixes Three.js, TensorFlow.js, Simplex noise, procedural materials, physics simulation, mesh deformation, and UI-heavy visual controls into single-file experiments.

The project is especially useful for:

- learning how neural-style fields can affect 3D meshes,
- experimenting with procedural deformation and material generation,
- building standalone browser graphics demos,
- testing real-time WebGL performance techniques,
- exploring generative visual systems without a backend,
- prototyping interactive creative-coding ideas quickly.

---

## Current Demos

| File | Description |
|---|---|
| `3DNeuralRenderingVisualization.html` | Advanced neural rendering lab using fBM Simplex noise, TensorFlow.js displacement, shape/material controls, background training, presets, screenshots, particle halos, ghost trails, and live loss/FPS telemetry. |
| `NeuralNoiseShape3D.html` | Neural Morph 3D Lab with trainable neural field deformation, multiple geometry modes, material modes, particle field control, random seed generation, screenshot capture, and keyboard shortcuts. |
| `NeuralShapeForge.html` | GAN-style 3D shape lab with neural deformation, style transfer, audio-reactive synthesis, presets, screenshots, live stats, TF memory display, and interactive mesh warping. |
| `neural-physics.html` | Neural Physics Rendering Lab combining Three.js rendering, TensorFlow.js GAN/field telemetry, Ammo.js rigid-body physics, fallback physics, collider spawning, style modes, audio reaction, splat clouds, and impact telemetry. |
| `neuralnet-texture-gen.html` | Neural Texture Lab for generating, mutating, evolving, exporting, saving, and inspecting AI-style material maps on reflective 3D geometry. |
| `loopingvisuals.html` | 3D Visual Loop Engine featuring collision splashes, trails, shockwaves, camera modes, particle/star fields, minimap, event log, capture mode, and keyboard shortcuts. |

---

## Features

### Real-Time 3D Rendering

- WebGL-powered rendering through Three.js.
- Responsive full-screen canvas layouts.
- Orbit, follow, cinematic, and mouse-aim camera styles depending on the demo.
- Fog, bloom-like glow effects, particle fields, shadows, wireframes, scanlines, and animated overlays.
- Screenshot/capture support in multiple demos.

### Neural and Procedural Systems

- TensorFlow.js-powered browser models.
- Neural displacement fields.
- GAN-inspired generator/discriminator experiments.
- Async-safe training loops that avoid freezing the render loop.
- Live loss displays and backend/tensor telemetry.
- Procedural Simplex/fBM field deformation.
- Neural-style texture generation from latent vectors.

### Physics and Interaction

- Ammo.js WASM physics support in `neural-physics.html`.
- Built-in fallback physics when Ammo.js cannot load.
- Collider spawning.
- Gravity controls.
- Impact/energy telemetry.
- Shockwaves, splashes, collision trails, and visual feedback.

### Texture and Material Generation

- AI-style texture generation.
- Style modes including nebula, biomorph, crystal, circuit, lava, oceanic, and monochrome.
- Export generated textures as PNG.
- Save/load texture presets.
- PBR-style controls for metalness, roughness, normal strength, displacement, and emissive glow.
- Geometry switching for box, sphere, cone, cylinder, torus, torus knot, dodecahedron, and icosahedron.

### UI and Controls

- HUD panels with live metrics.
- Sliders for deformation, neural blend, refresh rate, speed, gravity, splat density, material intensity, particle count, and more.
- Keyboard shortcuts for faster experimentation.
- Status logs and research-style telemetry panels.
- Presets for quick visual changes.

---

## Quick Start

### Option 1: Open directly

You can open any `.html` file directly in a modern browser.

```text
double-click 3DNeuralRenderingVisualization.html
````

This works for many features, but some browser APIs, WASM modules, and CDN-loaded scripts behave more reliably through a local server.

### Option 2: Run with a local server

Recommended:

```bash
git clone https://github.com/kai9987kai/Rendering-experiments.git
cd Rendering-experiments
python -m http.server 8000
```

Then open:

```text
http://localhost:8000/
```

Navigate directly to a demo, for example:

```text
http://localhost:8000/3DNeuralRenderingVisualization.html
http://localhost:8000/NeuralShapeForge.html
http://localhost:8000/neural-physics.html
http://localhost:8000/neuralnet-texture-gen.html
http://localhost:8000/loopingvisuals.html
```

---

## Recommended First Demo

Start with:

```text
3DNeuralRenderingVisualization.html
```

It gives the best overall introduction to the repo because it combines:

* neural deformation,
* TensorFlow.js training,
* procedural noise,
* shape switching,
* material switching,
* particle halos,
* ghost trails,
* presets,
* screenshots,
* live backend/loss/FPS telemetry.

For physics, try:

```text
neural-physics.html
```

For texture generation, try:

```text
neuralnet-texture-gen.html
```

For pure visual motion and collision effects, try:

```text
loopingvisuals.html
```

---

## Controls

Controls vary by demo, but common interactions include:

| Input       | Action                                     |
| ----------- | ------------------------------------------ |
| Mouse drag  | Orbit / rotate camera                      |
| Mouse wheel | Zoom                                       |
| `Space`     | Pause / resume                             |
| `R`         | Reset                                      |
| `T`         | Train neural model / field                 |
| `S`         | Apply style / screenshot depending on demo |
| `A`         | Toggle audio in audio-reactive demos       |
| `H`         | Hide/show HUD                              |
| `B`         | Burst effect in visual loop demo           |
| `1-4`       | Camera mode switching in loop demo         |

Most demos also include on-screen buttons and sliders, so the keyboard is optional.

---

## Tech Stack

This repository uses browser-native technologies:

* **HTML5**
* **CSS3**
* **JavaScript**
* **Three.js r128**
* **TensorFlow.js**
* **Simplex Noise**
* **Ammo.js WASM** for physics in `neural-physics.html`
* **Canvas API**
* **WebGL**
* **Web Audio API** in audio-reactive demos
* **LocalStorage** for saved settings/presets in supported demos

No Node.js build system is required.

---

## Project Structure

```text
Rendering-experiments/
├── 3DNeuralRenderingVisualization.html
├── NeuralNoiseShape3D.html
├── NeuralShapeForge.html
├── loopingvisuals.html
├── neural-physics.html
├── neuralnet-texture-gen.html
├── CODE_OF_CONDUCT.md
├── SECURITY.md
├── LICENSE
└── README.md
```

---

## Performance Notes

These demos are GPU-heavy and work best on a desktop browser.

For smoother performance:

* Use Chrome, Edge, or Firefox.
* Run through a local server instead of `file://`.
* Close other GPU-heavy tabs.
* Lower pixel quality where available.
* Reduce particle/star/splat density.
* Turn off shadows, trails, particles, or wireframes if FPS drops.
* Use fewer training epochs or lower batch sizes in TensorFlow.js demos.
* Keep DevTools closed when benchmarking performance.

---

## Troubleshooting

### The screen is blank

Try the following:

1. Open the browser console.
2. Check for CDN loading errors.
3. Serve the repo with `python -m http.server 8000`.
4. Make sure WebGL is enabled.
5. Try another browser.

### TensorFlow.js does not load

Some demos can still run in procedural/fallback mode, but neural features may be disabled. Check your network connection and CDN access.

### Ammo.js physics does not load

`neural-physics.html` includes fallback physics, so the demo should still run. Ammo.js gives better rigid-body physics when available.

### Audio does not start

Most browsers require a user gesture before audio can begin. Click the page or press the audio toggle button.

### FPS is low

Lower the visual quality sliders, disable extra particle effects, reduce splat density, or turn off high-quality mode where available.

---

## Development Notes

The repo is intentionally built as standalone HTML experiments. This makes each file easy to open, copy, remix, or deploy independently.

Good future improvements could include:

* a shared `index.html` launcher page,
* reusable shared utility modules,
* screenshot gallery,
* GitHub Pages deployment,
* mobile performance presets,
* WebGPU experiments,
* shader-based neural fields,
* import/export for more presets,
* automated linting,
* modular JavaScript structure,
* demo thumbnails in the README.

---

## Roadmap Ideas

* [ ] Add a polished gallery launcher for all demos.
* [ ] Add screenshots or GIF previews for each experiment.
* [ ] Add GitHub Pages live demo links.
* [ ] Split common UI/render utilities into shared modules.
* [ ] Add WebGPU renderer experiments.
* [ ] Add shader-based neural field visualizations.
* [ ] Add preset export/import JSON files.
* [ ] Add mobile-friendly low-power modes.
* [ ] Add benchmark mode for FPS and GPU load testing.
* [ ] Add README badges for live demo, version, and last commit.

---

## Contributing

Contributions, experiments, bug fixes, and creative rendering ideas are welcome.

Suggested contribution types:

* new single-file rendering demos,
* improvements to existing demos,
* better controls or UI panels,
* performance optimizations,
* shader experiments,
* accessibility improvements,
* screenshot/GIF documentation,
* bug fixes for browser compatibility.

Before contributing, please read:

* `CODE_OF_CONDUCT.md`
* `SECURITY.md`

---

## Security

This repo is a client-side experimental graphics project. It does not require a backend, login system, database, or secret API keys.

When reporting security issues, follow the guidance in `SECURITY.md`.

Do not commit:

* private API keys,
* tokens,
* credentials,
* personal data,
* generated files containing secrets.

---

## License

This project is licensed under the MIT License.

See `LICENSE` for details.

---

## Author

Created by [kai9987kai](https://github.com/kai9987kai).

Project website: [kai9987kai.co.uk](https://kai9987kai.co.uk/)

```
::contentReference[oaicite:2]{index=2}
```

[1]: https://github.com/kai9987kai/Rendering-experiments "GitHub - kai9987kai/Rendering-experiments: A grab-bag of single-file HTML rendering prototypes exploring “neural-ish” visual ideas in the browser: procedural deformation, toy TensorFlow.js modulation, texture generation experiments, and a physics/collision demo. Everything runs client-side with no build step—just open the .html files (ideally via a local server) · GitHub"
[2]: https://github.com/kai9987kai/Rendering-experiments/blob/main/3DNeuralRenderingVisualization.html "Rendering-experiments/3DNeuralRenderingVisualization.html at main · kai9987kai/Rendering-experiments · GitHub"
