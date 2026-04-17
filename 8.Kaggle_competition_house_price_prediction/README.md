# 🏠 House Price Prediction (Advanced ML Pipeline)

## 📌 Overview

This project focuses on predicting house prices using a **real-world messy dataset**.
It covers the complete machine learning pipeline — from preprocessing to model comparison.

Unlike simple tutorials, this project deals with:

* Missing values
* Mixed data types (numerical + categorical)
* High-dimensional feature space (200+ features after encoding)

---

## 🚀 What This Project Demonstrates

* End-to-end ML workflow
* Handling messy, real-world datasets
* Feature engineering and encoding strategies
* Comparing multiple models for performance

---

## 🧹 Data Preprocessing

### Handling Missing Values

* Filled categorical nulls using domain logic:

  * `"No Garage"`, `"No Basement"`, `"No Pool"`, etc.
* Filled numerical values using **median**

### Encoding

* Ordinal encoding for quality-based features (e.g., ExterQual)
* One-hot encoding for nominal features
* Final dataset expanded to **200+ features**

### Target Transformation

```python
y = np.log1p(y)
```

* Applied log transformation to handle skewness in house prices

---

## 📊 Data Preparation

* Train-test split (80/20)
* Feature scaling using `StandardScaler` (for Neural Network)

---

## 🤖 Models Used

### 1. Neural Network (PyTorch)

* Architecture:

  * Input → Linear → ReLU → Dropout
  * Hidden → Linear → ReLU → Dropout
  * Output layer
* Loss: MSELoss
* Optimizer: Adam

### 2. Random Forest Regressor

* Ensemble-based model
* Handles tabular data effectively

### 3. XGBoost Regressor

* Gradient boosting model
* Strong performance on structured data

---

## 📈 Results

| Model          | Performance |
| -------------- | ----------- |
| Neural Network | ~2.61 Loss  |
| Random Forest  | ~0.147 RMSE |
| XGBoost        | ~0.13 RMSE  |

---

## 📉 Visualization

A comparison bar chart was used to evaluate model performance.

---

## 🧠 Key Learnings

* Tree-based models outperform neural networks on tabular data
* Proper handling of missing values significantly improves performance
* Encoding strategy directly impacts model accuracy
* Neural networks are not always the best choice for structured data
* Feature engineering is more important than model complexity

---

## ⚙️ Tech Stack

* Python
* Pandas, NumPy
* PyTorch
* Scikit-learn
* XGBoost
* Matplotlib / Seaborn

---

## 📁 Project Structure

```
House_Price/
│── data/
│── notebooks/
│── README.md
```

---

## 💡 Future Improvements

* Hyperparameter tuning
* Feature selection / dimensionality reduction
* Cross-validation
* Model ensembling

---

## 🎯 Conclusion

This project highlights the importance of:

* Understanding data over blindly applying models
* Choosing the right algorithm for the problem
* Building complete, real-world ML pipelines

---

## 🙌 Author

Shreya

---
