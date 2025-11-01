# Gesture Recognition System 👋🖱️

An AI-powered virtual mouse system enabling hands-free computer control through intuitive hand gestures.

## ✨ Features

- **🖐️ Gesture-Based Control**: Control cursor movements and execute clicks using hand gestures
- **♿ Accessibility-Focused**: Designed to enhance computer accessibility for specially-abled individuals
- **⚡ Real-Time Processing**: Utilizes MediaPipe for efficient hand tracking and OpenCV for gesture recognition
- **🎯 High Accuracy**: Achieves 92-97% gesture recognition accuracy in controlled environments

## 🛠️ Technologies Used

- Python 3.8.5
- MediaPipe (Hand tracking)
- OpenCV (Computer vision)
- PyAutoGUI (Mouse control automation)

## 📦 Installation

### Step 1: Create a virtual environment
```bash
conda create --name gest python=3.8.5
conda activate gest
```

### Step 2: Install dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Run the application
```bash
python Gesture_Controller.py
```

## 🤲 Gesture Controls

| Gesture | Action |
|---------|--------|
| Move hand | Move cursor across the screen |
| Index finger extended | Left click |
| Middle finger extended | Right click |
| Quick double index motion | Double click |
| Closed fist | Drag and drop / Scroll |
| Open palm (5 fingers) | Cancel or reset current action |
| Pinch (Thumb + Index Up/Down) | Increase or decrease system volume |
| Pinch (Thumb + Index Left/Right) | Increase or decrease screen brightness |
| Left index + thumb pinch | Zoom in or zoom out (adjust page size) |

## 🔄 How It Works

The system captures video input from your webcam and processes it through a computer vision pipeline:

1. **Video Capture**: Acquires real-time video stream from webcam
2. **Hand Detection**: MediaPipe tracks 21 hand landmarks with sub-pixel accuracy
3. **Gesture Recognition**: Analyzes hand configurations to identify specific gestures
4. **Action Execution**: Translates recognized gestures into corresponding mouse actions

## 👥 Use Cases

- Accessibility assistance for individuals with limited mobility
- Hands-free computing in sterile environments (medical/lab settings)
- Convenient multitasking during presentations or cooking
- Touchless public kiosk interfaces

## 📋 Requirements

**Hardware:**
- Webcam (720p, 30 FPS minimum)
- Intel i5/AMD Ryzen 5 or equivalent
- 4GB RAM (8GB recommended)

**Software:**
- opencv-python
- mediapipe
- numpy
- pyautogui

## 🐛 Troubleshooting

- **Poor detection**: Ensure proper lighting and clear hand visibility
- **Cursor jitter**: Increase smoothing factor in configuration
- **Performance lag**: Close resource-intensive applications or reduce frame rate

**Built for accessible, intuitive human-computer interaction** ❤️

