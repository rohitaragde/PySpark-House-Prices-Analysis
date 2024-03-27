# PySpark House Prices Analysis

## Objectives
- Develop accurate predictive models for estimating residential property sale prices.
- Aid homeowners, buyers, and real estate professionals in decision-making by providing accurate price estimates.
- Identify and quantify the impact of property features on sale prices, empowering homeowners and guiding prospective buyers.
- Reveal market trends through the examination of historical data, providing insights for real estate investors and policymakers.
- Explore various regression techniques, from traditional linear regression to advanced algorithms, to support data scientists in selecting the most effective modeling approaches.
- Delve into feature engineering to optimize model accuracy, benefiting data scientists and analysts.

## Overview
This study delves into the intricate dynamics of residential property prices using Kaggle’s House Prices dataset, sourced from Ames, Iowa. With 79 distinct variables capturing various facets of homes, we embark on a journey to uncover the hidden patterns and influential factors behind sale prices. Our objective is to employ advanced regression techniques to develop accurate predictive models, shedding light on the complexities of the real estate market.

## Introduction
Our exploration of predictive analytics using Kaggle’s House Prices dataset takes us into the realm of residential properties in Ames, Iowa. This dataset offers a rich tapestry of variables, delving into every conceivable aspect of these homes. Unlike conventional assumptions that prioritize factors like room count or garden size in determining property value, this dataset reveals a nuanced interplay of features influencing sale prices.

We selected this dataset for its potential in feature engineering and its demand for advanced regression techniques, focusing on SalePrice as the target variable. Contrasting with more traditional datasets like the Boston Housing dataset, this presents a contemporary and intricate alternative, aligning perfectly with our pursuit of cutting-edge analysis.

Through this project, our objective is to unravel the intricacies of residential property prices, crafting accurate predictive models, and delivering actionable insights for stakeholders in the real estate market.

## Dataset
The dataset used in this study can be found on [House Prices Dataset](https://www.kaggle.com/competitions/house-prices-advanced-regression-techniques/data?select=train.csv)

## Methodology
- Data Source: Kaggle’s House Prices dataset
- Tools: PySpark, Pandas (for visualization purposes)
- Techniques: Advanced regression techniques, feature engineering, exploratory data analysis (EDA)

## Model Implementation
In our analysis, we implement the following machine learning models:

### Linear Regression
In order to find the best model to predict housing prices, we will start by trying a Linear Regression model . Linear Regression is known for its simplicity and interpretability which makes it a good starting point for regression problems like ours. Our dataset, which has key features like OverallQual, GrLivArea, GarageCars, and several others, in order to predict a single value is an ideal scenario to use this model. We aim to explore the relationship between these features and the house prices, hypothesizing from our EDA that factors like the overall quality of the house, living area, and garage capacity are significant predictors of price. Our goal here is to establish a baseline performance that the later, more complex models can be compared against. Our evaluation will not only involve assessing the model's accuracy but also involve a residual analysis to ensure the reliability and robustness of our predictions.

![Residual Plot](/images/residual_plot.png)

This plot shows the difference between predicted and real values. A perfect model would have a line of residuals across a horizontal line at 0, meaning that the predicted is the same as the real value at all areas. However, we can see from this plt that as the actual value increases, the residuals also increase. This suggests that the Linear Regression model may be underestimating the housing prices for higher-valued houses. while the Linear Regression model provides a useful baseline, the residual plot reveals that there are improvements to be made to better capture the nuances of the dataset and improve prediction accuracy, particularly for houses at the higher end of the price spectrum.

### Decision Tree
- Description: Decision trees are a non-linear model that uses a tree-like structure to make predictions. Each internal node represents a "decision" based on a feature, and each leaf node represents the outcome.
- Implementation: We utilize PySpark's DecisionTreeRegressor to train a decision tree model on the House Prices dataset.

### Random Forest
- Description: Random forests are an ensemble learning method that combines multiple decision trees to improve predictive performance and reduce overfitting.
- Implementation: Using PySpark's RandomForestRegressor, we train a random forest model on the House Prices dataset.


## Key Insights
- The dataset comprises 79 distinct variables capturing various facets of homes in Ames, Iowa.
- Advanced regression techniques were employed to develop accurate predictive models for estimating residential property sale prices.
- Market trends and influential factors behind sale prices were identified through comprehensive exploratory analysis and feature engineering.

## Future Work
- Further exploration of advanced regression techniques and feature engineering methods to enhance model accuracy.
- Integration of additional datasets to capture more comprehensive insights into residential property prices.

