# Sales Forecasting
Sales Forecasting (Python)
# Sales Forecasting Project(Python)

The purpose of this project is to forecast weekly sales for each department in 45 stores & also to carry out statistical analysis to help improve financial planning of the national retail store. A forecast is based on historical sales data and is done for a particular period of a time in the near future, usually the next calendar year. A sales forecast enables a company to make informed business decisions regarding inventory or cash flow or plan for growth.


# Methodology

 - Data Wrangling - `Analyzed outliers.`
 - Exploratory Data Analysis - `Analyzed the data and summarized the main characteristics & trends.`
 - Data Visualization - `Used boxplot, distribution plot, scatter plot, lineplot & barplot to visualize the data and it's characteristics.`
 - Machine Learning Algorithms Used - `Linear Regression, Polynomial Transformation, Ridge Regression and Random Forest`
 - Evaluation Metrics Used - `Mean Absolute Error(MAE) and R-squared`


# Technologies/Libraries Used
``` javascript
 - Python 3
 - Jupyter
 - Pandas
 - Numpy
 - Seaborn
 - Matplotlib
 - Scikit-Learn
 - Scipy
 ```

# Datasets available

The data for this model is relatively simplified as it has very few missing areas. The raw data consists of a training dataset with the features listed above and their corresponding weekly_sales. Twenty percent of this training dataset was split into a test dataset with corresponding weekly_sales so accuracy and error of the model could be determined.

## The features in this data set are described as below:

-   **Store:** The store number
-   **Department:**  The department number 
-   **Date:**  date of sale
-   **IsHoliday:**  Whether the week is a special holdiay week


# Summary

*Using a Random Forest Regressor Model gave the most accurate results. The result was a **mean absolute error of 1783.6** with the **r-squared score of 95.7%.**

This model can be used as a guide when determining Weekly_Sales since it results in a resonable predictions when given information on years of store, department, dates & whether it is a holdiay or not.*
