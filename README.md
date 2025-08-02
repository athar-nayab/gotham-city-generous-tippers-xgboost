# gotham-city-generous-tippers-xgboost
A machine learning model to predict generous tippers and help taxi drivers maximize revenue
# 💰 Predicting Generous Tippers using XGBoost

## 📌 Objective
This project aims to support taxi cab drivers in **maximizing their revenue** by predicting whether a customer is likely to be a **generous tipper**.

We use a classification model (XGBoost) to identify patterns in tipping behavior based on ride features such as fare, distance, vendor, pickup zones, and more.

---

## 🗂️ Dataset
The dataset contains New York City taxi trip records, including:
- Fare details (tip amount, total amount, etc.)
- Trip distance and duration
- Pickup & drop-off location IDs
- Vendor and rate codes
- Payment type

The target variable is whether a **tip was above average (generous)** or not.

---

## 🔍 Exploratory Data Analysis (EDA)
Key insights:
- Generous tippers are more likely to take longer or more expensive rides.
- Tips also vary by vendor, payment method, and time of day.
- Categorical variables like `VendorID` and `RateCodeID` were one-hot encoded.

---

## 🤖 Model: XGBoost Classifier
Multiple models were tested (Random Forest, XGBoost). XGBoost outperformed in all key metrics:

| Metric     | XGBoost (Test Data) |
|------------|---------------------|
| Accuracy   | 86.01%              |
| Precision  | 85.62%              |
| Recall     | 88.23%              |
| F1 Score   | 86.91%              |

---

## 📊 Confusion Matrix & Feature Importance
- Confusion matrix shows balanced performance for both classes.
- Feature importance plot shows which ride attributes most influence tipping behavior.

---

### 🔝 Feature Highlight: `VendorID_2`
The **most important feature** in the model is `VendorID_2`.

This indicates that the **ride vendor significantly influences tipping** — Vendor 2 is more strongly associated with generous tippers.

📌 **Recommendation**:
- Further investigate why Vendor 2 performs better — policies, routes, customer types?
- Share best practices or traits with other drivers or fl

