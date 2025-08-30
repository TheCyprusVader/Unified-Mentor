

# Forest Cover Type Classification

Predicting forest cover types using structured environmental data and machine learning.

## Project Overview
This project builds and benchmarks multi-class classifiers to predict `Cover_Type` from geospatial and environmental features. It compares Random Forest, XGBoost, and LightGBM, then fine-tunes the best model for optimal performance.
---
## Modeling Pipeline
- **Data Cleaning**: Dropped `Id`, verified no missing values
- **EDA**: Class distribution, feature importance
- **Models Benchmarked**:
  - Random Forest (Accuracy: 85.5%)
  - XGBoost (Accuracy: 85.4%)
  - LightGBM (Accuracy: 85.6%)
- **Hyperparameter Tuning**: GridSearchCV on LightGBM
  - Final Accuracy: 86.9%
- **Interpretability**: SHAP analysis and confusion matrix

---

## Results
- Elevation, Hydrology distances, and Hillshade metrics were top predictors
- SHAP plots highlight feature impact
- Confusion matrix shows strong performance on classes 4 and 7
---
## Notes
- Dataset: UCI Forest Cover Type
- All models trained on stratified 80/20 split
---
## 📦 Setup Instructions
```bash
# Clone repo
git clone https://github.com/yourusername/forest_cover_classification.git
cd forest_cover_classification

# Create virtual environment
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt