# Formula-1-race-prediction

This project contains two Google Colab notebooks for predicting Formula 1 race results. The code is intentionally simple and easy to follow.

## Files

- `Existing_models.ipynb` - standard machine learning models: Logistic Regression, Linear Regression, Random Forest, Gradient Boosting, and XGBoost.
- `Custom_model.ipynb` - a custom neural network built with TensorFlow/Keras.

## Dataset

The attached Zenodo JSON file contains record metadata, not the actual CSV tables. The notebooks download an open Ergast-style Formula 1 CSV archive.

Main tables used:

- `races.csv`
- `results.csv`
- `drivers.csv`
- `constructors.csv`
- `circuits.csv`
- `qualifying.csv`
- `status.csv`

## Experiment

- Train period: 2013-2022
- Test season: 2023
- Main target: race finishing position
- Additional target: podium probability
- Final comparison: predicted 2023 season points vs actual points

## Features

- driver
- constructor
- circuit
- country
- grid position
- qualifying position
- DNF flag
- average position in the last 3 races
- average season position before the current race
- podium percentage before the current race
- points in the last 5 races
- constructor form in the last 3 races
- weather = `unknown` because this dataset does not include race weather

## Custom neural network

The second notebook uses a custom TensorFlow/Keras model with Dense layers, ReLU activation, Dropout, Adam optimizer, MSE loss, and backpropagation through `model.fit()`.
