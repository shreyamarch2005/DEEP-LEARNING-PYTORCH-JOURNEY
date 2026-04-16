# Wine Classification using PyTorch (DataLoader + Neural Network)

## Overview

This project builds a classification model using PyTorch to predict wine classes based on chemical features.

It introduces dataset handling, batching, and training using PyTorch’s `Dataset` and `DataLoader`.

## Dataset

* Source: Wine dataset (CSV)
* Features: 13 numerical attributes
* Target: Wine class (3 categories)

## Pipeline

### 1. Custom Dataset

* Loaded data using NumPy
* Split into features (X) and labels (y)
* Converted to PyTorch tensors
* Adjusted labels to start from 0 for classification

### 2. DataLoader

* Used `DataLoader` for:

  * Batch processing
  * Shuffling data
* Batch size: 4

### 3. Model Architecture

* Input layer: 13 features
* Hidden layer: Linear + ReLU
* Output layer: 3 classes

### 4. Training

* Loss Function: CrossEntropyLoss
* Optimizer: Adam
* Training done in mini-batches using DataLoader

### 5. Prediction & Evaluation

* Used `torch.max()` to get predicted class
* Compared predictions with actual labels
* Calculated accuracy over dataset

## Results

* Model successfully learned class patterns
* Achieved ~91% accuracy on the dataset

## Key Concepts Learned

* Creating custom datasets using `Dataset`
* Using `DataLoader` for batching and shuffling
* Multi-class classification with `CrossEntropyLoss`
* Model training with mini-batch gradient descent
* Evaluating model performance using accuracy

## Tech Used

* Python
* PyTorch
* NumPy

## Notes

This project marks the transition from full-batch training to mini-batch learning using DataLoader, which is essential for real-world deep learning workflows.
