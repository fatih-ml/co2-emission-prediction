# CO2 Emission Prediction: A Comparison of Regression Methods

## Project Overview

This project aims to predict CO2 emissions from cars using a dataset provided by the Canadian Government. The dataset includes information such as make, model, fuel type, transmission, and gas consumption. Our goal is to understand how these details relate to CO2 emissions and create a predictive model.

We are passionate about the environment, and through this project, we aspire to contribute to making cars more eco-friendly. Our analysis forms part of a broader effort to reduce pollution caused by vehicles. By studying the dataset, we identify factors influencing CO2 emissions and build a model to predict emissions, ultimately encouraging practices for a cleaner, healthier environment.

## Objective of this Notebook

The primary objective of this Jupyter notebook is to provide a detailed implementation of regularization for linear regression, comparing their results and efficiencies. The notebook covers the need for regularization, explicit data analysis, and the challenges encountered during the process. Regularization plays a crucial role, especially in dealing with overfitting and improving the generalization capabilities of models.

## Data Preprocessing and Exploratory Data Analysis

The dataset is clean, requiring minimal preprocessing. However, with its current form, it becomes massive after encoding. We carefully handle categorical features, a core part of this dataset and project, to find the best combination for the trade-off between model cost and performance.

Initial exploration reveals that 'fuel consumption per mile' exhibits the highest correlation with the target CO2 emissions. Engine size and cylinder count also show strong correlations. The analysis highlights the presence of multicollinearity, leading to the dropping of certain columns to enhance model performance.

## Handling Categorical Features

Due to the numerous unique values in categorical columns, encoding would expand the dataset to over 2000 columns. Initial attempts with simple and multiple linear regression proved ineffective due to the vast number of features. Although regularization may help decrease complexity, working with 2000+ features is costly. Hence, we regrouped some variables and removed some with feature engineering.

## Regularization Implementation

After reducing the number of features, Linear Regression performs well. However, the notebook implements various regularization techniques, including Ridge (L2) and Lasso (L1) regularization with Cross-validation and hyperparameter tuning to optimize model performance. Lasso regularization, in particular, is chosen for its simplicity and outperforms Ridge regularization and Multiple Linear Regression alone, achieving an impressive 0.99 R2 score and 5.41 RMSE on the test data.

## Feature Selection

Given the extensive feature set, feature importances were examined. A subset of features with different numbers from 3 to 66 was selected, drastically reducing model complexity. Running Lasso regularization on this reduced feature set yields remarkably similar results after a certain number of features. With an R2 score of 0.99 and 5.53 RMSE, the decision is made to finalize the model using only these 10 selected features. Fuel Consumption values of cars are found to be the most important factor affecting CO2 emissions, followed by fuel types and engine size.

## Conclusion

This notebook delves into the intricate details of implementing and comparing various regression methods for CO2 emission prediction. From explicit data analysis to the successful application of regularization and feature selection, each step is thoroughly explored to provide a comprehensive understanding of the process.

## Contact

For further discussion or inquiries, feel free to connect with me on [LinkedIn](https://www.linkedin.com/in/fatih-calik-469961237/)
