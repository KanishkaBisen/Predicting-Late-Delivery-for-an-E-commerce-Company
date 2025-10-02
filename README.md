Predicting Late Deliveries in E-Commerce
Machine learning project using the Olist dataset to predict whether an order will arrive on time or late.
Helps businesses improve customer satisfaction by proactively flagging high-risk shipments.

✨ Overview
Dataset: Olist e-commerce (orders, products, sellers, customers, geolocation).

Goal: Predict late deliveries with ML models.

Approach:
Data cleaning & preprocessing (dates, missing values, numeric features).

Feature engineering:
Distance between seller & customer (Haversine formula).
Product bulkiness (volume × weight).
Holiday & weekend flags.
Multiple sellers/items per order.
Logistic delays (late to carrier).
Exploratory Data Analysis (EDA).
Model training & evaluation with cross-validation.

🧠 Models & Results

| Model               | ROC AUC  | Recall   | Precision | Accuracy |
| ------------------- | -------- | -------- | --------- | -------- |
| Logistic Regression | 0.64     | 0.59     | 0.11      | 0.61     |
| Random Forest       | 0.79     | 0.20     | 0.83      | 0.93     |
| **XGBoost (Best)**  | **0.78** | **0.66** | 0.19      | 0.75     |


👉 XGBoost selected for best trade-off between recall (capturing late orders) and generalizability.

📊 Key Insights

Late deliveries = ~9% of orders → strong class imbalance.

High-demand months → spikes in delays.

Long distances & cross-state shipments more likely to be late.

Surprisingly, holiday/weekend orders had slightly fewer delays.

Strongest predictor: given_to_carrier_after_estimated flag.

✅ Business Value

Proactively flag risky shipments in the order pipeline.

Improve logistics decisions (rerouting, prioritization).

Enhance customer communication by predicting delays early.

🔮 Future Work

Integrate real-time traffic, weather, courier capacity.

Collect warehouse handover times & courier performance metrics.

Experiment with deep learning / ensemble methods.

Add explainability tools (SHAP, LIME) for business insights.

🛠️ Tech Stack

Python: pandas, numpy, scikit-learn, xgboost

Visualization: matplotlib, seaborn

Geospatial: geopy (Haversine formula)

ML Pipeline: feature engineering, cross-validation, model evaluation
