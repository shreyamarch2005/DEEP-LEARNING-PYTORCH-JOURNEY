# Titanic Survival Prediction (PyTorch)

## Overview

This project builds a classification model using PyTorch to predict passenger survival on the Titanic dataset.

It demonstrates a complete end-to-end machine learning workflow including preprocessing, feature engineering, model training, and evaluation.

## Dataset

* Source: Titanic dataset (CSV)
* Samples: 891 passengers
* Target: Survival (0 = No, 1 = Yes)
* Features: Demographics, ticket info, and travel details

## Pipeline

### 1. Data Preprocessing

#### Missing Values

* `age` filled with mean
* `embarked` filled with mode

#### Feature Selection

* Dropped irrelevant column: `who`

#### Encoding Categorical Data

* Applied one-hot encoding for:

  * sex
  * embarked
  * class
  * alone

#### Removing Redundancy

* Dropped duplicate/dummy columns to avoid multicollinearity:

  * `sex_male`
  * `class_Third`
  * `embarked_S`
  * `alone_False`

### 2. Feature Scaling

* Standardized input features:
  [
  x = (x - mean) / std
  ]

### 3. Dataset & DataLoader

* Converted data into PyTorch tensors
* Used `TensorDataset` for pairing features and labels
* Used `DataLoader` for:

  * batching (batch size = 64)
  * shuffling

### 4. Model Architecture

* Input layer: 10 features
* Hidden layer: Linear + ReLU
* Output layer: 2 classes (binary classification)

### 5. Training

* Loss Function: CrossEntropyLoss
* Optimizer: Adam
* Trained over multiple epochs using mini-batch gradient descent

### 6. Evaluation

* Used `torch.max()` to get predicted class
* Compared predictions with actual labels
* Accuracy achieved: **~86.7%**

## Results

The model successfully learned survival patterns from structured data and achieved good classification performance.

## Key Concepts Learned

* Handling missing values in real datasets
* Encoding categorical variables using one-hot encoding
* Avoiding dummy variable trap (removing redundant columns)
* Using DataLoader for efficient training
* Multi-class/binary classification using CrossEntropyLoss

## Tech Stack

* Python
* PyTorch
* Pandas
* NumPy

## Notes

This project represents a real-world classification pipeline involving messy data preprocessing and model training, highlighting practical challenges beyond toy datasets.
