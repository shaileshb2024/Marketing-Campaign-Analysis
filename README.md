# Customer Subscription Prediction - Marketing Campaign Analysis

## Project Overview

This project aims to predict whether a customer will subscribe to a term deposit based on demographic, financial, and interaction data collected during a phone-based marketing campaign. The goal is to optimize marketing strategies by targeting the right customers, increasing the success rates of future campaigns.

## Business Understanding

The dataset represents a **marketing campaign** in which each customer is either subscribed to a term deposit (`yes`) or not (`no`). The analysis leverages machine learning models to identify patterns in the data that correlate with customer subscription behavior, with a focus on features such as age, education, previous marketing interactions, and financial indicators.

## Data Cleaning and Preprocessing

The dataset underwent several preprocessing steps:
- **Missing Data**: Rows with critical missing values were removed.
- **Categorical Variables Encoding**: Features like `job`, `marital`, `education`, and `contact` were encoded for model compatibility.
- **Rare Category Grouping**: Categories with few instances were grouped to improve model performance.

## Key Findings and Insights

### Descriptive Statistics:
- The dataset consists of **41,188 instances** and **21 features**.
- **Class imbalance**: About **89% of customers did not subscribe**, and **11% did**.
- Key features like `age`, `duration`, and `campaign` show significant variability across customers.
  
### Inferential Statistics:
- Variables like `education`, `contact type`, and `previous outcome` strongly correlate with subscription likelihood.
- **Age** and **duration** showed weaker correlations, indicating potential less importance when considered independently.

### Actionable Insights:
1. **Customer Segmentation**: Customers with certain demographic traits (e.g., older age, higher education) are more likely to subscribe.
2. **Campaign Effectiveness**: Focus on **quality over quantity** in communication. Longer, more meaningful calls lead to higher subscription rates.
3. **Targeted Marketing**: Segmenting campaigns by demographic factors like age and education could increase the overall conversion rate.

## Model Performance and Evaluation

Four machine learning models were tested:
1. **Logistic Regression**
2. **K-Nearest Neighbors (KNN)**
3. **Decision Tree**
4. **Support Vector Machine (SVM)**

### Model Comparison

| Model                 | Train Time (s) | Train Accuracy | Test Accuracy |
|-----------------------|----------------|----------------|---------------|
| **Logistic Regression**| 0.06           | 0.90           | 0.90          |
| **KNN**                | 0.06           | 0.92           | 0.90          |
| **Decision Tree**      | 0.05           | 0.91           | 0.90          |
| **SVM**                | 9.33           | 0.90           | 0.90          |

### Key Conclusions:
- **Logistic Regression** offers great **interpretability** but is slower than some other models.
- **Decision Tree** provides a **balanced performance** between accuracy and training speed.
- **KNN** is also fast and has similar performance but may require tuning for optimal results.
- **SVM** performs similarly to the other models but has much longer training times.

### Final Recommendations:
- **Logistic Regression**: Best for understanding feature impact and interpretability.
- **Decision Tree**: Offers a good balance between accuracy and efficiency.
- **KNN**: Fast and efficient, but can benefit from additional tuning.
- **SVM**: Less practical for large datasets due to long training times.

## Next Steps
1. Further **model tuning** and feature exploration.
2. **Ensemble methods** like Random Forests or Gradient Boosting could further improve performance.
3. Implement **personalized marketing** strategies based on customer segments.

## Access the Jupyter Notebook

The detailed analysis and model code can be found in the **Jupyter Notebook** here:


