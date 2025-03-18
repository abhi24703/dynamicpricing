# Dynamic Hotel Room Pricing Model
This project implements a Dynamic Hotel Room Pricing Model using Machine Learning and Agentic AI. The model predicts optimal room prices based on various factors, including day of the week, weekends, public holidays, occupancy rate, competitor pricing, and demand fluctuations.

🔹 Features
Machine Learning-Based Pricing: Uses XGBoost to train a model on historical hotel pricing data.
Occupancy-Based Pricing Tiers: Adjusts prices dynamically based on hotel occupancy levels.
Competitor Price Influence: Modifies the predicted price based on competitor pricing fluctuations.
One-Hot Encoding for Categorical Data: Handles categorical features like day of the week.
Standardization of Numerical Features: Scales features such as occupancy rate and competitor price.
Explainable Price Adjustments: Clearly defined pricing adjustments based on external factors.
📊 Data Preprocessing
The dataset is preprocessed to include relevant features:
Day_of_Week (encoded using one-hot encoding)
Is_Weekend (binary feature)
Is_Holiday (binary feature)
Occupancy_Rate (normalized)
Competitor_Price (normalized)
Feature scaling is applied using StandardScaler from sklearn.
🚀 Model Training
The model is trained using XGBoost Regressor, optimized with hyperparameters like learning_rate, max_depth, and subsample.
Performance is evaluated using Root Mean Squared Error (RMSE) and R² Score.
🎯 Dynamic Pricing Adjustments
Occupancy-Based Pricing:
0-30% occupancy → -12% price discount
30-50% occupancy → -5% price discount
50-70% occupancy → No change
70-80% occupancy → +6% price premium
80-90% occupancy → +10% price premium
90%+ occupancy → +15% price premium
Competitor Price Influence:
Adjusts based on competitor price deviations from a baseline (8000 INR), with a max 10% adjustment.
