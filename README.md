**Customer Personality Analysis 📊**

This project analyzes a customer dataset to understand their behavior and segment them based on their characteristics. The primary goal is to clean and preprocess the data to make it suitable for further analysis and machine learning modeling.

**📋 Table of Contents**

About the Project

Dataset

Data Processing Steps

Feature Engineering

How to Use

**About the Project**

The objective of this project is to perform a comprehensive exploratory data analysis (EDA) and data cleaning on a marketing campaign dataset. The process involves handling missing values, standardizing column names, engineering new features, and preparing the data for model building.

**Dataset**

The dataset used in this project contains information about customers, including their demographics, product spending, and campaign responses.

Source: The initial dataset was imported and handled.

Transformation: The data, originally in a format that required parsing, was converted into multiple rows, similar to using the "Text to Columns" feature in Excel, to structure it properly for analysis.

**🧹 Data Processing Steps**

The raw data was processed through several cleaning and transformation steps to ensure its quality and consistency.

1. Handling Missing Values
 
Missing values were identified using .isnull().sum() in pandas. The Income column was found to have null values. These were imputed using the minimum value of the column to maintain data integrity.

2. Removing Duplicates
   
Duplicate records were removed from the dataset to avoid data redundancy and ensure each record is unique.

3. Standardizing Categorical Columns
   
Categorical columns were standardized using LabelEncoder from scikit-learn to convert text-based categorical data into a numerical format, making it suitable for machine learning algorithms.

4. Renaming Columns
   
For better readability and understanding, several columns were renamed. For example, MntWines was changed to Wine and Dt_Customer to DateofEnroll.

5. Correcting Data Types
   
The DateofEnroll column was converted from an object data type to datetime to enable time-based calculations and analysis.

6. Dropping Constant Columns
   
The Z_CostContact and Z_Revenue columns were dropped as they contained constant values across all rows and offered no predictive power.

**✨ Feature Engineering**

New features were created from the existing data to provide deeper insights and improve the performance of potential machine learning models.

1. Total Spending
   
All individual spending columns (e.g., Wine, Fruits, Meat, etc.) were summed up to create a single TotalSpending feature, representing the total amount spent by each customer.

2. Total Children

The number of kids and teens at home (Kidhome and Teenhome) were combined into a single TotalChildren feature.

3. Customer Enrollment Duration

The DateofEnroll column was used to calculate the Enrollment_Duration for each customer, indicating how long they have been with the company.

4. Simplified Marital Status

The various categories in the Marital_Status column were grouped into simpler, more meaningful categories like 'In a relationship' and 'Single' to streamline analysis.
