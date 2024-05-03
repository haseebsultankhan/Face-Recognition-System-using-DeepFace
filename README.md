# Face Recognition System using DeepFace

This project implements a real-time face recognition system using the DeepFace library in Python. The system captures video from a webcam, detects faces in the video frames, and matches them against a reference image using DeepFace's facial recognition capabilities.

## Requirements

- Python 3.x
- OpenCV (`cv2` library)
- DeepFace library

## Installation

1. Install Python 3.x from the [official Python website](https://www.python.org/downloads/).
2. Install OpenCV library using `pip install opencv-python`.
3. Install DeepFace library using `pip install deepface`.

## Usage

1. Clone or download the project repository.
2. Replace the `reference.jpg` file with your own reference image. This image will be used as the template for face matching.
3. Run the Python script `main.py`
4. The webcam will be activated, and the system will start capturing video.
5. As faces are detected in the video frames, the system will compare them against the reference image.
6. If a match is found, the system will display "MATCH!" on the video frame; otherwise, it will display "NO MATCH!".

## Implementation Details
1. The program initializes a video capture object from the default webcam.
2. The check_face function is defined to perform face verification using DeepFace's verify function.
3. Within the main loop, the program reads frames from the video capture object.
4. Every 30 frames, a new thread is spawned to asynchronously check for face matches using the check_face function.
5. If a match is found, the system displays "MATCH!" on the video frame; otherwise, it displays "NO MATCH!".
6. Press 'q' to exit the program.


## Limitations
1. The system may not perform optimally in low-light conditions or with poor camera quality.
2. Performance may vary depending on the hardware capabilities of the system.
