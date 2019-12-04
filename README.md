# NHL Salary Prediction
Inspired by the past Kaggle competition of [NHL Data](https://www.kaggle.com/camnugent/predict-nhl-player-salaries#train.csv), using game stats on NHL Players, we will fit multiple models to predict the player salary. For USF's MSDS 699 course, we document our modeling process to demonstrate our Machine Learning efforts in this project.

## Workflow of this repository
1. Direct Feature engineering was done on the raw dataset
The direct feature engineering reads in the data from data/clean, and output the data to data/processed
2. Exploratory Data Analysis was done to find logical trends and visualization of data
3. Three different regressor models were fitted to the processed data
  - A lasso regression model was used as a baseline
  - A RandomForestRegression model
  - A KNN model
Models were processed using a pipeline and validated using cross-validation.
 
4. After model selection was done and the RandomForestRegression model was chosen, it was developed and a more comprehensive drop_list and feature importance were done to develop our final model. Hyper parameter turning was done using a Random Search to further improve the model.

All modeling was done in tidy format using sklearn's library of modeling tools

## Results

Evaluation metrics of MedAE and MAPE were used to look at the success of the various models. Testing was done on a test set of a 75/25 split.

  - Ridge Regression - MAPE = 72.48% error, MedAE = $713,134.33
  - Random Forest - MAPE = 54.4%, MedAE = $508,910.19
  - KNN - MAPE = 71.2% error, MedAE = $758,416.13
