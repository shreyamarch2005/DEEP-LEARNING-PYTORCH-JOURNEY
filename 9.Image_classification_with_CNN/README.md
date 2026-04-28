# 🐱🐶 Cat vs Dog Image Classifier (CNN)

## 📌 Overview

This project implements a Convolutional Neural Network (CNN) from scratch using PyTorch to classify images of cats and dogs.

The model is trained on a real-world dataset and evaluated using validation loss and custom test images.

---

## 🧠 Features

* Custom PyTorch Dataset class
* Data augmentation for robustness
* CNN architecture built from scratch
* GPU support (if available)
* Training + Validation pipeline
* Real-world image testing
* Confidence score output

---

## 📂 Dataset

Dataset used:

* Dog vs Cat Dataset (Kaggle)

Structure:

```
PetImages/
    ├── Cat/
    └── Dog/
```

---

## 🔧 Data Preprocessing

Includes:

* Resize (64x64)
* Random rotation & flipping
* Color jitter (lighting variations)
* Gaussian blur
* Random grayscale
* Normalization

These augmentations help the model generalize to real-world conditions.

---

## 🏗️ Model Architecture

CNN Structure:

* Conv2D → ReLU → MaxPool
* Conv2D → ReLU → MaxPool
* Conv2D → ReLU → MaxPool
* Conv2D → ReLU → MaxPool
* Fully Connected Layer (dynamic initialization)

---

## ⚙️ Training Details

* Optimizer: Adam
* Learning Rate: 0.001
* Loss Function: CrossEntropyLoss
* Epochs: 12
* Batch Size: 32

---

## 📊 Results

Training Loss (final):

```
~0.35
```

Validation Loss:

```
0.34
```

The model shows consistent learning and generalization.

---

## 🧪 Testing

Example:

```
Prediction: Cat
Confidence: [0.64, 0.36]
```

---

## ⚠️ Observations & Limitations

* Model performs well on normal images
* Struggles with:

  * extreme lighting conditions
  * heavy color distortions
* Shows bias toward learned patterns (distribution shift)

---

## 🔥 Key Learnings

* Data augmentation improves robustness
* Model confidence ≠ correctness
* Small CNNs have limited generalization
* Real-world testing is critical

---

## 🚀 Future Improvements

* Transfer Learning (ResNet)
* Higher resolution inputs (224x224)
* Better dataset diversity
* Cat breed classification extension
* Model deployment (web app)

---

## 💡 Author Notes

This project was built as a hands-on deep learning exploration, focusing on:

* building from scratch
* debugging training issues
* analyzing model behavior on edge cases

---

## 📌 Next Step

➡️ Upgrade to Transfer Learning (ResNet)
➡️ Build Cat Breed Classifier

---
