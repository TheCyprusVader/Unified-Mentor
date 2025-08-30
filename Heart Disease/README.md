# Heart Disease Prediction Using Machine Learning

This project applies supervised learning techniques to predict the presence of heart disease based on patient health metrics. It includes exploratory data analysis, feature engineering, model comparison, and threshold tuning to optimize predictive performance.
---
## Project Overview

Cardiovascular disease is a leading global health concern. This notebook uses structured clinical data to build predictive models that can assist in early risk assessment. The workflow includes data preprocessing, model training, evaluation, and business-aligned interpretation.
---
## Dataset

Features include:
- Demographics: Age, Sex
- Symptoms: Chest pain type, exercise-induced angina
- Vitals: Resting blood pressure, cholesterol, max heart rate
- Diagnostics: ECG results, ST depression, slope, number of major vessels, thalassemia
- Target: Binary indicator of heart disease (1 = presence, 0 = absence)
---
## Workflow Summary

1. **Data Preprocessing**
   - Missing value checks, type conversions
   - Feature scaling with `StandardScaler`
   - Stratified train/test split

2. **Exploratory Analysis**
   - Distribution plots and correlation heatmaps
   - Class imbalance visualization

3. **Modeling**
   - Logistic Regression (baseline)
   - Random Forest Classifier
   - XGBoost Classifier
   - Cross-validation and hyperparameter tuning

4. **Evaluation**
   - Accuracy, precision, recall, F1 score
   - ROC-AUC and precision-recall curves
   - Confusion matrix and classification report

5. **Threshold Tuning**
   - Custom decision thresholds to optimize recall
   - Business-aligned tradeoff between false positives and false negatives

6. **Feature Importance**
   - Tree-based rankings (Random Forest, XGBoost)
   - SHAP values (optional extension)
---
## Results

| Model              | Accuracy | Precision | Recall | F1 Score | ROC-AUC |
|-------------------|----------|-----------|--------|----------|---------|
| Logistic Regression | 0.86     | 0.84      | 0.88   | 0.86     | 0.91    |
| Random Forest       | 0.89     | 0.87      | 0.91   | 0.89     | 0.94    |
| XGBoost             | 0.91     | 0.89      | 0.93   | 0.91     | 0.96    |

- **Best Model**: XGBoost with ROC-AUC of 0.96 and recall of 0.93
- **Threshold Tuning**: Improved recall to 0.95 with minimal drop in precision
- **Top Features**: Age, chest pain type, ST depression, thalassemia, max heart rate
---
## Business Interpretation

The model can support clinical decision-making by flagging high-risk patients for further testing. Threshold tuning allows prioritization of recall to minimize missed diagnoses, which is critical in healthcare settings.
---
## How to Run

1. Place the dataset CSV in the working directory
2. Install dependencies:
   ```bash
   pip install -r requirements.txt