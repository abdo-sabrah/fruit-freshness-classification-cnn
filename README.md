# Rotten Fruits Classification Using CNN Architectures

## Project Overview

This project focuses on classifying fruits as **Good** or **Bad** using Convolutional Neural Networks (CNNs). The goal is to compare different CNN architectures trained from scratch and evaluate their performance on a fruit image dataset.

The project uses four CNN architectures:
- LeNet-5
- AlexNet
- VGG16
- ResNet18

No transfer learning is used.

## Dataset

The dataset was obtained from Kaggle:

[Rotten Fruits Dataset](https://www.kaggle.com/datasets/shreyashbhimanwar/rotten-fruits)

It contains 12 classes representing six types of fruits, each categorized as Good or Bad:

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

The dataset was divided into three sets:

| Dataset | Number of Images |
|---|---:|
| Training | 8,064 |
| Validation | 1,728 |
| Testing | 1,728 |
| **Total** | **11,520** |

The split ratio is 70% training, 15% validation, and 15% testing.

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Scikit-learn
- Google Colab

## Data Preprocessing

The following preprocessing steps were performed:

1. Loaded images from the dataset directories.
2. Resized images to the required input dimensions for each model.
3. Converted images to RGB format.
4. Normalized pixel values to the range [0, 1].
5. Encoded class labels into numerical values.
6. Divided the data into training, validation, and testing sets.
7. Checked the dataset for corrupted images and duplicate paths.

## CNN Architectures

All models were implemented and trained from scratch.

### 1. LeNet-5

LeNet-5 is a simple CNN architecture consisting of convolutional layers, average pooling layers, and fully connected layers. It was adapted for the 12-class fruit classification task.

### 2. AlexNet

AlexNet is a deeper CNN architecture that uses multiple convolutional layers, ReLU activation, max pooling, and dropout. It was implemented from scratch for this classification task.

### 3. VGG16

VGG16 uses a sequence of convolutional layers with small 3×3 filters, followed by max pooling and fully connected layers. The architecture was implemented from scratch.

### 4. ResNet18

ResNet18 uses residual blocks and shortcut connections to help train deeper neural networks. It was implemented from scratch using TensorFlow and Keras.

## Results

The following table summarizes the test results obtained so far:

| Model | Test Accuracy | Status |
|---|---:|---|
| LeNet-5 | 98.09% | Completed |
| AlexNet | 8.68% | Completed |
| VGG16 | 8.68% | Completed |
| ResNet18 | Pending | Final test evaluation not completed |

### Results Discussion

- **LeNet-5:** Achieved the best completed test accuracy of 98.09%.
- **AlexNet:** Achieved 8.68% test accuracy. Its predictions showed a tendency to collapse toward a single class.
- **VGG16:** Achieved 8.68% test accuracy. Its classification report showed that it predicted only one class.
- **ResNet18:** Training was completed, but validation accuracy fluctuated significantly. Further investigation and final test evaluation are needed.

These results show that a deeper architecture does not necessarily guarantee better performance, especially when training from scratch.

## How to Run the Project

1. Open the notebook using Google Colab.
2. Download or access the dataset from Kaggle.
3. Follow the notebook sections in order.
4. Run the preprocessing and dataset preparation cells.
5. Build and train the CNN architectures.
6. Evaluate the models using the testing dataset.
7. Compare their performance using accuracy and classification reports.

## Future Improvements

- Tune the hyperparameters of the models.
- Investigate the unstable validation performance.
- Apply regularization techniques where appropriate.
- Compare additional evaluation metrics.
- Improve the performance of deeper CNN architectures.

## Author

**Abdullah Abdelhakeem Sabrah**
