<h1>Eye Controlled Mouse using MediaPipe and OpenCV</h1>
<h2>Introduction</h2>
<p>This Python script demonstrates how to create an eye-controlled mouse using MediaPipe and OpenCV libraries. The script tracks facial landmarks, particularly eye movements, to control the mouse cursor on the screen. When the user blinks or maintains a specific eye gesture, it simulates a mouse click action.<p>

Prerequisites
Ensure you have the following libraries installed:

OpenCV (cv2)
MediaPipe (mediapipe)
PyAutoGUI (pyautogui)
You can install these libraries using pip:

pip install opencv-python mediapipe pyautogui

Eye Controlled Mouse using MediaPipe and OpenCV
Introduction
This Python script demonstrates how to create an eye-controlled mouse using MediaPipe and OpenCV libraries. The script tracks facial landmarks, particularly eye movements, to control the mouse cursor on the screen. When the user blinks or maintains a specific eye gesture, it simulates a mouse click action.

Prerequisites
Ensure you have the following libraries installed:

OpenCV (cv2)
MediaPipe (mediapipe)
PyAutoGUI (pyautogui)
You can install these libraries using pip:

bash
Copy code
pip install opencv-python mediapipe pyautogui
How it Works
The script captures video frames from the webcam using OpenCV (cv2.VideoCapture).
MediaPipe's FaceMesh model is used to detect and track facial landmarks in the video frames.
The script identifies specific landmarks corresponding to the eyes and calculates their positions relative to the screen.
PyAutoGUI is used to control the mouse cursor based on the eye movements.
If the vertical distance between certain eye landmarks falls below a threshold, it triggers a mouse click simulation.
Code Explanation
import cv2: Imports the OpenCV library for video capture and processing.
import mediapipe as mp: Imports MediaPipe library for face mesh detection.
import pyautogui: Imports PyAutoGUI for controlling the mouse cursor.
cam = cv2.VideoCapture(0): Initializes the webcam capture.
face_mesh = mp.solutions.face_mesh.FaceMesh(refine_landmarks=True): Initializes the MediaPipe FaceMesh model for landmark detection.
screen_w, screen_h = pyautogui.size(): Gets the screen size for mouse control.
The script enters a continuous loop to process each frame from the webcam.
Facial landmarks are detected and extracted from the current frame.
Eye landmarks are used to calculate the position of the mouse cursor.
Mouse cursor movement is simulated based on the eye movements.
If a specific eye gesture (e.g., blinking) is detected, a mouse click is simulated using PyAutoGUI.
The processed frame with visualizations is displayed using OpenCV (cv2.imshow).
cv2.waitKey(1) waits for a key press to exit the loop.
Conclusion
This script demonstrates a basic implementation of an eye-controlled mouse using MediaPipe, OpenCV, and PyAutoGUI. It captures facial landmarks, particularly those corresponding to the eyes, to control the mouse cursor on the screen. Additional improvements and optimizations can be made to enhance the accuracy and responsiveness of the eye-controlled mouse.

