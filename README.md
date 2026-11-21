# Rotten Fruits Classification Using CNN Architectures

## Project Overview

This project focuses on classifying fruit images into **Good** and **Bad (Rotten)** categories using Convolutional Neural Networks (CNNs).

The goal is to compare different CNN architectures trained from scratch using TensorFlow and Keras, and evaluate their performance on a 12-class image classification task.

The project is implemented in **Python using Google Colab**.

## Dataset

The dataset is obtained from Kaggle:

[Rotten Fruits Dataset](https://www.kaggle.com/datasets/shreyashbhimanwar/rotten-fruits)

It contains 12 classes:

- Apple_Bad
- Apple_Good
- Banana_Bad
- Banana_Good
- Guava_Bad
- Guava_Good
- Lime_Bad
- Lime_Good
- Orange_Bad
- Orange_Good
- Pomegranate_Bad
- Pomegranate_Good

### Dataset Split

The dataset was divided into three subsets:

| Dataset | Number of Images | Percentage |
|---|---:|---:|
| Training | 8,064 | 70% |
| Validation | 1,728 | 15% |
| Testing | 1,728 | 15% |
| **Total** | **11,520** | **100%** |

All images were checked for corruption, and no corrupted images were found.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn
- Google Colab

## Data Preprocessing

The preprocessing pipeline includes:

1. Loading images from the dataset directories.
2. Resizing images to the required input dimensions for each architecture.
3. Converting images to RGB format
