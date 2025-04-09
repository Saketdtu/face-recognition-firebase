# Face Recognition with Real-Time Database

This project implements a real-time face recognition system using Python, OpenCV, and Firebase Realtime Database. It detects faces from a webcam feed and recognizes known individuals based on pre-encoded facial features stored in Firebase.

## Features

* Real-time face detection from webcam feed.
* Recognition of known faces.
* Integration with Firebase Realtime Database for storing and retrieving face encodings and associated data (e.g., names, IDs).
* Efficient data synchronization for live updates.

## Technologies Used

* **Python:** Core programming language.
* **OpenCV (`opencv-python`):** For computer vision tasks (face detection).
* **face_recognition (`face-recognition`):** For generating face encodings and matching faces.
* **Firebase (`firebase-admin`):** For interacting with Firebase services (Realtime Database).
* **NumPy:** For numerical operations, especially with image arrays.

## Setup Instructions

1.  **Clone the repository:**
    ```bash
    git clone <https://github.com/Saketdtu/face-recognition-firebase.git>
    cd face-recognition-firebase
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *Note: Installing `dlib` (a dependency of `face-recognition`) might require `cmake` and C++ compiler tools. Refer to the `face-recognition` library's documentation for detailed installation guides if you encounter issues.*

4.  **Set up Firebase:**
    * Create a Firebase project at [https://console.firebase.google.com/](https://console.firebase.google.com/).
    * Set up Realtime Database or Firestore.
    * Go to Project Settings -> Service Accounts.
    * Generate a new private key and download the JSON file. **IMPORTANT:** Rename this file (e.g., `firebase-credentials.json`) and place it in the project directory.
    * Update the `main.py` (or a separate `config.py`) file with your Firebase database URL and the path to your credentials file.

5.  **Encode Known Faces (if applicable):**
  
6.  **Run the application:**
    ```bash
    python main.py
    ```

