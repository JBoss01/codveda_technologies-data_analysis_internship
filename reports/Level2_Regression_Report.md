# Level 2 Report: Regression Analysis

**Codveda Technologies Data Analysis Internship**
**Author:** Ozoeze Wilord Ugonna

---

## What I Did

In this task, I built a machine learning model to predict house prices using the Boston Housing dataset. The goal was to use information about a neighborhood such as crime rate, number of rooms, and pollution levels to predict the median value of homes in that area.

---

## The Dataset

I worked with the House Prediction dataset, which contained 506 records and 14 columns. The column I was trying to predict was MEDV, the median home value in thousands of dollars. The remaining 13 columns were the inputs I used to make that prediction.

---

## Steps I Took

### 1. Preparing the Data
I separated the dataset into inputs (the 13 features) and the target (MEDV). I then split the data into a training set (80%) and a testing set (20%). The model learned from the training set, and I tested how well it performed on the testing set, which it had never seen before.

### 2. Building the Model
I used a linear regression model from scikit-learn. This type of model works by drawing the best possible straight line through the data. It learns how much each feature contributes to the final home value prediction.

### 3. Evaluating the Model
I measured how well my model performed using two metrics:

**1. R-squared** tells me what percentage of the variation in house prices my model can explain. A score closer to 1.0 is better.

**2. Root Mean Squared Error (RMSE)** tells me how far off my predictions were on average, in the same units as the target (thousands of dollars).

---

## What I Discovered

- **Room count (RM)** had the strongest positive effect on house prices. Homes with more rooms were worth significantly more.
- **Lower status population percentage (LSTAT)** had the strongest negative effect. Neighborhoods with higher proportions of lower-income residents had lower home values.
- **Crime rate (CRIM)** also pulled prices down, which matched my expectations.
- My model captured the broad relationship between features and prices, but I noticed it struggled a little at the very high end of the price range where values appeared to be capped at $50,000.

---

## Limitations I Observed

- Linear regression assumes a straightline relationship between inputs and the target, which is not always true in real housing data.
- The price cap at $50,000 in the dataset likely made it harder for my model to predict accurately for the most expensive homes.
- In future work, I would try more advanced models like Random Forest or Gradient Boosting to capture nonlinear patterns.

---

## What I Learnt

A model can look good on paper but still have weaknesses. Looking at my residual plots, the gap between what I predicted and what actually happened showed me patterns that the simple R-squared number alone would have hidden. I learned to always look beyond a single performance metric.