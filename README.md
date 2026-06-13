# Chronic Kidney Disease Detection using Classical and Quantum Deep Learning

This project focuses on **Chronic Kidney Disease (CKD) stage classification** using medical images with a two-phase approach:

1. **Classical Deep Learning Baseline** using ResNet-50
2. **Quantum-Enhanced Hybrid Model** using ResNet features with a Variational Quantum Circuit (VQC)

The goal is to study whether adding a quantum layer can improve classification performance compared to a purely classical model.

## Project Overview

Chronic Kidney Disease is a progressive condition that can be categorized into multiple stages. Early and accurate stage prediction is important for timely treatment and disease management. This notebook builds an image-based pipeline for CKD stage classification and compares classical and quantum-enhanced approaches.

## Workflow

### 1. Data Preprocessing
- Load CKD image dataset
- Merge stage-wise image folders
- Apply preprocessing such as resizing and CLAHE
- Store processed images for training

### 2. Classical Model
- Use **ResNet-50** as the baseline CNN model
- Train on processed CKD stage images
- Evaluate with validation accuracy, confusion matrix, and classification report

### 3. Quantum Hybrid Model
- Use ResNet-50 as a feature extractor
- Reduce extracted features to a lower-dimensional representation
- Pass features through a **Variational Quantum Circuit (VQC)** built with PennyLane
- Combine quantum outputs with classical layers for final stage prediction

### 4. Comparison
- Compare classical and hybrid quantum models using:
  - Validation accuracy
  - Training curves
  - Confusion matrix
  - Classification report

## Tech Stack

- **Python**
- **PyTorch**
- **Torchvision**
- **PennyLane**
- **NumPy**
- **OpenCV**
- **Scikit-learn**
- **Matplotlib / Seaborn**
- **Google Colab**

## Model Ideas Used

### Classical
- ResNet-50 transfer learning
- Data augmentation
- Weighted sampling for class imbalance handling
- Validation-based comparison

### Quantum
- Variational Quantum Circuit (VQC)
- Angle embedding / rotation-based encoding
- Hybrid quantum-classical model
- Manual batch-safe quantum layer integration in PyTorch

## Repository Structure

```bash
CKD/
├── CKD.ipynb
├── README.md
└── outputs/
```

## How to Run

1. Open `CKD.ipynb` in Google Colab
2. Install required dependencies
3. Run preprocessing cells
4. Train the classical ResNet baseline
5. Run the quantum hybrid section
6. Compare the results

## Possible Improvements

- Use stratified train-validation split
- Try EfficientNet or DenseNet baselines
- Optimize the quantum circuit depth and qubit count
- Use k-fold cross-validation
- Save plots and trained weights systematically
- Deploy the best model as a lightweight demo app

## Objective

The main objective of this project is not only to classify CKD stages, but also to explore how **quantum machine learning** can be integrated into medical image analysis in a meaningful and reproducible way.

## Author

**Rishith K**  
AI/ML Student | Quantum Machine Learning Enthusiast
