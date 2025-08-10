# **SYNTHETIC DATA GENERATION USING GENERATIVE AI**
## 🩺 Diabetes Synthetic Data Generator (GAN-based)

This project implements a **Generative Adversarial Network (GAN)** to create **realistic synthetic diabetes patient data** using the **Diabetes Health Indicators Dataset** from Kaggle.  
It can be used for **data augmentation**, **privacy-preserving research**, and **health data simulations**.

---

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

