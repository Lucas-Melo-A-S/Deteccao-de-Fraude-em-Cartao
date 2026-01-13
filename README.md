# Credit Card Fraud Detection — Precision-Oriented Modeling

This project implements a complete and leakage-safe machine learning pipeline
for credit card fraud detection using the Kaggle Credit Card Fraud dataset.

## 🎯 Objective
Maximize **precision** while maintaining a reasonable recall, minimizing false
positives in a highly imbalanced dataset (~0.17% fraud).

## 🔍 Dataset
- Source: Kaggle – Credit Card Fraud Detection (ULB)
- Features: PCA-transformed numerical variables
- Target: `Class` (1 = Fraud, 0 = Legit)

## 🧠 Methodology
- Stratified train / calibration / test split
- XGBoost with conservative hyperparameters
- Probability calibration (Sigmoid)
- Threshold selection based on target precision
- Evaluation with ROC-AUC, PR-AUC, confusion matrix

## 📊 Final Results
- Precision ≈ 40%
- Recall ≈ 83%
- False Positives: 22–133 (depending on threshold)
- Robust, interpretable and production-oriented solution

## 📁 Repository Structure
- `data/` → raw and processed datasets
- `notebooks/` → step-by-step analysis
- `src/` → reusable modeling and evaluation code

## 🚀 Key Takeaways
- Accuracy is misleading in fraud detection
- Threshold tuning is as important as model choice
- Calibration is essential for reliable decision-making

## 📌 Author
Lucas Melo Silva  
Data Science & Machine Learning
