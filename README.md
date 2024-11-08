# Sign Language Recognition System

This project is an AI-based **Sign Language Recognition System** that utilizes hand tracking and deep learning to detect and recognize various sign language gestures in real-time. The project leverages Mediapipe for hand tracking and Keras for building a deep learning model to classify hand signs.

## Table of Contents
- [Introduction](#introduction)
- [Technologies Used](#technologies-used)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Model Training](#model-training)
- [Data Collection](#data-collection)
- [Usage](#usage)


## Introduction
The Sign Language Recognition System is designed to detect and recognize hand signs from a video feed using computer vision and deep learning. The model is trained to classify gestures from a defined set of signs and can be expanded to include more actions as needed.

## Technologies Used
- **Python**: Main programming language.
- **OpenCV**: For real-time video capture and image processing.
- **Mediapipe**: For efficient and accurate hand tracking.
- **Keras**: Deep learning framework for building and training the neural network.
- **NumPy**: Handling numerical computations and data manipulation.

## Project Structure
The project contains the following main scripts:

1. **app.py**: Runs the real-time sign language recognition system.
2. **function.py**: Contains helper functions for hand tracking and keypoint extraction using Mediapipe.
3. **data.py**: Script for collecting and saving sign language gesture data.
4. **datacollection.py**: Uses OpenCV to capture and save images of hand signs.
5. **trainmodel.py**: Code for training the LSTM model to classify sign language gestures.

## Installation
Follow these steps to set up the project on your local machine:

1. **Clone the Repository**:
   ```bash
   git clone [https://github.com/Bhaavya22/Sign-Language-Recognition-System.git
   cd Sign-Language-Recognition-System

2. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
3. **Install Mediapipe**:
   ```bash
   pip install mediapipe
4. **Install Git LFS**:
   ```bash
   brew install git-lfs
   git lfs install

## Model Training
The LSTM model is trained using the sequences of keypoints extracted from Mediapipe's hand landmarks. The training data consists of multiple sequences for each sign, and the model uses categorical_crossentropy loss and the Adam optimizer.

### Neural Network Architecture
- **Input Layer**: 30 time steps with 63 keypoints per frame.
- **3 LSTM Layers**: Extract temporal features from the input sequences.
- **Dense Layers**: Classify the gestures with a softmax activation function.

# Data Collection
To collect images for training:

- Ensure a stable background and good lighting.
- Use the datacollection.py script, which saves cropped and resized hand images for consistency.

## Usage
Running the System

1. **To start the Sign Language Recognition System**:
   ```bash
   python app.py
2. **To collect new sign language gesture data, run**:
   ```bash
   python data.py
  This script captures images of various hand signs and saves them in the MP_Data folder.

3. **To train the LSTM model, run**:
   ```bash
   python trainmodel.py

