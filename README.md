# Electricity Consumption Prediction Using Machine Learning

## Project Overview

Electricity Consumption Prediction is a machine learning project that predicts electricity consumption based on environmental conditions, building characteristics, occupancy, and usage-related features.

The project implements and compares multiple regression algorithms to evaluate their performance in predicting electricity consumption.

## Objectives

- Analyze electricity consumption data using Exploratory Data Analysis (EDA).
- Perform data preprocessing and feature engineering.
- Implement multiple machine learning regression algorithms.
- Evaluate model performance using MAE, RMSE, and R² score.
- Compare the performance of different algorithms.
- Predict electricity consumption for new input data.

## Dataset

The project uses a CSV dataset containing 1,000 records and 11 original columns.

### Features

| Feature | Description |
|---|---|
| Timestamp | Date and time of observation |
| Temperature | Temperature measurement |
| Humidity | Humidity level |
| SquareFootage | Building area |
| Occupancy | Number of occupants |
| HVACUsage | HVAC usage status |
| LightingUsage | Lighting usage status |
| RenewableEnergy | Renewable energy value |
| DayOfWeek | Day of the week |
| Holiday | Holiday indicator |

### Target Variable

- `ElectricityConsumption`: The target variable used to predict electricity consumption.

The original timestamp is converted into useful time-based features, and categorical variables are encoded before model training.

**Note:** The dataset contains 1,000 records. Its source and whether it is synthetic or real-world data should be verified and acknowledged appropriately.

## Technologies Used

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- GitHub

## Machine Learning Algorithms

The following regression algorithms are implemented and compared:

1. Linear Regression
2. Decision Tree Regression
3. Random Forest Regression
4. Gradient Boosting Regression

## Project Workflow

1. Dataset loading
2. Data inspection
3. Timestamp conversion and feature extraction
4. Categorical variable encoding
5. Exploratory Data Analysis
6. Train-test split
7. Model training
8. Model evaluation
9. Algorithm comparison
10. Electricity consumption prediction

## Evaluation Metrics

The models are evaluated using the following metrics:

- **Mean Absolute Error (MAE):** Measures the average absolute difference between actual and predicted values. Lower is better.
- **Root Mean Squared Error (RMSE):** Measures prediction error while penalizing larger errors. Lower is better.
- **R² Score:** Measures how much variation in the target is explained by the model. Higher is generally better.

## Results

The models were evaluated using a test set containing 200 records.

| Algorithm | MAE | RMSE | R² Score |
|---|---:|---:|---:|
| Linear Regression | 4.1203 | 5.1524 | 0.5947 |
| Random Forest | 4.3373 | 5.4072 | 0.5536 |
| Gradient Boosting | 4.4387 | 5.5430 | 0.5309 |
| Decision Tree | 5.8895 | 7.4263 | 0.1580 |

### Best Performing Model

Linear Regression achieved the best overall results among the four tested algorithms, with the lowest MAE and RMSE and the highest R² score.

Its R² score was approximately 0.595, indicating that it explained about 59.5% of the variation in electricity consumption on the test set.

These results apply to the current dataset and train-test split. Performance may differ with other datasets or validation methods.

## Visualizations

The project includes the following visualizations:

- Electricity consumption distribution
- Temperature versus electricity consumption
- Correlation heatmap
- MAE comparison
- RMSE comparison
- R² score comparison
- Actual versus predicted electricity consumption
- Prediction error distribution

## Project Structure

```text
Electricity-Consumption-Prediction/
│
├── Electricity_Consumption_Prediction.ipynb
├── data/
│   └── Electricity_consumption.csv
├── results/
│   ├── model_comparison_results.csv
│   └── graphs/
│       ├── consumption_distribution.png
│       ├── temperature_vs_consumption.png
│       ├── correlation_heatmap.png
│       ├── algorithm_comparison.png
│       ├── actual_vs_predicted.png
│       └── prediction_error_distribution.png
├── README.md
├── requirements.txt
└── .gitignore
