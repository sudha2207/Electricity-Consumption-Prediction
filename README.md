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

## Project Conclusion

The Electricity Consumption Prediction project demonstrates the application of machine learning regression algorithms to predict electricity consumption using environmental conditions, building characteristics, occupancy, and usage-related features.

Four algorithms—Linear Regression, Decision Tree Regression, Random Forest Regression, and Gradient Boosting Regression—were implemented and evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R² score.

Among the four models, **Linear Regression achieved the best overall performance**, with an MAE of 4.12, an RMSE of 5.15, and an R² score of 0.5947. Random Forest and Gradient Boosting also demonstrated reasonable predictive performance, while Decision Tree Regression performed comparatively less effectively on the test dataset.

The results highlight the importance of evaluating multiple algorithms to identify a suitable model for a given prediction task. The project also demonstrates how data preprocessing, feature engineering, exploratory data analysis, and model evaluation contribute to a complete machine learning workflow.

Overall, this project provides practical experience in developing and comparing regression models for electricity consumption prediction. Future improvements could include hyperparameter tuning, cross-validation, and testing on larger, independently sourced real-world datasets to further evaluate and improve predictive performance.
