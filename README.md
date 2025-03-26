# ❤️ Predicting Heart Disease with a Keras-Based MLP  
This project demonstrates how to build and train a **Multilayer Perceptron (MLP)** using the **Keras** framework to predict heart disease from clinical data. The project includes data preprocessing, model building, evaluation, and advanced visualizations to interpret the model's performance.  

---

## 🎯 **Objective**  
The goal of this project is to develop a reliable heart disease prediction model using a neural network. We aim to:  
- Process and clean clinical data  
- Build a Keras-based MLP with **batch normalization** and **dropout**  
- Use **early stopping** to prevent overfitting  
- Evaluate model performance using detailed classification reports and visual tools  

---

## 📂 **Dataset Overview**  
**Dataset:** Heart Disease Dataset (UCI Repository)  
- **Samples:** 1025  
- **Features:** 14 clinical and demographic variables:  
    - `age` – Age of the patient  
    - `sex` – Gender (1 = male, 0 = female)  
    - `cp` – Chest pain type  
    - `trestbps` – Resting blood pressure  
    - `chol` – Serum cholesterol level  
    - `fbs` – Fasting blood sugar level  
    - `restecg` – Resting electrocardiogram result  
    - `thalach` – Maximum heart rate achieved  
    - `exang` – Exercise-induced angina  
    - `oldpeak` – ST depression induced by exercise  
    - `slope` – Slope of the peak exercise ST segment  
    - `ca` – Number of major vessels colored by fluoroscopy  
    - `thal` – Thalassemia  
    - `target` – 1 = Disease, 0 = No Disease  

**Target Classes:**  
- `0` → No Disease  
- `1` → Disease  

---

## 🏗️ **Model Overview**  
### **Model: Keras MLP Classifier**  
The model is built using a **Multilayer Perceptron** (MLP) with:  
✅ Fully connected layers  
✅ ReLU activation  
✅ Sigmoid output for binary classification  
✅ Batch Normalization and Dropout for better generalization  

### **Architecture**  
| Layer Type               | Output Shape | Parameters |
|--------------------------|--------------|------------|
| Dense(64, ReLU)          | (None, 64)    | 1280        |
| BatchNormalization       | (None, 64)    | 256         |
| Dropout(0.3)             | (None, 64)    | 0           |
| Dense(32, ReLU)          | (None, 32)    | 2080        |
| BatchNormalization       | (None, 32)    | 128         |
| Dropout(0.3)             | (None, 32)    | 0           |
| Dense(16, ReLU)          | (None, 16)    | 528         |
| Dense(1, Sigmoid)        | (None, 1)     | 17          |

**Total Parameters:** 4,289  

---

## 🔎 **Performance Metrics**  
| Metric | Value |
|--------|-------|
| **Accuracy** | 99% |
| **Precision** | 99% |
| **Recall** | 99% |
| **F1-Score** | 99% |
| **AUC Score** | 1.0 (Perfect) |

---

## 📊 **Results and Visualizations**  
### 1. **Polar Annotated Confusion Matrix**  
- True Positives: 105  
- True Negatives: 97  
- False Positives: 3  
- False Negatives: 0  

### 2. **Smoothed ROC Curve**  
- AUC = 1.0 → Excellent separation of classes  

### 3. **Radar Chart**  
- Top contributing features: `thalach`, `cp`, `oldpeak`, `exang`, `age`  

### 4. **Swarm Plot**  
- Displays predicted probabilities against true labels  

### 5. **Exponential Moving Average (EMA)**  
- Smoothed validation loss curve shows stable convergence  

---

## ⚙️ **How to Run the Project**  
### 1. **Clone the Repository**  
```bash
git clone https://github.com/your-username/heart-disease-prediction.git





