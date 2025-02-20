# Building Energy Efficiency Prediction

## Overview

This project focuses on analyzing and predicting the energy efficiency of buildings based on various architectural and energy-related parameters. The goal is to assess the heating and cooling load requirements of buildings as a function of their features, such as glazing area, roof area, overall height, and orientation.

### Project Objective

The aim of this project is to predict the energy efficiency of buildings using a set of key building parameters. Specifically, it seeks to predict the heating load and cooling load based on features such as the building's surface area, wall area, roof area, and orientation. This project demonstrates a regression analysis approach to predicting energy consumption and evaluating model performance using Linear Regression and Random Forest Regressor models.

### Dataset

The dataset contains 768 samples and 10 features, including two target variables: Heating Load and Cooling Load. The data was simulated using 12 different building shapes in Ecotect, where each building's characteristics, including glazing area, glazing area distribution, and orientation, were varied.

The dataset contains the following columns:

- Relative_Compactness: Relative compactness of the building.
- Surface_Area: Total surface area of the building.
- Wall_Area: Area of the walls.
- Roof_Area: Area of the roof.
- Overall_Height: Height of the building.
- Orientation: Orientation of the building (e.g., North, South, East, West).
- Glazing_Area: Area covered with glass.
- Glazing_Area_Distribution: Distribution of the glazing area over the building's surface.

Targets:

- Heating_Load: Amount of energy required for heating the building.
- Cooling_Load: Amount of energy required for cooling the building.

The dataset has 768 samples, and the goal is to predict the heating and cooling load based on the 8 features.

### Steps Involved in the Analysis

1. Load and Inspect Data
- The data is loaded from a CSV file and inspected for missing values and data types. The dataset's descriptive statistics and data types are examined to ensure that all features are correctly defined.

2. Data Summary
- Descriptive statistics are calculated to summarize the distribution of features, including the mean, standard deviation, minimum, and maximum values. Outliers are identified using the Interquartile Range (IQR) method.

3. Correlation Analysis
- A correlation matrix is generated to identify relationships between features and the target variables (Heating Load and Cooling Load). Strong correlations are highlighted, and a heatmap is created for visual analysis.

4. Feature Distribution Analysis
- Histograms are plotted for each feature to understand their distributions. Skewness and kurtosis are also calculated to understand the shape of the data and determine if any transformations are required.

5. Data Preparation
- The data is split into training and test sets, and the features are scaled using StandardScaler to normalize the data. The data is now ready for modeling.

6. Train and Evaluate Models

Two regression models are trained and evaluated:

- Linear Regression: A simple linear model that predicts heating and cooling loads based on the features.
- Random Forest Regressor: A more complex, ensemble model used to predict the heating and cooling loads.

Both models are evaluated using R² Score and Root Mean Squared Error (RMSE).

7. Feature Importance Analysis
- Feature importance is analyzed using the Random Forest model, highlighting which features contribute the most to predicting energy efficiency. A bar chart is generated to visualize the feature importance.

![Linear](https://github.com/user-attachments/assets/d84097de-0616-4b2f-93b4-6ab65d634eae)

### Key Results

1. Descriptive Statistics
- Surface_Area: Range from 514.5 to 808.5 square units, with a mean of 671.71.
- Heating_Load: Ranges from 6.01 to 43.10 units, with an average of 22.31.
- Cooling_Load: Ranges from 10.9 to 48.03 units, with an average of 24.59.

2. Model Evaluation for Heating Load
- Linear Regression: R² Score: 0.9122 // RMSE: 3.0254
- Random Forest: R² Score: 0.9976 // RMSE: 0.4973

3. Model Evaluation for Cooling Load
- Linear Regression: R² Score: 0.8932 // RMSE: 3.1454
- Random Forest: R² Score: 0.9679 // RMSE: 1.7256

The Random Forest Regressor outperformed Linear Regression for both heating and cooling load predictions, with higher R² scores and lower RMSE.

### Feature Importance

The most important features for predicting heating and cooling loads are Surface_Area, Overall_Height, and Glazing_Area.

### Key Observations

- The Random Forest Regressor outperformed Linear Regression for both heating and cooling load predictions, with higher R² scores and lower RMSE values. This suggests that the Random Forest model is better at capturing the non-linear relationships in the data.
- The most important features for predicting heating and cooling loads were found to be Surface_Area, Overall_Height, and Glazing_Area.

### Source

Dataset: [Energy Efficiency Dataset on Kaggle](https://www.kaggle.com/datasets/ujjwalchowdhury/energy-efficiency-data-set)
