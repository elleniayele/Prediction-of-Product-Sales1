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
rmse, mae and r2 score for linear regression model for testing data are:

                                                                        - r2:0.5673120131342877,

                                                                        - MAE:803.3697084936649,
                                                                        
                                                                        - RMSE:1092.6007177689773
              
the data is well balanced for training and testing data and the regression tree model is not balanced, it is overfit. so i choose linear regression model.
   # linear regression                                                                     
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/blob/main/download%20(1).png)

 outlet_identifier_out027:
outlet_identifier_out027 is the most impactful feature in which increased the predicted sale by 968.517 dollars.

outlet_type_supermarket type 3 :
the outlet type supermarket type 3 increased the predicted sale by 968.517 dollars.

outlet_type_supermarket type 3 :
the outlet_type_supermarket type 3 increased the predicted sale by 931.342 dollars. 
# random forest regression 
the top five important features are 
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/blob/main/importances.png)

### a summary plot (bar version)
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/assets/61632568/f73e0f95-579d-41f5-bb98-2c8d84c27b40)

in the shap bar plot , item_mrp is the top important feature just as plot of important features so is outlet_type_supermarket type1 but in shap plots the most important 3rd feature is outlet_type_3 but in the plot of original feature importances figure the third important is item_weight and then the next important is out_let identifier_out027 where as in the feature important role, it is the last important feature from the 5 most important feature.outlet_type_supermarket type1 ,outlet_type_3  and outlet_identifier_OUT027 show that the higher their values the higher the model is going to predict the sales so they are most important features for predicting sales in shap where as in feature importances plot item_mrp, outlet type supermarket type 1, item weight and the others follow.

### create a summary plot (dot version)
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/assets/61632568/b21f76c6-df59-478d-892f-77336f98799c)
# Interpreting the SHAP values for our model:
 
  #### ITEM_MRP
    
  since positive values are on the right, we can see that the greater the number of ITEM_MRP , the more likely the model would predict the sales .we see that at the left, the blue values, for the lower  values of ITEM_MRP, the less likely the model will predict the sales that is towards the left.The lowest the values of the ITEM_MRP the less chance it will pridicting  the sales.so the higher values of the item_mrp the more likely it's going to pridict the sales.

 #### outlet_type_supermartket_type1
 
 since the red value is on the right, the more the values of outlet_type_supermarket_type1, the more likely it is going to predict the sales

 #### outlet_type_supermartket_type3

In here also, the more the values of the ourtlet_type_supermarket_type3, the more chances of predicting the sales.( direct relation)
# EXPLAINING LIME AND FORCE PLOTS
i chose item_mrp, and item_weight since item_mrpin here, we can see that item_wight has a value of 3069.86 dollars in predition of sales at this example. 
all the other columns except for outlet type supermarket type 1 and item_mrp of value 147.41 which have postively influecnced towards maximum item_weight.and hence sales.
the outlet_type wis postive with value greater than 0 while item_mrp greater than 141.88. has higher contributions to the prediction of sales when we ploted the importance of features also wanted to see how item_weight has contributed to the prediction of sales.
# A Lime tabular explanation
## ITEM_MRP
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/commit/0de557f46db30ff5fd8a7ddc37f28d7221058218)

As we can see above, this item type has a predicted value of sales which is 5158 dollars of predicted value.
This item_mrp has negative impacts from features in predicting sales such as outlet_type supermarket(uknown), item_type breads, item_type_fruits, and item_type_others while features that helped it or has postive influences are item_MRP which is greater than 188.22 and outlet type _supermarket type 1 which is greater than 0 also item type seafood has postively contributed to the prediction of sales.

## ITEM_WEIGHT
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/commit/0de557f46db30ff5fd8a7ddc37f28d7221058218)

in here, we can see that item_wight has a value of 3069.86 dollars in predition of sales at this example. 
all the other columns except for outlet type supermarket type 1 and item_mrp of value 147.41 which have postively influecnced towards maximum item_weight.and hence sales.
the outlet_type wis postive with value greater than 0 while item_mrp greater than 141.88.

# A sharp force plot
## ITEM_MRP
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/commit/767d6e4750fa8721f8e06640c57465e888e83a3c)

as can be seen in the force plot, the features that helped greatly for the prediction of sales are ITEM_MRP which has 265.2 value, item_weight with values of 10 and outlet_type_supermarket type 1, the other features have lower values so not very important for the prediction of sales.

## ITEM_WEIGHT
![image](https://github.com/elleniayele/Prediction-of-Product-Sales1/commit/767d6e4750fa8721f8e06640c57465e888e83a3c)

outlet_type_supermarket type1 has the greater contribution to prediction of the sales,item_mrp has the second with values of 147.4 and item_weight which has values of 21.25  and item_type_household=1, the other features were not important for predicion of sales.
