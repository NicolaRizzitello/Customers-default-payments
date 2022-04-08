# [Customers Default Payments](https://github.com/NicolaRizzitello/SVM-Application/blob/main/RizzitelloSVM.ipynb)
In this project I used the support vector machine to see how many customers are not in default and how many are in default

**Languages**

![alt text](https://user-images.githubusercontent.com/103247709/162460347-b68b8dee-4268-4e8b-9757-575bc90ce393.png) ![alt text](https://user-images.githubusercontent.com/103247709/162470531-cd094e49-7515-4b13-856b-9e9944325b12.png)
## About Dataset
The dataset used for the analysis has been downloaded by [Machine Learning UCI repository](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients). This research aimed at the case of customers default payments in Taiwan and compares the predictive accuracy of probability of default among six data mining methods. this dataset is composed by 30000 rows and 24 columns: 
* **Limit_bal**: credit limit (numeric)
* **Sex**: customer's sex (categorical)
* **Marriage**: civil status (categorical)
* **Age**: customer's age (numeric)
* **Pay_**: historical past payaments from April to September 2005 (categorical)
* **Bill_AMT**: amount statement from April to September 2005 (numeric)
* **Pay_amt**: past payament amount (numeric)
* **Default**: payment, response variable (categorical)
 ## About Analysis
First step to begin the analysis is check null values and cleaning the dataset. 
Next step has been to balance the observations in the training and test set and I standardized the attributes then I used nested cross validation to estimate generalization error and hyper-parameter simultaneously.  
In the last step, I used the Support Vector Machine to my dataset divided into training and test set. 
