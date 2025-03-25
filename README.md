# **Image-Classification-using-CNN**

## **CIFAR-10 Dataset**

The **CIFAR-10** (Canadian Institute for Advanced Research) dataset is a widely used benchmark dataset in computer vision and deep learning. It consists of **60,000 color images** categorized into **10 classes**, with **6,000 images per class**. The dataset is divided into:
- **45,000 training images**
- **5,000 validation images**
- **10,000 test images**

Each image is **32×32** pixels with **3 color channels (RGB)**. The dataset is often used for training and evaluating image classification models.

**Classes in CIFAR-10**

The dataset includes the following 10 object categories:


<img src="https://github.com/narpat78/Image-Classification-using-CNN/blob/main/cifar10.png" width="400">
Image Source: <a href="https://paperswithcode.com/dataset/cifar-10" target="_blank">Papers With Code</a>


## **CNN Model**

The CNN model built for classification task of CIFAR-10 dataset has the following architecture:


| **Layer Type**      | **Filters** | **Kernel Size** | **Activation** | **Other Features** |
|----------------|---------|-------------|------------|----------------|
| **Conv2D**     | 32      | (3,3)       | ReLU       | L2 Regularization, BatchNorm |
| **Conv2D**     | 32      | (3,3)       | ReLU       | L2 Regularization, BatchNorm |
| **MaxPooling2D** | -     | (2,2)       | -          | Reduces spatial size |
| **Dropout**    | -       | -           | -          | 40% dropout to prevent overfitting |
| **Conv2D**     | 64      | (3,3)       | ReLU       | L2 Regularization, BatchNorm |
| **Conv2D**     | 64      | (3,3)       | ReLU       | L2 Regularization, BatchNorm |
| **MaxPooling2D** | -     | (2,2)       | -          | Downsampling |
| **Dropout**    | -       | -           | -          | 40% dropout |
| **Conv2D**     | 128     | (3,3)       | ReLU       | L2 Regularization, BatchNorm |
| **Conv2D**     | 128     | (3,3)       | ReLU       | L2 Regularization, BatchNorm |
| **MaxPooling2D** | -     | (2,2)       | -          | Downsampling |
| **Dropout**    | -       | -           | -          | 50% dropout |
| **Conv2D**     | 256     | (3,3)       | ReLU       | L2 Regularization, BatchNorm |
| **Conv2D**     | 256     | (3,3)       | ReLU       | L2 Regularization, BatchNorm |
| **MaxPooling2D** | -     | (2,2)       | -          | Downsampling |
| **Dropout**    | -       | -           | -          | 50% dropout |
| **Flatten**    | -       | -           | -          | Converts 2D features to 1D |
| **Dense**      | 256     | -           | ReLU       | L2 Regularization, Dropout (30%) |
| **Dense**      | 10      | -           | Softmax    | Final classification layer |


## **Model Performance & Generalization**

- With a **test accuracy** of **88.49%**, our model demonstrates strong generalization to unseen data. This balance between accuracy and efficiency highlights its ability to learn meaningful patterns rather than just memorizing the training data.
- The model's effectiveness was further validated by testing on **5 unseen images** sourced from Google. Impressively, it correctly classified **all 5 images**, demonstrating its strong generalization beyond the training dataset.
