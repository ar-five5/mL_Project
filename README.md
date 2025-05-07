# mL_Project






















# Multi-Step Regression + Classification for Employee Attrition & Salary Estimation

## Overview

This project goes beyond standard HR analytics by combining classification (who might leave) and regression (future salary for those who stay) to assess potential financial impact.

## Objectives

* Predict employee attrition
* Estimate future salary for likely stayers
* Calculate potential salary loss from attrition

## Dataset

* [IBM HR Analytics Employee Attrition Dataset](https://www.kaggle.com/datasets/pavansubhasht/ibm-hr-analytics-attrition-dataset)

## Breakdown

### 1. Attrition Prediction

* **Models**: Logistic Regression, Decision Tree, SVM
* **Metrics**: F1, AUC-ROC, Precision-Recall AUC

### 2. Salary Simulation

* **Methods**:

  * Fixed: `FutureSalary = MonthlyIncome * 1.08`
  * Performance-based:

    ```python
    df["Increment"] = df["PerformanceRating"].apply(lambda x: 1.10 if x == 4 else 1.05)
    df["FutureSalary"] = df["MonthlyIncome"] * df["Increment"]
    ```

### 3. Future Salary Prediction

* **Models**: Random Forest, Ridge, Lasso, SVR
* **Metrics**: R², RMSE, MAPE (optional)
* **Goal**: Replace static rules with feature-based predictions

### 4. Filtering "Likely to Stay"

* Use attrition model: `P_stay = 1 - P_leave`
* Threshold example: `P_stay > 0.6`

### 5. Estimating Salary Loss

* Combine attrition risk and future salary
* Answer: "If this person leaves, how much are we losing?"

## Tools

Python, Pandas, Scikit-learn, Matplotlib/Seaborn

## Impact

* Spot high-risk, high-value employees
* Support HR with data-backed retention strategies

## License

Academic use only. Cite sources accordingly.

---

Fork or contribute freely!






























SE23UCSE005 - Charan --> contribution:  16.5 % 

SE23UCSE006 - Vivardhan --> contribution:  23.5 % 

SE23UCSEO22 - Amogh  --> contribution:  23.5 % 

SE23UCSE075 - Pradhyumna --> contribution:  16.5 % 

SE23UCSE096 - Koushik --> contribution:  20% 
