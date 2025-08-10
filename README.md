# **SYNTHETIC DATA GENERATION USING GENERATIVE AI**
## 🩺 Diabetes Synthetic Data Generator (GAN-based)

This project implements a **Generative Adversarial Network (GAN)** to create **realistic synthetic diabetes patient data** using the **Diabetes Health Indicators Dataset** from Kaggle.  
It can be used for **data augmentation**, **privacy-preserving research**, and **health data simulations**.

## 📌 Features
- Downloads **Diabetes Health Indicators Dataset** automatically using `kagglehub`.
- Preprocesses the data with **MinMax Scaling** for GAN training.
- Builds a **Generator** and **Discriminator** model using TensorFlow/Keras.
- Trains the GAN to generate **realistic synthetic patient records**.
- Post-processes generated data to match:
  - Binary columns (`0`/`1`)
  - Ordinal columns (e.g., Age, Income)
  - Clipped numerical ranges for health metrics (e.g., BMI, Mental Health days).
- Compares **real vs synthetic distributions** using Seaborn.
- Saves clean synthetic dataset as `synthetic_patients_clean.csv`.
---
## Credit Card Fraud GAN
### 📌 Overview
This project compares a real-world credit card fraud dataset from Kaggle with a synthetic dataset generated to mimic its statistical properties.
The goal is to assess how closely the synthetic dataset replicates the distribution, correlations, and fraud characteristics of the real data.

### 📂 Datasets
1. **Real Dataset**
- Source: Kaggle - Credit Card Fraud Detection

- Description: Contains 284,807 transactions made by European cardholders in September 2013.

- Class distribution:
    - Fraudulent transactions: ~0.17% of total.
    - Highly imbalanced dataset.

- Features:
    - 30 columns: Time, V1–V28 (PCA components), Amount, and Class (target: 0 = non-fraud, 1 = fraud).

2. **Synthetic Dataset**
- File: improved_synthetic_creditcard.csv
- Description: Artificially generated dataset meant to simulate the statistical characteristics of the real dataset while preserving privacy.
- Purpose: To test whether fraud detection models trained on synthetic data can generalize to real-world cases.

### 🛠 Methods Used for Comparison

- Basic Statistical Summary
    - Mean, median, standard deviation for numerical features.
    - Fraud ratio comparison.
- Distribution Analysis
    - Histograms and KDE plots to compare feature distributions.
    - Time and amount distribution comparisons.
- Correlation Analysis
    - Pearson correlation heatmaps for feature relationships.
- Class Imbalance Evaluation
    - Fraud-to-non-fraud ratios.
- Visualization
    - Side-by-side plots for real vs synthetic data.


### 🎯 Objectives
- Validate that the synthetic dataset mimics the real dataset's statistical patterns.
- Ensure privacy preservation by avoiding leakage of sensitive real-world information.
- Test fraud detection models on both datasets to check generalization.


### 📊 Next Steps
- Implement machine learning models (Logistic Regression, Random Forest, XGBoost, Neural Networks).
- Train models on synthetic data and evaluate performance on real data.
- Assess potential domain shift and performance drop.

### 📜 License
Real dataset: Licensed by the original Kaggle dataset provider.

Synthetic dataset: Publicly shareable (no sensitive data).


# Project Evaluation: Synthetic vs Real Credit Card Fraud Data Comparison

## Overview
This project compares a real-world credit card fraud dataset with an improved synthetic version.  
Key goals include:
- Checking how closely the synthetic data matches the real dataset in terms of distribution, correlations, and fraud class imbalance.
- Evaluating the synthetic data’s usefulness for training models without compromising sensitive real-world financial data.

---

## Impact on the 2025 Job Market

### 1. **Data Privacy & Compliance**
- In **finance, healthcare, and government**, companies are increasingly adopting **synthetic datasets** to avoid breaching GDPR, CCPA, and RBI compliance rules.
- This project demonstrates a **practical method to protect customer privacy** while retaining data utility.

### 2. **AI & ML Model Development**
- Synthetic datasets allow **safe model experimentation**, enabling startups and enterprises to test fraud detection systems without accessing live banking data.
- Directly useful for **ML engineers, data scientists, and fintech developers**.

### 3. **Industry Demand**
- With 2025 seeing **a surge in AI-driven fraud detection tools**, companies actively seek professionals who can:
  - Validate synthetic data quality.
  - Ensure statistical similarity to real data.
  - Build high-accuracy fraud prediction models.
- Skills in **data validation, statistical analysis, and Python-based EDA** are highly employable.

### 4. **Ethical AI**
- This project aligns with the global push for **Responsible AI**, helping companies prove that their fraud detection models are trained on **non-identifiable, bias-checked datasets**.



