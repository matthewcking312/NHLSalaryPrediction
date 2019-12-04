# NHL Salary Prediction
Inspired by the past Kaggle competition of [NHL Data](https://www.kaggle.com/camnugent/predict-nhl-player-salaries#train.csv), using game stats on NHL Players, we will fit multiple models to predict the players' salary. For USF's MSDS 699 course, we document our modeling process to demonstrate our Machine Learning efforts in this project.

## Workflow of this repository
All work consolidated onto [one jupyter notebook](https://github.com/matthewcking312/NHLSalaryPrediction/blob/master/The_Big_One_Final_Project_Notebook.ipynb)
1. Direct Feature engineering was done on the raw dataset
The direct feature engineering reads in the data from data/clean, and output the data to data/processed
2. Exploratory Data Analysis was done to find logical trends and visualization of data
3. Three different regressor models were fitted to the processed data
  - A ridge regression model was used as a baseline
  - A RandomForestRegression model
  - A KNN model
Models were processed using a pipeline and validated using cross-validation.

4. After model selection was completed and the RandomForestRegression model was chosen, it was developed and a more comprehensive drop_list and feature importance were done to develop our final model. Hyperparameter tuning was done using a Random Search to further improve the model.

All modeling was done in tidy format using sklearn's library of modeling tools

## Results

Evaluation metrics of MedAE and MAPE were used to look at the success of the various models. Testing was done on a test set of a 75/25 split.

  - Ridge Regression
  - Random Forest
  - KNN

  The Random Forest Model was chosen as our final model. After looking at feature important in relation to this model using Github user Parrt's [rfpimp package](https://github.com/parrt/random-forest-importances), we dropped unimportant columns and refit. This model was then run on our test set to establish the final evaluation score for our model.

EDA and Model Visualizations can be found [here](https://github.com/matthewcking312/NHLSalaryPrediction/tree/master/images)
