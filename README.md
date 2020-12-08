# Lead-Score-Case-Study
Finding the possible leads to the company

Problem Statement

An education company named X Education sells online courses to industry professionals. On any given day, many professionals who are interested in the courses land on their website and browse for courses and fill the form if interested with their details. The company also gets leads through past referrals. Once these leads are acquired, employees from the sales team start making calls, writing emails, etc. Through this process, some of the leads get converted while most do not. The typical lead conversion rate at X education is around 30%. We need to help them select the most promising leads, i.e. the leads that are most likely to convert into paying customers.

Solution Approach

Build a model wherein you need to assign a lead score to each of the leads such that the customers with higher lead score have a higher conversion chance and the customers with lower lead score have a lower conversion chance.

Model Objective

Build a logistic regression model to assign a lead score between 0 and 100 to each of the leads which can be used by the company to target potential leads. A higher score would mean that the lead is hot, i.e. is most likely to convert whereas a lower score would mean that the lead is cold and will mostly not get converted.

Detailed Steps Followed while building the model

1. Firstly, we have imported the data and the libraries needed to build this model
2. Data Cleaning:
  Firstly, converted the columns have "Select" as their values to null as this gives us the information that either the user hasn’t selected any option or chose not to sele ct.
  Have dropped the columns with greater than 45% missing values and even with one unique value
  Performed binary mapping
  Used the appropriate data imputation technique for other columns with missing values.
3. Data Analysis:
  Identified the outlier data and handled it.
  Performed the EDA on all the columns and have plotted them against ‘Converted’ and inferred which columns might be suitable for further analysis
4. Data Preparation:
  Have created a dummy variable for the categorical columns
  Performed the test train split
  Feature scaling have been done
5. Have started building the logistic regression model and using RFE technique chose the top 20 variables which will give more accurate results.
6. Dropping the columns p values greater than 0.05 and VIF greater than 2.5
7. Calculated the model evaluation parameters like accuracy, sensitivity, specificity, Precision and recall
8. The optimal cut off was 0.35 so we have considered it as a cut off probability
9. Make predictions on test data and using the same threshold value of 0.35 predicted if the lead is converted or not.
Adding of a lead score column to the final model which is populated by multiplying the conversion probability value with 100 so that we get the score between 0-100.


Kaggle url:https://www.kaggle.com/harshabelurkar/lead-scoring-case-study
