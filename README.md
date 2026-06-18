# Real-Time Hand Sign Recognition System using MediaPipe & Machine Learning

## Overview

This project is a real-time Hand Sign Recognition System that detects and classifies hand gestures using Computer Vision and Machine Learning. The system leverages MediaPipe Hands for hand landmark detection, OpenCV for image processing, and a Random Forest Classifier for gesture recognition.

The project follows a complete machine learning workflow including dataset collection, feature extraction, model training, and real-time prediction through a webcam feed.

---

## Features

* Real-time hand tracking using MediaPipe Hands
* Custom dataset collection using webcam
* Automatic hand landmark extraction
* Landmark-based feature engineering
* Multi-class hand sign classification
* Real-time webcam prediction
* Bounding box and gesture label visualization
* Lightweight and efficient ML-based solution

---

## Tech Stack

* Python
* OpenCV
* MediaPipe
* NumPy
* Scikit-learn
* Pickle

---

## Project Structure

```text
Real-Time-Hand-Sign-Recognition/
│
├── image_collection.py
├── Creation_Dataset.py
├── train_classifier.py
├── Classifier.py
├── data.pickle
├── model.p
└── README.md
```

---

## Workflow

### 1. Dataset Collection

Run:

```bash
python image_collection.py
```

This script captures gesture images through a webcam and stores them in separate class folders.

---

### 2. Dataset Creation

Run:

```bash
python Creation_Dataset.py
```

This script:

* Detects hand landmarks using MediaPipe
* Extracts landmark coordinates
* Converts landmarks into numerical feature vectors
* Saves processed data into `data.pickle`

---

### 3. Model Training

Run:

```bash
python train_classifier.py
```

This script:

* Loads the processed dataset
* Splits data into training and testing sets
* Trains a Random Forest Classifier
* Evaluates model accuracy
* Saves the trained model as `model.p`

---

### 4. Real-Time Prediction

Run:

```bash
python Classifier.py
```

This script:

* Opens the webcam feed
* Detects hand landmarks in real time
* Extracts features
* Predicts hand signs
* Displays the prediction along with a bounding box

---

## Machine Learning Pipeline

1. Image Collection
2. Hand Landmark Detection
3. Feature Extraction
4. Dataset Generation
5. Model Training
6. Model Evaluation
7. Real-Time Inference

---

## Sample Classes

The current implementation recognizes the following gestures:

* A
* B
* E

Additional classes can be added by collecting more gesture images and retraining the model.

---

## Installation

Clone the repository:

```bash
git clone https://github.com/your-username/real-time-sign-language-recognition.git
cd real-time-sign-language-recognition
```

Install dependencies:

```bash
pip install opencv-python mediapipe numpy scikit-learn
```

---

## Future Improvements

* Support for the complete ASL alphabet
* Deep Learning based classification
* Word and sentence formation
* GUI application
* Model deployment using Streamlit
* Improved accuracy with larger datasets

---

## Author

**Granth Chhabra**

B.Tech CSE Student | Machine Learning & Computer Vision Enthusiast
