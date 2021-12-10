## Problem Statement

As real estate analysts in Iowa, we are responsible for managing our organization's real estate holdings.
We are tasked with understanding real estate market trends and to minimize current and future real estate holding risks.
We will be conducting data analysis on the Iowa real estate market and determine which are the factors that affects property prices.
The purpose of this analysis is to better understand  property prices and provide suitable insights to management and potential buyers of the organization's real estate.

## Datasets used
AMES Housing Dataset

## Summary of Analysis
The dataset consists of 81 variables about a house. There are not much missing values to impute except for Lot Frontage which occurs mainly in low density residental areas thus 0 is imputed. The biggest challenge of this dataset is there are too many variables which are correlated to each other. Dumbifying the categorical variables increase the dataset even more. A pairplot with the target variable is created after dumbifying to remove variables that are skewed. Many of these occur in cases where only a few houses have that amenality but not the rest. Robust Scalar was used to scale the data as it creates values between 0 and 1 and gives stable cross validation scores. Ridge regression was the model that produces the best results as it is able to penalise the multi-collinear features.

## Conclusion
Both Robust Scalar and Ridge Regression can address the issues of multi-collinear features. The features coefficients that are on the top list of the Ridge Regression is neighbourhood, floor area and exterior. The top variables found in Lasso are zoning, condition and house style. This shows the factor affecting the price of the house are location, size, exterior looks, style and condition. The location remains to be the single most important feature. The top neighbourhood is StoneBr follow by NoRidge. NAmes is the worse neighbourhood to be in.

## Recommendations
For buyers, I will recommend buying a house in StoneBr or NoRidge as they fetch high value. For sellers, I will recommend furnish and upkeep your house so that the condition remains mint. My current model is well customised to Ames as location is the carries the highest coefficient. Location plays such a huge factor because it gives accessibilty to alot of amenalities nearby. Other factors such as exterior and condition i applicable to other towns as well.