# Credit Score Risk & Loan Classification/Prediction (“CMHDR Bank”)

### Team Members: 
Marry Shintaku, Hetal Prajapati, Daniel Cabera, Ray Lucero, Cindy Duong

### Introduction:
We are a group of data analysts working for CMHDR Bank and we have been tasked with classifying the bank’s customers based on their credit score and credit information. We will also be creating a machine learning model that will predict whether a client’s loan application is a default or not based on specific features related to their demographics, education, payment history, annual income data, etc. Our presentation will utilize tableau to visualize the data of our customers and clients to convey our results and findings. 

Banks and financial services institutions utilize credit score classification to assess a borrower's creditworthiness, enabling them to make calculated decisions about managing risk and profitability. There are 5 credit score brackets that a person can fall into, however, for simplicity purposes, our project will focus on 3 categories of credit which are Good, Standard, or Bad.

Financial loan services are utilized by many companies, especially, in the financial services and banking industry. The goal of financial loan services is to mitigate the risk of default payments and ensure that clients are paying back their loans in compliance with their loan contract. Clients will either be deemed default (high risk) or not (low risk).

### Language: 
Python Machine learning - Neural Networks (google.colab)

### Data Sources: 
Loan data:
Yamuna Nagar (2023).
Loan Default Prediction [Dataset]. Kaggle. 
https://www.kaggle.com/datasets/nikhil1e9/loan-default

Credit Card data: 
Rohan Paris (2022).
Credit Score Classification. Kaggle.
https://www.kaggle.com/datasets/parisrohan/credit-score-classification

### Note:
CMHDR Bank is a fictional bank that was made up for project work purposes.

### Cleaning the datasets:
- [Cleaning the Credit and Loan Dataset](https://github.com/cindyd97/Project_4_Group_4/blob/main/cleaning_credit_loan_data.ipynb)
- Credit data: We removed certain columns that were deemed unnecessary to the overall features of the data set like the customer id, name, SSN, and type of loan. While the type of loan could be deemed significant as a feature, there were more than 6,000 rows with unique values which we concluded that the data set would be too large to normalize using the onehotencoder method. We then converted columns that were meant to be numeric to an integer (originally string objects). There were random characters in the 'Payment_Behaviour' column so we removed the rows of the entire data set for that column with the random characters. The 'Credit_History_Age' column specified the amount of years and months of each customer's age of credit as a string so we converted it to a float. The 'Age' column had null values and logically, shouldn't be replaced with 0, so we removed the rows in the entire data set that had a null value in this column. The other columns with null values were replaced with a 0 integer as it is logically acceptable for certain credit features to be 0 for these columns. Our label column, 'Credit_Mix', was also cleaned to remove null values in the entire data set for this column and converted it to integers for proper labeling. The label column includes 3 labels: Standard (0), Good (1), and Bad (2).
- [Original Credit Dataset](https://github.com/cindyd97/Project_4_Group_4/blob/main/Resources/Credit_data.csv)
- [Cleaned Credit Dataset](https://github.com/cindyd97/Project_4_Group_4/blob/main/Resources/clean_credit_data.csv)
- Loan Data: We checked the data set for duplicate values and found none. We dropped the 'LoanID' column as it was deemed unnecessary to include as a feature. We then converted columns that were meant to be numeric to an integer (originally string objects). The 'Default' column is the label column which includes 2 labels: Default (1) and Not Default (0). 
- [Original Loan Dataset](https://github.com/cindyd97/Project_4_Group_4/blob/main/Resources/Loan_default.csv)
- [Cleaned Loan Dataset](https://github.com/cindyd97/Project_4_Group_4/blob/main/Resources/clean_loan_data.csv)


### Credit Score Classification
We've built a machine-learning model that would segregate the bank's customers into credit score brackets to reduce manual effort.



### Loan Default Prediction
We've created a machine-learning model to predict which clients' are at the highest risk of default on their loans, for the bank to make strategic decisions on each individual's account. 






