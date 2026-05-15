# 🧠 Early-Seizure-prediction-using-Machine-Learning

## 📌 Project Overview
This project focuses on detecting **epileptic seizures** using EEG (Electroencephalogram) signal data through machine learning techniques. The goal is to build a reliable classification model that can distinguish between **epileptic (seizure) and non-epileptic brain activity**.

The project follows a complete **end-to-end machine learning pipeline**, including preprocessing, feature engineering, model training, optimization, and evaluation.

---

## 🎯 Objectives 
- Detect epileptic seizures using EEG features  
- Compare multiple machine learning models  
- Handle class imbalance effectively  
- Improve model performance using optimization techniques  
- Identify important EEG features contributing to prediction  

---

## 📂 Dataset
- EEG dataset with extracted features (power bands, statistical features, etc.)  
- ~2200 samples  
- ~600+ features  
- Target column:
  - `0` → Non-epileptic  
  - `1` → Epileptic  

---

## ⚙️ Workflow

### 🔹 1. Data Analysis (EDA)
- Explored dataset structure and feature distributions  
- Analyzed class balance (epileptic vs non-epileptic)  
- Identified skewness and outliers in EEG features  
- Statistical summary of features  

---

### 🔹 2. Data Preprocessing
- Feature-target split  
- Skewness correction:
  - Log transformation (right-skewed features)  
  - Square transformation (left-skewed features)  
- Missing value handling (imputation)  
- Outlier handling using **RobustScaler**  

---

### 🔹 3. Train-Test Split
- Split data into training and testing sets (80:20)  
- Applied stratified sampling  

---

### 🔹 4. Handling Class Imbalance
- Applied **SMOTE (Synthetic Minority Oversampling Technique)**  
- Performed only on training data to prevent data leakage  

---

### 🔹 5. Feature Scaling
- Applied **RobustScaler** for scaling  
- Ensured consistent transformation for test data  

---

### 🔹 6. Model Training
- Implemented multiple models:
  - Logistic Regression (Baseline)  
  - Support Vector Machine (SVM)  
  - Random Forest  
  - XGBoost  

---

### 🔹 7. Ensemble Learning
- Implemented **Voting Classifier (Soft Voting)**  
- Combined predictions of:
  - SVM  
  - Random Forest  
  - XGBoost  
- Improved model robustness and generalization  

---

### 🔹 8. Model Optimization
- Hyperparameter tuning using:
  - GridSearchCV  
  - RandomizedSearchCV  
- Improved performance and reduced overfitting  

---

### 🔹 9. Model Evaluation
- Evaluated models using:
  - Accuracy  
  - Precision  
  - Recall  
  - F1-Score  
  - ROC-AUC  
- Generated confusion matrix and classification reports  

---

### 🔹 10. Visualization & Interpretation
- ROC Curve analysis  
- Confusion Matrix visualization  
- Feature importance analysis  
- Identified key EEG features contributing to prediction  

---

### 🔹 11. Model Selection
- Compared all models based on performance metrics  
- Selected best-performing model (Random Forest / Ensemble)  

---

### 🔹 12. Model Saving
- Saved trained models using `joblib`  
- Ensured reproducibility  

---

## 🤖 Models Used

### 1️⃣ Logistic Regression (Baseline)
- Simple reference model  

### 2️⃣ Support Vector Machine (SVM)
- Kernel: RBF  
- Captures nonlinear relationships  

### 3️⃣ Random Forest ⭐
- Best performing individual model  
- Robust and interpretable  

### 4️⃣ XGBoost ⭐⭐
- Strong gradient boosting model  
- High ROC-AUC  

### 5️⃣ Voting Ensemble ⭐⭐⭐
- Combines SVM + Random Forest + XGBoost  
- Best overall stability and performance  

---

## 📊 Model Performance

| Model | Accuracy | Precision | Recall | F1-Score | ROC-AUC |
|------|--------|----------|--------|--------|--------|
| Logistic Regression | ~70–75% | - | - | - | ~80% |
| SVM | ~78% | ~72% | ~86% | ~78% | ~87% |
| Random Forest | **~87%** | ~88% | ~85% | **~86%** | **~92%** |
| XGBoost | ~86% | ~85% | ~86% | ~85% | ~91% |
| Voting Ensemble | **~88–90%** | ~88% | ~87% | **~88%** | **~94%** |

**Best Model:** Voting Ensemble / Random Forest  

---

## 📈 Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1-Score  
- ROC-AUC  

---

## ⚡ Optimization Techniques
- Hyperparameter tuning  
- Feature selection  
- Cross-validation  

---

## 🏥 Real-World Impact
- Early seizure detection  
- Helps clinicians in diagnosis  
- Useful in wearable EEG monitoring systems 

---

## 🛠️ Tech Stack
- Python  
- Scikit-learn  
- XGBoost  
- Pandas, NumPy  
- Matplotlib, Seaborn  

---

## 📌 Conclusion
This project demonstrates a complete ML pipeline for seizure detection using EEG data.  
Random Forest and XGBoost achieved high accuracy and reliability, making them suitable for real-world healthcare applications.

