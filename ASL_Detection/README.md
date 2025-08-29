# American Sign Language Detection

This project uses transfer learning with MobileNetV2 to classify American Sign Language (ASL) gestures from images. Trained on a subset of 1000 images per class, the model achieves a final validation accuracy of **95.5%** after fine-tuning.

---

## Dataset

Source: [ASL Alphabet dataset on Kaggle](https://www.kaggle.com/datasets/grassknoted/asl-alphabet)  
Subset: 1000 images per class (29 classes) used for training and validation.

---

## Model

- MobileNetV2 pretrained on ImageNet
- Dropout and dense layers added for classification
- Early stopping and checkpointing used during training
- Fine-tuned for deeper feature learning

---

## Results

- Validation Accuracy: **95.5%**
- Classification Report and Confusion Matrix included
- Misclassified samples visualized for error analysis

---

## Future Work

- Real-time webcam-based ASL detection using OpenCV
- Grad-CAM visualizations to interpret model decisions
- TensorFlow Lite conversion for mobile deployment
- Streamlit or Flask app for interactive demo
- Benchmarking with EfficientNet or ResNet50 for comparison

---

## Setup

Install dependencies:

```bash
pip install -r requirements.txt