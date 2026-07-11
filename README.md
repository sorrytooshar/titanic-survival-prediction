# 🚢 Titanic Survival Prediction

An end-to-end machine learning project that predicts passenger survival on the Titanic using multiple classification algorithms. This project was later revisited after learning Feature Engineering to evaluate the impact of engineered features on model performance.

---

## 📌 Project Overview

The objective of this project is to predict whether a passenger survived the Titanic disaster using demographic and travel-related information.

The project follows a complete machine learning workflow:

- Exploratory Data Analysis (EDA)
- Data Cleaning & Preprocessing
- Feature Engineering
- Model Training
- Model Evaluation
- Performance Comparison

---

## 📂 Dataset

**Source:** Kaggle – Titanic: Machine Learning from Disaster

- Training Samples: **891**
- Target Variable: **Survived**

---

## 📊 Exploratory Data Analysis

Some key observations from the dataset:

- Female passengers had a significantly higher survival rate.
- First-class passengers survived more frequently than passengers in lower classes.
- The largest number of survivors were between **20–30 years** of age.
- The **Cabin** feature contained a large number of missing values.
- The **Age** feature also required imputation before model training.

---

## ⚙️ Data Preprocessing

The preprocessing pipeline included:

- Median imputation for numerical features
- Most-frequent imputation for categorical features
- One-Hot Encoding
- Scikit-learn Pipelines
- ColumnTransformer for preprocessing
- Train/Validation split (`random_state=42`)

---

## 🔬 Feature Engineering

After completing Kaggle's **Feature Engineering** course, I revisited the project and engineered several new features based on domain knowledge.

### Features Created

- **FamilySize** = SibSp + Parch + 1
- **IsAlone**
- **Passenger Title** (extracted from Name)
- **Deck** (extracted from Cabin)
- **TicketGroup** (number of passengers sharing the same ticket)

Instead of adding every engineered feature directly into the model, each feature (or feature combination) was evaluated independently to measure its impact on model performance.

---

## 🤖 Models Used

- Logistic Regression
- Random Forest Classifier
- XGBoost Classifier

---

## 📈 Results

### Baseline Model Performance

| Model               | Accuracy |
| ------------------- | -------: |
| Logistic Regression |    79.9% |
| Random Forest       |    84.9% |
| XGBoost             |    84.4% |

---

### Feature Engineering Experiments

| Engineered Features         | Random Forest |       XGBoost |
| --------------------------- | ------------: | ------------: |
| FamilySize                  |         84.9% |             — |
| FamilySize + IsAlone        |    **85.47%** |        84.35% |
| Deck                        |             — |    **86.00%** |
| FamilySize + IsAlone + Deck |             — | **86.59%** ⭐ |

---

## 💡 Key Findings

- **FamilySize** alone did not improve Random Forest performance.
- Combining **FamilySize** and **IsAlone** improved Random Forest accuracy from **84.9%** to **85.47%**.
- The engineered **Deck** feature significantly improved XGBoost performance.
- Combining **Deck**, **FamilySize**, and **IsAlone** produced the best XGBoost accuracy of **86.59%**.
- Passenger **Title** and **TicketGroup** did not improve validation accuracy and were excluded from the final XGBoost feature set.

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Matplotlib
- Seaborn

---

## 📚 Skills Demonstrated

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Missing Value Imputation
- Feature Engineering
- One-Hot Encoding
- Machine Learning Pipelines
- Model Evaluation
- Classification
- Hyperparameter Tuning
- Comparative Model Analysis

---

## 🎯 What I Learned

This project reinforced several important machine learning concepts:

- Feature engineering should be driven by domain knowledge rather than guesswork.
- Every engineered feature should be validated experimentally before being retained.
- Different machine learning algorithms respond differently to engineered features.
- Proper preprocessing pipelines help prevent data leakage and improve reproducibility.
- Small improvements in feature representation can significantly improve model performance.

---

## 🚀 Future Improvements

- Perform hyperparameter optimization using GridSearchCV or Optuna.
- Experiment with ensemble methods.
- Perform feature importance analysis using SHAP.
- Train using stratified cross-validation for more robust evaluation.
