# Rendering-experiments

A grab-bag of **single-file HTML rendering prototypes** exploring “neural-ish” visual ideas in the browser: procedural deformation, toy TensorFlow.js modulation, texture generation experiments, and a physics/collision demo. Everything runs client-side with **no build step**—just open the `.html` files (ideally via a local server). :contentReference[oaicite:0]{index=0}

## What’s inside

This repository is currently **HTML-only** and consists of several standalone demos: :contentReference[oaicite:1]{index=1}

- `3DNeuralRenderingVisualization.html` — 3D scene + animated mesh deformation + “neural” noise modulation.
- `NeuralNoiseShape3D.html` — rotating 3D shape with procedural + neural-modulated noise.
- `NeuralShapeForge.html` — interactive demo with UI buttons (train / style transfer / audio toggle).
- `neural network based texture generation.html` — experimental neural-ish texture generation pipeline.
- `neural-physics.html` — 3D demo with physics + collisions + the same UI controls.

(Exact filenames are as listed in the repo.) :contentReference[oaicite:2]{index=2}

## Requirements

- A modern desktop browser (Chrome/Edge/Firefox).
- Recommended: run via a local HTTP server (some browser APIs + WASM loads behave better than `file://`).  
- No package manager required.

## Run locally

### Option A — quick open
You *can* double-click any `.html` file and open it in your browser.

### Option B — local server (recommended)
From the repo folder:

**Python**
```bash
python -m http.server 8000
````

Then open:

* `http://localhost:8000/`

Click the demo you want (or navigate directly to the file URL).

## Controls (varies per demo)

Some demos include on-page UI buttons such as:

* **Train Network** — runs a small TensorFlow.js training step (toy model).
* **Apply Style Transfer** — applies a visual/material “style” tweak.
* **Toggle Audio** — enables/disables an audio layer (typically Web Audio oscillator).

(Only present in the “Forge” / “physics” style pages.)

## Notes / gotchas

* These are **experiments/prototypes**: “neural” elements are intentionally lightweight (often a tiny model used to modulate parameters rather than a full ML pipeline).
* If a demo appears blank:

  * open DevTools Console for CDN load errors,
  * try serving over HTTP (not `file://`),
  * ensure your browser allows WebGL and (if used) WASM.

## License

No license file is currently included; add one (MIT/Apache-2.0/etc.) if you want clear reuse terms. ([GitHub][1])

```
::contentReference[oaicite:4]{index=4}
```

[1]: https://github.com/kai9987kai/Rendering-experiments "GitHub - kai9987kai/Rendering-experiments"
