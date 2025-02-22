# Hand Gesture Control

This project implements a hand gesture-based control system using OpenCV and MediaPipe to interact with the system through webcam-based hand tracking. The script allows users to perform various actions like controlling system volume, scrolling, and opening websites using predefined hand gestures.

## Features
- **Volume Control**: Adjust system volume using index finger (increase) and thumb (decrease) gestures.
- **Scrolling**: Use hand gestures to scroll up and down on a page.
- **Media Control**: Open Netflix and YouTube with specific gestures.
- **Gesture Recognition**: Uses MediaPipe to track hand movements and recognize predefined gestures.

## Dependencies
Ensure you have the following Python libraries installed:

```sh
pip install opencv-python mediapipe pyautogui scipy comtypes pycaw numpy pynput keyboard
```

## How to Run
1. Connect a webcam to your computer.
2. Run the script:
   ```sh
   python app.py
   ```
3. Perform the following gestures to trigger actions:
   - **Index Finger Up** → Increase volume
   - **Thumb Up** → Decrease volume
   - **All Fingers Open (FIVE)** → Scroll down
   - **Fist (All Fingers Closed)** → Scroll up
   - **Victory Sign** → Open Netflix (only once per session)
   - **Swag Gesture (Index and Pinky Extended)** → Open YouTube (only once per session)
4. Press 'q' to exit the application.

## Code Breakdown
- **Camera Capture**: Uses OpenCV (`cv2.VideoCapture`) to get video feed.
- **Hand Detection**: MediaPipe's `Hands` module detects hand landmarks.
- **Gesture Interpretation**: Compares finger positions to recognize gestures.
- **System Control**:
  - Volume control uses `pycaw`.
  - Scrolling utilizes `pyautogui`.
  - Web browsing via `webbrowser.open()`.

## Notes
- Ensure proper lighting conditions for accurate gesture recognition.
- Hand gestures should be clear and distinct for proper detection.
- The script prevents multiple launches of Netflix and YouTube in a session.

## License
This project is open-source and available for modification and redistribution.

