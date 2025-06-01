# CNN Architecture Comparison for Image Classification

This repository presents a comprehensive exploration of Convolutional Neural Network (CNN) architectures applied to a multi-class image classification task. The project compares 9+ models using various activation functions, regularization techniques, optimizers, and loss functions to evaluate their performance based on accuracy, F1 score, and training time.

## 🚀 Final Result
The best-performing model, **Improved Model 3**, achieved:
- **Validation Accuracy:** 75.33%
- **Validation F1 Score:** 74.88%
- **Training Time:** 38.22 minutes
- **Trainable Parameters:** ~2.82 million

## 🧠 Models Compared

| Model | Activation | Regularization | Loss Function | Optimizer | Val Accuracy | Val F1 |
|-------|------------|----------------|---------------|-----------|--------------|--------|
| Model 1 | ReLU       | L2              | Cross-Entropy  | Adam      | 61.30%       | 58.23% |
| Model 2 | Leaky ReLU | Dropout         | Cross-Entropy  | SGD       | 75.27%       | 75.99% |
| Model 3 | Leaky ReLU | BatchNorm+Dropout | Cross-Entropy | Adam      | 77.22%       | 76.91% |
| **Improved Model 3** | ReLU | BatchNorm+Dropout | Label Smoothing | Adam | **75.33%** | **74.88%** |
| Model 4–9 | Various | Various | CE / Focal | Adam / RMSProp | 55–72% | 52–71% |

## 📊 Key Features
- Comparative study across multiple CNN configurations
- Visualizations of training vs validation loss, accuracy, and F1 score
- Label smoothing and focal loss implementation
- Learning rate scheduler support
- Model saving with `torch.save`
- Final model plots and parameter count analysis

## 🛠️ Requirements

```bash
torch
torchvision
matplotlib
numpy
scikit-learn
