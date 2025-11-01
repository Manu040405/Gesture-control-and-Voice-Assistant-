# Gesture Recognition System 👋🖱️

An AI-powered virtual mouse system enabling hands-free computer control through intuitive hand gestures captured via webcam.

## ✨ Features

### 🖐️ Complete Gesture Control Suite
- **Move Cursor**: Natural hand movement translates to cursor position
- **Left Click**: Index finger gesture for primary click action
- **Right Click**: Two-finger gesture for context menu access
- **Double Click**: Quick gesture for opening files and folders
- **Scrolling**: Fist gesture with vertical motion for page navigation
- **Drag and Drop**: Grab and move gesture for file manipulation
- **Multiple Item Selection**: Extended gesture for selecting multiple objects
- **Volume Control**: Pinch gesture to adjust system volume
- **Brightness Control**: Dedicated gesture for screen brightness adjustment

### 🎯 Advanced Capabilities
- **Real-Time Processing**: 25-35 FPS gesture recognition using MediaPipe
- **High Accuracy**: Achieves 92-97% gesture recognition in controlled environments
- **Contactless Operation**: Completely touch-free interaction with your computer
- **Accessibility-Focused**: Designed for specially-abled individuals with hand mobility limitations

## 🛠️ Technologies Used

- **Python 3.8.5**: Core programming language
- **OpenCV**: Computer vision for video capture and processing (BGR format)
- **MediaPipe**: Advanced hand tracking with 21 landmark detection
  - Palm Detection Model
  - Hand Landmark Model
- **PyAutoGUI**: Mouse control automation

## 🔬 How It Works

### Hand Tracking Pipeline

1. **Video Capture**: Webcam captures real-time video in BGR format via OpenCV
2. **Palm Detection**: MediaPipe's palm detection model identifies hand presence
3. **Landmark Tracking**: Hand landmark model renders 21 coordinates in 2.5D space
4. **Gesture Recognition**: 
   - IDs assigned to each finger tip and knuckle
   - Coordinates calculated for all landmark points
   - Operations performed based on distances and angles between points
5. **Action Execution**: Recognized gestures translated to mouse functions

### Example: Left Click Detection
- **Frame 1**: Index finger (Tip ID 1) and middle finger (Tip ID 2) must be extended upward
- **Frame 2**: Index finger (Tip ID 1) moves down while middle finger (Tip ID 2) stays up
- **Trigger Condition**: Both fingers produce an angle greater than 33.5°

## 🤲 Gesture Controls

### Cursor Movement
- **Gesture**: Move your hand naturally in the air
- **Action**: Cursor follows hand position on screen
- **Note**: Coordinates mapped from hand space to screen space

### Click Operations

| Gesture | Description | Action |
|---------|-------------|--------|
| **Neutral Gesture** | Natural hand position | Move cursor |
| **Index Finger Up** | Extend index finger alone | Left click |
| **Index + Middle Finger Up** | Extend two fingers | Right click |
| **Rapid Index Gesture** | Quick index finger extension twice | Double click |

### Advanced Gestures

| Gesture | Description | Action |
|---------|-------------|--------|
| **Closed Fist** | All fingers folded | Drag and drop / Scroll mode |
| **Pinch (Thumb + Index)** | Bring thumb and index together | Volume control |
| **Three Finger Pinch** | Thumb, index, and middle pinch | Brightness control |
| **Open Palm (5 fingers)** | All fingers extended | Multiple selection / Cancel |

## 📦 Installation

### Prerequisites
- Python 3.8.5
- Webcam (minimum 1.3 megapixel resolution)
- Windows/Linux/MacOS

### Step 1: Create Virtual Environment
```bash
conda create --name gest python=3.8.5
conda activate gest
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Run the Application
```bash
python Gesture_Controller.py
```

## 📋 System Requirements

### Minimum Hardware
- **Webcam**: 1.3 megapixel resolution, 30 FPS
- **Processor**: Intel Core2Duo (2nd generation) or equivalent
- **RAM**: 2GB (4GB recommended)
- **Hard Disk**: 320GB
- **OS**: Windows 10+, Linux, or MacOS

### Software Dependencies
```
opencv-python>=4.5.0
mediapipe>=0.8.0
numpy>=1.19.0
pyautogui>=0.9.52
```

## 🎯 Applications & Use Cases

### Accessibility
- Assistance for individuals with limited hand mobility
- Alternative input method for specially-abled users
- Reduced physical stress and prevention of repetitive strain injuries

### Health & Safety
- **COVID-19 Safe**: Contactless operation eliminates shared surface contact
- **Ergonomic**: Reduces back pain, posture defects from prolonged mouse use
- **Eye Strain Reduction**: Natural hand movements promote better posture

### Professional Applications
- **Sterile Environments**: Medical and laboratory settings
- **Distance Control**: Robotics, classrooms, military applications
- **AR/VR Integration**: Virtual and augmented reality gaming
- **Presentations**: Hands-free control during demonstrations

## 🔄 Data Flow

```
Webcam Input → OpenCV Capture (BGR) → MediaPipe Processing
                                            ↓
                                   Palm Detection Model
                                            ↓
                                   Hand Landmark Model (21 points)
                                            ↓
                                   Coordinate Calculation
                                            ↓
                            Angle & Distance Computation
                                            ↓
                                   Gesture Classification
                                            ↓
                                   PyAutoGUI Execution
                                            ↓
                                   Mouse Action Performed
```

## 🐛 Troubleshooting

### Poor Hand Detection
- **Solution**: Ensure proper lighting (avoid backlighting)
- **Tip**: Use plain background for better detection
- **Note**: Works best with different hand complexions in well-lit conditions

### Cursor Jitter/Instability
- **Solution**: Increase smoothing factor in configuration
- **Tip**: Keep hand steady at comfortable distance from camera (50-100 cm)

### Performance Lag
- **Solution**: Close resource-intensive applications
- **Advanced**: Reduce frame rate or use lower resolution

### Gesture Not Recognized
- **Solution**: Ensure fingers are clearly visible and not overlapping
- **Tip**: Practice gestures slowly to understand trigger angles
- **Note**: Some gestures require specific angle thresholds (e.g., 33.5° for left click)

## 🚀 Future Enhancements

- **Enhanced Window Management**: Enlarge, shrink, and close windows using palm gestures
- **Multi-Finger Gestures**: Complex actions using 3-5 finger combinations
- **Lighting Adaptation**: Better detection across various lighting conditions
- **Distance Flexibility**: Recognition at varying distances from camera
- **Skin Tone Invariance**: Improved detection across different hand complexions
- **Two-Hand Support**: Simultaneous detection of both hands for advanced control

## 🤝 Contributing

We welcome contributions to improve the gesture recognition system!

### How to Contribute
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingGesture`)
3. Implement your changes with proper documentation
4. Test thoroughly across different conditions
5. Submit a pull request with detailed description

### Areas for Contribution
- New gesture patterns
- Performance optimization
- Cross-platform compatibility
- Accessibility features
- Documentation improvements

## 📚 References

This project builds upon research in Human-Computer Interaction (HCI):

- **S. Shriram et al. (2021)**: "Machine Learning based real-time AI Virtual Mouse system using computer vision to avoid COVID-19 spread"
- **Hritik Joshi et al. (2022)**: "Towards controlling mouse through hand gestures: A novel and efficient approach"
- **N. Subhash Chandra et al. (2015)**: "A Real-Time Static & Dynamic Hand Gesture Recognition System"

## 📜 License

This project uses open-source libraries with the following licenses:
- OpenCV: Apache 2.0
- MediaPipe: Apache 2.0
- PyAutoGUI: BSD License

## 📞 Contact & Support

- **Issues**: Report bugs or request features via GitHub Issues
- **Discussions**: Join our community forum for help and ideas
- **Documentation**: Check the wiki for detailed guides

---

**🌟 Star this repo if you find it useful!**

**Built with ❤️ for accessible, contactless human-computer interaction**
