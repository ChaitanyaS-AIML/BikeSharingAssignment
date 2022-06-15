# Bike Sharing Assignment
Build a multiple linear regression model for the prediction of demand for shared bikes.

## General Information
A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state. 

I am required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. 

data.csv has been provided that contains 730 rows and 16 variables for analysis. I have taken 80% of the data for training and 20% of the data for testing the model.


## Conclusions

Following were the observations from the categorical variables. 
-The bikes rental seems to grow in 2019, as compared to 2018
-The bike rental seems to be higher in months May till October
-The bike rentals seems to be higher on non-holidays
-Weekday doesnt seem to have much impact on the demand of bikes
-Working day doesnt seem to have much impact on the demand of bikes
-Weather situation seems to impact the demand of bikes, with less demand in category 3 and 4

The final model is as given below:

cnt = 0.3333 + (0.2285 x yr) - (0.0692 x holiday) + (0.0229 x workingday) + (0.5093 x temp) - (0.2582 x hum) - (0.2490 x windspeed) + (0.0722 x "2") - (0.0135 x "1") - (0.0076 x "2") - (0.0294 x "2") - (0.0505 x "2") + (0.0300 x "8") + (0.1171 x "9") + (0.1308 x "10")

The model has a R Squared score of 0.772 on the test data, which means that 77.2% of the variation can be explained by this linear regression model.

Based on this model, the top 3 features contributing significantly towards explaining the demand of shared bikes are temperature, humidity and year.


## Technologies Used
- numpy 
- pandas
- matplotlib.pyplot
- seaborn
- sklearn
- statsmodels