# JETWAY — Browser Flight Racer

A small Three.js flight-racing prototype inspired by a jet racing through a steel-frame tunnel.

## Run locally

This is a static site. From the project root:

```bash
python -m http.server 8000
```

Open http://localhost:8000. An internet connection is required to load Three.js from jsDelivr.

## Controls

- **A / D** or **← / →**: steer
- **W / S** or **↑ / ↓**: adjust speed
- **Shift** or **Space**: afterburner boost
- **P**: pause / resume
- **R**: reset the run

Lap timing and the best lap are kept in the browser; the fastest lap uses local storage.

## GitHub Pages

1. Open **Settings → Pages**.
2. Under **Build and deployment**, choose **GitHub Actions** as the source.
3. The workflow at `.github/workflows/deploy-pages.yml` publishes the root folder after pushes to `main`. It can also be run manually from **Actions**.

For a **private repository**, GitHub Pages availability and site visibility depend on your GitHub plan and Pages visibility settings. The website can be accessible to anyone even if the source repository stays private, depending on those settings.

## Blender / model handoff

The aircraft, road, and tunnel are generated procedurally so they can be replaced incrementally. A natural next step is to export a jet model from Blender as `.glb` and load it with Three.js' `GLTFLoader`. Keep the gameplay, camera, HUD, and model-loading code separate as the prototype grows.
