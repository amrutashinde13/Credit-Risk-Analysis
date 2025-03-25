## Credit Risk Analysis using Machine Learning
### Predicting the risk of client default using XGBoost, LightGBM and CatBoost

- Credit risk refers to the likelihood of a client failing to fulfill their financial obligations, such as mortgages, credit card payments, and various types of loans.

- Reducing the risk of default is a key priority for financial institutions. As a result, organizations such as commercial and investment banks, venture capital firms, asset management companies, and insurance providers are increasingly leveraging technology to assess which clients are more likely to default on their debts.

- Machine learning models have significantly enhanced the accuracy of credit risk assessment by offering a data-driven approach to identifying high-risk clients before they default.

### About the Data
Nubank, a Brazilian digital bank and one of the largest fintech companies in Latin America, is widely recognized for its data-driven approach. The company leverages technology to optimize decision-making and improve financial services.

### Data Analysis

The dataset used consists of 43 features for 45,000 clients, with target_default as the target variable (True/False), indicating whether a client has defaulted. During the exploratory data analysis, we identified the presence of missing values and outliers in certain features, requiring appropriate handling before model training.

### Machine Learning Models
We experimented with the following three gradient boosting algorithms to determine which one provides the most accurate predictions:

1. XGBoost
2. LightGBM
3. CatBoost

### Results

- The primary objective of this study was to develop machine learning models capable of identifying potential defaulters, thereby minimizing financial losses for the company. The ideal model would effectively balance minimizing false negatives (to correctly identify defaulters) and false positives (to prevent mistakenly classifying reliable clients as defaulters).

- Striking this balance is challenging due to the trade-off between precision and recall. Increasing one often leads to a decrease in the other. Given the importance of minimizing financial losses, we prioritized reducing false positives, fine-tuning hyperparameters to enhance the recall rate.

- Among the three gradient boosting algorithms tested, XGBoost produced the best recall rate of 81%, though it resulted in a relatively high false positive rate of 56%. In contrast, LightGBM and CatBoost achieved lower false positive rates (38% and 33%, respectively), but at the cost of a higher false negative rate, leading to weaker recall performance compared to XGBoost.

This analysis highlights the trade-offs in selecting an optimal model and emphasizes the importance of hyperparameter tuning to align model performance with business priorities.

