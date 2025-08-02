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

## 🤖 Model Development

We trained two models and compared their performance:

| Model     | F1 Score | Accuracy |
|-----------|----------|----------|
| Random Forest (Test) | 0.8389    | 0.8319    |
| XGBoost (Test)       | 0.8691    | 0.8601    |

### 🔄 Why XGBoost?
We first trained a **Random Forest** model, which performed well.  
However, to further improve **precision, recall, and F1 score**, we moved to **XGBoost**, which outperformed RF — especially in **recall**, helping us better capture generous tippers.

---

## 📊 Confusion Matrix & Feature Importance
- Confusion matrix shows balanced performance for both classes.
- Feature importance plot shows which ride attributes most influence tipping behavior.

---

### 🔝 Key Feature Insights

The model's **top influential features** for predicting generous tippers were:

| Rank | Feature         | Insight |
|------|------------------|---------|
| 1️⃣   | `VendorID_2`     | Vendor 2 rides show stronger tipping behavior than Vendor 1 |
| 2️⃣   | `fare_amount`    | Higher fares are often correlated with higher tipping |
| 3️⃣   | `trip_distance`  | Longer trips tend to receive better tips |
| 4️⃣   | `tip_percentage` | Directly linked to our target — generous tipping |
| 5️⃣   | `RatecodeID_1`   | A specific rate code often used in tipping routes |
| 6️⃣   | `pickup_hour`    | Tipping patterns vary by time of day (e.g., rush hour) |

📌 **Recommendation**:
- Further investigate **Vendor 2's performance** — policies, routes, customer types?
- Share best practices from high-tipping vendors or ride profiles with other drivers/fleets.

---

## 💼 Business Impact
This model helps stakeholders:
- Identify high-tipping ride patterns
- Offer insights to improve driver earnings
- Develop customer targeting or incentive strategies
- 
## 👨‍💼 About Me

I’m a Business Intelligence Analyst with 8+ years of experience in analytics, including 5 years at Amazon.  
I have also worked on high-impact analytics initiatives for Google, currently continuing on the same project as part of my role at Tech Mahindra.

My focus is on transforming data into strategic insights through storytelling, dashboards, and machine learning.  
This project reflects my growing specialization in predictive modeling and stakeholder-driven analytics — key skills I’m sharpening as I transition deeper into data science roles.
