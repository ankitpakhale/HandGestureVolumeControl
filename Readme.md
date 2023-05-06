# Hand Gesture Volume Control

**Note: This code will only run in Python versions below 3.10 due to compatibility issues with the mediapipe library.**

## Purpose

The code uses OpenCV, NumPy, and PyCaw libraries to detect hand gestures and control system volume. It uses hand tracking module to track hand landmarks and calculates volume level based on the distance between thumb tip and index finger tip, and displays a real-time graphical interface, including a volume bar and the current volume percentage.

## Installation

1. Ensure you have Python installed on your system.
2. Install the necessary dependencies by running the following command: `pip install mediapipe opencv-python comtypes numpy pycaw`

## Usage

1. Connect an audio output device (e.g., speakers or headphones) to your computer.
2. Run the project by executing the following command: `python HandGestureVolumeControl.py`
3. A video window will open, displaying the live camera feed.
4. Make a fist with your hand and extend your thumb and index finger to resemble a "pinch" gesture.
5. Move your hand closer or further away from each other to control the volume level.
6. The current volume percentage will be displayed on the screen.
7. To exit the program, press 'q' on your keyboard.

## Code Structure

The code can be divided into the following sections:

1. Importing Dependencies: The necessary libraries and modules are imported, including `comtypes`, `cv2` (OpenCV), `time`, `math`, `numpy`, `HandTrackingModule`, and `pycaw` (Python Core Audio Windows).

2. Setting up the Webcam: The code configures the webcam, sets the frame dimensions, and initializes variables for processing the video stream.

3. Initializing Hand Detection: An instance of the `HandTrackingModule` class is created to detect and track hand gestures in the video frames.

4. Obtaining Audio Endpoint: The code retrieves the audio output device (speakers) using the `pycaw` library.

5. Volume Control Loop: The main loop captures video frames from the webcam and performs the following operations:

- Detects and tracks the user's hand in the frame using the hand detection module.
- Calculates the distance between the thumb and index finger.
- Maps the hand distance to the volume range and adjusts the volume level accordingly using the audio endpoint interface.
- Updates the volume bar and percentage display on the screen.
- Changes the color of the volume bar and percentage based on the current volume level.
- Calculates and displays the frames per second (FPS) on the screen.
- Displays the processed frame in a window.
- Breaks the loop if the user presses the 'q' key.

6. Cleanup: The code releases the webcam and closes all open windows when the program ends.

This code is designed to provide a basic example of hand gesture volume control. It can be extended and customized as needed to fit specific requirements.

## Known Issues

- The code assumes a single hand in the frame and may not work correctly with multiple hands.

## License

This project is licensed under the [MIT License](LICENSE).

For more information, please refer to the [license file](LICENSE).

For questions or support, please contact [Ankit Pakhale](mailto:akp3067@gmail.com).
