# [Wine-Quality-Prediction](https://ngozinneke.github.io/Wine-Quality-Prediction/)

In this project, the wine quality dataset was used to demostrate how to model red wine quality based on physicochemical tests and also explain the model predictions using different explainability frameworks. 

## Task 1: Red Wine Quality Prediction Using Regression Models.
**Dataset Background:**

The dataset was downloaded from the UCI machine learning repository (https://archive.ics.uci.edu/ml/index.php). The dataset is related to red wine samples from the north of Portugal.The first task is to model the red wine quality using red wine samples based on physicochemical tests. The dataset has 11 independent variables, 1,599 observations and 1 output variable (a scale of 0 - 10).

**Here are the Independent Variables:** 

•	Fixed acidity

•	Volatile Acidity

•	Citric Acid

•	Residual Sugar

•	Chlorides

•	Free Sulfur Dioxide

•	Total Sulfur Dioxide

•	Density

•	PH

•	Sulphates

•	Alcohol.

**Dependent Variable: Quality (scale of 0 - 10)**

**Data Preparation:**

The major steps were to clean the data and prepare the data for analysis. The data went through different steps of data cleaning. Data types and missing values were checked. Features statistical summary were detected to identify outliers and abnormal distributions. Also, correlations analysis was carried out to detect the any correlations that existed in the data. 

**Modelling:**
A minimal exploratory data analysis were carried out on the data because the main aim is to explain the model to the stakeholders. 
Three potential models namely Linear Regression, Random Forest and Gradient Boosting) were used in the modelling part. Then, the models were evaluated using scikit learn metrics such as **Mean Absolute Error, R2 Score, and Root Squared Mean Error.** The best performing model was chosen to be used in the explainability part of the project.

## TASK 2: Explainability of the Model

For stakeholders to trust any black box models decisions, the reasoning of such model decisions needs to be understandable and communicable to the stakeholders. Most of the models are regarded as Black box models because their predictions are opaque. With explainability methods, these black box models’ inner workings can be explained to the stakeholders. Such methods are categorised as Global Methods and Local Methods.

**Global Methods:**

Global methods are explainability tools for explaining model behaviour from the global points of view. SHAP (Shapley Additive exPlanation) and Partial Dependence plot (PDP) are good examples of Global Methods.

**SHAP Feature Importance:**

SHAP Feature Importance is based on the magnitude of feature attribution. From figure 3, the most contributing factors to the prediction of wine quality can be identified clearly. The first five contributing factors are Alcohol, Volatile acidity, Sulphates, Total Sulfur dioxide and PH.

![Wine Quality Feature Importance](https://github.com/Ngozinneke/Wine-Quality-Prediction/blob/main/Picture%201.png)


**SHAP SUMMARY PLOT:**

Summary plot combines both the feature importance (fig 3) with feature effects. With the summary plot (fig 5) the features values will be on y-axis and impact on the prediction is x-axis. Blue colour decreases the prediction quality wine while red colour increases the model prediction.

![Wine Quality Summary plot](https://github.com/Ngozinneke/Wine-Quality-Prediction/blob/main/Picture%202.png)

**Partial Dependence Plot (PDP):**

With PDP plots, the relationship of the feature with prediction could be determined.The relationship could be linear, monotonic or complex.

![Wine Quality Alcohol PDP PLOT](https://github.com/Ngozinneke/Wine-Quality-Prediction/blob/main/Picture%203.png)

**Partial Dependence Plot Features Interactions Plot:**

![Wine Quality Features Interactions Plot](https://github.com/Ngozinneke/Wine-Quality-Prediction/blob/main/Picture%204.png)

**Local Methods:**

Local methods are explainability methods for explaining single observation prediction. In that regards, SHAP force plot will be used to explain the probability of an instance from the dataset been predicted as a good wine or not.

![Wine Quality Single Feature Prediction](https://github.com/Ngozinneke/Wine-Quality-Prediction/blob/main/Picture%205.png)

![](https://github.com/Ngozinneke/Wine-Quality-Prediction/blob/main/Picture%206.png)

## TASK 3: Build a Web App using Dashboard Explainer

I develop a dashboard using a python package called Explainer Dashboard. According to the author Oege Dijk, the dashboard would help the non-developers to understand the predictive models without the help of data scientist. 
The dashboard consists of:

•	Features importance

•	Model performance

•	Feature contributions to individual predictions

•	Partial Dependence plots

•	SHAP(Interaction) values

•	Visualization of individual decision trees

View the Dashboard using the Link (https://mkqgk565ei-496ff2e9c6d22116-8050-colab.googleusercontent.com/)

