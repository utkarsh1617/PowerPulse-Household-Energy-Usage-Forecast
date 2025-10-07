PowerPulse: Household Energy Usage Forecast

This project develops and evaluates several regression models to predict household Global Active Power consumption based on minute-by-minute historical data and engineered features.

Project Deliverables

This submission includes two main files:

powerpulse_model.py: The complete Python script for data loading, preprocessing, feature engineering, model training (Linear Regression, Random Forest, XGBoost), and final evaluation/visualization.

Project Report PowerPulse Household Energy Usage Forecast.pdf: A comprehensive report summarizing the methodology, results, and key insights (including final model performance and feature importance).

1. Data Source
The project uses the Individual Household Electric Power Consumption dataset.

Original Data Format: Semicolon (;) separated text file.

Target Variable: Global_active_power (in kilowatts).

2. Setup and Dependencies
To run the powerpulse_model.py script, you must have the following Python libraries installed:

pip install pandas numpy scikit-learn matplotlib xgboost

3. How to Run the Code
Locate the Data: Ensure your data file (household_power_consumption.txt) is in the same directory as powerpulse_model.py.

Update File Path (if necessary): If your data file is in a different location, open powerpulse_model.py and update the file_path variable in Section 1 (SETUP AND DATA LOADING) with the correct absolute path.

Execute the Script: Run the script from your terminal or command line:

python powerpulse_model.py

4. Key Methodology Highlights
Time-Series Integrity: Data was split sequentially (80% Train, 20% Test) to ensure strict chronological separation.

Imputation: Missing values (? converted to NaN) were handled using a combination of Forward Fill (ffill) and Backward Fill (bfill) for maximum data continuity.

Feature Engineering: Includes custom time-based features (Hour, DayOfWeek) and a critical 24-hour Rolling Mean lagged feature to capture recent consumption trends.

5. Summary of Results
Best Model: XGBoost Regressor

Performance: R 
2
 =0.9984 | RMSE =0.0356

Primary Insight: The model's prediction is overwhelmingly driven by the Global_intensity (current), followed by specific sub-metered appliances (Sub_metering_1 and Sub_metering_3).

Refer to the attached PDF report for full analysis, model comparison tables, and detailed visualizations.
