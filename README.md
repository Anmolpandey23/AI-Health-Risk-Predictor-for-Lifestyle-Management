# AI-Health-Risk-Predictor-for-Lifestyle-Management

## About the Project

This is a machine learning-based system that predicts the risk of developing chronic conditions such as diabetes and heart disease. It combines two healthcare datasets, simulates future risk changes based on lifestyle improvements, clusters individuals into risk groups, and gives personalized health recommendations.

---

## 🌟 Objective

- Predict an individual's health risk.
- Simulate how gradual lifestyle improvements lower risk over time.
- Group individuals based on health/lifestyle indicators.
- Provide specific lifestyle recommendations.

---

## 📂 Datasets Used

[Diabetes Disease Link](https://github.com/Anmolpandey23/AI-Health-Risk-Predictor-for-Lifestyle-Management/blob/498aaf421f48970726ae844294395e7bb09c2664/diabetes.csv)
 
- Features: `Pregnancies`, `Glucose`, `BloodPressure`, `SkinThickness`, `Insulin`, `BMI`, `DiabetesPedigreeFunction`, `Age`, `Outcome`

[Heart Disease Link](https://github.com/Anmolpandey23/AI-Health-Risk-Predictor-for-Lifestyle-Management/blob/498aaf421f48970726ae844294395e7bb09c2664/heart.csv)

- Features: `age`, `sex`, `cp`, `trestbps`, `chol`, `fbs`, `restecg`, `thalach`, `exang`, `oldpeak`, `slope`, `ca`, `thal`, `target`

### Combined Dataset

- Aligned field names
- Merged with `pd.concat`

---

## ✨ Unique Features

- Weekly simulation of risk with improving health indicators
- Personalized lifestyle recommendations
- Visual insights via heatmaps and plots

---

## Preprocessing

- **Imputation:** Filled missing values using mean strategy
- **Scaling:** Standardized all features using `StandardScaler`
- **Split:** 80% training, 20% testing

---

## Machine Learning Models

### Logistic Regression

- **Accuracy:** 80%
- **ROC AUC:** 0.87

### Random Forest Classifier

- **Accuracy:** 79%
- **ROC AUC:** \~0.85

Random Forest was used for risk simulation due to interpretability.

---
## Visuals

Random Forest Vs Logistic Regression
<img width="1205" alt="Random Forest Vs Logistic Regression
" src="https://github.com/Anmolpandey23/AI-Health-Risk-Predictor-for-Lifestyle-Management/blob/498aaf421f48970726ae844294395e7bb09c2664/Logistic%20vs%20Random%20Forest.png" />


Confusion Matrix of Random Forest
<img width="1205" alt="Random Forest – Actual vs Predicted
" src="https://github.com/Anmolpandey23/AI-Health-Risk-Predictor-for-Lifestyle-Management/blob/498aaf421f48970726ae844294395e7bb09c2664/Confusion%20Matrix.png" />


---
## ⏳ Risk Simulation Function

**simulate\_risk\_over\_time()**:

- Inputs: Initial health data, number of weeks
- Simulates weekly improvement in `BMI`, `Glucose`, `chol`, etc.
- Predicts weekly risk scores
- Output: List of risk values over time

---

## Clustering and Recommendations

- Used `KMeans(n_clusters=3)` on lifestyle-related features

### Clusters:

| Cluster | Risk Level | Recommendation                     |
| ------- | ---------- | ---------------------------------- |
| 0       | Low        | Maintain physical activity         |
| 1       | Moderate   | Start low-impact exercise          |
| 2       | High       | Consult physician, adopt diet plan |

---

## ⚙️ Tech Stack

| Component     | Tool                |
| ------------- | ------------------- |
| Language      | Python              |
| ML            | scikit-learn        |
| Visualization | seaborn, matplotlib |
| Environment   | Jupyter Notebook    |

---


## Conclusion

- Logistic Regression had slightly higher ROC AUC
- Random Forest enabled interactive simulations
- Clustering and recommendations offer personalized insights
- Ideal for use in personal health apps and early screening tools

---

## 📘 License

This project is licensed under the [MIT License](https://github.com/Anmolpandey23/AI-Health-Risk-Predictor-for-Lifestyle-Management/blob/a420c5eb0d3191d523df7a79e4d2152db62c70ab/LICENSE).

