# NHL Salary Prediction
Inspired by the past Kaggle competition (https://www.kaggle.com/camnugent/predict-nhl-player-salaries#train.csv), using game stats on NHL Players, we will fit multiple models to predict the player salary. For USF's MSDS 699 course, we document our modeling process to demonstrate our Machine Learning efforts in this project.

## Workflow of this repository
1. Direct Feature engineering was done in the Processing_Data.ipynb.
The notebook would read in the data from data/clean, and output the data to data/processed
2. Exploratory Data Analysis was done to find logical trends and visualization of data in the EDA.ipynb notebook
3. Three different Models were fitted to the processed data
  - A lasso regression model was used as a baseline and was fitted in the Baseline_Model.ipynb notebook
  - A RandomForestRegression model was fitted in the ML_Lab_Project_Practice.ipynb notebook
  - A KNN model was fitted in the KNN.ipynb notebook
4. After model selection was done and the RandomForestRegression model was chosen, it was further developed in the ML_Lab_Project.ipynb notebook. A more comprehensive drop_list and feature importance was done to develop our final model

All modeling was done in tidy format using sklearn's library of modeling tools

##
