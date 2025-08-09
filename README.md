#  Heart Disease Prediction using Machine Learning

## 📌 Overview
This project predicts the likelihood of a person having heart disease based on medical attributes such as age, cholesterol levels, blood pressure, and other clinical parameters.  
It demonstrates the **end-to-end machine learning pipeline** — from data preprocessing to model evaluation and optimization.

---

## 🗂 Dataset
The dataset used is the **Heart Disease UCI dataset**, containing clinical data of patients with labels indicating the presence or absence of heart disease.  

**Features include:**
- Age  
- Sex
- Chest Pain Type
- trestbps
- Cholesterol  
- Fasting Blood Sugar  
- ECG results  
- Maximum Heart Rate Achieved  
- Exercise Induced Angina  
- ST Depression (oldpeak)  
- And more...
---

| Feature                                              | Description                                                             | Type / Values                                                                                                 |
| ---------------------------------------------------- | ----------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------- |
| **age**                                              | Age of the patient (in years).                                          | Numerical                                                                                                     |
| **sex**                                              | Gender of the patient.                                                  | Categorical → `0` = Female, `1` = Male                                                                        |
| **cp** *(Chest Pain Type)*                           | Type of chest pain experienced.                                         | Categorical → `0` = Typical angina, `1` = Atypical angina, `2` = Non-anginal pain, `3` = Asymptomatic         |
| **trestbps** *(Resting Blood Pressure)*              | Resting blood pressure (in mm Hg) measured on admission.                | Numerical                                                                                                     |
| **chol** *(Serum Cholesterol)*                       | Serum cholesterol level (in mg/dl).                                     | Numerical                                                                                                     |
| **fbs** *(Fasting Blood Sugar)*                      | Fasting blood sugar > 120 mg/dl.                                        | Categorical → `0` = No, `1` = Yes                                                                             |
| **restecg** *(Resting Electrocardiographic Results)* | Results of resting ECG test.                                            | Categorical → `0` = Normal, `1` = ST-T wave abnormality, `2` = Probable/definite left ventricular hypertrophy |
| **thalach** *(Maximum Heart Rate Achieved)*          | Maximum heart rate achieved during exercise.                            | Numerical                                                                                                     |
| **exang** *(Exercise Induced Angina)*                | Whether exercise induced angina occurred.                               | Categorical → `0` = No, `1` = Yes                                                                             |
| **oldpeak**                                          | Depression induced by exercise relative to rest (ST depression in ECG). | Numerical                                                                                                     |
| **slope** *(Slope of the Peak Exercise ST Segment)*  | The slope of the peak exercise ST segment.                              | Categorical → `0` = Upsloping, `1` = Flat, `2` = Downsloping                                                  |
| **ca**                                               | Number of major vessels colored by fluoroscopy (0–3).                   | Numerical                                                                                                     |
| **thal**                                             | Thalassemia blood disorder type.                                        | Categorical → `0` = Normal, `1` = Fixed defect, `2` = Reversible defect                                       |
| **target**                                           | Heart disease diagnosis.                                                | Binary → `0` = No heart disease, `1` = Heart disease present                                                  |

---

## ⚙️ Machine Learning Models Used
- **Logistic Regression** (Best performing — 82% accuracy)
- Random Forest (for comparison)
- Gradient Boosting (for comparison)

---

## 🔍 Steps Implemented
1. **Data Preprocessing**
   - Handling missing values
   - Encoding categorical variables
   - Feature scaling
2. **Model Training & Evaluation**
   - Train-test split
   - Cross-validation
   - Evaluation using Accuracy, Precision, Recall, F1-score, and ROC-AUC
3. **Hyperparameter Tuning**
   - GridSearchCV for optimal parameters
4. **Threshold Optimization**
   - ROC curve-based optimal decision threshold
5. **Model Comparison**
   - Selected best model based on performance metrics

---

## 📊 Results

| Model                  | Accuracy | ROC-AUC |
|------------------------|----------|---------|
| Logistic Regression    | 82%      | 0.90    |
| Random Forest          | 74%      | 0.87    |
| Gradient Boosting      | 78%      | 0.85    |

**Confusion Matrix (Best Model — Logistic Regression):**
[[27  8]
 [ 6 35]]

## 🔮 Future Improvements
- 🧩 **Use stacking/ensemble learning** for better performance  
- 📊 **Collect large datasets** to improve model generalization 
