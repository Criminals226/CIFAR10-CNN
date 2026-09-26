# CIFAR-10 Image Classification using CNN

## Project Overview

This project was completed as part of the EncoderX AI/ML Internship Task.

The objective of this project was to build a Convolutional Neural Network (CNN) capable of classifying images from the CIFAR-10 dataset into 10 different categories.

The project covers image preprocessing, CNN model development, training, validation, evaluation, and analysis of classification results.

---

## Dataset

The project uses the CIFAR-10 dataset.

CIFAR-10 contains 60,000 color images belonging to 10 classes:

- Airplane
- Automobile
- Bird
- Cat
- Deer
- Dog
- Frog
- Horse
- Ship
- Truck

The images have a resolution of 32 × 32 pixels with three color channels (RGB).

### Dataset Split

The dataset was divided into:

| Dataset | Number of Images |
|---|---:|
| Training | 45,000 |
| Validation | 5,000 |
| Testing | 10,000 |

---

## Technologies Used

- Python
- TensorFlow
- Keras
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

## Data Preprocessing

The images were normalized before training by scaling pixel values from the original range of 0–255 to a range of 0–1.

The training data was further divided into training and validation sets.

---

## CNN Architecture

The model consists of the following layers:

1. Convolutional layer with 32 filters
2. Max Pooling layer
3. Convolutional layer with 64 filters
4. Max Pooling layer
5. Flatten layer
6. Dense layer with 128 neurons
7. Dropout layer with a rate of 0.5
8. Dense output layer with 10 neurons and softmax activation

The final output contains 10 probabilities corresponding to the 10 CIFAR-10 classes.

---

## Model Training

The model was compiled using:

- Optimizer: Adam
- Loss Function: Sparse Categorical Crossentropy
- Metric: Accuracy

The model was trained for 10 epochs with a batch size of 64.

---

## Results

The trained CNN achieved the following results:

| Metric | Result |
|---|---:|
| Test Accuracy | 66.56% |
| Test Loss | 0.9746 |
| Best Validation Accuracy | 69.84% |
| Training Epochs | 10 |

The training accuracy increased from 38.82% during the first epoch to 68.59% by the tenth epoch.

The highest validation accuracy was 69.84% at Epoch 8.

---

## Model Evaluation

Several evaluation techniques were used:

### Accuracy and Loss

Training and validation accuracy and loss were plotted to observe the learning behavior of the model.

### Confusion Matrix

A confusion matrix was generated to examine correct predictions and misclassifications for each CIFAR-10 class.

The matrix showed noticeable confusion between visually similar classes, particularly:

- Cat and Dog
- Automobile and Truck

### Classification Report

A classification report was generated containing:

- Precision
- Recall
- F1-score
- Support

for each of the 10 classes.

---

## Sample Predictions

The project also visualizes sample test images together with their predicted and actual class labels.

This provides a visual way to examine correct and incorrect classifications.

---

## Observations

The model successfully learned useful visual features from the CIFAR-10 images.

The training accuracy consistently increased throughout the training process. However, after reaching the highest validation accuracy at Epoch 8, validation performance decreased while training accuracy continued to increase. This suggests that the model may have started to overfit the training data.

The confusion matrix also showed that some visually similar categories were more difficult for the model to distinguish.

---

## Possible Improvements

The model could potentially be improved by:

- Applying data augmentation
- Adding additional convolutional layers
- Using Batch Normalization
- Tuning the learning rate
- Experimenting with different optimizers
- Using Early Stopping
- Training with a more advanced CNN architecture
- Performing additional hyperparameter tuning

---

## Project Files

```text
EncoderX_AI_ML_Task1/
│
├── notebook.ipynb
├── cifar10_cnn_model.keras
├── README.md
└── screenshots/