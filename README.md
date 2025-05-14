# H2_heart-disease-analysis-prediction

This project focuses on exploratory data analysis, data preprocessing, and machine learning modeling using the Heart Disease UCI dataset. The primary emphasis is on outlier detection, data cleaning, and preparation for predictive modeling.

## Project Overview

The Heart Disease UCI dataset was collected by the Cleveland Clinic Foundation to aid in diagnosing heart disease. This project analyzes the dataset to understand the factors that influence heart disease risk and builds a predictive model to help identify individuals at risk.

## Dataset Description

The Heart Disease UCI dataset includes several clinical features:

- **id**: Patient identifier
- **age**: Age of the patient in years
- **sex**: Gender of the patient (Male/Female)
- **dataset**: Source of the data (Cleveland, Hungary, Switzerland, VA Long Beach)
- **cp**: Chest pain type (typical angina, atypical angina, non-anginal, asymptomatic)
- **trestbps**: Resting blood pressure in mm Hg
- **chol**: Serum cholesterol in mg/dl
- **fbs**: Fasting blood sugar > 120 mg/dl (True/False)
- **restecg**: Resting electrocardiographic results
- **thalch**: Maximum heart rate achieved
- **exang**: Exercise induced angina (True/False)
- **oldpeak**: ST depression induced by exercise relative to rest
- **slope**: Slope of the peak exercise ST segment
- **ca**: Number of major vessels colored by fluoroscopy (0-3)
- **thal**: Thalassemia (normal, fixed defect, reversable defect)
- **num**: Diagnosis of heart disease (0-4, where 0 = no presence, 1-4 = presence with increasing severity)

## Core Files

- `Hafta_2_Odev.ipynb`: **Main assignment notebook** containing:
  - Complete data loading and exploration
  - Comprehensive missing value analysis
  - Outlier detection and treatment techniques
  - Data preprocessing for machine learning
  - Statistical insights into heart disease factors

- Supporting files:
  - `heart_disease_uci.csv`: Contains 920 patient records with 16 features

## Key Techniques Demonstrated

The assignment notebook showcases several essential data analysis skills:

### 1. Data Loading and Initial Exploration
```python
import pandas as pd
path = 'heart_disease_uci.csv'
df = pd.read_csv(path)
```

### 2. Comprehensive Data Analysis
- Examining dataset structure with detailed views
- Analyzing dimensions (920 rows, 16 columns)
- Investigating data types and column characteristics
- Calculating statistical summaries of numeric features

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
- Implementation of the IQR (Interquartile Range) method:
```python
Q1 = df['age'].quantile(0.25)
Q3 = df['age'].quantile(0.75)
IQR = Q3 - Q1
lower_bound = Q1 - 1.5 * IQR
upper_bound = Q3 + 1.5 * IQR
```
- Careful handling of outliers with appropriate techniques
- Before/after comparisons to evaluate treatment effectiveness

### 5. Data Preprocessing and Feature Engineering
- Handling missing values with appropriate strategies 
- Categorical feature encoding for machine learning compatibility
- Feature scaling and normalization techniques
- Data preparation for modeling

## Key Insights

The analysis reveals several important insights:
- Several clinical features show significant correlations with heart disease presence
- Features like 'ca' (number of major vessels) and 'thal' (thalassemia) have high proportions of missing values
- Age, sex, and chest pain type (cp) are important predictors of heart disease
- Outlier treatment significantly improves data quality for modeling
- The prepared dataset provides a solid foundation for machine learning models

## Technical Challenges

- **Missing Data**: Several features have significant missing values, requiring careful imputation strategies
- **Outliers**: Detecting and handling outliers in medical data requires domain knowledge
- **Feature Engineering**: Transforming categorical variables appropriately for statistical modeling
- **Data Interpretation**: Understanding the clinical significance of various features

## Requirements

- Python 3.x
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn (for preprocessing)
- Jupyter Notebook/Google Colab

## Additional Resources

- `MO_2_Case_Output.ipynb`: Supplementary case study with alternative analyses
- `Ödev Kısmı.txt`: Detailed assignment requirements and dataset context

## Technical Approach

The main assignment notebook emphasizes:
- Systematic data exploration techniques
- Statistical methods for outlier identification and handling
- Data visualization for insight generation
- Preparation of clean, analysis-ready data
- Development of reproducible data processing workflows

## Technologies and Techniques

- **Python Data Science Stack**: pandas, numpy, matplotlib, seaborn
- **Statistical Methods**: IQR-based outlier detection, descriptive statistics
- **Data Visualization**: Box plots, histograms, correlation matrices
- **Custom Functions**: Creation of reusable data exploration utilities 