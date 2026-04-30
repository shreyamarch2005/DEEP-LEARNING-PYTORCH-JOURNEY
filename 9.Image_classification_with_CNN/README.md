# 🐱🐶 Cat vs Dog Image Classifier (CNN + ResNet)

## 📌 Overview

This project implements both:

* A **Convolutional Neural Network (CNN)** built from scratch
* A **Transfer Learning approach using ResNet18**

to classify images of cats and dogs using PyTorch.

The models are trained on a real-world dataset and evaluated using validation loss and custom test images.

---

## 🧠 Features

* Custom PyTorch Dataset class
* Data augmentation for robustness
* CNN architecture built from scratch
* Transfer Learning using pretrained ResNet18
* Feature extraction (frozen layers) + fine-tuning
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

### CNN Input (64×64)

* Resize (64x64)
* Random rotation & flipping
* Color jitter (lighting variations)
* Gaussian blur
* Random grayscale
* Normalization

### ResNet Input (224×224)

* Resize (224x224)
* Random horizontal flip
* Color jitter
* Normalization

These augmentations improve generalization across different lighting and image conditions.

---

## 🏗️ Model Architecture

### 🔹 CNN (From Scratch)

* Conv2D → ReLU → MaxPool
* Conv2D → ReLU → MaxPool
* Conv2D → ReLU → MaxPool
* Conv2D → ReLU → MaxPool
* Fully Connected Layer (dynamic initialization)

---

### 🔹 ResNet18 (Transfer Learning)

* Pretrained on ImageNet
* Frozen convolutional layers (feature extractor)
* Replaced final fully connected layer:

```
512 → 2 classes (Cat, Dog)
```

* Optional fine-tuning of deeper layers

---

## ⚙️ Training Details

### CNN

* Optimizer: Adam
* Learning Rate: 0.001
* Epochs: 12
* Batch Size: 32

### ResNet

* Optimizer: Adam (FC layer initially)
* Learning Rate: 0.001
* Epochs: 5–10 (faster convergence)
* Batch Size: 16–32

---

## 📊 Results

### CNN

* Training Loss: ~0.35
* Validation Loss: ~0.34

### ResNet

* Faster convergence
* Better generalization
* More stable predictions on unseen images

---

## 🧪 Testing

Example:

```
Prediction: Cat (92.3%)
```

Confidence is computed using softmax probabilities.

---

## ⚠️ Observations & Limitations

* CNN struggles with:

  * extreme lighting conditions
  * heavy color distortions

* ResNet improves robustness but still:

  * can be overconfident
  * struggles with distribution shift

---

## 🔥 Key Learnings

* Data augmentation improves robustness
* Model confidence ≠ correctness
* Transfer learning significantly improves performance
* Pretrained models generalize better than small CNNs
* Real-world testing is critical

---

## 🚀 Future Improvements

* Cat breed classification (multi-class problem)
* Fine-tuning deeper ResNet layers
* Higher dataset diversity
* Model deployment (Streamlit app)
* Explainability (Grad-CAM / feature visualization)

---

## 💡 Author Notes

This project focuses on:

* building models from scratch
* understanding transfer learning
* debugging real-world issues
* analyzing model behavior beyond metrics

---

## 📌 Next Step

➡️ Cat Breed Classification (12 classes)
➡️ End-to-End ML App (Streamlit)
