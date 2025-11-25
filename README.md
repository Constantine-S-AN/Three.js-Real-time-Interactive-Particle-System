# Three.js Real-time Interactive Particle System

Gesture-driven particle sculpture built with Three.js (r128), MediaPipe Hands, and Tailwind via CDNs. The page renders ~18k GPU-accelerated particles that morph into multiple shapes and react to your pinch (thumb–index) distance in real time through the webcam feed.

## Features
- Multiple particle presets: heart, flower, saturn, buddha, fireworks, sphere.
- Hand-tracking pinch controls for collapse/expand effects; dynamic rotation and breathing noise.
- Color picker for live particle tinting.
- Mini mirrored webcam overlay with skeleton landmarks; fullscreen toggle.
- Zero build tooling: single `index.html` served from CDNs.

## Quick Start (local)
```bash
git clone https://github.com/Constantine-S-AN/Three.js-Real-time-Interactive-Particle-System.git
cd Three.js-Real-time-Interactive-Particle-System
python3 -m http.server 8000
```
Open http://localhost:8000 and allow camera access when prompted. (Most browsers block `getUserMedia` on `file://`; a local server is required.)

## Controls
- **Shapes:** Click a preset button (heart/flower/saturn/buddha/fireworks/sphere).
- **Color:** Use the color picker; value is shown alongside.
- **Pinch gesture:** Thumb–index distance controls collapse/expansion strength; UI meter shows the normalized value.
- **Fullscreen:** Click “全屏模式”.

## Tech Notes
- All dependencies are loaded from CDNs; no install/build step needed.
- Works best on Chrome/Edge; ensure good lighting for stable hand tracking.
- For remote hosting with webcam access, serve over HTTPS.

## Files
- `index.html` — full demo (Three.js scene, MediaPipe Hands integration, UI).
