# House-Prices - Advanced Regression Techniques
#### Northwestern University
##### School of Professional Studies
###### Practical Machine Learning MSDS422
###### Assignment 2: Evaluating Regression Models


### Summary: 

The goal of this project was to build a predictive model that can help predict the house prices in Ames, Iowa. I obtained the data from Kaggle by participating in the ongoing Kaggle competition. I perform EDA, feature engineering, feature selection, modeling, and finally prediction using the provided test dataset. I used multiple algorithms and compared their performances. 

### Analysis: 

I performed a quick exploratory data analysis to see what the data is and what each field represents. During EDA, I noticed that the target variable “SalePrice” was skewed, and the majority of the features had missing values. I fixed the skewness of the target variable by applying a logarithmic transformation. Next, I imputed the missing values using various techniques such as filling with “None”, 0, and the mode of the feature. 
The feature engineering involved encoding the existing variable and creating new features. Since most of the categorical variables were ordinal, I had to encode them manually to avoid labeling. I also used Scikit’s LabelEncoder to encode nominal features. After feature encoding and feature creation, I had 130 features that could cause overfitting. I narrowed down the features to 32 using multiple feature selection algorithms. 
For modeling, I tried Ordinary Least Squares, Lasso Regression, and Ridge Regression models using a grid search algorithm. I used Root Mean Squared Error and Negative Mean Squared Error as my scoring functions. Ridge regression resulted in better performance over the other two algorithms. Next, I wanted to try ElasticNet, Support Vector Regressor, Gradient Boosting Regressor, Lightgbm, and XGboost. The booting algorithms performed better than Ridge and Lasso. For the Kaggle submission, I tried stacking all of the models above and achieved a relatively better RMSE than using one algorithm alone. 

### Conclusion: 

Although the dataset was small, I was able to get better performance with a relatively low RMSE score. I was impressed to see how I could achieve better performance with only 32 features out of 130. For future analysis, I would like to spend some more time tunning the parameters of each model. I also would like to define a range for outliers and run the model with the outliers removed. 
The entire notebook is available on my github here
