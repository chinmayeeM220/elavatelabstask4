# 🧪 Breast Cancer Classification using Logistic Regression  

## 📌 Project Overview  
This project builds a **binary classification model** to predict whether a breast tumor is **Malignant (M)** or **Benign (B)** using the **Breast Cancer Wisconsin Diagnostic Dataset**.  
We use **Logistic Regression**, a fundamental machine learning algorithm for classification, and evaluate it with different metrics.  

---

## ⚙️ Steps Followed  

### **1. Dataset Loading**  
- Used the Breast Cancer dataset (`569 rows × 33 columns`).  
- Dropped unnecessary columns:  
  - `id` → Identifier, not useful for training.  
  - `Unnamed: 32` → Empty column.  

### **2. Preprocessing**  
- Target column: `diagnosis`  
  - Encoded:  
    - **M → 1 (Malignant)**  
    - **B → 0 (Benign)**  
- Features: 30 numerical columns.  
- Performed **Train-Test Split** (80% train, 20% test).  
- Standardized features with **StandardScaler** to ensure equal scale.  

### **3. Model Training**  
- Trained a **Logistic Regression** model (`max_iter=1000`).  

### **4. Model Evaluation**  
- **Confusion Matrix**: To visualize correct vs incorrect predictions.  
- **Classification Report**: Shows Precision, Recall, F1-score.  
- **ROC-AUC Score**: Evaluates model performance across thresholds.  
- **ROC Curve**: Plots True Positive Rate vs False Positive Rate.  

### **5. Threshold Tuning**  
- Default threshold = 0.5 (if probability ≥ 0.5 → predict Malignant).  
- We experimented with custom thresholds (e.g., 0.3) to see trade-offs between Precision and Recall.  

---

## 📊 Example Outputs  

- **Confusion Matrix**: Shows counts of TP, TN, FP, FN.  
- **ROC Curve**: Plots AUC score (closer to 1 = better model).  
- **Classification Report**: Provides detailed metrics.  

---

## 🧠 Logistic Regression & Sigmoid Function  

- Logistic Regression outputs probabilities using the **sigmoid function**:  

\[
\sigma(z) = \frac{1}{1 + e^{-z}}
\]

where \(z = w^T x + b\).  
- Maps values between **0 and 1**.  
- Threshold decides classification boundary (default = 0.5).  

---

## 🚀 Future Improvements  
- Try other models (Random Forest, SVM, XGBoost).  
- Perform hyperparameter tuning.  
- Build a **Streamlit app** to interactively set thresholds and view results.  

---
