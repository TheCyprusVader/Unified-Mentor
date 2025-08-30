# Vehicle Price Prediction with XGBoost

This project builds a machine learning pipeline to predict vehicle prices using structured automotive data. It includes data cleaning, feature engineering, model benchmarking, hyperparameter tuning, and visual storytelling — all wrapped in a reproducible Google Colab workflow.
---
## Project Overview

- **Goal**: Predict vehicle prices based on features like make, model, engine, fuel type, mileage, and configuration.
- **Dataset**: 978 cleaned entries from `/content/dataset.csv`, with 17 columns including `price` as the target.
- **Final Model**: Tuned XGBoost regressor with R² = **0.8709**, MAE ≈ **₹3,707**, RMSE ≈ **₹6,829**.
---
## Workflow Summary

1. **Data Audit**: Missing values imputed contextually (e.g., `cylinders = 0` for EVs, `description = ""`).
2. **Feature Engineering**: Categorical encoding via `OneHotEncoder`, numeric scaling via `StandardScaler`.
3. **Model Benchmarking**: Compared 6 models (Linear, Ridge, RF, XGBoost, LightGBM, HistGB).
4. **Hyperparameter Tuning**: GridSearchCV on XGBoost with 288 combinations.
5. **Evaluation**: Metrics and visualizations for performance and interpretability.
6. **Deployment Prep**: Final pipeline saved as `xgb_price_model.pkl`.
---
## Key Visuals

- **Predicted vs Actual Prices**: Tight clustering around the diagonal — strong predictive alignment.
- **Residual Distribution**: Centered and symmetric — no major bias or skew.
- **Feature Importance**: `cylinders`, `fuel_Gasoline`, `make_BMW`, and `engine_type` are top drivers.
- **Mileage vs Predicted Price**: Brand-specific depreciation trends visualized.
---

## Tech Stack

- Python (Pandas, NumPy, Matplotlib, Seaborn)
- Scikit-learn (Pipeline, GridSearchCV, metrics)
- XGBoost, LightGBM
- Google Colab (GPU-accelerated, reproducible)

---
## How to Run

1. Upload `dataset.csv` to `/content/` in Google Colab.
2. Run `notebook.ipynb` step-by-step.
3. Final model will be saved as `xgb_price_model.pkl`.

---
