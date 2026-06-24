# Exploratory Data Analysis (EDA)

The Titanic dataset contains information for **891 passengers**, of whom **342 survived** and **549 did not survive**.

## Key Findings

- The overall survival rate was approximately **38.4%**.
- Female passengers had a significantly higher survival rate than male passengers.
- Passengers traveling in **First Class (Pclass = 1)** had the highest survival rate, suggesting that passenger class influenced survival chances.
- The age group **20–30 years** contained the largest number of survivors.
- The dataset contains missing values that require preprocessing:
  - **Cabin:** 687 missing values
  - **Age:** 177 missing values
  - **Embarked:** 2 missing values

- The **Cabin** column has a large proportion of missing data and may require special handling or removal.
- The **Age** column contains a moderate number of missing values and will require imputation before model training.

## Next Steps

- Handle missing values.
- Encode categorical variables such as **Sex** and **Embarked**.
- Split the data into training and testing sets.
- Train and evaluate classification models including Logistic Regression and Random Forest.
