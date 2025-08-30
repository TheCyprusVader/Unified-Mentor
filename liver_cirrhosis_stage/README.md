# Liver Cirrhosis Stage Prediction

This project builds a multi-class classification model to predict the stage of liver cirrhosis based on clinical and demographic features. It uses Random Forest with hyperparameter tuning and includes feature importance, ROC curves, and calibration analysis.
---
## Dataset Overview

The dataset contains 25,000 patient records with the following features:
- Demographics: Age, Sex
- Clinical indicators: Ascites, Edema, Hepatomegaly, Spiders
- Biochemical markers: Bilirubin, Albumin, Cholesterol, Copper, SGOT, Alk Phos, Platelets, Prothrombin
- Treatment status: Drug, Status
- Target: Cirrhosis stage (1, 2, or 3)
---
## Workflow Summary

1. **Data Preprocessing**
   - One-hot encoding of categorical features
   - Train/test split (80/20)

2. **Modeling**
   - Baseline Random Forest
   - GridSearchCV for hyperparameter tuning
   - Final model trained with best parameters

3. **Evaluation**
   - Accuracy, precision, recall, F1 score
   - Confusion matrix visualization
   - Cross-validation for stability
   - Multi-class ROC curves
   - Feature importance ranking

4. **Results**

| Stage | Precision | Recall | F1 Score | Support |
|-------|-----------|--------|----------|---------|
| 1     | 0.97      | 0.94   | 0.95     | 1657    |
| 2     | 0.94      | 0.96   | 0.95     | 1697    |
| 3     | 0.97      | 0.97   | 0.97     | 1646    |

- **Overall Accuracy**: 96%
- **5-Fold CV Accuracy**: 95.13% ± 1.19%
- **ROC-AUC**: Stage 1 = 0.99, Stage 2 = 0.99, Stage 3 = 1.00
- **Top Features**: Prothrombin, Platelets, Albumin, N_Days, Age
---
## Business Interpretation

The model can assist clinicians in staging liver cirrhosis using non-invasive features. High recall ensures minimal under-staging, while calibrated probabilities support risk stratification and treatment planning.
---
## How to Run

1. Place the dataset CSV in the working directory
2. Install dependencies:
   ```bash
   pip install -r requirements.txt