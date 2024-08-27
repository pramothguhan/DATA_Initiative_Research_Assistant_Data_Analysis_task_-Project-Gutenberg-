## Project Gutenberg Data Analysis :books:

## Overview :memo:

This project is focused on analyzing the metadata and download patterns of books from Project Gutenberg using various statistical methods and machine learning techniques. The analysis aims to understand the factors influencing the popularity of books (as measured by download counts) and to identify key predictors of book downloads. The project involves merging multiple datasets, handling missing values, performing feature engineering, and applying regression models.

## Abstract :notebook_with_decorative_cover:

The analysis uses metadata from Project Gutenberg, including Kullback-Leibler divergence (KLD) measures, genre classifications, and sentiment scores, to predict the log-transformed download counts of books. Through statistical and machine learning techniques such as OLS regression and LASSO regression, we identify the most influential features that drive book popularity. The project also addresses multicollinearity and other statistical challenges to ensure the robustness of the findings.

## Project Goals :dart:

1. **Data Integration:** Merge multiple datasets to create a comprehensive dataset for analysis.
2. **Feature Engineering:** Calculate book-level measures of KLD and other relevant features.
3. **Model Development:** Fit OLS and LASSO regression models to identify key predictors of book downloads.
4. **Performance Evaluation:** Assess the model's performance using R-squared, F-statistics, and other relevant metrics.
5. **Result Documentation:** Document insights and findings from the analysis, including variable descriptions and predictive performance.

## Technologies Used :computer:

[![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)](https://numpy.org/)
[![Statsmodels](https://img.shields.io/badge/Statsmodels-FFDD44?style=for-the-badge&logo=python&logoColor=black)](https://www.statsmodels.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)

## Methodology :gear:

1. **Data Loading and Merging:**
   - Loaded and merged data from multiple sources including metadata, KLD scores, and extra controls.

2. **Feature Engineering:**
   - Calculated KLD measures such as mean, variance, and slope.
   - Created dummy variables for categorical features and handled missing values.

3. **Model Development:**
   - Applied OLS regression to assess the relationship between features and log-transformed download counts.
   - Used LASSO regression to identify the most predictive variables.

4. **Multicollinearity Check:**
   - Checked for multicollinearity using Variance Inflation Factor (VIF) and dropped variables with high VIF scores.

5. **Performance Evaluation:**
   - Evaluated models using R-squared, F-statistics, and p-values.
   - Interpreted coefficients to understand the impact of different variables on book downloads.

## Results :chart_with_upwards_trend:

- **Key Predictors Identified:** 
   - Significant predictors of book downloads include KLD slope, genres like fantasy, science fiction, horror, and word count.
   - High multicollinearity was found in some variables, which were subsequently removed to improve model accuracy.

- **Model Performance:**
   - The OLS regression model achieved an R-squared value of 0.118, indicating that the model explains 11.8% of the variability in log downloads.

## Project Folder Structure :file_folder:
``
📦 Project_Gutenberg_Analysis
├── data
│   ├── SPGC-metadata-2018-07-18.csv
│   ├── KLDscores.csv
│   ├── extra_controls.csv
├── notebooks
│   └── Data_Analysis_Task_Project_Gutenberg.ipynb
├── results
│   └── regression_results.txt
└── README.md
``
