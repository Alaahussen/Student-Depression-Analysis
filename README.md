# Student Depression Analysis
This project aims to analyze a dataset of student data to identify patterns that could help in predicting depression. The dataset includes various features related to students' personal and academic information. Our goal is to process and analyze the data to better understand the factors contributing to depression and apply machine learning models for prediction.

# 🚀 Project Overview
This repository contains the code and documentation for Student Depression Analysis. We are using a dataset that includes features like CGPA, Study Hours, Sleep Duration, Family Income, and other factors that are hypothesized to affect student mental health.

# Dataset Overview
The dataset for this project can be accessed from the following link:  
[Kaggle Dataset - Depression Dataset](https://www.kaggle.com/datasets/hopesb/student-depression-dataset/data)

The dataset consists of various attributes related to student life, including:

CGPA: Cumulative Grade Point Average of the student (numeric).
Sleep Hours: Number of hours a student sleeps per day (numeric).
Study Hours: Number of hours a student spends studying per day (numeric).
Age: Age of the student (numeric).
Depression: Whether the student suffers from depression (categorical, yes/no).
City: The student's city of residence (categorical).
Gender: The student's gender (categorical).

# 📋 Steps of Analysis
## 1. Data Preprocessing

Handling Missing Values: We started by checking for missing values in the dataset. Missing values were either filled with appropriate techniques (mean/median for numerical values, mode for categorical variables) or dropped if there were too few instances.

Outlier Detection: Outliers were detected using Boxplots. The following steps were taken:

Boxplots: Identified extreme values in columns like Age ,CGPA and Sleep Hours.

## 2. Data Transformation
**Binarization:** The Depression column was binarized, converting it into a binary classification problem (1 for Yes, 0 for No).

**Numerical to Categorical Conversion:** Some numerical columns, such as Work Pressure and  Study Satisfaction, were converted to categorical features. This was achieved by grouping continuous values into predefined ranges (Very Dissatisfied: 0.0,Dissatisfied: 1.0 - 2.0,Neutral: 3.0,
Satisfied: 4.0)

**Label Encoding:** We applied Label Encoding to categorical features such as Gender and City to convert string labels into numerical values for machine learning models.

**Scaling:** Features like CGPA, Sleep Hours, and Study Hours were scaled using Min-Max Scaling to bring all variables to a comparable scale.

## 3. Feature Selection

To identify the most important features, we used several techniques:
**Correlation Analysis:** Analyzed correlations between features and the target variable (Depression).

**Random Forest:** Used feature importance to rank the features and select the top ones for model training.

## 4. Modeling

We split the data into training and testing sets using an 80-20 split.
We applied several machine learning models, such as Random Forest.
