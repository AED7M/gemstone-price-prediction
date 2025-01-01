# Gemstone Price Prediction Project

## Overview
This project develops a predictive model for pricing cubic zirconia gemstones based on their physical characteristics. The model aims to help buyers and sellers in the market by providing accurate price estimates based on various gemstone attributes.

## Problem Statement
The goal is to create an accurate prediction model for cubic zirconia prices using various physical characteristics as input features. This tool will assist market participants in making informed decisions about gemstone pricing.

## Dataset Description

### Features
- **Carat**: Weight of the cubic zirconia (Numeric)
- **Cut**: Quality of the cut (Ordinal: Fair, Good, Very Good, Premium, Ideal)
- **Color**: Color grade (Ordinal: D [best] to J [worst])
- **Clarity**: Clarity grade (Ordinal: FL, IF, VVS1, VVS2, VS1, VS2, SI1, SI2, I1, I2, I3)
- **Depth**: Height to average girdle diameter ratio (Numeric)
- **Table**: Table width as percentage of average diameter (Numeric)
- **X**: Length in mm (Numeric)
- **Y**: Width in mm (Numeric)
- **Z**: Height in mm (Numeric)
- **Price**: Target variable - price of the cubic zirconia (Numeric)

## Methodology

### 1. Data Preprocessing
- Removal of unnecessary columns
- Data validation and type checking
- Handling duplicates and missing values
- Outlier analysis and treatment
- Multicollinearity detection
- Feature engineering (including volume calculation)
- Log transformation of key features
- Train-test split
- Categorical variable encoding
- Feature scaling/normalization

### 2. Model Development
Three regression models were implemented and compared:
- Multiple Linear Regression (MLR)
- Ridge Regression
- Lasso Regression

### 3. Model Evaluation
Models were evaluated using:
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score
- 5-fold Cross-Validation

## Results

### Model Performance Comparison

#### Multiple Linear Regression (MLR)
- Train RMSE: 0.149
- Test RMSE: 0.150
- Train/Test MAE: 0.116
- R² Score: 0.978
- CV-RMSE: 0.150

#### Ridge Regression
- Train RMSE: 0.149
- Test RMSE: 0.150
- Train MAE: 0.115
- Test MAE: 0.116
- R² Score: 0.978
- CV-RMSE: 0.150

#### Lasso Regression
- Train RMSE: 0.150
- Test RMSE: 0.151
- Train MAE: 0.115
- Test MAE: 0.116
- R² Score: 0.977
- CV-RMSE: 0.150

## Conclusions
- All models demonstrated strong performance with R² scores around 0.978
- Multiple Linear Regression and Ridge Regression showed nearly identical performance
- The models exhibited excellent stability across different validation methods
- Due to similar performance metrics and simplicity, the Multiple Linear Regression model is recommended for implementation

## Key Findings
- Models explain approximately 97.8% of the variance in gemstone prices
- Consistent performance across training and test sets indicates good generalization
- Feature engineering and transformations significantly improved model performance
- Regularization (Ridge and Lasso) did not provide substantial improvements over the base MLR model


## Requirements
- Python 3.12.5
- pandas
- numpy
- scikit-learn
- matplotlib
- seaborn

## Usage
1. Prepare the data in the required format
2. Run the preprocessing steps
3. Train the model
4. Make predictions on new data

