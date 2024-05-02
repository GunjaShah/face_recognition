# Face Recognition 

# Overview
This Python script enables real-time face recognition utilizing a webcam. It employs facial detection techniques to locate faces within the live video stream. Subsequently, it matches these detected faces against a pre-established database of known faces. The annotated video feed showcases the recognized individuals' names in real-time.

# Requirements

- Python 3.x
- `face_recognition` library
- OpenCV (`cv2`)
- Numpy
- A dataset of images containing one image per person to recognize

# Installation

1. Install Python 3.x from [python.org](https://www.python.org/downloads/).
2. Install the required libraries using pip:

   ```bash
   pip install face_recognition opencv-python numpy
   ```
# Usage

1. Clone or download the provided code.
2. Ensure that you have a dataset of images containing one image per person to recognize. Place these images in a directory (`image_path`) specified in the code.
3. Run the script:

   ```bash
   python face_recognition_webcam.py
   ```

4. A window will open displaying the webcam feed. Detected faces will be annotated with the names of recognized individuals.

# Code Structure

`face_recognition_webcam.py`: The main Python script.
`image_path`: Path to the directory containing images of known individuals. Update this variable with the path to your dataset.
`known_face_encodings`: List to store the face encodings of known individuals.
`known_face_names`: List to store the names corresponding to the known face encodings.
`load_known_faces()`: Function to load images from the dataset, encode them, and store the encodings and names.
`video_capture`: Object to capture video from the webcam.
`while True:`: Infinite loop to continuously capture frames from the webcam and perform face recognition.
`face_locations`: List to store the locations of detected faces in each frame.
`for face_location in face_locations:`: Loop through each detected face.
`face_image`: Extract the face region from the frame and resize it for consistency.
`face_encoding`: Compute the face encoding of the detected face.
`matches`: Compare the face encoding against the known face encodings to identify the individual.
Annotation: Draw a bounding box around the detected face and label it with the name of the recognized individual.
`cv2.imshow()`: Display the annotated video feed.
`cv2.waitKey()`: Check for user input to exit the program.

# Limitations and Future Improvements

Performance: The script may experience reduced performance with a large number of faces in the dataset.
Accuracy: The accuracy of face recognition depends on the quality and diversity of the training dataset.
Speed: Real-time face recognition may be slow on low-end hardware. Optimization techniques can be applied for improved speed.
Security: This script is for demonstration purposes and may not be suitable for high-security applications without additional measures.

# References

(https://github.com/ageitgey/face_recognition) library by Adam Geitgey.
[OpenCV Documentation](https://opencv-python-tutroals.readthedocs.io/en/latest/index.html) for image processing and video capture.


