# 🔷 Geometric Shape Classification using Machine Learning & Deep Learning

**Course Project — IDC409 | Group 3**

A comprehensive comparative study of classical ML and deep learning models for classifying geometric shapes from images. The project explores two datasets and multiple algorithms to identify the best-performing approach for shape recognition.

---

## 📌 Project Overview

This project classifies geometric shapes using computer vision and machine learning techniques. We experiment with:

- **Dataset 1 (5 Shapes):** Circle, Triangle, Square, Hexagon, Pentagon — generated using Python's `Turtle` library with varying colors and sizes.
- **Dataset 2 (4 Shapes):** Circle, Square, Star, Triangle — simpler grayscale images sourced from Kaggle.

---

## 🧠 Models Implemented

### Classical Machine Learning
| Model | Feature Extraction |
|---|---|
| Support Vector Machine (SVM) | HOG + ORB + Color Histogram |
| Random Forest | HOG + ORB + Color Histogram |
| Logistic Regression | Chain Histogram + Geometric Features |
| Decision Tree | Chain Histogram + Geometric Features |
| XGBoost | Chain Histogram + Geometric Features |

### Deep Learning
| Model | Details |
|---|---|
| CNN (5-class) | 2 Conv blocks, BatchNorm, MaxPooling — trained on 64×64 grayscale images |
| CNN (4-class) | 4 Conv blocks with Dropout — trained on 200×200 grayscale images |

---

## ⚙️ Feature Engineering

**HOG (Histogram of Oriented Gradients):** Captures edge and gradient structure of shapes.

**ORB (Oriented FAST and Rotated BRIEF):** Keypoint-based descriptor used as an alternative to SURF.

**Color Histogram (HSV):** Encodes hue, saturation, and value distributions for color-aware classification.

**Chain Code Histogram:** Encodes contour direction changes to distinguish shape boundaries.

**Geometric Features:** Area, perimeter, aspect ratio, extent, solidity, circularity, and number of corners — derived from contour analysis using OpenCV.

---

## 🔄 Data Augmentation

To improve model generalization, images were augmented with:
- 90° and 270° rotations (SVM dataset)
- 90°, 180°, 270° rotations + horizontal flip (Random Forest dataset)

---

## 📊 Evaluation Metrics

- Classification Report (Precision, Recall, F1-score)
- Overall Accuracy
- Confusion Matrix
- ROC Curve with AUC scores (per class)
- Cross-validation scores (Random Forest)

---

## 🛠️ Tech Stack

- **Language:** Python
- **Libraries:** OpenCV, scikit-learn, TensorFlow/Keras, XGBoost, NumPy, Matplotlib, Seaborn, Joblib, scikit-image, tqdm
- **Environment:** Google Colab + Google Drive

---

## 📁 Repository Structure

```
├── idc409project_grp3.ipynb   # Main notebook with all models and experiments
└── README.md
```

---

## 🚀 How to Run

1. Open `idc409project_grp3.ipynb` in Google Colab.
2. Mount your Google Drive and update the dataset paths:
   ```python
   image_folder = '/content/drive/MyDrive/your-dataset-folder'
   ```
3. Run cells sequentially — dataset loading → feature extraction → training → evaluation.

---

## 👥 Team

**Group 3 — IDC409**
GitHub: [ritika3105](https://github.com/ritika3105)
