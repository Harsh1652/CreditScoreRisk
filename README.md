# **CIBIL Score Prediction and Recommendation System**

## 📌 **Project Overview**

The **CIBIL Score Prediction and Recommendation System** is a machine learning–based web application that predicts whether a borrower is likely to **default on a loan**.  
It provides **real-time predictions** and **personalized recommendations** to help users understand and improve their creditworthiness.

The system integrates multiple machine learning models with a Flask-powered web interface to deliver accurate risk assessment and an intuitive user experience.

---

## 🧩 **Project Structure**

├── IBMMidTerm.py # Model training and evaluation
├── app.py # Flask web application
├── credit_risk_dataset.csv # Dataset
├── model_features.pkl # Saved feature columns
├── random_forest_credit_risk_model.pkl
├── templates/
│ └── index.html # Frontend UI
└── static/
└── style.css # Styling


---

## 🧠 **Machine Learning Pipeline**

### **1. Model Training — `IBMMidTerm.py`**

**Purpose:**  
Train and evaluate multiple models for credit default prediction.

**Models Evaluated:**
- Random Forest Classifier *(Primary Model)*
- Support Vector Machine (SVM)
- K-Nearest Neighbors (KNN)

**Process:**
1. Load `credit_risk_dataset.csv`
2. Handle missing values using mean imputation
3. Perform one-hot encoding on categorical features
4. Split dataset (80% training, 20% testing)
5. Train and evaluate models
6. Select best-performing model
7. Save trained model and features:
   - `random_forest_credit_risk_model.pkl`
   - `model_features.pkl`

---

### **2. Web Application — `app.py`**

**Framework:** Flask

**Core Functionality:**
- Loads trained Random Forest model
- Provides user interface for predictions
- Accepts user input:

**Personal Information**
- Age  
- Income  
- Credit history length  

**Employment Details**
- Home ownership  
- Employment length  

**Loan Information**
- Loan intent  
- Loan grade  
- Loan amount  
- Interest rate  
- Loan-to-income ratio  

**Processing & Output**
- Preprocesses input data  
- Generates prediction:  
  - **Defaulter**  
  - **Not a Defaulter**  
- Produces personalized credit improvement recommendations

---

### **3. Frontend**

**Files**
- `templates/index.html`
- `static/style.css`

**Features**
- Multi-step interactive form  
- Progress indicator  
- Tooltips and validation  
- Responsive layout  
- Visual feedback for predictions  
- Hero section and feature cards  

---

## 📊 **Dataset**

- **File:** `credit_risk_dataset.csv` (~1.7 MB)
- Contains historical borrower data used for training and evaluation

---

## 🔄 **System Workflow**

User Input → Flask App → Data Preprocessing → Trained Model → Prediction → Recommendations → Display Result


---

## ⭐ **Key Features**

- Real-time credit risk prediction  
- Ensemble of ML models  
- Feature importance analysis  
- Step-by-step guided form  
- Personalized improvement recommendations  
- Mobile-responsive user interface  

---

## 🛠️ **Technical Stack**

| Layer | Technology |
|------|-----------|
| Backend | Python, Flask |
| Machine Learning | scikit-learn (Random Forest, SVM, KNN) |
| Data Processing | pandas, numpy |
| Frontend | HTML, CSS, JavaScript |
| Model Storage | joblib (`.pkl` files) |

---

## 🎯 **Objective**

This system enables users to:
- Understand their current credit risk  
- Identify weaknesses in their credit profile  
- Receive actionable recommendations to improve financial standing  

---
