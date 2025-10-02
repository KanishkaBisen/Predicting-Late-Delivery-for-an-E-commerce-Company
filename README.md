Predicting Late Deliveries in E-Commerce

This project uses machine learning to predict late deliveries in Brazilian e-commerce, leveraging the Olist dataset. Timely deliveries are critical for customer satisfaction and business reputation. By identifying at-risk orders before they ship, businesses can take proactive measures to reduce delays and improve customer experience.

Project Overview:

Dataset: Olist e-commerce (orders, customers, sellers, products, geolocation).

Objective: Predict if an order will be delivered on time or late.


Key Steps:

Data cleaning & preprocessing (dates, missing values, numeric features).

Feature engineering:

Distance between seller & customer (Haversine formula).

Product bulkiness (volume × weight).

Holiday & weekend flags.

Multiple sellers/items per order.

Logistic delays (late to carrier).

Exploratory Data Analysis (EDA).

Machine learning model training & evaluation.


Models Tested:

Logistic Regression (baseline): AUC 0.64, Recall 0.59, low precision.

Random Forest: AUC 0.79, Precision 0.83, but Recall only 0.20.

XGBoost (Best Model): AUC 0.78, Recall 0.66, Precision 0.19.

XGBoost selected for best balance between recall and overall predictive power.


Key Insights:

Only ~9% of orders are late → strong class imbalance.

High-demand months show spikes in delays.

Cross-state & long-distance orders are more likely delayed.

Surprisingly, holiday/weekend orders perform slightly better.

Strongest predictor: given_to_carrier_after_estimated flag.


Conclusion:

This solution provides a scalable, data-driven method to identify delivery risks in e-commerce.

XGBoost outperforms other models by capturing complex interactions.

Businesses can proactively flag risky shipments, reroute logistics, and notify customers early.


Future Work:

Integrate real-time data: traffic, weather, courier capacity.

Add courier performance metrics and warehouse handling times.

Explore deep learning or ensemble methods.

Use SHAP/LIME for interpretability in production.


Tech Stack:

Python (pandas, numpy, scikit-learn, xgboost)

Data viz: matplotlib, seaborn

Geospatial: geopy (Haversine distance)

EDA & preprocessing: StandardScaler, feature engineering
