# Handwritten Digit Recognition using MNIST

This project implements a simple handwritten digit recognition model using a Neural Network in TensorFlow/Keras. The model is trained on the MNIST dataset and can predict digits from 0-9.

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Setup](#setup)
- [Usage](#usage)
- [Results](#results)

## Introduction

Handwritten digit recognition is a classic problem in the field of machine learning and computer vision. This project demonstrates how to build, train, and evaluate a neural network to perform this task. The model is capable of achieving high accuracy in classifying handwritten digits.

## Dataset

This project uses the **MNIST dataset**, which is a large database of handwritten digits that is commonly used for training various image processing systems. The dataset consists of 60,000 training images and 10,000 testing images. Each image is a 28x28 pixel grayscale image.

## Model Architecture

The model is a simple feedforward neural network built with Keras. It consists of:

- An `Input` layer that flattens the 28x28 input images into a 784-element vector.
- Two `Dense` (fully connected) hidden layers with 50 neurons each, using the ReLU activation function.
- An `Output` layer with 10 neurons (one for each digit 0-9), using the Sigmoid activation function.

## Setup

To run this notebook, you will need the following libraries:

- `numpy`
- `matplotlib`
- `seaborn`
- `opencv-python` (`cv2`)
- `tensorflow`
- `Pillow` (`PIL`)

You can install them using pip:

```bash
pip install numpy matplotlib seaborn opencv-python tensorflow Pillow
```

## Usage

1.  **Load the dataset**: The `mnist.load_data()` function is used to load the training and testing sets.
2.  **Preprocess the data**: The image pixel values are normalized by dividing by 255 to scale them between 0 and 1.
3.  **Build and Compile the Model**: The neural network is defined and compiled using the Adam optimizer and `sparse_categorical_crossentropy` loss function.
4.  **Train the Model**: The model is trained for 10 epochs on the training data.
5.  **Evaluate the Model**: The model's performance is evaluated on the test set, and its accuracy is reported.
6.  **Make Predictions**: The trained model can be used to predict the digit in a new image. The notebook includes an example of loading an external image, preprocessing it, and getting a prediction.

To predict a digit from an image, ensure the image is in the `/content/` directory or provide the full path to the image. The notebook will then display the image and predict the digit.

## Results

The model typically achieves an accuracy of around 97-98% on the test dataset. A confusion matrix is also generated to visualize the model's performance across different digits.
