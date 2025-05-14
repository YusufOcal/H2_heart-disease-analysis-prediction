# Heart Disease Prediction and Analysis

This project focuses on exploratory data analysis, data preprocessing, and machine learning modeling using the Heart Disease UCI dataset. The project demonstrates various data science techniques including handling missing values, outlier detection and suppression, and developing a basic machine learning model for heart disease prediction.

## Project Overview

The Heart Disease UCI dataset was collected by the Cleveland Clinic Foundation to aid in diagnosing heart disease. This project analyzes the dataset to understand the factors that influence heart disease risk and builds a predictive model to help identify individuals at risk.

## Dataset Description

The Heart Disease UCI dataset includes several clinical features such as:
- Demographic information (age, sex)
- Clinical measurements (blood pressure, cholesterol levels)
- Results from various medical tests
- The target variable 'num' indicating the presence and severity of heart disease

## Project Components

1. **Data Loading and Exploration**
   - Loading the dataset and understanding its structure
   - Analyzing data dimensions, column names, and data types
   - Generating summary statistics to understand feature distributions

2. **Missing Value Analysis**
   - Identifying columns with missing values
   - Implementing appropriate strategies for handling missing data

3. **Outlier Detection and Treatment**
   - Using visualization techniques (box plots) to identify outliers
   - Applying the IQR method to detect statistical outliers
   - Implementing outlier suppression by capping values at upper and lower boundaries

4. **Data Preprocessing**
   - Converting categorical variables to numerical format
   - Normalizing or standardizing numerical features
   - Preparing data for machine learning model development

5. **Machine Learning Model**
   - Building a basic machine learning model to predict heart disease
   - Evaluating model performance and interpreting results

## Files in this Directory

- `Hafta_2_Odev.ipynb`: Main Jupyter notebook containing the assignment work
- `MO_2_Case_Output.ipynb`: Case study output with detailed analysis
- `heart_disease_uci.csv`: The dataset used for analysis
- `Ödev Kısmı.txt`: Assignment instructions and dataset story

## Setup and Usage

To run this project:

1. Clone the repository
2. Ensure you have Python and necessary libraries installed (pandas, numpy, matplotlib, scikit-learn)
3. Open the Jupyter notebooks to view the analysis and code
4. Run the cells sequentially to reproduce the analysis

## Key Insights

- The analysis reveals important relationships between clinical features and heart disease risk
- Outlier detection and treatment significantly improve data quality for modeling
- The machine learning model provides a basis for identifying patients at risk of heart disease

## Technologies Used

- Python
- Pandas for data manipulation
- NumPy for numerical operations
- Matplotlib and Seaborn for data visualization
- Scikit-learn for machine learning modeling 