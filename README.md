# Titanic Survival Prediction

An end-to-end machine learning classification project that predicts whether a passenger survived the Titanic disaster based on passenger demographics and travel information.

This project demonstrates the complete machine learning workflow, including exploratory data analysis, data preprocessing, model training, and model comparison using multiple classification algorithms.

---

## Project Overview

The objective of this project is to build a classification model capable of predicting passenger survival using the Titanic dataset from Kaggle.

The project covers:

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Missing Value Imputation
- Categorical Feature Encoding
- Train-Test Split
- Model Training
- Model Evaluation
- Model Comparison

---

## Dataset

**Source:** Kaggle - Titanic: Machine Learning from Disaster

The dataset contains **891 passenger records** with features such as:

- Passenger Class
- Age
- Sex
- Fare
- Number of Siblings/Spouses (SibSp)
- Number of Parents/Children (Parch)
- Embarkation Port
- Survival Status (Target Variable)

---

## Exploratory Data Analysis

Some key observations:

- Total passengers: **891**
- Total survivors: **342**
- Female passengers had significantly higher survival rates than males.
- First-class passengers had the highest survival rate.
- The 20–30 age group contained the largest number of survivors.
- Missing values identified:
  - Cabin – 687
  - Age – 177
  - Embarked – 2

---

## Data Preprocessing

The following preprocessing steps were performed:

### Missing Value Handling

- Age → Median Imputation
- Embarked → Most Frequent Value

### Removed Columns

- PassengerId
- Name
- Ticket
- Cabin

### Encoding

One-Hot Encoding was applied to:

- Sex
- Embarked

### Data Splitting

The dataset was divided into training and testing sets using an 80:20 train-test split.

---

## Models Trained

Three machine learning models were trained and evaluated using identical preprocessing.

| Model                    | Accuracy      |
| ------------------------ | ------------- |
| Logistic Regression      | **79.89%**    |
| XGBoost Classifier       | **84.36%**    |
| Random Forest Classifier | **84.92%** ⭐ |

Random Forest achieved the highest accuracy on the test set.

---

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Confusion Matrix
- Precision
- Recall
- F1-Score

These metrics provide a more comprehensive evaluation than accuracy alone, especially for classification tasks.

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Jupyter Notebook

---

## Skills Demonstrated

- Exploratory Data Analysis (EDA)
- Data Cleaning
- Missing Value Imputation
- One-Hot Encoding
- Machine Learning Pipelines
- Logistic Regression
- Random Forest
- XGBoost
- Classification Metrics
- Confusion Matrix Interpretation
- Model Comparison

---

## Project Structure

```
Titanic-Survival-Prediction/
│
├── data/
│   ├── train.csv
│   └── test.csv
│
├── notebooks/
│   ├── 01_eda.ipynb
│   └── 02_preprocessing_and_models.ipynb
│
├── README.md
└── requirements.txt
```

---

## Future Improvements

This project represents the baseline implementation.

Planned improvements include:

- Feature Engineering (Family Size, IsAlone, Passenger Title, Deck Extraction)
- Hyperparameter Tuning
- Cross-Validation
- Model Explainability using Feature Importance
- Final model optimization after feature engineering

---

## Results

Among the baseline models, **Random Forest Classifier** achieved the highest accuracy (**84.92%**) while maintaining strong precision and recall. Future iterations of the project will focus on feature engineering and model optimization to further improve predictive performance.
