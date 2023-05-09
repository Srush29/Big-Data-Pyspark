# Big-Data-Pyspark

# Used Car Listings Price Prediction

## Overview of the project

We know that the prices of brand-new cars are increasing day by day. This has led to an increase in the number of customers who prefer buying used cars. We aim to examine the used car pricing data, gain insights, and predict the prices of the used cars. Using these insights, people who need to sell their car can decide an estimated price. Similarly, anyone who would be interested in purchasing the car will be able to determine the appropriate price beforehand.

## Description of dataset

The attributes in dataset are either integer or string. Dimensions: 852,122 rows * 8 columns
<img width="1078" alt="image" src="https://github.com/Srush29/Big-Data-Pyspark/assets/54467767/7b4b3e15-65b2-4a0f-8b2f-a4784c0a935d">

## Predictors
We are using the following columns as our predictor columns:

<img width="1033" alt="image" src="https://github.com/Srush29/Big-Data-Pyspark/assets/54467767/50a3083b-977f-41b7-8461-730ed127b8f0">

## Interesting insights

<img width="564" alt="image" src="https://github.com/Srush29/Big-Data-Pyspark/assets/54467767/143f46d2-93e1-4df4-b70e-8c52623c3712">


According to the summary statistics for Price and Mileage, the standard deviation values are extremely large and the maximum and minimum values are far apart
It is surprising that some cars having extremely low mileage have been put up for sale

<img width="635" alt="image" src="https://github.com/Srush29/Big-Data-Pyspark/assets/54467767/deda07a0-7391-4978-92b5-fde4edd5d14e">

![Uploading image.png…]()

•	The density plot shown above for car prices is right skewed
•	The Kurtosis value is around 87 which is high
•	This suggests that there are many outliers in the data which need to be removed
•	If we see the states, Wyoming and Texas have the highest average price of used cars. On the other hand, lowest prices of used cars can be seen in the state of Ohio and Hawaii

## Inferences
We have used a user defined function to check which are the best columns and in what order should the variables be added to the regression equation to generate the least MSE. Using that, the features that impact the price prediction of used cars are:
•	Year
•	Make

## Challenges
The following were the challenges faced:
•	The data had a lot of outliers, and even after cleaning, there were still a lot of them. As a result, the prediction model did not perform as predicted, leading to poor scores.
•	About 2500 unique values were included in the City and Model column (high cardinality), which affected the performance of Random Forrest and GBT since a large number for the "Max Bins" parameter was required. They had to be taken out of the prediction model as a result.
•	There were far more rows in the data than there were columns. The effectiveness of the model was also impacted as a result.

## Conclusion Summary
None of the models performed as predicted, with fairly large Mean squared errors and low R squared values, due to the data's high degree of skewness and small number of columns. In comparison to linear regression and random forest regression models, the GBT regression model generated the best results for us. More variables would be needed if we want better results.




