# Face Detector (Python + OpenCV)

Real-time face detection from a webcam using OpenCV and a Haar cascade classifier.


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
pip install opencv-python
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
