# Car Price Prediction
Oasis InfoByte Internship | Task 3

This project aims to develop a machine learning model to predict the selling price of used cars based on various features. The dataset used in this project was obtained from a popular car sales platform.

## Table of Contents
- [Introduction](#introduction)
- [Data Exploration](#data-exploration)
- [Feature Engineering](#feature-engineering)
- [Model Building](#model-building)
- [Results](#results)
- [Conclusion](#conclusion)

## Introduction
The used car market is a complex and dynamic ecosystem, with various factors influencing the selling price of vehicles. Accurately predicting the price of a used car can be challenging, but it is crucial for both buyers and sellers to make informed decisions. This project explores the application of machine learning techniques to tackle this problem and provide a reliable price prediction model.

## Data Exploration
The dataset consists of 301 used car listings, with features such as car name, year of manufacture, selling price, present price, driven kilometers, fuel type, selling type, transmission, and owner count. The data was thoroughly analyzed, and key insights were drawn:

- The selling price distribution is right skewed, indicating that most used cars sell for less than 10 lakhs, with a few outliers at significantly higher prices.
- Strong multicollinearity was observed among the selling price, present price, and year of manufacture features, suggesting the need for feature reduction.

## Feature Engineering
To enhance the model's performance, several feature engineering steps were taken:

1. **Extracting Car Age**: The car age was calculated by subtracting the year of manufacture from the current year (2025).
2. **Extracting Brand Names**: The car brand was extracted from the car name feature.
3. **Computing Car Depreciation**: The car depreciation was calculated as the difference between the present price and the selling price.
4. **Label Encoding**: Categorical features, such as fuel type, selling type, and transmission, were label-encoded to prepare them for the machine learning models.
5. **Target Encoding**: The car brand feature was target encoded using the mean selling price for each brand.

## Model Building
Two regression models were trained and evaluated:

1. **Linear Regression**: A linear regression model was trained on the scaled feature set.
2. **Random Forest Regressor**: A Random Forest Regressor model was trained on the original feature set.

## Results
The evaluation metrics for the two models are as follows:

**Linear Regression**:
- RMSE: 0.3274
- R² Score: 0.8358

**Random Forest Regressor**:
- RMSE: 0.1514
- R² Score: 0.9649

The Random Forest Regressor outperformed the Linear Regression model, achieving a significantly lower RMSE and a higher R² score, indicating better predictive accuracy and a stronger ability to capture complex patterns in the data.

## Conclusion
This project demonstrates the effectiveness of using machine learning techniques, particularly the Random Forest Regressor, to predict the selling price of used cars. The feature engineering and model selection steps played a crucial role in achieving high performance results. The insights gained from this analysis can be valuable for both car buyers and sellers in making informed decisions.
