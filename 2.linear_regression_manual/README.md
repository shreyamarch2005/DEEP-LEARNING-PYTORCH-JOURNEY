# Linear Regression (Manual) — PyTorch

## Overview

This notebook implements linear regression from scratch using PyTorch without relying on built-in optimizers or loss functions.

## What This Covers

* Defining model parameters manually (weights & bias)
* Forward pass using matrix multiplication
* Mean Squared Error (MSE) loss implementation
* Backpropagation using `.backward()`
* Manual gradient descent updates

## Key Concepts Learned

* How gradients are computed in PyTorch
* Importance of zeroing gradients to avoid accumulation
* Relationship between predictions, loss, and parameter updates

## Workflow

1. Initialize weights and bias randomly
2. Perform forward pass to get predictions
3. Compute loss using MSE
4. Backpropagate to compute gradients
5. Update parameters using gradient descent
6. Repeat for multiple epochs

## Result

The model learns to approximate the relationship between input features and targets by minimizing the loss over time.

## Tech Used

* Python
* PyTorch
* NumPy

## Notes

This is a foundational implementation meant to build intuition before using higher-level PyTorch modules like `nn.Linear` and optimizers.
