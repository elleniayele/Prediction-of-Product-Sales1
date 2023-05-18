# Prediction-of-Product-Sales1

Author: Elleni Ayele
# Project Desciption

# Overview

The data scientists at BigMart have collected 2013 sales data for 1559 products across 10 stores in different cities. Also, certain attributes of each product and store have been defined. The aim is to build a model and predict the sales of each product at a particular outlet.

The goal of this is to help the retailer understand the properties of products and outlets that play crucial roles in predicting sales.

There are 8523 rows, and 12 columns. The rows represent 8523 observations, and the columns represent 11 features and 1 target variable.
# outlets
# Total outlet by sales
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/assets/61632568/5ba7fd5d-77fe-4b71-b84e-41f8409910e5)

Outlet OUT027 significantly outperformed the other outlets with 3,453,926.05 dollars of total sales.

Outlets OUT010 and OUT019 significantly underperformed the other outlets, having only 188,340.17 dollars and 179,694.09 dollars in total sales respectively.

# Outlet Types

Supermarket Type1 outlets may have contributed the most to Total Company Sales, however they do not have the highest Average Outlet Sales.

Supermarket Type3 has only only one outlet, and it has the highest Outlet Sales , and they have the least Outlet Sales.

![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/assets/61632568/eea9ea58-f9ad-47e2-ada2-56f51f3ea30a)
# Outlet Size
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/assets/61632568/685d5f66-26dd-4d4f-b9a3-c0461fba2c48)
Outlet Size does have some correlation with the Outlet Type's Average Outlet Sales. 
Medium Size outlets contributed the most, and Small and Unknown Sized Outlets contributed the least to Total Company Sales.

Though High Size outlets contributed a lessor amount than either Small or Unknown Size to Total Company Sales, their Average Outlet Sales were higher.
# Outlet Location Types
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/assets/61632568/a1aaaab3-38ce-4112-9566-79a42693181c)
Tier 3 Outlet Location Types contributed the most to Total Company Sales.
Though Tier 2 Outlet Location Types contributed a lessor amount than either Tier 3 to Total Company Sales, their Average Outlet Sales were higher.
# Items
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/assets/61632568/d2449a70-0d8e-4cb6-ba76-3bb33e595de1)

 It is of interest to note
 that the Seafood Item has the highest Item Sales.
# Model Performance based on linear regression model

here are the scores for this model

# Coefficient of Determination (r2)
The Coefficient of Determination is the proportion (%) of the variation in the dependent variable, or target variable, that a model is able to predict, or explain, from the independent variables, or features. It is a measure of the goodness of fit of a regression model.  calculates how much better our model's predictions are vs if the mean was used instead. It should have a value between 0 and 1, however a poor model may have a negative.
Advantages:
It uses a consistent scale, which is used for all datasets, and thus may be used for comparison.
Disadvantages:
It is difficult to interpret and very difficult to explain to non-technical audiences.
based on our data 

model training r2:0.5614117741571462

model testing r2:0.5673120131342877

# mean sqare error

To calculate the MSE, you take the difference between your model's predictions and the ground truth, square it, and average it out across the whole dataset.

model training MSE:1297982.4269088164

model testing MSE:1193776.3284692846

# evaluate the performance based on rmse
Root mean square error or root mean square deviation is one of the most commonly used measures for evaluating the quality of predictions. It shows how far predictions fall from measured true values using Euclidean distance. it is the square root of MSE.

model training RMSE:1139.2903172189328

model testing RMSE:1092.6007177689773

# evaluate the performance based on mae(mean absolute error)
Mean Absolute Error calculates the average difference between the calculated values and actual values.
model training MAE:847.2653346057572
model testing MAE:803.3697084936649

# using Regression tree model to predict sales

here are the scores  for the model

# Compare the performance of your model based on r^2

model training r2:0.999942098755146

model testing r2:0.13974891304556325

# Compare the performance of your model based on mse

model training MSE:171.35616938263135

model testing MSE:2373413.2107182783

# Compare the performance of your model based on rmse

model training RMSE:13.090308223362479

model testing RMSE:1540.5885922978523

# Compare the performance of your model based on mae

model training MAE:0.2315509073842304

model testing MAE:1052.2769041295167


In here we can say that the data is overfit. comparing the linear regression model with regression tree model, linear regression model did better. The 
rmse, mae and r2 score for linear regression model for testing data are:- r2:0.5673120131342877,

                                                                        - MAE:803.3697084936649,
                                                                        
                                                                        - RMSE:1092.6007177689773
              
the data is well balanced for training and testing data and the regression tree model is not balanced, it is overfit. so i choose linear regression model.
                                                                        





