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
3. Converting images to RGB format.
4. Normalizing pixel values to the range `[0, 1]`.
5. Encoding the 12 class labels into numerical values.
6. Creating training, validation, and testing datasets.

The training dataset is shuffled, while validation and testing datasets are kept in a fixed order.

## CNN Architectures

Four CNN architectures are investigated. All models are implemented and trained from scratch without transfer learning.

### 1. LeNet-5

A simplified modern adaptation of LeNet-5 using convolutional layers, average pooling, and fully connected layers.

- Input size: 32 × 32 × 3
- Output classes: 12

### 2. AlexNet

An AlexNet-inspired architecture containing five convolutional layers followed by fully connected layers and dropout.

- Input size: 128 × 128 × 3
- Output classes: 12

### 3. VGG16

A VGG16-based architecture consisting of 13 convolutional layers arranged into five blocks, followed by fully connected layers.

- Input size: 128 × 128 × 3
- Output classes: 12

### 4. ResNet18

A ResNet18-style architecture using residual blocks and shortcut connections to support deeper feature learning.

- Input size: 128 × 128 × 3
- Output classes: 12

## Model Results

The following table presents the test results currently available:

| Model | Test Accuracy | Status |
|---|---:|---|
| LeNet-5 | 98.09% | Completed |
| AlexNet | 8.68% | Completed |
| VGG16 | 8.68% | Completed |
| ResNet18 | Pending | Final test evaluation not completed |

### Results Discussion

LeNet-5 achieved the highest test accuracy among the models with completed evaluations, reaching **98.09%**.

AlexNet and VGG16 achieved 8.68% test accuracy. Their predictions showed a strong tendency to classify images into a single class, indicating that these training runs did not produce satisfactory classification performance.

ResNet18 showed high training accuracy but unstable validation performance. Further investigation and evaluation are required before drawing a final conclusion about its performance.

## Project Structure

A suggested repository structure is:

```text
Rotten-Fruits-Classification/
│
├── README.md
│
├── notebooks/
│   ├── data_preprocessing.ipynb
│   ├── lenet5.ipynb
│   ├── alexnet.ipynb
│   ├── vgg16.ipynb
│   └── resnet18.ipynb
│
├── results/
│   ├── accuracy_plots/
│   ├── loss_plots/
│   └── classification_reports/
│
└── models/
    └── saved_models/
```

*This is a suggested structure; adjust the filenames and folders to match the files actually included in the repository.*

## How to Run

1. Clone or download this repository.
2. Open Google Colab.
3. Upload or open the required notebook.
4. Download the dataset from Kaggle.
5. Update the dataset paths in the notebook if necessary.
6. Run the notebook cells in order.

Make sure the required Python libraries are available in your environment.

## Future Improvements

- Investigate the unstable training behavior of AlexNet and VGG16.
- Improve ResNet18 training stability and complete its evaluation.
- Compare confusion matrices and classification reports across models.
- Investigate model optimization and regularization techniques.
- Save and document the best-performing model.

## Author

**Abdullah Abdelhakeem Sabrah**

Computer Science Graduate

## License

This project is intended for educational and research purposes. Please refer to the original Kaggle dataset page for dataset licensing and usage conditions.
