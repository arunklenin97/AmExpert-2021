# AmExpert 2021 - Machine Learning Hackathon
## About
The competition was conducted by American Express on [Analytics Vidhya](https://datahack.analyticsvidhya.com/contest/amexpert-2021-machine-learning-hackathon/)
## Dataset
| Column Name             | Description                                 |
| ----------------------- | ------------------------------------------- |
| Customer_ID             | unique identification of customer           |
| Gender                  | Gender of customer                          |
| Age                     | age of customer (Years)                     |
| Vintage                 | No. of months customer has been active      |
| Is_Active               | whether a customer is active or not         |
| City_Category           | City category of the customer               |
| Customer_Category       | Category of the customer                    |
| Product_Holding_B1         | List of products owned by the customer now   |
| Product_Holding_B2         | List of products owned by the customer in the future- 6 months

## Approach 
The columns Product_Holding_B1 and Product_Holding_B2 are converted into one hot columns as the these features are list of products.

New features like count of current product, converted discrete columns like age and vintage to categorical

Used count based label encoding technique and one hot encoding technique to convert categorical features 

Trained the dataset after scaling using logistc regression and the top products are sorted based on the distnace from predicted probability and decison cutoff for all the products. A cutoff vector which maximizes ROC AUC has been calculated. 

