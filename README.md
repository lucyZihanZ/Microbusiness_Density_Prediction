# XGBoosting and LightGBM to Predict the microbusiness density

1.**Dataset**:
-The dataset used in this study is sourced from Kaggle`https://www.kaggle.com/competitions/godaddy-microbusiness-density-forecasting/data`, focusing on predicting micro-business density**. 

2.**Data Analysis**:

Machine learning algorithms `XGBoost (XGB)` and `LightGBM` are utilized for the prediction task. 

3.**Feature engineering**:

*Feature engineering* contains three different parts:

1)`Exploratory Data Analysis (EDA)` to handle outliers and fill the missing value in three ways:

County and other Categorical variables, delete them
microbusiness density and active volume, use the day lag to fill in.
    - population and else, use the mean value to fill in.
2)`geographic factors`: 
    
    neighboring counties may influence each other, and the mean value of the micro-enterprise density of adjacent counties is used to predict the density for a given county.
3)`time factors`: past data can affect current enterprise density, so lagged terms are incorporated.

4.**Model Improvement**:

    - For `XGB` and `LightGBM` model, we flexibly selected the number of important features and predicted data with varying numbers of features. 
    - The `vSMAPE` and `SMAPE` functions were employed to measure the discrepancy between the true values and the fitted values.
