## CustomerChurn
## Capstone Project - Telco Customer Churn Prediction

1. Introduction-
Customer churn means that the customer has churned. In this scenerio, churn means the customer has unsubcribed or canceled using the service. Customer churn is an important factor for a growing business, it will tell you about how your business is doing and if the customer are statisfied with the service provided. Knowing the churn rate is crucial because this will enable the company representatives to take decisions for retaining the customer from further churning in a cost efficient mannor.

In this project I will predict if the customer is about to leave the services provided by the company using data analysis and machine learning. For this, the dataset used is of a telecom company (link - https://www.kaggle.com/blastchar/telco-customer-churn).

2. Data Overview and Cleaning-
After importing the dataset, I wanted to understand how the data is distributed and the features it contains. This is a supervied dataset as we have the churn value associated with each customer already present in dataset. It consists of 7043 rows (i.e enteries) and 21 columns (i.e features). It tells us about the type of service they are using like phone or internet service, payments methods, thier monthly charges, whether they have partner or dependents etc.

It is important to understand what data type each column represent. If the data type is not correct then we have to change it. So we can see that the column TotalCharges is of object type, this needs to be changed in numeric for further analysis.

3. Data Exploration-
After looking into the dataset, I explored it further by creating multiple visualizations. This was done using matplotlib and seaborn libraries. In this section I created visualizations of various columns to identify the trends in dataset for analysis.

4. Churn-
The below graph shows that the customer that are churing is more than one third of the customer that are not churing, churn rate is about 27%. The count of customer who did not churn is 5163 as compared to those who churned 1869.

5. Payment Method-
The payment can be done using 4 different ways - elctronic, mailed check, bank transfer, credit card. Largest payment recieved to the company is through electronic check with 2365 count. The second graph represents the distribustion of churn with respect to payment methods.

It is observed from the graph that the churn rate is high in electronic check at around 15% of the count.

6. Senior Citizen-
Senior Citizens contributes to only 16% of customers, however, they have significantly higher churn rate counting to 7%, almost half of their population. The non senior citizen are about 64% and the churn rate is 20% which is one third of their population.

The second graph is combination of sex, gender and churn rate, we can see that the gender does not play important role in churn. In both senior and non senior citizen the churn with respect to gender is almost same.

7. Partner-
Customers that don't have partners are more likely to churn as represented in the following graph.

8. Dependents-
Customers that don't have dependents are more likely to churn as represented in the following graph.

9. Internet Service-
The column of internet service has 3 different segement- DSL, Fiber optic and No internet service. Majority of the customer are using fiber optic service. There are about 22% of customer who do not use the internet service.

The subsequent pie graph shows the distribution of customer with respect to segement and the bar graph represent the percentage of customer churning in each segment. From the graphs it is observed that customers with fiber optic service are more likely to churn.

10. Customer Distribution-
The following set of pie chart represents the percentage of customer in the following 4 categories- Gender, Partner, Dependetns, Senior Citizen

11. Contract-
There are 3 types of contract a customer can have and the following graph shows that most of the customers have the month to month contract. Followed by 2 years and then 1 year contract.

The second graph shows distribution of contract along the months(tenure). Interestingly most of the monthly contracts last for 1-4 months, while the 2 year contracts tend to last for about 70 months before the customer starts churing. This shows that the customers taking a longer contract are more loyal to the company and tend to stay with it for a longer period of time.

12. Correlation Matrix-
Out of 21 columns there are only three numerical columns: tenure, monthly charges and total charges. Through this correlation matrix we can see that tenure and total charges are highly correlated.

13. From the plots we can conclude that-
There are only three numerical columns: tenure, monthly charges and total charges. The probability density distribution can be estimated using the seaborn kdeplot function.
    a. Recent clients are more likely to churn
    b. Clients with higher MonthlyCharges are also more likely to churn
    c. Tenure and MonthlyCharges are probably important features

14. Additional Service-
Additional services include Online Security, Online Backup, Device Protection, Tech Support, Streaming TV and Streaming Movies. The first plot shows the total number of customers for each additional service, while the second shows the number of clients that churn. We can observe that:
    a. Customers with the first 4 additionals (security to tech support) are less likely to churn
    b. Streaming service is not predictive for churn

15. Machine Learning- 
Now that we are done with the data analysis and identified the trends in the dataset, we will do the machine learning to build a model which will actually predict if the customer is churning or not.

16. Data Seperation-
Seperating the data with 80% training and 20% testing.

17. Logistic Regression-
Logistic regression is a statistical model that uses a logistic function to model a binary dependent variable (as we have 2 possible outcomes - either churining or not churning).

18. Suppoer Vector Machine (SVM)-
In the case of SVM, a data point is viewed as a p-dimensional vector (a list of p numbers), and we want to know whether we can separate all points in the dataset with two (p-1)-dimensional hyperplanes. We will choose the hyperplanes that represents the largest separation, or margin, between the two classes.

19. SVM with Standard Scaler-
Above the accuracy provided by SVM is 77%, we will Standardize the dataset and see if the accuracy changes. After standard scaler the percent of accuracy increased by 2% making it 78%

20. KNN-
The KNN algorithm assumes that similar things exist in close proximity. In other words, similar things are near to each other. In this algorithm, for the purpose of classification we identify k points near the target, and assign it the value of the majority of those points. On this dataset, the optimum value of k is observed to be 6 as represented in the graph below.

21. Decision Tree- 
A decision tree is a flowchart-like structure in which each internal node represents a "test" on an attribute (e.g. whether a customer is senior citizen or not), each branch represents the outcome of the test, and each leaf node represents a class label (weather the customer is churning or not).

22. Random Forest-
Random forests or random decision forests are an ensemble learning method for prediction that operate by constructing a multitude of decision trees at training time and outputting the label that is the mode of the prediction labels of the individual trees.

23. Final Graph-
The final graph of this project is the comparison of the different Machine learning models used. It shows that Logistic Regression performed the best with 78.6% accuaracy on this particular dataset.