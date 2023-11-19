# CO2 Emission Prediction: A Comparison of Regression Methods

## Project Overview

This project aims to predict CO2 emissions from cars using a dataset provided by the Canadian Government. The dataset includes information such as make, model, fuel type, transmission, and gas consumption. Our goal is to understand how these details relate to CO2 emissions and create a predictive model.

We are passionate about the environment, and through this project, we aspire to contribute to making cars more eco-friendly. Our analysis forms part of a broader effort to reduce pollution caused by vehicles. By studying the dataset, we identify factors influencing CO2 emissions and build a model to predict emissions, ultimately encouraging practices for a cleaner, healthier environment.

## Objective of this Notebook

The primary goal of this notebook is to provide a detailed implementation of regularization for linear regression, comparing their results and efficiencies. The implementation covers the need for regularization, explicit data analysis, and the challenges encountered during the process. Regularization is crucial especially for dealing with overfitting and improving generalization capabilities for models. Moreover, a detailed representation of feature selection included in the notebook.

## Data Preprocessing and Exploratory Data Analysis

The dataset is clean, requiring minimal preprocessing. However, with its current form, it becomes massive after encoding. We carefully handle categorical features, a core part of this dataset and project, to find the best combination for the trade-off between model cost and performance.

Initial exploration reveals that 'fuel consumption per mile' exhibits the highest correlation with the target CO2 emissions. Engine size and cylinder count also show strong correlations. The analysis highlights the presence of multicollinearity, leading to the dropping of certain columns to enhance model performance.

## Handling Categorical Features

Due to the numerous unique values in categorical columns, encoding would expand the dataset to over 2000 columns. Initial attempts with simple and multiple linear regression proved ineffective due to the vast number of features. Although regularization may help decrease complexity, working with 2000+ features is costly. Hence, we regrouped some variables and removed some with feature engineering.

## Regularization Implementation

After reducing the number of features, Linear Regression performs well. However, the notebook implements various regularization techniques, including Ridge (L2) and Lasso (L1) regularization with Cross-validation and hyperparameter tuning to optimize model performance. Lasso regularization, in particular, is chosen for its simplicity and outperforms Ridge regularization and Multiple Linear Regression alone, achieving an impressive 0.99 R2 score and 5.41 RMSE on the test data.

## Feature Selection

Given the extensive feature set, feature importances were examined. Initially our dataset had 12 features, after feature engineering this number dropped to 6 features. However, does our model really need 6 features as input? we performed our datapreprocessing and model runs with a subset of features with different numbers from 1 to 6 to find the balance in a trade-off between model-complexity and model-performance. Altough, as the number of features included in the model increase the performance increase but with only marginal improvements. We observed that apart from 6, 2 features were enough to explain the co2 emission values. Our scores of R2 has only dropped from 0.993 to 0.992 and RMSE incresed from 4.58 to 5.08. By the end 'Fuel Consumption Comb (L/100 km)' and 'Fuel Type' found to be enough for explaining CO2 Emissions with a R2 value of 0.992

## Conclusion

This notebook delves into the intricate details of implementing and comparing various linear regression methods and regularization techniques for CO2 emission prediction. From explicit data analysis to the successful application of regularization and feature selection, each step is thoroughly explored to provide a comprehensive understanding of the process.

## Contact

For further discussion or inquiries, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/fatih-calik-469961237/)
