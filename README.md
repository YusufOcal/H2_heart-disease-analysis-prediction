# Heart Disease Prediction and Analysis

This project focuses on exploratory data analysis, data preprocessing, and machine learning modeling using the Heart Disease UCI dataset. The primary emphasis is on outlier detection, data cleaning, and preparation for predictive modeling.

## Project Overview

The Heart Disease UCI dataset was collected by the Cleveland Clinic Foundation to aid in diagnosing heart disease. This project analyzes the dataset to understand the factors that influence heart disease risk and builds a predictive model to help identify individuals at risk.

## Dataset Description

The Heart Disease UCI dataset includes several clinical features such as:
- Demographic information (age, sex)
- Clinical measurements (blood pressure, cholesterol levels)
- Results from various medical tests
- The target variable 'num' indicating the presence and severity of heart disease

## Main Assignment: Hafta_2_Odev.ipynb

The primary notebook `Hafta_2_Odev.ipynb` demonstrates a complete data analysis workflow:

### 1. Data Loading and Initial Exploration
```python
import pandas as pd
path = '/content/drive/MyDrive/Acun Medya/Hafta_2/heart_disease_uci.csv'
df = pd.read_csv(path)
```

### 2. Comprehensive Data Analysis
- Examining dataset structure with detailed views of first and last rows
- Analyzing dimensions (920 rows, 16 columns)
- Thorough investigation of data types and column characteristics
- Detailed statistical summary of all numeric features

### 3. Missing Value Analysis
- Creation of comprehensive missing value reports:
```python
missing_data = df.isnull().sum()
data_types = df.dtypes
result = pd.concat([missing_data, data_types], axis=1)
result.columns = ['Eksik Veri Sayısı', 'Veri Tipi']
```
- Development of custom exploration functions for data understanding

### 4. Outlier Detection and Treatment
- Visualization of data distributions to identify anomalies
- Implementation of the IQR (Interquartile Range) method to detect outliers
- Careful suppression of outliers using statistically sound techniques
- Before/after comparisons of outlier treatment effects

### 5. Data Preprocessing and Model Preparation
- Handling of missing values with appropriate strategies
- Transformation of categorical features for machine learning compatibility
- Feature scaling and normalization for optimal model performance

## Additional Resources

- `MO_2_Case_Output.ipynb`: Supplementary case study with alternative analyses
- `heart_disease_uci.csv`: The dataset containing 920 patient records and 16 features
- `Ödev Kısmı.txt`: Detailed assignment requirements and dataset context

## Technical Approach

The main assignment notebook emphasizes:
- Systematic data exploration techniques
- Statistical methods for outlier identification and handling
- Data visualization for insight generation
- Preparation of clean, analysis-ready data
- Development of reproducible data processing workflows

## Key Insights

- Several features show significant correlations with heart disease presence
- Outlier detection and treatment dramatically improve data quality
- Missing values are concentrated in specific features (especially 'ca' and 'thal')
- The prepared dataset provides a solid foundation for predictive modeling

## Technologies and Techniques

- **Python Data Science Stack**: pandas, numpy, matplotlib, seaborn
- **Statistical Methods**: IQR-based outlier detection, descriptive statistics
- **Data Visualization**: Box plots, histograms, correlation matrices
- **Custom Functions**: Creation of reusable data exploration utilities 