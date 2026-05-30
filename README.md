# Air Handwriting

Draw on screen using only your hand and a webcam—no mouse or stylus required.

This project uses [MediaPipe Hands](https://developers.google.com/mediapipe/solutions/vision/hand_landmarker) to track your hand in real time. Your index fingertip acts as a cursor; hold **Shift** to paint smooth golden strokes on a dark canvas. Press **Space** to clear everything.

## Demo

Open `is.html` in a modern browser, allow camera access, and start drawing in the air.

## Features

- Real-time hand tracking via webcam  
- Index-finger cursor with smoothing for steady lines  
- Draw while holding **Shift**; release to stop  
- Hand skeleton overlay for feedback  
- Mirrored view for natural movement  
- Golden glow strokes on a dark background  
- Single HTML file—no build step or server  

## Controls

| Input | Action |
|-------|--------|
| **Shift** (hold) | Draw while moving your index finger |
| **Space** | Clear all strokes |

## Getting started

### Prerequisites

- A modern browser (Chrome or Edge recommended)  
- A working webcam  
- Camera access (use `localhost` or HTTPS when opening the file)

### Run locally

1. Clone the repository:
   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPO.git
   cd YOUR_REPO
   ```
2. Open `is.html` in your browser (double-click or drag into a tab).
3. Allow camera permissions when prompted.
4. Point with your index finger, hold **Shift** to draw, press **Space** to reset.

## How it works

1. The webcam feed is processed frame by frame with MediaPipe Hands.  
2. Landmark **8** (index fingertip) maps to screen coordinates.  
3. Cursor position is smoothed so strokes stay steady.  
4. While **Shift** is held, points are added to the current stroke and rendered on canvas.  
5. Completed strokes are stored so they persist until you press **Space**.

## Tech stack

- HTML5 Canvas  
- Vanilla JavaScript  
- [@mediapipe/hands](https://www.npmjs.com/package/@mediapipe/hands)  
- [@mediapipe/camera_utils](https://www.npmjs.com/package/@mediapipe/camera_utils)  
- [@mediapipe/drawing_utils](https://www.npmjs.com/package/@mediapipe/drawing_utils)  

Dependencies are loaded from [jsDelivr](https://www.jsdelivr.com/)—no `npm install` required.

## Project structure

```
.
└── is.html    # Full app (HTML, CSS, and JavaScript)
```

## Author

**Matin Kafashian**

## License

This project is open source. Add your preferred license (e.g. MIT) if you plan to share it publicly.

---

Copy this into a `README.md` in your repo and replace `YOUR_USERNAME` / `YOUR_REPO` with your GitHub details. If you want this file created in the project automatically, switch to **Agent mode** and ask me to add it.
