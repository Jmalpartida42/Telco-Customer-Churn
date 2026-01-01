# Customer Churn Analysis | Telco Dataset

This project performs a predictive analysis of customer attrition using the **Kaggle Telco Customer Churn** dataset. The primary objective is to identify behavioral patterns and develop a machine learning model capable of predicting which users are most likely to cancel their service.

---

## 🔍 Exploratory Data Analysis (EDA)

To understand the drivers of customer churn, I conducted a rigorous statistical analysis:

* **Categorical Variables:** I utilized **Chi-Square ($\chi^2$)** tests to determine the statistical significance and dependency between categorical features (such as contract type, payment method, and tech support) and the target variable (Churn).
* **Numerical Variables:** I applied **T-Student** tests to compare the distributions and means of continuous variables (like `MonthlyCharges` and `Tenure`) between churned and retained customers.
* **Visualization:** Advanced data visualizations were implemented using **Matplotlib** and **Seaborn** to validate statistical hypotheses and observe risk distribution across segments.



---

## 🛠️ Feature Engineering

Following the EDA, the data was pre-processed for Machine Learning:
* **Encoding:** Transformation of categorical variables into numerical format.
* **Scaling:** Normalization of numerical features to ensure model convergence.
* **Class Imbalance:** Handled the skewed distribution of the target variable to improve model sensitivity.

---

## 🤖 Model Comparison

I trained and evaluated three distinct architectures to find the optimal solution for identifying at-risk customers:

| Model | Key Advantages | Performance (Recall Class 1) |
| :--- | :--- | :--- |
| **Random Forest** | High interpretability and robust to outliers. | **59%** |
| **XGBoost** | High-performance Gradient Boosting. | **70%** |
| **Neural Network** | Captures complex non-linear patterns. | **78%** |



### 🏆 Model Selection
After comparing metrics—prioritizing **Recall** to minimize false negatives (failing to identify customers about to leave)—the **Neural Network** was selected as the best performing model.
