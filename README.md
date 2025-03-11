# UC_Berkeley_Module11_CRISP-DM_UsedCarPrices
 INTRODUCTION
 Module 11 introduces CRISP-DM as framework for a data mining data science capstone project. This assignment requires exploring an external dataset, which contains information on 426K cars. The goal is to understand what factors make a car more or less expensive, using several machine learning models and techniques, such as multiple regression. The results will be delivered to the primary clientele, whom are used car dealers. The deliverable is a basic report with details of primary findings and recommendations for what consumers value in a used car. 

BACKGROUND
Team Kelly is the name of my data science consulting firm and our clients are used vehicle car dealers. Our team is provided data on about half a million used cars and we are tasked with identifying key factors that may be considered for influencing higher sale prices for used cars.

BUSINESS OBJECTIVE
Team Kelly will approach this problem with data science techniques, using machine learning tools to understand which features, or combination of features, may provide the most value for a used car. As a result, our team will derive and provide recommendations to our clients about which features are most work considering when setting prices of used cars. 

BUSINESS SUCCESS CRITERIA
Success criteria will be determined by successful end-to-end repeatable CRISP-DM implementations and delivery of recommended features to clients.

INVENTORY OF RESOURCES
Resources available is myself as the data scientist and my experience with machine learning. 

REQUIREMENTS
The primary requirements would be to approach the problem with machine learning tools learned in UC Berkeley's ML/AI course. 

ASSUMPTIONS
Team Kelly will use 70% data availability as a threshold for selecting initial features. In other words, any feature that is incomplete and missing more than 30% of values for that feature in the dataset, will be omitted from this evaluation. 

CONSTRAINTS
The machine learning models will be limited to linear regression and data science techniques covered in Module 7 through 11. Another constraint, certain features seem promising at first glance, however due to incompleteness of data values available, those features are excluded from being evaluated to avoid bias.

RISKS AND CONTINGENCIES
The biggest risk factor is unknown delays in completion of project and delivery of features to client. Team Kelly is a high-performing team, however time-constraint is very high due to competing priorities, such as an existing very full work schedule and high schedule demands from family. Contingency plan is to provide a minimum of one feature to be recommended to client.

TERMINOLOGY
The business proposal will be presented in the CRISP-DM format. CRISP-DM is a framework that organizes data mining activities into 6 phases; business understanding, data understanding, modeling, evaluation, and deployment; with repeatable cycles between phases. Other terminology may include functions and libraries from the Python programming language, used to perform primary data processing.

COSTS AND BENEFITS
Other than labor cost and time, including opportunity cost, there is no added costs for completing this proposal. The benefits will be realized by Team Kelly at the conclusion of this assignment by gaining additional practice with CRISP-DM framework. On the other hand, our clients will benefit from the recommendations provided in the proposal and achieve higher profits with successful implementation. With continued success, we hope the client would return for additional data science consultation services from Team Kelly. 

DATA MINING GOALS
Data mining goals are to use model and feature selection techniques, such as sequential features selection and regularization to withe the right mix of features and fit and train different models with the least amount of bias, overfitting, and errors.

DATA MINING SUCCESS CRITERIA
Result with a model or two that provides the lowest prediction error when testing model on unseen test data, while achieving low bias/low variance or low bias/high variance.


PROJECT PLAN

The project will be broken down into 3 phases. 
Phase 1 will consist of: Data Exploration, Preprocessing, and Feature Engineering. 
This includes: 
-Loading and analyzing dataset, pre-selecting features that meet certain criteria, such as complete or availability of data, numerical values.
-Handling missing values, outliers, and encoding non-numeric features; 
-Creating new features if necessary, or transform existing ones for better predictive power.
Phase 2 will consist of: Model Selection and Evaluation.
This includes:
-Using Scikit learn libraries in Python to build pipelines to fit and build models with different combinations of features to generate predictions and obtain coefficients. 
-Evaluating models by calculating prediction errors and comparing them, plot the thetas, plot the models, fix high bias by adding more polynomial input features, fix high variance by limiting features to the more important ones, plot the models and go through the process of elimination to result in the best model with features.
Phase 3 will consist of Interpretation of Results and Develop Recommendations to Clients.
This includes: 
-Understanding the impact of different features on car prices.
-Providing actionable insights based on the feature importance and model interpretations.

INITIAL ASSESSMENT OF TOOLS AND TECHNIQUES
The following techniques will be in scope for this project: 
Multiple Linear Regression (7.3)
Dummies for non-numerical categorical features (7.4)
Non-numeric Features (7.10)
Nonlinear Features (8.1)
Pipeline (8.5)
Sequential Feature Selection (9.1, 9.3)
Scaling and StandardScaler (9.6)
Ridge Regression (9.2, 9.7)
GridSearchCV and model_finder.best_estimator (9.7)
LASSO Regression (9.8)
Cross validation (9.9)

RESULTS
Linear Regression: RMSE: 2.7504894078042303
Random Forest Regressor: RMSE: 1.937606412659097
XGBoost: RMSE: 2.523089106149895

Top features influencing car price from Linear Regression model: Feature Importance 
year 0.062918 
title_status 0.042364

Top features influencing car price from Random Forest model: Feature Importance 
odometer 0.702458 
manufacturer 0.125271

Top features influencing car price from XGBoost model: Feature Importance 
type 0.292679
odometer 0.264273

EVALUATION METHODOLOGY
Using the ranked results of each model, each of the features suggested by each model were graded with a point and multiplied by the proportionate weight given to each ranked model, where the features were derived. 
From each model, the top 2 features were chosen. The 1st suggested feature is assigned a weight 0.6 out of 1.0, the 2nd suggested feature was assigned a weight of 0.4 out of 1.0. As a result, for each feature, the total sum of the weight of ranked model plus weight of ranked feature results in the model performance score assigned to each feature.

When all the scores were added up for each feature, the top scoring features were:
odometer, with 43%/100
manufacturer, with 20%/100
type, with 20%/100

The percentage can be understood as the feature's confidence level or the percentage version of the model performance score, which is a metric that represents how effective that feature performed amongst the different models used. Odometer was suggested by 2 models so it received a higher score than the others. 


RECOMMENDATIONS FOR USED CAR DEALERSHIPS
Based on Team Kelly's robust machine learning model approach, we derived the following actionable insights:

The models suggested placing the most emphasis on mileage (odometer), then manufacturer, and type as the features that would most likely influence higher pricing for used cars. 

Top understand the difference in level of confidence for each feature compared to other features, below are the percentages calculated for each feature: 
43% odometer
20% manufacturer
20% type

In other words, the models predicted a 43% level of confidence that the odometer value, representing vehicle mileage, can be utilized to set higher vehicle prices. For example, analyzing at the relationship between odometer value and price, client may utilize lower prices to set higher prices. 

Next, the models predicted a 20% level of confidence for utilizing the manufacturer feature and equally for the type feature, can be used to set higher prices. For example, analyzing the relationship between manufacturer and price, certain manufactures, like Mercedes, may indicate the ability to set higher prices for those used cars by the same manufacturer. Similarly with the same confidence level, analyzing the relationship between type and price, certain types of vehicles, like SUVs, may yield higher sale prices.

These 3 features outperformed the rest of the features in the dataset because the models predicted less than 10% level of confidence for the rest of the features tested.