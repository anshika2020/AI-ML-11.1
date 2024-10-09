# AI-ML-11.1
This is the capstone Project 11.1

Step #1: Business Understanding This research assignment uses a vehicle dataset and analyses the data using different model. I followed the CRISP-DM methodology for the data analysis.

Step #2 - 3: Data Understanding and preparation I used the following steps to understand the vehicles dataset:

Executed Dataframe.info() to get the list of columns, number of rows etc
Removed null values from the dataframe.
Used different barplots and countplots to review the data.
The plot result showed that the data was not evenly distributed across different values of the columns. So, I decided to filter the data for further analysis: list_of_manufacturers = ["ford","chevrolet"] list_of_condition = ["excellent","good","like new"] list_of_fuel = ["gas"] list_of_title = ["clean"] list_of_type = ["SUV","sedan","truck"] list_of_size = ["full-size","mid-size","compact"] list_of_paint = ["red","blue","black","grey","silver","white"] list_of_cylinders = ["4 cylinders","6 cylinders","8 cylinders"]
Removed price outliers using quantile method.
Executed Dataframe.corr() to determine the correlation of price and various
attributes and found posivite and negative correlation of various attributes to price.
Split the dataset into training and test datasets.
Step #4: Modeling In this step, I created several models using:

Linear Regression
Ridge Regression
Ridge Regression with optimal alpha (using GridSeachCV)
Sequential Feature Selection
Lasso Regression
Step #5: Evaluation Evaluated all the models using the mean squared error for training and test datasets. Best features found using Sequential Feature Selectors are - condition_excellent
condition_like new
drive_4wd
size_compact size_full-size
type_SUV
type_truck
paint_color_red

The Lasso model was found to have the least training MSE. But the training MSE was higher.

After evaluating the training and test MSEs of all the models, I concluded that the model generated using sequential feature selection is the best as the difference between the training and test MSEs is on the lower side compared to that of the other models.

Step #5: Deploy the Readme and jupyter notebook to GIT Hub.


