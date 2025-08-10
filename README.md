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
This project implements a Generative Adversarial Network (GAN) to generate synthetic credit card fraud transactions based on the highly imbalanced Kaggle Credit Card Fraud Dataset.

The main goal is to address class imbalance in fraud detection problems by producing realistic synthetic fraud samples for training and experimentation.

### Features
Automated dataset download from Kaggle via kagglehub.

- Preprocessing: 
     - Standard scaling for PCA-transformed features (V1–V28).
     - Min-Max scaling for Amount.
     - Normalization for Time.
- GAN Architecture:
     - Generator: Dense layers with LeakyReLU, BatchNorm, and tanh output.
     - Discriminator: Dense layers with LeakyReLU, Dropout, and sigmoid output.
- Training loop:
     - Separate training for real and fake batches.
     - Tracks discriminator and generator losses.
- Synthetic Data Generation:
     - Generates fraud-only transactions (Class = 1).
     - Postprocessing ensures realistic ranges, rounding, and non-negative values.
- Evaluation Tools:
     - Loss curves.
     - Distribution comparisons (real vs synthetic).
- Correlation matrix analysis.
- Export: Saves synthetic dataset to CSV.
