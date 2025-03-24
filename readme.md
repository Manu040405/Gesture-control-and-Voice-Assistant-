# Gesture Recognition and Voice Control System 👋🎤🖱️

An AI-based virtual mouse system enabling hands-free computer control through hand gestures and voice commands.

## ✨Features

- **🖐️Gesture-Based Control**: Control cursor movements and clicks using hand gestures
- **🎙️Voice Command Integration**: Execute system-level commands through speech recognition
- **♿Accessibility-Focused**: Designed to enhance computer accessibility for specially-abled individuals
- **⚡Real-Time Processing**: Utilizes MediaPipe for efficient hand tracking and OpenCV for gesture recognition

## 🛠️ Technologies Used

- Python 3.8.5
- MediaPipe (Hand tracking)
- OpenCV (Computer vision)
- Speech Recognition
- PyAudio (Audio processing)

## Installation, Setup, and Execution

### Step 1: Create a virtual environment
```bash
conda create --name gest python=3.8.5
```

### Step 2: Activate the virtual environment
```bash
conda activate gest
```

### Step 3: Install the required libraries
```bash
pip install -r requirements.txt
```

### Step 4: Install PyAudio and pywin32
```bash
conda install PyAudio
conda install pywin32
```

### Step 5: Run the Gesture Controller
```bash
python Gesture_Controller.py
```

### Step 6: Run the Voice-based control
```bash
python Jerry.py
```

## 🤲Gesture Controls

- **Hand Movement**: Move your hand to control cursor position
- **Index Finger Extension**: Left click
- **Index and Middle Finger Extension**: Right click
- **Fist Gesture**: Grab and scroll
- **Open Palm**: Release/cancel action

## 🎙️ Voice Commands

- **System Controls**: "Copy", "Paste", "Cut", "Select All", "Save"
- **Application Controls**: "Open Chrome", "Open Word", "Close Window"
- **Navigation**: "Scroll Up", "Scroll Down", "Go Back", "Refresh"
- **Media Controls**: "Play", "Pause", "Volume Up", "Volume Down"

## 🔄How It Works

The system consists of two primary components:

1. **Gesture Controller**:
   - Captures video input from your webcam
   - Tracks hand landmarks using MediaPipe
   - Translates hand positions and gestures into mouse controls
   - Interprets specific hand configurations as click or scroll actions

2. **Voice Command System**:
   - Continuously listens for audio input
   - Converts speech to text using speech recognition
   - Matches recognized text against command library
   - Executes corresponding system actions via keyboard/mouse simulation

## 👥 Use Cases

- Accessibility assistance for individuals with limited mobility
- Hands-free computing in sterile environments (medical settings)
- Convenient multitasking during presentations or cooking
- Educational tools for interactive learning

## Requirements

See `requirements.txt` for a complete list of dependencies. Key requirements include:
- opencv-python
- mediapipe
- numpy
- pyautogui
- SpeechRecognition
- PyAudio
- pywin32

## Troubleshooting

- **Hand detection issues**: Ensure proper lighting and hand visibility
- **Voice recognition problems**: Check microphone settings and environmental noise
- **Performance lag**: Close resource-intensive applications while running the system

## 🤝Contributing

Contributions to improve the system are welcome. Please feel free to submit a pull request or open an issue for discussion.

## 📞Contact

For questions or support, please reach out to the project maintainers or open an issue on GitHub.
