# 🚗 Car Price Prediction — From Raw Data to Business Value

<p align="center">
  <b>An end-to-end machine learning project focused on real-world pricing strategy</b><br>
  Transforming messy automotive data into accurate, deployable price predictions
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue">
  <img src="https://img.shields.io/badge/Machine%20Learning-End--to--End-green">
  <img src="https://img.shields.io/badge/Focus-Business%20Impact-orange">
  <img src="https://img.shields.io/badge/Status-Production%20Ready-brightgreen">
</p>

---

## 🎯 The Goal

Car pricing is complex — influenced by engine specs, brand perception, fuel efficiency, and hidden interactions between them.

This project answers a practical question:

> **How accurately can we predict car prices using only technical and categorical features?**

And more importantly:

> **Which factors actually drive price — and how can businesses use that insight?**

---

## 💼 Why This Project Matters

* 🚗 **Dealerships** → Price vehicles competitively
* 📊 **Market analysts** → Understand value drivers
* 💰 **Consumers** → Avoid overpaying
* 🏢 **Businesses** → Optimize inventory and margins

---

## ⚡ What I Built

A **complete ML pipeline**, not just a model:

* Data cleaning & preprocessing
* Feature engineering based on domain intuition
* Model training + hyperparameter tuning
* Cross-validation for reliability
* Model comparison across 4 algorithms
* Automatic **best-model selection**
* Exportable pipeline (ready for deployment)
* Diagnostic visualizations for interpretation

---

## 🧠 Key Insight (The “Aha” Moment)

> **Car prices are not linear.**

Simple models (Ridge) struggle because:

* The impact of horsepower depends on **brand**
* Fuel efficiency matters differently for **economy vs luxury cars**
* Engine size interacts with **cylinder configuration**

👉 **Tree-based models (XGBoost, Gradient Boosting)** outperform because they *learn these interactions automatically*.

---

## 🏆 Results That Matter

* 📈 Strong predictive performance (low RMSE, high R²)
* 🔁 Stable cross-validation scores (low variance)
* 🧠 Clear feature importance patterns
* ⚙️ Fully reusable trained model pipeline

✔ The model is not just accurate — it’s **reliable and deployable**

---

## 🔍 What Drives Car Prices?

From both feature importance and domain interpretation:

### 🚀 Performance matters most

* `horsepower`
* `engine size`
* `power-to-weight ratio`

### 🏷️ Brand influence is real

* Extracted from raw text (`CarName`)
* Cleaned and standardized
* Strong signal in tree-based models

### ⚖️ Weight & efficiency trade-off

* Heavier cars → higher cost
* Better MPG → lower cost (in most cases)

---

## 🧪 Technical Highlights

### Feature Engineering (where most value came from)

* `power_to_weight` → performance proxy
* `avg_mpg` → simplified efficiency
* `cc_per_cyl` → engine refinement

👉 These features significantly improved model performance

---

### Smart Modeling Choices

* Used **log transformation** to stabilize skewed prices
* Applied **RobustScaler** to handle outliers
* Chose **RandomizedSearchCV** for efficient tuning
* Built a **composite scoring system** instead of relying on one metric

---

### Model Selection Strategy

Instead of picking the “best RMSE”, I used:

```
Composite Score = 40% R² + 35% (1/RMSE) + 25% (1/MAPE)
```

👉 This balances:

* Accuracy
* Error magnitude
* Business relevance

---

## 📊 Visual Evidence

<p align="center">
  <img src="outputs/model_comparison.png" width="30%">
  <img src="outputs/feature_importance.png" width="30%">
  <img src="outputs/learning_curves.png" width="30%">
</p>

<p align="center">
  <img src="outputs/actual_vs_predicted.png" width="45%">
  <img src="outputs/residuals.png" width="45%">
</p>

---

## 🚀 From Model → Production

This project doesn’t stop at training:

✔ Best model saved (`best_model.pkl`)
✔ Preprocessing pipeline saved (encoders + scaler)
✔ Ready for:

* API deployment (Flask / FastAPI)
* Dashboard (Streamlit)
* Integration into pricing systems

---

## ⚠️ Challenges & How I Solved Them

| Challenge                 | Solution                          |
| ------------------------- | --------------------------------- |
| Messy brand names         | Extracted + standardized manually |
| Skewed price distribution | Log transformation                |
| Small dataset             | Cross-validation for reliability  |
| Non-linear relationships  | Ensemble models                   |
| Outliers                  | IQR filtering + RobustScaler      |

---

## 📈 What I’d Improve Next

* Add **SHAP explainability** for decision transparency
* Use **Optuna** for smarter hyperparameter tuning
* Integrate **external brand value data**
* Build a **live pricing app (Streamlit)**

---

## 🧰 Tech Stack

* Python (pandas, numpy)
* scikit-learn
* XGBoost
* matplotlib / seaborn
* joblib

---

## 📌 Final Takeaway

> This project demonstrates not just model building, but **end-to-end problem solving**:

* Turning raw data into meaningful features
* Choosing the *right* models (not just complex ones)
* Balancing metrics with business impact
* Delivering a solution that can actually be used

---
