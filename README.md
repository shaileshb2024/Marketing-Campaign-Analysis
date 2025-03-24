# Customer Subscription Prediction - Marketing Campaign Analysis

## Project Overview

This project focuses on predicting whether a customer will subscribe to a term deposit based on demographic, financial, and interaction data gathered from a phone-based marketing campaign. The target variable, **'y'**, indicates whether a customer subscribed to a term deposit ("yes" or "no"). The goal is to use machine learning to optimize marketing strategies, ensuring that campaigns target the right customers to increase success rates.

## Business Understanding

The primary objective of this analysis is to understand the factors that influence customer subscription behavior during a marketing campaign. By identifying key patterns in the data, we aim to provide actionable insights for improving campaign targeting and increasing conversion rates.

## Data Cleaning and Preprocessing

The dataset was cleaned and preprocessed with the following steps:
- **Handling Missing Data**: Rows with missing values in critical features were removed.
- **Categorical Variables Encoding**: Categorical variables such as `job`, `marital`, `education`, and `contact` were encoded for compatibility with machine learning algorithms.
- **Rare Category Grouping**: Low-frequency categories in features like `job`, `marital`, and `education` were grouped together to enhance model performance.

## Key Findings and Insights

### Descriptive Statistics:
- The dataset consists of **41,188 instances** and **21 features**.
- **Class Imbalance**: About **89% of customers did not subscribe** to a term deposit, and **11% did**.
- **Age and Campaign Duration**: Key continuous features like `age` and `duration` exhibit significant variability across customers, highlighting diverse profiles.
- The average **age** is **40.02 years**, and the average campaign **duration** is **258.29 seconds**.

### Inferential Statistics:
- Features like `education`, `contact type`, and `previous outcome` show strong correlations with the subscription outcome.
- **Age** and **duration** show weaker correlations, suggesting they may be less critical when used independently.

### Actionable Findings for Non-Technical Audience:
1. **Customer Segmentation**: Certain **demographics**, such as **age**, **job type**, and **education level**, play a significant role in predicting subscription. Older clients and those with higher education are more likely to subscribe.
2. **Campaign Effectiveness**: Focus on **longer, more detailed calls** rather than frequent short calls to improve conversion rates.
3. **Target Specific Groups**: Older clients and those with higher education show a higher likelihood of subscribing. Targeting these groups in future campaigns could improve results.

## Model Interpretation and Evaluation

### Logistic Regression Coefficients:
- **age: 0.0264** — Each additional year increases the likelihood of subscription.
- **default: -0.2163** — A history of default reduces the likelihood of subscription.
- **duration: 1.3743** — A longer call duration significantly increases the likelihood of subscription.
- **campaign: -0.0765** — More contact attempts decrease the likelihood of subscription.

### SVM Coefficients:
- **age: 0.0117** — Slight positive relationship with subscription.
- **default: -0.0703** — Defaulting reduces subscription likelihood.
- **duration: 0.5834** — Longer calls increase the likelihood of subscription.

### Decision Tree Feature Importance:
- **duration: 0.5204** — Most important feature.
- **euribor3m: 0.4353** — Strong influence on predictions.

### Model Performance Summary:

| Model                 | Train Time (s) | Train Accuracy | Test Accuracy |
|-----------------------|----------------|----------------|---------------|
| **Logistic Regression** | 0.06           | 0.90           | 0.90          |
| **KNN**                | 0.06           | 0.92           | 0.90          |
| **Decision Tree**      | 0.05           | 0.91           | 0.90          |
| **SVM**                | 9.33           | 0.90           | 0.90          |

### Conclusion:
- **Decision Tree** provides the best performance with a **90% accuracy**, but **Logistic Regression** is preferred for interpretability.
- **KNN** is also effective and fast, while **SVM** is accurate but slower in training.

## Next Steps and Recommendations

### Model Improvements:
1. **Tuning**: Further tuning of models and adding new features (e.g., customer behavior) could enhance performance.
2. **Ensemble Methods**: Using methods like Random Forests or Gradient Boosting could boost accuracy, especially for harder-to-predict cases.

### Customer Outreach Strategy:
1. **Target High-Potential Segments**: Direct marketing efforts toward older clients or those with higher education.
2. **Personalized Messaging**: Tailor campaigns based on customer demographics to improve engagement.

### Campaign Design Adjustments:
1. **Optimize Call Duration**: Focus on **quality** of calls over quantity, reducing the number of interactions but making them more impactful.
2. **Data Collection**: Future campaigns should incorporate more granular data on **customer behavior** and feedback to refine predictive models.

## Access the Jupyter Notebook

For detailed analysis, model code, and visualizations, please refer to the Jupyter Notebook: https://github.com/shaileshb2024/Marketing-Campaign-Analysis/blob/main/mywork_prompt.ipynb



 

