# Fraud Detection with Time-Based Features

This project builds a fraud detection model using customer and terminal-level rolling features over time. It leverages XGBoost for classification and includes threshold tuning for business-aligned decision making.
---
## Project Structure

- `notebooks/`: Jupyter notebook with full pipeline.
- `requirements.txt`: Reproducible environment setup.
- `README.md`: Project overview and usage guide.
---
## Features

- Rolling transaction counts and amounts over 1, 7, and 30 days.
- Terminal-level fraud rate computation.
- Time-based train/test split to avoid leakage.
- Class imbalance handling via `scale_pos_weight`.
- Threshold tuning for precision-recall tradeoff.
- Feature importance visualization.
---
## Model

- **Algorithm**: XGBoost Classifier
- **Evaluation**: Confusion matrix, classification report, threshold tuning
- **Fraud Rate**: ~0.8% (highly imbalanced)
---
## How to Run

1. Clone the repo and place `.pkl` files in `data/`
2. Install dependencies:
   ```bash
   pip install -r requirements.txt