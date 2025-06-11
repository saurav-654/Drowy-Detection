# Drowsiness Detection System

A real-time drowsiness detection system using computer vision and facial landmarks detection.

## Description

This project implements a drowsiness detection system that monitors a person's eyes using a webcam and alerts them when signs of drowsiness are detected. It uses facial landmark detection to analyze eye movements and blinking patterns.

## Features

- Real-time face detection
- Eye blink monitoring
- Three states detection:
  - Active (Not Sleeping)
  - Drowsy
  - Sleeping
- Audio alert when sleeping is detected
- Visual status display with color coding:
  - Green: Active
  - Red: Drowsy
  - Blue: Sleeping

## Prerequisites

- Python 3.x
- Required Python packages:
  ```
  opencv-python
  numpy
  dlib
  imutils
  playsound
  ```
- shape_predictor_68_face_landmarks.dat (facial landmark predictor model)

## Installation

1. Clone the repository
2. Install the required packages:
   ```
   pip install opencv-python numpy dlib imutils playsound
   ```
3. Download the `shape_predictor_68_face_landmarks.dat` file
4. Update the path to your alarm sound file in the code

## Usage

Run either of the following files:
```
python drowy.py
```
or
```
python main.py
```

Press 'ESC' to exit the program.

## How It Works

1. The system captures video from your webcam
2. Detects faces in each frame
3. Identifies facial landmarks, particularly around the eyes
4. Calculates the eye aspect ratio (EAR) to detect blinks
5. Monitors blinking patterns to determine drowsiness level
6. Triggers an alarm if sleeping is detected

## Project Structure

- `drowy.py` / `main.py` - Main program files
- `shape_predictor_68_face_landmarks.dat` - Facial landmark predictor model
- `Alarm-Fast-A1-www.fesliyanstudios.com.mp3` - Alert sound file

## License

This project is open source and available under the MIT License.
