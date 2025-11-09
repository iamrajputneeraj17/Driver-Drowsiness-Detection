# Driver-Drowsiness-Detection
🚗 Driver Drowsiness Detection

This project detects driver drowsiness in real time using OpenCV, Dlib, and Python.
It monitors eye blinks through facial landmarks to determine if a person is active, drowsy, or sleeping.

🧠 Project Logic

The system uses:

Dlib’s face detector – to locate faces in a video frame.

68 facial landmark predictor – to identify key facial points (especially around the eyes).

The project calculates an eye aspect ratio (EAR) using the following logic:

Ratio = (Sum of distances of vertical eye landmarks) / (2 × distance of horizontal eye landmarks)

Depending on the ratio:

👁️ Active – Eyes are open

😴 Drowsy – Eyes partially closed

💤 Sleeping – Eyes closed

Threshold values in the code determine when a person transitions between these states.

📂 Project Structure
Driver-Drowsiness-Detection/
│
├── driver_drowsiness.py              # Main script
├── shape_predictor_68_face_landmarks.dat   # Facial landmark model (to be downloaded)
└── README.md                         # Project documentation

⚙️ Installation

Make sure you have Python 3.8+ installed.

Install dependencies:

pip install opencv-python
pip install dlib
pip install imutils
pip install numpy


Then, download the shape_predictor_68_face_landmarks.dat file from the official Dlib repository and place it inside your project folder:

Driver-Drowsiness-Detection/
    ├── driver_drowsiness.py
    └── shape_predictor_68_face_landmarks.dat

🚀 How to Run

Open your terminal (or command prompt).

Navigate to your project directory:

cd Driver-Drowsiness-Detection


Run the Python script:

python driver_drowsiness.py


Allow camera access.
Two windows will appear:

Frame: Live camera feed with status text.

Result of detector: Face landmarks visualization.

Status Indicators:

🟢 Active :)

🔵 Drowsy !

🔴 SLEEPING !!!

Press ESC to exit.

⚠️ Notes

Ensure good lighting and clear face visibility.

The thresholds for eye ratio can be fine-tuned based on camera quality.

Works best on a laptop webcam or external camera.
