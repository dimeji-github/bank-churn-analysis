## Bank Churn Analysis
### Project Overview
This project was presented in one of my classes at school. It was challenging but worth every challenge, as I learned a great deal while developing it.
#### Objective:
This project aims to analyze customer data from ABC Bank and predict customer churn, allowing the bank to implement strategies to retain customers. Reducing churn is critical because retaining existing customers is generally more cost-effective than acquiring new ones. The analysis uses machine learning models (Logistic Regression and Random Forest) to predict whether a customer will leave the bank. It compares their performance based on key metrics like precision, recall, and accuracy.

#### Dataset
Source:
The dataset used for this analysis is from Kaggle and contains information about ABC Bank's customers. The dataset consists of 13 features and 165,034 observations, with each row representing an account holder.

#### Key Features:
Credit Score: Numerical credit score of the customer
Geography: Country of the customer (France, Spain, Germany)
Gender: Male or Female
Age: Age of the customer
Tenure: Number of years the customer has been with the bank
Balance: Account balance of the customer
Number of Products: Number of bank products held by the customer
Has Credit Card: Indicator if the customer owns a credit card
Is Active Member: Indicator if the customer is actively using the bank's services
Estimated Salary: The customer's estimated annual salary
Exited: Target variable indicating if the customer churned (1 = Yes, 0 = No)

#### Data Preparation and Cleaning
Duplicates: 30 duplicate rows were found and removed from the dataset.
Handling Null Values: The dataset contained no missing values.
Feature Engineering: New variables for age and tenure categories were created to further analyze customer segments.
Encoding: Categorical variables such as "Geography" were one-hot encoded, and "Gender" was label encoded.
Standardization: Numerical features were standardized using various scaling methods (e.g., standard scaling, robust scaling), and standard scaling was chosen for model development.

#### Exploratory Data Analysis (EDA)
The analysis revealed the following insights:
Credit Scores: Customers who left typically had credit scores below 450.
Age: Younger customers, especially those under 35, were more likely to churn.
Tenure: Customers with less than 3 years of tenure were more likely to leave.
Geography: Germany had the highest proportion of customers who churned.
Gender: A larger proportion of female customers left compared to male customers.
Balance Distribution: A significant portion of customers had zero balance, contributing to the right-skewed distribution of balance data.

#### Machine Learning Models
- Logistic Regression
Training/Test Split: 70% of the data was used for training, and 30% was reserved for testing.
Grid Search: Used to optimize hyperparameters.
Performance Metrics (After Hyperparameter Tuning):
Accuracy: 70.20%
Recall: 80.50%
Precision: 39.75%
ROC AUC: 82.13%
- Random Forest
Training/Test Split: 70% training, 30% testing.
Random Search: Used for hyperparameter tuning.
Performance Metrics (After Hyperparameter Tuning):
Accuracy: 75%
Recall: 54%
Precision: 73%
ROC AUC: 87.68%
The Random Forest model outperformed the Logistic Regression model in terms of precision and ROC AUC score, making it the optimal model for this analysis.

Model Evaluation
Confusion matrices were used to evaluate both models, showing the following trade-offs:

True Positives: The number of customers correctly identified as churned.
False Positives: Customers who were incorrectly identified as churned but stayed.
False Negatives: Customers predicted to stay but actually left.

#### Insights
Germany had the highest churn rate relative to its customer base, while France had the lowest.
A larger percentage of female customers churned compared to males.
Younger customers and those with shorter tenure were more likely to churn.
Customers with lower balances and estimated salaries were more likely to leave the bank.

#### Recommendations
Tailor retention strategies for customers in Germany through localized marketing and customer service improvements.
Focus on providing products and services that meet the needs of customers under 35.
Build stronger relationships with customers during their first three years with the bank to improve retention.
Investigate why a higher percentage of female customers are leaving and tailor services to address their concerns.
