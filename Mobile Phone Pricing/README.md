# Phone Price Range Prediction

This project builds a multi-class classification model to predict the price range of mobile phones based on hardware specifications. It compares Logistic Regression, Random Forest, XGBoost, and LightGBM, and includes feature engineering and SHAP-based explainability.
---
## Dataset Overview

The dataset contains 2,000 samples with 20 features including:
- Battery power, RAM, internal memory
- Screen dimensions and resolution
- Camera specs (front and primary)
- Connectivity (3G, 4G, WiFi, Bluetooth)
- Target: `price_range` (0 = low, 1 = medium, 2 = high, 3 = very high)
---
## Workflow Summary

1. **Data Preprocessing**
   - Column normalization to `snake_case`
   - Missing value and duplicate checks
   - Stratified train/validation/test split (70/15/15)

2. **Exploratory Analysis**
   - Correlation heatmap and boxplots
   - Top correlated features: RAM, battery power, pixel width/height

3. **Modeling**
   - Logistic Regression (baseline)
   - Random Forest
   - XGBoost
   - LightGBM
   - SHAP summary plot for LightGBM

4. **Feature Engineering**
   - Screen resolution and area
   - Pixels per inch (PPI)
   - Battery power per gram

5. **Evaluation Metrics**

| Model               | Validation Accuracy |
|--------------------|---------------------|
| Logistic Regression| 96%                 |
| XGBoost            | 94%                 |
| LightGBM           | 90%                 |
| Random Forest      | 88%                 |

- Final test accuracy (Logistic Regression): **97%**
- Macro F1 score: **0.97**
- Confusion matrix shows balanced performance across all classes
---
## Business Interpretation

The model can be used by retailers or manufacturers to estimate price tiers based on device specs. Feature engineering improves interpretability, and SHAP values highlight RAM, resolution, and battery efficiency as key drivers.
---
## How to Run

1. Place the dataset CSV in the working directory
2. Install dependencies:
   ```bash
   pip install -r requirements.txt