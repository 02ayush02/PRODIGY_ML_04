# 👋 Hand Gesture Recognition using CNN

A deep learning project that uses Convolutional Neural Networks (CNNs) to recognize various hand gestures from grayscale images. The dataset is preorganized into gesture-labeled subfolders, and the model is trained to classify 10 distinct hand gestures with very high accuracy.

---

## 📁 Dataset Overview

- **Dataset Name:** `leapGestRecog`
- **Structure:**
- **Classes:**
  - `01_palm`
  - `02_l`
  - `03_fist`
  - `04_fist_moved`
  - `05_thumb`
  - `06_index`
  - `07_ok`
  - `08_palm_moved`
  - `09_c`
  - `10_down`

---

## 🧠 Model Architecture

- Layers:
- `Conv2D`, `MaxPooling2D`, `BatchNormalization`
- `Flatten`, `Dense`, `Dropout`
- Activation Functions:
- ReLU (hidden layers)
- Softmax (output layer)
- Optimizer: `Adam`
- Loss Function: `Categorical Crossentropy`

---

## 🔄 Workflow

1. **Data Loading & Preprocessing**
 - Traverse person-wise and gesture-wise folders
 - Resize all images to 64×64
 - Normalize and convert labels to one-hot encoding

2. **Model Training**
 - 80-20 train-test split
 - Trained with `EarlyStopping`
 - Achieved validation accuracy of up to **100%**

3. **Evaluation**
 - Classification report and confusion matrix
 - Visual check of predictions vs actual classes

4. **Saving the Model**
 - `.h5` format using `model.save()`

5. **Visualization**
 - Shows 10 randomly selected predictions with images and labels

---

## 📊 Model Performance

- **Final Training Accuracy:** 99.79%
- **Validation Accuracy:** ~99.95% to 100%
- **Loss:** < 0.01 in final epochs
- **Visualization:** Accurate classification across samples

---

## 🗂 Requirements

Install the required libraries:

```bash
pip install numpy opencv-python matplotlib scikit-learn tensorflow
