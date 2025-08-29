# Lung Cancer Survival Prediction

This project builds a machine learning model to predict survival outcomes for lung cancer patients using clinical, demographic, and treatment data. The goal is to identify high-risk individuals with high recall, enabling early intervention and informed decision-making.

---

## Dataset Summary

- **Samples:** 570,032 patients  
- **Features:** 17 columns including age, gender, cancer stage, treatment type, and diagnosis dates  
- **Target:** `survived` (binary: 1 = survived, 0 = did not survive)  
- **Challenge:** Strong class imbalance (78% non-survivors)

---

## Workflow Overview

1. **Preprocessing**
   - Dropped rows with missing target
   - Imputed missing values using mode/median

2. **Feature Engineering**
   - Created `treatment_duration_days`, `risk_score`, and `age_duration`
   - Added time-aware feature `diagnosis_bucket` (5-year intervals)
   - One-hot encoded categorical variables

3. **Class Balancing**
   - Applied SMOTE to training data for equal class representation

4. **Modeling**
   - Trained both **XGBoost** and **LightGBM**
   - Tuned thresholds to optimize recall and F1 score
   - Compared performance across models

5. **Interpretability**
   - Used **SHAP** to explain global and individual predictions
   - Plotted precision-recall curve to justify threshold selection

---

## Results

| Model     | Threshold | Precision | Recall | F1 Score |
|-----------|-----------|-----------|--------|----------|
| XGBoost   | 0.12      | 0.220     | 1.000  | 0.361    |
| LightGBM  | 0.12      | 0.220     | 1.000  | 0.361    |

- High recall ensures no survivor is missed  
- SHAP revealed key drivers: smoking status, asthma, treatment type, cancer stage  
- Time-aware features improved interpretability in LightGBM

---


---

## Reproducibility

To install dependencies:

```bash
pip install -r requirements.txt