# Project 2 - Ames Housing Data and Kaggle Challenge

### Problem Statement
- Predicting the price of house at sale in Ames, Iowa
- Which features affect the valuation of houses in Ames, Iowa 

### Executive Summary


### Exploration and Modeling of the Ames, Iowa Housing Dataset


### Cleaning, EDA, and Feature Engineering
- Combine existing train and test data for cleaning and feature engineering. Consistant cleaning and feature engineering methodology.
- Consult the data dictionary and use domain knowledge to decide values to be filled in null counts
- Most null values were filled with 'NA's or 0, mode for features that had less than 50 null values
- Countplots and histograms were plotted to inspect on distribution of features. Features that were too skewed (E.g. 80% counts were in 'NA') were dropped. This is due to a lack of variation affecting sale prices.
- For a pair of highly correlated features, one of the two was dropped in order not to cause bias weightage.
- For categorical and ordinal features, values were engineered to numbers for modeling purposes
- Dummy for categorical and nominal features

### Modeling
- Seeing as the target variable is continuous, a linear regression model seemed a suiting start in the process. Also I ran tests with the ridge and lasso models, as well as using data that hadn't been run through polynomial transformation. After these tests I've decided the best model is the lasso model using the data that hadn't used the polynomial transformation. Though it did not have the highest r_squared score (.930) on the training data, it was very close to the r_squared score (.926) on the test data. And, more importantly, it had the highest r_squared for the test data and the highest cross validation score (.841). From these scores, we can tell a few things about the model. Firstly, the close pairing of the train/test R_squared scores as well as the robust .841 cross validation score show the model is not overtrained and should fairly fit other housing data in this area. And secondly, the .926 R_squared value on the testing data shows that the model explains 92.6 % of the variance in the data that the baseline model does not.

### Interesting Finds