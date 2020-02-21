## Problem Statement

C&C Siding is a house flipping business, and they hired me as a data scientist to determine what adds the most value to a residential property. They wish to use their resources in the most efficient way to resell the house they purchase at a greater value.

## Executive Summary
### Data Cleaning
I began by cleaning the data. There were a ton of missing values, so I had to deal with those first. Columns with more than 15% of their values missing I dropped because there isn't enough information to build an accurate model. I found that some null values likely represented the 'None' category for garage and basement, so I imputed these values with the string, 'none.' The remaining missing values I imputed with the mean or median. I corrected data types that were incorrect. I also dropped properties that were not residential because the company that hired me only flips residential properties. Finally, I located an two rows that were outliers in three different columns. I decided it was best to drop these because of their negative effect on the performance of the model.
### EDA
Next, I did some exploratory data analysis. I looked at the distribution of sale price and found that it was right skewed. This makes sense because there are few houses that are way more expensive than average. Most importantly, I observed trends between features within in the company's control and property sale price. This allowed me to determine the best recommendations to make.
### Feature Selection
To build a model that predicts the sale price, I first created dummy variables for all of my categorical features. I then looked at the correlation between those features and chose the most correlated features to be my candidate features. I fed these through a test model, and then ran a function that determines the optimal number of features and the best combination of that many features. I used these features for my production model. I also used ridge and lasso regularization to help with high variance. 
### Limitations
I did not have time to build a model with the features I selected to make recommendations on. I would like to build a linear model to determine how much a unit increase of one of the features would have on the sale price. This way I can compare this added value to the cost of creating that added value. 

## Conclusions
I was able to discover five features that added a lot of value to a residential property. 
- Overall Quality
- Exterior Type
- Size
- Bedrooms
- Driveway Type

*This project was completed through General Assembly's Data Science Immersive Program*