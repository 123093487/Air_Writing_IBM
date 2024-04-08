# Air_Writing_IBM
Computer Vision Project paired with OCR and feature extraction 

Imports: Libraries for camera(cv2), image processing(numpy), hand detection(mediapipe), and (math) are loaded.  To install : pip install opencv-python numpy mediapipe math

Fingertip Positions: A function extracts the index finger and thumb tip locations from detected hands in a frame.

Distance Calculation: Another function calculates the distance between two points (like fingertips).

Smoothing Function: This function smooths out jittery finger movements when drawing lines by considering past positions.

Main Program:

Opens camera and sets up hand detection.

Creates a white canvas for drawing.

Tracks drawing state (on/off) and previous fingertip position.

Main Loop (Continuous):

Reads a frame from the camera.

Flips and converts the frame for processing.

Detects hands and draws landmarks (optional).

Gets fingertip positions (if hands are detected).

Drawing Control (Optional):

Stops drawing if fingertips are close.
Clears canvas, saves image, or quits based on fingertip location in the top frame section.
Drawing Loop (if drawing):

Draws a black circle at the fingertip on the frame.
Smoothly connects the current fingertip to the previous one on the canvas (optional).
Updates the previous fingertip position.
Display: Shows the camera frame with the drawing overlaid and text labels for clear/save/quit actions.

Exit: Stops the camera, closes windows, and exits the program when 'q' is pressed.


Instructions to run the program:
1. Open complete.ipynb notebook and run the first block which will open up the camera frame as well as the blank canvas.

2. Draw the writing as needed following the functionalities mentioned above and save the image

3. On the next block replace the file name with your path to the saved image to obtain ocr prediction.

4. For feature extraction direct to recognition.ipynb and run the last block to obtain features from your written text.
