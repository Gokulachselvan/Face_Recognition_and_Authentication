# Face Recognition using FaceNet and MTCNN

## Project Overview

This Python-based project is a face recognition system that leverages **MTCNN** for face detection and **FaceNet** for generating face embeddings. Recognized faces are classified using an **SVM classifier**. The system offers real-time face detection, extraction of face embeddings, and recognition via webcam.

## Features

* **Face Detection:** Detects faces in real-time using MTCNN.
* **Face Recognition:** Recognizes faces through FaceNet embeddings and an SVM classifier.
* **Real-time Recognition:** Utilizes webcam for live face detection and classification.
* **Dataset Support:** Handles a dataset of labeled faces for training.

### Project Structure

``` bash
.
├── dataset/        # Folder containing labeled images of faces
├── facenet_model/   # Pre-trained FaceNet model
├── requirements.txt # List of required dependencies
└── face_recognition.py # Main Python script for face recognition
```

### How It Works

1. **Face Detection:** The MTCNN detector identifies faces within an image frame.
2. **Face Embeddings:** Each detected face gets resized and processed through FaceNet to generate a 128-dimensional embedding vector.
3. **Classification:** Embeddings are classified using a linear SVM classifier.
4. **Real-time Recognition:** The system recognizes faces in real-time, labeling them within the webcam feed.

## Installation

1. **Clone the repository:**

```bash
git clone git@github.com:Ruthwik2610/Face_recognition_using_FaceNet_and_MTCNN.git

cd Face_recognition_using_FaceNet_and_MTCNN  

```

### Install dependencies:

```bash
pip install -r requirements.txt 
```

### Setting up the dataset: 

Create a folder named dataset/.
Place images in subfolders within dataset/, where each subfolder is named after the person in the images (e.g., dataset/Alice/, dataset/Bob/).
Running the Script

```bash
python face_recognition.py
```

### Dataset Format

The dataset should consist of images of faces organized in subfolders.
Each subfolder represents a unique person.
Ensure images are clear and frontal-facing.
example:
```bash
dataset/
├── Alice/
│   ├── alice_1.jpg
│   ├── alice_2.jpg
├── Bob/
│   ├── bob_1.jpg
│   ├── bob_2.jpg
```

### Code Overview

***Face Loading Class***: Loads face images from the dataset, detects faces, and extracts face embeddings.
***SVM Classifier***: Trains an SVM classifier on the generated face embeddings.
***Real-time Recognition***: Uses OpenCV to capture webcam input and recognize faces in real-time.
Future Enhancements

