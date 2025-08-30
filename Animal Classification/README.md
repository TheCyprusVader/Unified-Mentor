# Animal Image Classification with Transfer Learning

This project builds a robust image classifier to identify animals from photos using transfer learning with MobileNetV2 and ResNet50. It demonstrates best practices in data preprocessing, model fine-tuning, and performance evaluation.

## Dataset
- Source: Custom animal image dataset (Zebra, Lion, Dog, Cat, etc.)
- Format: Folder-based image classification
- Split: Train / Validation / Test

## Features
- Transfer learning with MobileNetV2 and ResNet50
- Data augmentation and preprocessing
- Early stopping and model checkpointing
- Fine-tuning with frozen and unfrozen base layers
- Evaluation: Accuracy, precision, recall, F1-score, confusion matrix
- Visualization: Misclassified images, per-class performance

## Results
- MobileNetV2: ~91% validation accuracy
- ResNet50 (fine-tuned): ~98.9% validation, ~97% test accuracy
- Strongest classes: Zebra, Panda, Horse, Giraffe
- Improved classes: Dog, Lion, Deer

##  Setup

```bash
cd animal-classification
pip install -r requirements.txt