# Data Science House Prediction: Project Overview
This data science project series walks through step by step process of how to build a real estate price prediction website. We will first build a model using sklearn and linear regression using banglore home prices dataset from kaggle.com. Second step would be to write a python flask server that uses the saved model to serve http requests. Third component is the website built in html, css and javascript that allows user to enter home square ft area, bedrooms etc and it will call python flask server to retrieve the predicted price. During model building we will cover almost all data science concepts such as data load and cleaning, outlier detection and removal, feature engineering, dimensionality reduction, gridsearchcv for hyperparameter tunning, k fold cross validation etc. Technology and tools wise this project covers,

1.Python

2.Numpy and Pandas for data cleaning

3.Matplotlib for data visualization

4.Sklearn for model building

5.Jupyter notebook, visual studio code and pycharm as IDE

6.Python flask for http server

7.HTML/CSS/Javascript for UI

# Data Cleaning

- Numerical imputation of missing values

- Made columns for price per sqft.

- Created dummy variable for location columns.

- Remove outliers, negative values, Suspecious value from columns.

- Transformed founded date into age of company

# Model Building

First, I transformed the categorical variables into dummy variables. I also split the data into train and tests sets with a test size of 20%.
I tried three different models and evaluated them using Mean Absolute Error. I chose MAE because it is relatively easy to interpret and outliers aren’t particularly bad in for this type of model.

I tried three different models:

-  Multiple Linear Regression – Baseline for the model.

-  Lasso Regression – Because of the sparse data from the many categorical variables, I thought a normalized regression like lasso would be effective.

-  Random Forest – Again, with the sparsity associated with the data, I thought that this would be a good fit.

# Model Performance

The Random Forest model far outperformed the other approaches on the test and validation sets.

Random Forest : MAE = 11.22

Linear Regression: MAE = 18.86

Ridge Regression: MAE = 19.67

# Productionization

In this step, I built a flask API endpoint that was hosted on a aws webserver by following along with the TDS tutorial in the reference section above. The API endpoint takes in a request with a list of values from a location,sqft,bath,bhk and give price predicted.

