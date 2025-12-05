# Credit Card Fraud Detection Using Machine Learning

This project builds an end-to-end supervised Machine Learning system to detect fraudulent credit card transactions using a real-world dataset. The goal is to compare multiple ML algorithms, evaluate their performance, and select the best model based on Recall and ROC-AUC to ensure maximum fraud detection.

---

## 🚀 Project Overview
Credit card fraud is rare but highly impactful. This project develops a machine learning solution that analyzes transaction patterns to identify suspicious activities. The dataset is highly imbalanced, so special attention is given to Recall (fraud-catch rate) and AUC (ranking ability).

The workflow covers:
- Data loading and inspection  
- Data cleaning & preprocessing  
- Feature engineering  
- Exploratory Data Analysis (EDA)  
- Model training and comparison  
- Train vs Test evaluation  
- Final model selection  
- Prediction on new/unseen data  

---

## 📂 Dataset
The dataset is taken from **Kaggle**:  
`Credit Card Fraud Detection - European cardholder transactions (2013)`

Key characteristics:
- 284,807 transactions  
- Only 492 fraud cases (0.17%)  
- Highly imbalanced  
- Features V1–V28 are PCA-transformed for privacy  
- Includes `Time`, `Amount`, and `Class` (target)

---

## 🛠️ Data Preprocessing
Steps performed:
1. **Handled class imbalance** using `class_weight='balanced'`
2. **Scaled the `Amount` column** (`Amount_scaled`)
3. **Engineered new feature `Hour`** from the `Time` column
4. **Dropped unnecessary columns** (`Time`, `Amount`)
5. Ensured no missing values

These steps improve model stability and interpretability.

---

## 📊 Exploratory Data Analysis (EDA)
Visualizations created:
- Fraud vs Non-Fraud countplot  
- Distribution of transaction amounts  
- Hour-wise transaction pattern  
- Correlation heatmap  

These helped understand patterns and potential indicators of fraud.

---

## 🤖 Machine Learning Models Used
We trained and compared 5 different ML algorithms:

- **Logistic Regression**
- **Naive Bayes**
- **K-Nearest Neighbors (KNN)**
- **Support Vector Machine (SVM - RBF Kernel)**
- **Decision Tree Classifier**

Each model was trained using a **Pipeline** to avoid data leakage and ensure consistent scaling.

---

## 📈 Model Evaluation (Train + Test)
We evaluated each model on **BOTH training and testing sets** using:

- Accuracy  
- Precision  
- **Recall (most important)**  
- F1 Score  
- ROC-AUC  
- Confusion Matrix  

We used Recall as the primary metric because missing fraudulent transactions is extremely costly.

---

## 🏆 Best Model Selection
The best model was selected based on:

- Highest **Test Recall**  
- Strong ROC-AUC  
- Balanced Precision  
- Minimal overfitting (Train vs Test comparison)

The chosen model provides the **best fraud-capture ability** while maintaining acceptable false positives.

---

## 🔮 Prediction on New Data
The final model can be used to predict fraud on new or unseen transactions by supplying input values for all required numerical features.

---

## 📌 Limitations
- Dataset is PCA-transformed, limiting feature interpretability  
- Highly imbalanced dataset  
- KNN and SVM may be slow on large datasets  
- More advanced models (XGBoost, LightGBM) not used due to project scope  

---

## 📚 Future Improvements
- Deploy model using Flask/FastAPI  
- Real-time transaction stream monitoring  
- Threshold tuning to improve Recall further  
- Add ensemble models for higher accuracy  
- SHAP-based model interpretability  

---

## 🙌 Acknowledgment
This project was developed as part of INT-395 under faculty guidance and teamwork. Dataset courtesy of Kaggle.

---

## 📎 Author
**Tac (Aryan Chand) & Team**  
