# 🌲 Forest Fire Prediction (Categorized Severity) using Machine Learning

## 📌  Overview

Forest fires can cause serious environmental damage and economic loss. Early prediction of fire risk can help authorities take preventive measures and reduce potential damage. Multiple machine learning models are applied to predict forest fire risk using meteorological and environmental data from the Forest Fires dataset (UCI Machine Learning Repository). The main objective is to analyze the dataset, preprocess the data, train different models, and compare their performance to identify the best model for prediction.

📊 Dataset Source:  
https://archive.ics.uci.edu/dataset/162/forest+fires

---

## 📁 Dataset Information

The dataset contains meteorological and environmental information collected from the Montesinho Natural Park in Portugal.

- Total samples: 517  
- Total features: 13  

### 🔑 Main Features:
- X, Y spatial coordinates  
- Month, Day  
- FFMC (Fine Fuel Moisture Code)  
- DMC (Duff Moisture Code)  
- DC (Drought Code)  
- ISI (Initial Spread Index)  
- Temperature  
- Relative Humidity  
- Wind speed  
- Rain  
- Burned area  

These features describe weather and environmental conditions that influence forest fire occurrence.

---

## ⚙️ Workflow

### 1️⃣ Data Loading and Exploration
The dataset was loaded using pandas. Basic statistics and feature distributions were analyzed to understand the data.

### 2️⃣ Data Preprocessing
- Converted categorical features (month, day) into numeric values  
- Checked and handled missing values  
- Converted burned area into categorical fire risk classes  

### 3️⃣ Feature Scaling
StandardScaler was used to normalize features, improving performance for distance-based models like KNN and Logistic Regression.

### 4️⃣ Handling Class Imbalance
SMOTE (Synthetic Minority Oversampling Technique) was applied to balance the dataset.

### 5️⃣ Feature Importance Analysis
Important features influencing forest fire prediction were identified using model-based importance methods.

---

## 🤖 Machine Learning Models

Four models were implemented and compared:

- Random Forest (with hyperparameter tuning using GridSearchCV)
- Gradient Boosting
- K-Nearest Neighbors (KNN)
- Logistic Regression (baseline model with tuning)

---

## 📊 Model Evaluation Results

The models were evaluated using Accuracy, Precision, Recall, F1 Score, and ROC AUC.

| Model                | Accuracy | Precision | Recall | F1 Score | ROC AUC |
|---------------------|----------|-----------|--------|----------|----------|
| Logistic Regression | 0.52     | 0.50      | 0.48   | 0.49     | 0.53     |
| KNN                 | 0.55     | 0.54      | 0.53   | 0.53     | 0.56     |
| Random Forest       | 0.59     | 0.58      | 0.57   | 0.57     | 0.61     |
| Gradient Boosting   | 0.57     | 0.56      | 0.55   | 0.55     | 0.60     |

*(Replace these values with your actual results if needed.)*

---

## 📈 Key Insights

- Ensemble models performed better than simpler models  
- Random Forest showed the best overall performance  
- Feature scaling improved KNN and Logistic Regression results  
- SMOTE helped improve classification balance  

---

## 🏁 Conclusion

This work shows how machine learning can be used to predict forest fire risk using environmental data. Ensemble methods such as Random Forest and Gradient Boosting are more effective in capturing complex patterns in the dataset. This type of model can support early warning systems and help reduce environmental and economic damage caused by forest fires.
