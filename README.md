# Used Car Price Prediction

A machine learning project that predicts the resale price of used cars based on features such as brand, model year, mileage, fuel type, transmission, and engine specifications.

## Overview

Buying and selling used cars is a market where pricing is often inconsistent and driven by guesswork or negotiation rather than data. This project builds a regression model that estimates a fair market price for a used car given its key attributes, helping buyers avoid overpaying and sellers price competitively.



## Problem statement

Given historical data on used car listings, predict the selling price of a car using its characteristics. This is framed as a supervised regression problem.

## Dataset

- Source: [add dataset source, e.g. Kaggle link]
- Size: [add number of rows and columns]
- Key features: brand, model, year of manufacture, kilometers driven, fuel type, transmission, owner type, mileage, engine capacity, power, seats
- Target variable: selling price

## Approach

1. Data cleaning: handled missing values, removed duplicates, standardized units (e.g. mileage in km/l, engine in CC)
2. Exploratory data analysis: examined price distribution, correlations between features and price, and outliers
3. Feature engineering: derived car age from manufacture year, encoded categorical variables, scaled numerical features
4. Model training: compared multiple regression algorithms
5. Model evaluation: assessed performance using R-squared, RMSE, and MAE
6. Model selection: chose the best performing model based on evaluation metrics and generalization on test data

## Tech stack

- Python
- Pandas and NumPy for data manipulation
- Matplotlib and Seaborn for visualization
- Scikit-learn for model building and evaluation
- [Add if used: XGBoost, LightGBM, Streamlit, Flask]

## Project structure

```
used-car-price-prediction/
├── data/
│   ├── raw/                  # Original dataset
│   └── processed/            # Cleaned and processed dataset
├── notebooks/
│   └── eda.ipynb             # Exploratory data analysis
│   └── model_training.ipynb  # Model building and evaluation
├── src/
│   ├── preprocessing.py      # Data cleaning and feature engineering
│   ├── train.py              # Model training script
│   └── predict.py            # Inference script
├── models/
│   └── model.pkl             # Saved trained model
├── requirements.txt
└── README.md
```

## Installation

Clone the repository and install the required dependencies.

```bash
git clone https://github.com/your-username/used-car-price-prediction.git
cd used-car-price-prediction
pip install -r requirements.txt
```

## Usage

Train the model:

```bash
python src/train.py
```

Run a prediction:

```bash
python src/predict.py --brand Honda --year 2018 --km_driven 45000 --fuel Petrol --transmission Manual
```

## Results

| Model             | R-squared | RMSE | MAE |
|-------------------|-----------|------|-----|
| Linear Regression | [value]   | [value] | [value] |
| Random Forest     | [value]   | [value] | [value] |
| XGBoost           | [value]   | [value] | [value] |

The final model achieved an R-squared of [value] on the test set, indicating that it explains [value]% of the variance in used car prices.

## Future improvements

- Incorporate additional features such as location and accident history
- Deploy the model as a web app for interactive price estimation
- Experiment with ensemble and stacking methods to improve accuracy

