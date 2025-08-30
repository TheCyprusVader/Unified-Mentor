# Thyroid Cancer Recurrence Prediction

This project builds a binary classification model to predict recurrence of thyroid cancer based on clinical, pathological, and demographic features. It includes data cleaning, preprocessing, model training, evaluation, and feature importance analysis.
---
## Dataset Overview

The dataset contains 364 patient records with the following features:
- Demographics: Age, Gender
- Clinical history: Smoking, Hx Smoking, Hx Radiotherapy
- Thyroid function and pathology: Function type, Adenopathy, Pathology, Focality
- Staging: Risk, T/N/M classification, Stage
- Treatment response and recurrence status

Target variable: `Recurred` (Yes/No)
---
## Workflow Summary

1. **Data Cleaning**
   - Deduplication and whitespace trimming
   - Category standardization (e.g., pathology labels)

2. **Preprocessing**
   - One-hot encoding for categorical features
   - Standard scaling for numeric features
   - ColumnTransformer pipeline

3. **Modeling**
   - Logistic Regression (baseline)
   - Random Forest with class weighting
   - ROC-AUC and confusion matrix evaluation

4. **Feature Importance**
   - Raw and grouped importance scores
   - Top predictors visualized

5. **Calibration Curve**
   - Reliability of predicted probabilities
   - Random Forest shows strong calibration
---
## Results

| Model              | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|-------------------|----------|-----------|--------|----------|---------|
| Logistic Regression | 94.5%    | 0.98 / 0.88 | 0.94 / 0.96 | 0.96 / 0.91 | 0.975 |
| Random Forest       | 94.5%    | 0.98 / 0.88 | 0.94 / 0.96 | 0.96 / 0.91 | 0.974 |

- **Best Model**: Both models perform similarly; Random Forest offers better interpretability and calibration.
- **Top Features**: Response type, Risk level, Adenopathy, N-stage, Age
---
## Business Interpretation

This model can assist oncologists in identifying patients at higher risk of recurrence. Calibrated probabilities support clinical decision-making, and feature importance aligns with known medical risk factors.
---
## How to Run

1. Place the dataset CSV in the working directory
2. Install dependencies:
   ```bash
   pip install -r requirements.txt