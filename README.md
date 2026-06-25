# Titanic Survival Prediction

A machine learning classification project that predicts whether a passenger survived the Titanic disaster based on demographic and travel-related features. This project demonstrates a complete supervised machine learning workflow, including exploratory data analysis, data preprocessing, feature engineering, model training, and performance evaluation.

---

## Project Overview

The objective of this project is to build a classification model capable of predicting passenger survival using information such as age, passenger class, fare, family size, and embarkation port.

The project follows an end-to-end machine learning pipeline, beginning with data exploration and ending with model evaluation using multiple classification metrics.

---

## Dataset

**Dataset:** Titanic - Machine Learning from Disaster (Kaggle)

The dataset contains information for **891 passengers**, including:

- Passenger Class
- Age
- Sex
- Fare
- Number of Siblings/Spouses Aboard
- Number of Parents/Children Aboard
- Embarkation Port
- Survival Status (Target Variable)

---

## Exploratory Data Analysis

Some important insights discovered during EDA:

- Dataset contains **891 passengers**
- **342 passengers survived**
- Female passengers had a significantly higher survival rate than males.
- First-class passengers showed the highest survival rate.
- The 20–30 age group contained the largest number of survivors.
- Missing values were identified before model training:
  - Cabin – 687 missing values
  - Age – 177 missing values
  - Embarked – 2 missing values

Several visualizations were created to better understand feature distributions and relationships with survival.

---

## Data Preprocessing

The following preprocessing steps were performed:

- Removed unnecessary columns:
  - PassengerId
  - Name
  - Ticket
  - Cabin

- Imputed missing values:
  - Age → Median
  - Embarked → Most Frequent Value

- One-Hot Encoded categorical variables:
  - Sex
  - Embarked

- Split the dataset into training and testing sets using an 80:20 ratio.

---

## Model

The final model was trained using **XGBoost Classifier**.

### Why XGBoost?

XGBoost is an ensemble boosting algorithm that combines multiple decision trees to improve predictive performance while reducing overfitting. It is widely used in structured/tabular machine learning problems because of its high accuracy and efficiency.

---

## Model Evaluation

The model achieved:

- **Accuracy:** **84%**

Confusion Matrix:

```text
[[102   8]
 [ 20  49]]
```

Classification Report:

| Metric    | Class 0 | Class 1 |
| --------- | ------- | ------- |
| Precision | 0.84    | 0.86    |
| Recall    | 0.93    | 0.71    |
| F1 Score  | 0.88    | 0.78    |

### Interpretation

The model performs well in predicting passengers who did not survive while maintaining good precision for predicting survivors. The lower recall for the survivor class indicates that some surviving passengers are still misclassified, providing opportunities for further feature engineering and model improvement.

---

## Technologies Used

- Python
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

## Skills Demonstrated

- Exploratory Data Analysis (EDA)
- Missing Value Handling
- Data Cleaning
- Feature Encoding
- Train-Test Split
- Classification
- XGBoost
- Model Evaluation
- Confusion Matrix Analysis
- Precision, Recall and F1-Score Interpretation

---

## Future Improvements

- Compare Logistic Regression, Random Forest and XGBoost.
- Perform feature engineering (Family Size, IsAlone, Title extraction).
- Tune hyperparameters using GridSearchCV or RandomizedSearchCV.
- Perform cross-validation for more robust model evaluation.
- Deploy the trained model as a web application.
