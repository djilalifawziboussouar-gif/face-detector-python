<h1 align="center" id="title">face-detector-python</h1>

<p align="center"><img src="https://socialify.git.ci/djilalifawziboussouar-gif/face-detector-python/image?description=1&amp;font=KoHo&amp;language=1&amp;name=1&amp;owner=1&amp;pattern=Circuit+Board&amp;theme=Light" alt="project-image"></p>

<p id="description">Here's a short description (~6 lines): **Face Detector (Python + OpenCV)** is a lightweight real-time face detection project that uses your webcam to detect faces and draw bounding boxes around them. Built with Python and OpenCV's Haar cascade classifier it requires no extra model downloads. Each frame is converted to grayscale and scanned with `detectMultiScale` to locate faces. Press `q` `Esc` or close the window to quit. All processing happens locally — no frames are saved or sent anywhere. Simple to install easy to run and a great starting point for computer vision beginners.</p>

# Face Detector (Python + OpenCV)

Real-time face detection from a webcam using OpenCV and a Haar cascade classifier.

![demo](assets/demo.gif)

## Features
- Live webcam face detection with bounding boxes
- Quit with `q`, `Esc`, or by closing the window
- Uses the cascade file bundled with OpenCV (no extra downloads)

## Requirements
- Python 3.8+
- A webcam

## Installation
```bash
git clone https://github.com/<your-username>/face-detector-python.git
cd face-detector-python
python -m venv .venv
# Windows: .venv\Scripts\activate    macOS/Linux: source .venv/bin/activate
pip install -r opencv-python
```

## Usage
```bash
python face_detector.py
```

## How it works
1. Each frame is read from the webcam and converted to grayscale.
2. `detectMultiScale` scans the image at multiple scales with a Haar cascade
   (Viola-Jones: Haar-like features + AdaBoost in a cascade of stages).
3. A rectangle is drawn around every detected face.

### Parameters
- `scaleFactor=1.3`: image shrink at each scale (smaller = more accurate, slower)
- `minNeighbors=6`: higher = fewer false positives, but may miss faces

## Limitations
Haar cascades work best on frontal, well-lit faces and can miss tilted or partly hidden ones.

## Roadmap
- [ ] Compare with MediaPipe / YuNet
- [ ] Show FPS on screen
- [ ] Command-line options for camera and parameters

## Privacy
Frames are processed locally and are not saved or sent anywhere.

