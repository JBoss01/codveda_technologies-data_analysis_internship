# Level 3 Report: Predictive Modeling (Classification)

**Codveda Technologies Data Analysis Internship**
**Author:** Ozoeze Wilord Ugonna

---

## What I Did

In this task, I built and compared several machine learning models to predict whether a customer would churn, meaning stop using a service. Being able to identify customers who are likely to leave gives a business the chance to step in and retain them before it is too late.

---

## The Dataset

I worked with the churn dataset, which was already split into a training set (80%) and a testing set (20%). The target column was Churn, a Yes or No label indicating whether a customer had left. The remaining columns contained information about each customer's usage patterns, account details, and service interactions.

---

## Steps I Took

### 1. Preparing the Data
I handled categorical columns by converting them into numbers using label encoding, since machine learning models work with numbers rather than text. I also scaled the numerical features using StandardScaler so that no single column would dominate the model simply because of its size.

### 2. Models I Trained
I trained and compared three different models:

**Logistic regression** is a simple but interpretable model that works like a weighted scoring system.

**A decision tree** is a model that makes decisions by asking a series of yes or no questions about the data.

**Random Forest** is a more powerful model that combines hundreds of decision trees and takes a majority vote.

### 3. Hyperparameter Tuning
For the Random Forest model, I used GridSearchCV to test different combinations of settings to find the version that performed best. I tested different numbers of trees, maximum tree depths, and minimum sample requirements.

### 4. How I Measured Performance
I used four metrics instead of just accuracy:

**1. Accuracy** is the percentage of all predictions that were correct.

**2. Precision** measures how many of the customers I flagged as churners actually churned.

**3. Recall** measures how many of the customers who actually churned I correctly predicted.

**4. The F1 score** is a combined score that balances precision and recall.

I paid special attention to Recall because missing a real churner is more costly to a business than occasionally flagging a loyal customer by mistake.

---

## What I Discovered

- The tuned Random Forest model outperformed both Logistic Regression and the basic Decision Tree across all four metrics.
- The most important features for predicting churn were the number of customer service calls, total daytime minutes used, and whether the customer had an international plan.
- Customers who contacted customer service frequently were significantly more likely to churn, suggesting dissatisfaction that the business could have addressed earlier.

---

## Limitations I Observed

- The dataset had more non-churners than churners, which means a lazy model could score high accuracy by simply predicting everyone stays. This is why I focused on F1 score and recall rather than accuracy alone.
- Techniques like SMOTE, which creates synthetic examples of the minority class, could further improve the model's ability to catch churners.

---

## What I Learnt

Accuracy is a misleading metric when one outcome is much rarer than the other. A model that predicts every customer stays would be 85% accurate but completely useless in practice. This task taught me to always match my evaluation metric to the real-world cost of being wrong.