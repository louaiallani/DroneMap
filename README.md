# DroneMap

DroneMap is a browser-based drone simulation that blends a realistic quadcopter feel with real satellite imagery.

![Uploading image.png…]()


## Big Idea

What if one drone could scan the entire Earth and collect every visible detail of our planet?

That is the core thesis behind this project:
- Use existing satellite imagery as the world foundation.
- Simulate one persistent drone platform that can move, scan, and detect objects.
- Treat the whole Earth like a giant, continuously explorable data surface.

## Reality Check (The Hard Part)

The vision is exciting, but it runs into real limits fast:
- Compute: world-scale analysis would require massive GPU/TPU power.
- Storage: keeping high-detail global data is extremely expensive.
- Throughput: ingesting and processing planet-scale imagery is a huge data pipeline challenge.
- Latency: real-time detection and synchronization across global regions is non-trivial.

In short: conceptually possible, operationally very demanding.

## What This Demo Does

This project gives you a focused, fun sandbox version of that idea:
- Pilots a detailed 3D quadcopter over a Leaflet satellite map.
- Uses smooth drone-like movement physics instead of arcade instant motion.
- Runs COCO-SSD object detection from a webcam source.
- Draws detection overlays in a compact mission-style UI.

## Controls

- W / S: Forward / backward
- A / D: Strafe left / right
- Q / E: Yaw left / right
- R / F (or PageUp / PageDown): Altitude up / down

## Tech Stack

- HTML, CSS, JavaScript (no framework)
- Three.js for 3D rendering
- Leaflet for geospatial map rendering
- TensorFlow.js + COCO-SSD for object detection

## Why It Is Cool

You are flying a cinematic drone over real map tiles while live AI detection runs in the same interface.

It is part simulator, part geospatial experiment, and part thought experiment about what Earth-scale sensing systems could become.

## Quick Start

1. Open index.html in a modern browser.
2. Allow camera access when prompted.
3. Click CONNECT CAMERA.
4. Fly the drone and watch detections update live.

## Next Evolution

If you wanted to push this toward the full thesis, likely steps are:
- Multi-drone orchestration instead of a single vehicle.
- Tiled global chunking and hierarchical storage.
- Distributed inference pipelines.
- Smarter caching and regional prioritization strategies.

This repo is the first fun step in that direction.
