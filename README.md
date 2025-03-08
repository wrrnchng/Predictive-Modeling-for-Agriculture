# 🌱 Soil Nutrient Analysis for Crop Prediction 🌾

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.2%2B-orange.svg)](https://scikit-learn.org/stable/)
[![GridSearchCV](https://img.shields.io/badge/Hyperparameter%20Tuning-GridSearchCV-green)](https://scikit-learn.org/stable/modules/generated/sklearn.model_selection.GridSearchCV.html)

### Disclaimer
*This project is based on files and datasets provided by DataCamp as part of their real-world projects. The dataset and structure align with educational content from DataCamp to help learners practice machine learning techniques in real-world scenarios.*

### 📌 Project Overview
This project analyzes soil nutrients (**Nitrogen, Phosphorus, Potassium**) and **pH levels** to predict the best **crop type** using **Logistic Regression**.  
We use **hyperparameter tuning (GridSearchCV)** to improve model accuracy by optimizing regularization and solver selection.

### 🔬 Dataset Description
The dataset contains 5 columns:
- **Nitrogen content (N)** 🌱 - Essential for plant growth
- **Phosphorus content (P)** 🌾 - Affects root development
- **Potassium content (K)** 🌻 - Helps in disease resistance
- **pH value (pH)** ⚗️ - Determines soil acidity/alkalinity
- **Crop (Target Variable)** 🌽 - Type of crop (categorical)

### 🚀 How the Code Works
1. **Load and Preprocess Data**  
   - Reads the dataset (`dataset.csv`).  
   - Encodes the target variable (**crop type**) using **LabelEncoder**.  

2. **Hyperparameter Tuning with GridSearchCV**  
   - Trains a **Logistic Regression model** for each feature separately.  
   - Optimizes parameters:  
     - `C` (Regularization Strength)  
     - `penalty` (`l1`, `l2`)  
     - `solver` (`liblinear`, `lbfgs`, `saga`, etc.)  

3. **Model Evaluation**  
   - Splits data into **training (80%)** and **testing (20%)**.  
   - Trains the **best model** for each feature using GridSearchCV.  
   - Compares accuracy and selects the **best predictor** for crop classification.  

### 🔧 Installation & Usage
1️⃣ Install Dependencies

    pip install pandas numpy scikit-learn

2️⃣ Run the Python Script

    python crop_prediction.py

### 📈 Results & Insights

  - Nitrogen content produced the best accuracy (~78% in our test).
  - Using GridSearchCV, we optimized hyperparameters to find the best solver and regularization.
  - The dataset could be further improved with multi-feature selection or deep learning models.

### 🤝 Contributing

Feel free to fork this repository and submit pull requests.

### 📜 License

This project is licensed under the MIT License.
