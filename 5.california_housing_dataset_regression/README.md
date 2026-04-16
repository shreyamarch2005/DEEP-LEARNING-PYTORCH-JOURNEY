# California Housing Price Prediction (PyTorch)

## Overview

This project builds a regression model using PyTorch to predict house prices from the California Housing dataset.

It demonstrates a complete machine learning pipeline, from data preprocessing to model evaluation.

## Dataset

* Source: California Housing dataset
* Features: 8 numerical attributes (e.g., location, population, income)
* Target: Median house value

## Pipeline

### 1. Data Preparation

* Loaded dataset using pandas
* Split features (X) and target (y)
* Converted data to PyTorch tensors

### 2. Normalization

* Standardized features using:
  [
  x = (x - mean) / std
  ]
* Used **training data statistics** to normalize test data (avoids data leakage)

### 3. Model Architecture

* Input layer: 8 features
* Hidden layer: Linear + ReLU
* Output layer: Single value (regression)

### 4. Training

* Loss Function: Mean Squared Error (MSE)
* Optimizer: Adam
* Training performed over multiple epochs

### 5. Evaluation

* Model evaluated on separate test dataset
* Final test loss used as performance metric

## Key Concepts Learned

* Importance of normalization in neural networks
* Avoiding data leakage during preprocessing
* Building custom models using `nn.Module`
* Training and evaluation workflow in PyTorch

## Results

The model successfully learned patterns in the dataset and achieved a low test loss after proper normalization and training.

## Tech Stack

* Python
* PyTorch
* Pandas
* NumPy

## Notes

This project represents a transition from simple models to real-world datasets, focusing on building a clean and structured ML pipeline.
