# Thyroid Disease Classification using Neural Networks

## Description
This project leverages a neural network to classify thyroid diseases accurately using clinical data. The work demonstrates the effectiveness of machine learning in medical diagnostics, aiming to improve early detection and treatment of thyroid disorders.

## Introduction
Thyroid diseases often exhibit subtle and varied symptoms, making accurate classification a challenge. This project addresses this issue by applying neural networks to clinical data, thereby enhancing diagnostic precision and patient care outcomes.

This project was developed as part of the CS4082 course under the supervision of Dr. Mohammed Nauman.

## Data Preprocessing
Key preprocessing steps include:
1. Handling missing values using median (numerical) and mode (categorical).
2. Encoding categorical variables with a label encoder.
3. Balancing the dataset using upsampling for minority classes.
4. Standardizing features using `StandardScaler`.

## Model Architecture
The neural network model is built using TensorFlow and Keras. The architecture consists of:
- **Input Layer:** Matches the number of features.
- **Hidden Layers:** Two layers with 128 neurons each and ReLU activation.
- **Output Layer:** A softmax layer matching the number of target classes.

### Model Summary
| Layer (type)      | Output Shape | Parameters |
|-------------------|--------------|------------|
| Dense (128 units) | (None, 128)  | 3,840      |
| Dense (128 units) | (None, 128)  | 16,512     |
| Dense (64 units)  | (None, 64)   | 8,256      |
| Dense (Output)    | (None, 32)   | 2,080      |

**Total trainable parameters:** `30,688`

## Training and Evaluation
The model was trained for **10 epochs** with the following results:
- **Training Accuracy:** ~93.35%
- **Validation Accuracy:** ~92.80%

### Performance Metrics
- **Accuracy:** 92.8%
- **Precision:** 93.25%
- **Recall:** 92.8%
- **F1-score:** 92.75%

### Training & Validation Loss
<!-- Replace with actual image -->
![Loss Plot](https://github.com/user-attachments/assets/96795d6d-adcc-48af-9aef-d4d4afdfc820)

### Training & Validation Accuracy
![Accuracy Plot](https://github.com/user-attachments/assets/9d010e5c-d26c-42bf-aec8-217b9f91b199)

## Results
The model effectively classifies thyroid diseases with high accuracy. The confusion matrix and detailed evaluation metrics indicate robust performance across all classes.

## Acknowledgments
I would like to thank my instructor, Dr. Mohammed Nauman, for her guidance and support throughout this course.

Special thanks to my teammates, Shumokh Alhattami and Deema Hamidah for their collaboration and valuable contributions.

