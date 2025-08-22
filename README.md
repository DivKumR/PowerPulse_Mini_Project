# PowerPulse energy forecasting model
**Project Description**
PowerPulse is a machine learning-based energy forecasting model designed to predict household energy consumption using historical data.
Predicting energy usage accurately enables better planning, cost reduction, and resource optimization.
📄 Detailed Project Description: https://docs.google.com/document/d/1CGaV9KGSUZnM5B-Nyc_4Uu6Jc76gx5Gx_xFBNJQIdrM/edit?tab=t.0

**Data Understanding and Exploration:**

Dataset Source
- UCI Repository: Household Electric Power Consumption
- Data Retrieval Code:
from ucimlrepo import fetch_ucirepo
data_power_consumption = fetch_ucirepo(id=235)

Output:
Supervised Learning Approach
Since we have labeled data (input-output pairs), we train regression models to predict Global_active_power based on features.
- Features (X): Voltage, Global Intensity, Sub-Metering values
- Target (y): Global Active Power

**Data Preprocessing:**

Steps Taken

✅ Handled missing or inconsistent data

✅ Parsed date/time into separate features

✅ Scaled data to improve model performance

✅ Addressed dataset issues, including:

- Data types & conversions
- Null values & memory optimization
- Distribution analysis & feature statistics
- Outlier detection & anomaly handling

**Feature Engineering:**
Feature Selection Approach

- Applied Z-score for outlier detection
- Used histograms & boxplots to analyze feature distributions
- Checked correlations to identify high-impact features
📊 Final Features Used for Modeling:

✅ Global_intensity, Voltage, Global_reactive_power

✅ Hour, Day, Month (Time-Based Features)

**Model Selection and Training:**
Regression Models Evaluated

1️⃣ Linear Regression → Simple statistical model

2️⃣ Random Forest → Ensemble decision trees for accuracy

3️⃣ Gradient Boosting → Powerful iterative correction method

4️⃣ RandomForestClassifier (Classification Approach)


**Model Evaluation:**

Key Metrics Used

✅ RMSE (Root Mean Squared Error) → Measures average prediction error

✅ MAE (Mean Absolute Error) → Measures absolute differences

✅ R² Score → Explains variance captured by the model

Evaluation Visualizations

📈 Residual Plots → Analyzes prediction errors

📊 Actual vs. Predicted Value Plots → Detects underfitting/overfitting

📊 R² Score Comparison Bar Plot → Compares overall model accuracy

 **Model Performance Comparison**
Example: 
Regression Model Results
| Model | RMSE | MAE | R² Score | 
| Linear Regression | 0.0432 | 0.0286 | 0.9983 | 
| Random Forest | 0.0318 | 0.0143 | 0.9991 | 
| Gradient Boosting | 0.0373 | 0.0219 | 0.9988 | 

**Best Model Choice:**
- Random Forest (lowest RMSE & MAE, highest accuracy)
- Gradient Boosting is a strong alternative

**Classification Model Insights**
Class Distribution in the Dataset
| Category | Count | 
| Low | 1,923,656 | 
| Medium | 108,077 | 
| High | 17,547 | 

Most values fall in the "Low" category, indicating that high-power consumption events are rare.
Classification Model Performance
✅ Random Forest Classifier Accuracy: 99.82%
- Features (Voltage, Global_intensity, etc.) are highly predictive.
- However, dataset imbalance could affect recall for minority classes.


📂 Documentation:
Results.pdf → Screenshots showing analysis results
