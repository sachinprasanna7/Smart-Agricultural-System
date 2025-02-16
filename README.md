# 🌿 Disease Classification Using CNN & Classical Machine Learning Models

## 📌 Overview
This repository contains an end-to-end pipeline for **plant disease classification** using both **deep learning (CNN-based models)** and **classical machine learning models**. The workflow includes:

- Extracting **features from pre-trained CNN models** (ResNet-50, ResNeSt-50, ResNeXt-50, SE-ResNet-50).
- Extracting **handcrafted features** (HOG, LBP, Color Histograms).
- Training a **Neural Network** on extracted CNN features.
- Training **Random Forest, SVM, and Logistic Regression** models using CNN and handcrafted features.
- Evaluating the models and storing the results in a structured format.

---

## 📂 Dataset Structure
The dataset consists of three sources:

- **1_UCI_Dataset**
- **2_Rice_Leaf_Disease_Images**
- **3_Rice_Disease_Image_Dataset**

For each CNN model, the extracted features are stored in `.npy` files.

---

## 🛠 Handcrafted Feature Extraction
In addition to CNN-based features, we extract handcrafted features:

1. **HOG (Histogram of Oriented Gradients)** – Captures structural and edge-based patterns.
2. **LBP (Local Binary Patterns)** – Extracts texture-based features for disease detection.
3. **Color Histograms (RGB)** – Quantifies color variations in the leaf.

These features complement deep learning-based representations and improve classification performance.

---

## 🚀 Model Training
The following models are trained:

- **Neural Network** (on extracted CNN features).
- **Classical ML Models**:
  - Random Forest
  - SVM (Support Vector Machine)
  - Logistic Regression

The models are trained for **each dataset** and **each CNN model** separately.

---

## 🔢 Training & Evaluation
### 🏋️ Training Configuration:
- **Epochs:** 30  
- **Batch Size:** 64  
- **Optimizer:** Adam  
- **Train/Test Split:** 80-20  

### 📊 Results:
The results are stored in tabulated format for easy comparison across datasets and models.

Example Table:

| CNN Model      | Classifier            | Kaggle | UCI  | Mendeley |
|---------------|----------------------|--------|------|----------|
| ResNet-50     | Neural Network        | 78.06  | 87.5 | 100      |
| ResNet-50     | Random Forest         | 83.23  | 100  | 100      |
| ResNet-50     | SVM                   | 80     | 95.83| 100      |
| ResNet-50     | Logistic Regression   | 84.52  | 100  | 100      |

Full results are available in the **results directory**.

---

## 🛠 How to Run
### 📌 Prerequisites:
- Python 3.8+
- Required Libraries:
  ```bash
  pip install -r requirements.txt


