# Credit-Card-Transactions-Fraud-Detection
Project of the Machine Learning Course Offered in Fall 2021 @ Zewail City

This project leverages the "Fraud Detection" dataset from Kaggle to develop a machine learning model for identifying fraudulent activities. By analyzing various features and patterns within the dataset, the goal is to build a robust fraud detection system that can accurately classify fraudulent transactions. The project aims to enhance security measures and minimize financial risks by effectively identifying and preventing fraudulent behavior.




## Dataset:

The [dataset](https://www.kaggle.com/datasets/kartik2112/fraud-detection) utilized is a simulated credit card transaction dataset encompassing both legitimate and fraudulent transactions recorded between January 1, 2019, and December 31, 2020. It encompasses transactions made by 1000 customers using credit cards from a pool of 800 merchants. The dataset comprises a total of 23 features, providing a comprehensive range of information for analysis and modeling purposes.

The "Fraud Detection" dataset available on Kaggle is a highly detailed collection of transactional data that is specifically curated for fraud detection purposes. It includes a wide range of features that provide valuable information for analyzing and identifying fraudulent activities. Some of the key features of this dataset are:

1. Transaction Features: The dataset includes transaction-related features such as transaction amount, currency, and time stamps. These features offer insights into the characteristics and patterns of fraudulent transactions, helping to distinguish them from legitimate ones.

2. Merchant Information: The dataset provides information about the merchants involved in the transactions, including their unique identifiers, merchant category codes (MCC), and location details. Analyzing merchant-related features can help in detecting patterns associated with fraudulent merchants or specific types of fraudulent transactions.

3. Card Information: The dataset contains features related to the cards used in the transactions, such as card types, cardholders' information, and card issuance details. These features can be valuable in identifying suspicious card activities and potential fraud patterns associated with specific card attributes.

4. Transaction Context: Additional features provide contextual information about the transactions, including the presence of multiple transactions from the same card, proximity to previous transactions, and the sequence of transactions. These features assist in capturing temporal patterns and dependencies that are indicative of fraudulent behavior.

5. Target Variable: The dataset includes a target variable that indicates whether a transaction is fraudulent or not. This binary classification label enables the development and evaluation of fraud detection models using supervised learning techniques.


## Data Preprocessing: 

* No nulls were found.
* No duplicates were found.
* Feature engineering: the datatype of dob and data_trans_time were changed to date time.
* Ordinal encoding was used to encode the features category, trans_day, gender, and job.
* The redundant columns trans_date_trans_time, cc_num, merchant, category, first, last, gender, street, city, state, job, dob, trans_num, trans_day, trans_month, and trans_year_month were dropped.
* The data was completely imbalanced towards legitimate transactions, so we used SMOTE oversampling to overcome such a problem.

## Model Selection:

These models were selected as they have proven to be efficient when used in binary classification problems.

* Logistic regression.
* Random forest.
* Decision tree.
* AdaBoost
* Bagging

## Results:

Since it is important for us to detect true fraud transactions, we used recall and F1 scores to assess the models preformance. Bagging model achieved higher performance.

- Accuracy = 99.81
- Recall = 82.517
- F1-score = 83.21
- Precision = 83.91
