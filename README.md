# Cats vs Dogs Classification

A deep learning project that uses a **Convolutional Neural Network (CNN)** built with **PyTorch** to classify images as either cats or dogs.

## Overview

The main goal of this project is to build a CNN from scratch and see how well it can identify whether an image contains a cat or a dog.

The dataset was split into:

- **20,000 images** for training
- **2,500 images** for validation
- **2,500 images** for testing

All input images were resized to **224 × 224 pixels**.

## Data Augmentation

To make the model more robust to different image variations, the training images were augmented using:

- Random resized crop
- Random horizontal flip
- Random rotation

Validation and test images were only resized and were not randomly augmented.

## Model

The CNN was built from scratch using **PyTorch**. It consists of:

- 3 convolutional layers
- ReLU activation functions
- Max pooling
- Adaptive average pooling
- Fully connected layers
- Dropout
- A single output neuron for binary classification

For training, **BCEWithLogitsLoss** was used as the loss function and **Adam** was used as the optimizer.

The model was trained for **10 epochs**.

## Results

After training, the model was evaluated on the **2,500-image test set**.

| Metric | Score |
|---|---:|
| Accuracy | 89.08% |
| Precision | 86.50% |
| Recall | 92.43% |

The model correctly classified **2,117 out of 2,500 test images**.

## Project Structure

```text
Cats-Dogs-Classification/
├── data/              # Dataset (not included in the repository)
├── models/            # Trained model
├── notebooks/         # Jupyter/Colab notebooks
├── results/           # Evaluation results and plots
├── src/               # Source code
├── .gitignore
└── README.md