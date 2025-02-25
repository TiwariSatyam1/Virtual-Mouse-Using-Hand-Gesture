Virtual Mouse Using Hand Gesture

Overview

This project implements a virtual mouse that allows users to control their computer cursor using hand gestures detected via a webcam. It utilizes OpenCV for video processing, Mediapipe for hand tracking, and PyAutoGUI for controlling the cursor.

Features

Tracks hand movements using a webcam.

Moves the cursor based on the index finger's position.

Performs a mouse click when the index finger and thumb come close together.

Provides real-time hand gesture recognition and cursor control.

Requirements

To run this project, ensure you have the following dependencies installed:

pip install opencv-python mediapipe pyautogui

How It Works

The webcam captures video frames.

Mediapipe detects hand landmarks in the video.

The index finger's position is used to move the cursor.

If the index finger and thumb come close, a click event is triggered.

The program runs in real-time and continuously updates cursor movements.

Usage

Run the script using:

python virtual_mouse.py

Make sure your webcam is enabled.

Key Functions

cv2.VideoCapture(0): Captures video from the webcam.

mp.solutions.hands.Hands(): Detects hand landmarks.

pyautogui.moveTo(x, y): Moves the cursor to the calculated position.

pyautogui.click(): Triggers a mouse click when the index finger and thumb come close.

Customization

Adjust the sensitivity of the click gesture by modifying the distance threshold in the condition if abs(index_y - thumb_y) < 20:.

Modify cursor movement speed by tweaking the scaling factor of index_x and index_y.

Known Issues

The accuracy of hand tracking may vary depending on lighting conditions and webcam quality.

The cursor movement may not be smooth if the hand is not detected properly.

Future Improvements

Add scrolling and right-click functionality using additional gestures.

Improve gesture recognition for more precise control.

Implement multi-hand tracking for extended functionality.

License

This project is open-source and available for modification and distribution.

Author

Developed by [Your Name]
