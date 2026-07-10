# VigilEye — Real-Time Object Detection Web App

A Flask-based web application for real-time object detection using YOLOv8, supporting both live webcam streaming and uploaded video file analysis.

## Features
- Live webcam object detection (runs locally)
- Upload video files (mp4, avi, mov, mkv) for detection
- Detects: person, backpack, handbag, suitcase, bottle
- Real-time bounding boxes with confidence scores
- Browser-based MJPEG video streaming

## Tech Stack
- Backend: Flask
- Detection Model: YOLOv8 (Ultralytics)
- Computer Vision: OpenCV
- Frontend: HTML, CSS, JavaScript

## Project Structure

```
├── app.py                 # Main Flask application
├── requirements.txt        # Python dependencies
├── yolov8n.pt              # YOLOv8 nano model weights
├── Procfile                # Deployment start command
├── static/
│   ├── css/                 # Stylesheets
│   ├── gifs/                 # Demo animations
│   └── images/               # UI images
├── templates/
│   ├── base.html
│   ├── index.html
│   ├── theory.html
│   ├── detection_menu.html
│   ├── upload_detect.html
│   ├── play_uploaded.html
│   └── live_detect.html
└── uploads/                # User-uploaded videos (runtime, gitignored)

```

## Setup & Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/realtime-object-detection-yolov8.git
cd realtime-object-detection-yolov8
```

3. Install dependencies
```bash
pip install -r requirements.txt
```

4. Run the app
```bash
python app.py
```

5. Open your browser at `http://127.0.0.1:5000`

## Notes
- Live webcam detection requires running the app locally (needs direct hardware access to a webcam) — this is not available in any hosted/cloud deployment.
- Cloud deployment was tested on Render; free-tier hosting (512MB RAM) is insufficient for the torch + YOLOv8 memory footprint, so the app is intended to run locally for evaluation and demo purposes.

## Author
Pavithra Sharma