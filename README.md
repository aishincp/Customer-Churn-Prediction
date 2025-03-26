# Customer-Churn-Prediction 
### (Exploratory Data Analysis & Machine Learning)

## *Description*:
*Developed an ML-based classification model to predict customer churn, applying exploratory data analysis (EDA) to understand churn drivers, followed by feature engineering and training models using Random Forest, XGBoost, and Logistic Regression to optimize prediction accuracy and retention strategies.*

Documentation can be found [here](https://github.com/aishincp/Customer-Churn-Prediction/blob/main/CustomerChurnPrediction.ipynb)

## Model Overview
- **Model**: Random Forest
- **Accuracy**: 77.14%
- **Objective**: Predict whether a customer will churn or not based on various customer features.

## 1. Model Accuracy
The model's accuracy of **77.14%** means it correctly classified 77.14% of all customers as either churners or non-churners.

## 2. Key Insights from the Classification Report

| Metric          | No Churn (0) | Churn (1)  |
|-----------------|--------------|------------|
| **Precision**   | 0.84         | 0.58       |
| **Recall**      | 0.84         | 0.57       |
| **F1-Score**    | 0.84         | 0.58       |
| **Support**     | 1539         | 574        |

### What This Means:
- **No Churn (0)**:
  - Precision: 84% of customers predicted as non-churners are correctly predicted.
  - Recall: 84% of actual non-churners are correctly identified.
  
- **Churn (1)**:
  - Precision: 58% of customers predicted as churners are correctly predicted.
  - Recall: 57% of actual churners are correctly identified, meaning 43% are missed.

## 3. Confusion Matrix

|               | Predicted No Churn (0) | Predicted Churn (1) |
|---------------|------------------------|---------------------|
| **True No Churn (0)** | 1300                   | 239                 |
| **True Churn (1)**    | 244                    | 330                 |

### Breakdown:
- **True Positives (TP)**: 330 (Correctly predicted churners)
- **True Negatives (TN)**: 1300 (Correctly predicted non-churners)
- **False Positives (FP)**: 239 (Incorrectly predicted churners for non-churners)
- **False Negatives (FN)**: 244 (Incorrectly predicted non-churners for churners)

### What This Means:
- **Non-Churners (No)**:
  - The model correctly predicted 1300 out of 1539 non-churners, achieving an **84%** accuracy for non-churners.
  
- **Churners (Yes)**:
  - The model only correctly predicted 330 out of 574 churners, leading to a **57%** accuracy for churners.
  
- The model struggles more with predicting **churners** (higher False Negatives), which means it often misses churners, falsely classifying them as non-churners.

## 4. Conclusion: What Does 77% Accuracy Mean?

- **Overall Accuracy**: 77.14% of all predictions (both churners and non-churners) were correct.
- **Strengths**: The model performs well in predicting customers who will stay (non-churners), with an 84% accuracy rate for "No Churn."
- **Weaknesses**: The model struggles with churners, only correctly identifying 57% of them, leading to a high rate of **False Negatives**.
- **Improvement**: The model can be improved by addressing the **class imbalance** (since churn cases are fewer). Techniques like **SMOTE** (Synthetic Minority Over-sampling Technique) or other sampling methods could help improve churn prediction.

### Next Steps:
- Investigate further data preprocessing or balancing techniques.
- Experiment with other machine learning models (e.g., XGBoost, Logistic Regression) to improve churn prediction.
