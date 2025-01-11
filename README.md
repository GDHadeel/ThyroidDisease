# Thyroid Disease Classification using Neural Networks

<!-- Replace with an actual image link if available -->
![Project Overview](https://example.com/project-image.png)

## Overview
This project leverages a neural network to classify thyroid diseases accurately using clinical data. The work demonstrates the effectiveness of machine learning in medical diagnostics, aiming to improve early detection and treatment of thyroid disorders.

## Table of Contents
- [Introduction](#introduction)
- [Dataset](#dataset)
- [Data Preprocessing](#data-preprocessing)
- [Model Architecture](#model-architecture)
- [Training and Evaluation](#training-and-evaluation)
- [Results](#results)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction
Thyroid diseases often exhibit subtle and varied symptoms, making accurate classification a challenge. This project addresses this issue by applying neural networks to clinical data, thereby enhancing diagnostic precision and patient care outcomes.

This project was developed as part of the CS4082 course under the supervision of Dr. Mohammed Nauman.

**Team Members:**
- Shumokh Alhattami (S21107192)
- Hadeel Balahmar (S20106481)
- Deema Hamidah (S20106517)

## Dataset
The dataset is sourced from [Kaggle](https://www.kaggle.com/) and features:
- A multiclass target variable representing various thyroid diseases.
- Clinical features, including demographic information and thyroid-related tests.

**Initial dataset shape:** `(9172, 31)`  
**Post-processing shape:** `(13542, 31)`

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
![Loss Plot](https://example.com/loss-plot.png)

### Training & Validation Accuracy
<!-- Replace with actual image -->
![Accuracy Plot](https://example.com/accuracy-plot.png)

## Results
The model effectively classifies thyroid diseases with high accuracy. The confusion matrix and detailed evaluation metrics indicate robust performance across all classes.

## Conclusion
Our study demonstrates the potential of neural networks in medical diagnostics, particularly for thyroid disease classification. Future work may explore incorporating additional clinical features to further improve model performance.

## References
- **Dataset:** [Kaggle - Thyroid Disease Dataset](https://www.kaggle.com/)
- **Tools:** Python, TensorFlow, Keras, Matplotlib, Scikit-learn
- **Course:** CS4082 - Supervised by Dr. Mohammed Nauman
