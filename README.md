# Data Mining Churn Rate Project
This is a data mining project where my group analyzed a credit card companies data to build a model that predicts customer churn
## Table of Contents
* [General Info](#general-information)
* [Technologies Used](#technologies-used)
* [Exploratory Analysis](#Exploratory-Analysis)
* [Models](#Models)
* [Interpretation Of Best Model](#Interpretation-Of-Best-Model)
* [Conclusion and Recommendations ](#Conclusion-and-Recommendations )


## General Information
Background:  

A manager at a bank is concerned with an increased number of customers leaving their credit card services. They would like someone to solve this problem by developing a model to predict the churning of customers so they can proactively go to the customer and provide them with better services and change the customers' minds about leaving. In this report, we will analyze the results of our model’s performance and show how it can be implemented in the company for practical use. 
<br/> <br/>
**Target Variable:** Attritted: We have only 16.07% of customers who have churned, which creates a highly unbalanced dataset. 
## Technologies Used
- R - v2022.02.2+485
- RStudio - v2022.02.2+485
- Rattle (package written in R providing a graphical user interface to very many other R packages that provide functionality for data mining)

## Exploratory Analysis
Key takeaways from features 

- Customers with lower number of transactions and lower total transactions amounts are more likely to churn (Graphic 1 ).  
  ![Screenshot 2022-05-17 164428](https://user-images.githubusercontent.com/90923213/168915337-b4d54a74-a5a6-4754-b9f7-bbc134faf60b.png)
- Customers with lower total revolving balance and lower average utilization ratio are also more likely to churn. (Graphic 2)  <br/>
   ![Screenshot 2022-05-17 164439](https://user-images.githubusercontent.com/90923213/168915335-c669b349-5d41-48b1-b1ed-a856c931c7f1.png)
- Customers with fewer total products through the company are more likely to churn. (Graphic 3) 
   ![Screenshot 2022-05-17 164448](https://user-images.githubusercontent.com/90923213/168915334-c016757d-b87d-42b8-a485-433d2dd7daab.png)

## Models
We used all classification models such as gradient boosting, Ada boost, Logistic regression, random forest, and SVM. We did cross-validation with all models with random seeds 42, 294290, and 990998. We chose the best model by looking at the ROC curve and AUC and the lowest error provided by the error matrix. We also looked at the Precision-Recall curve because since our data was highly unbalanced, the AUC could be misleading. The best model was a gradient boosting model with an AUC of .9911 and an average error rate of 7.6%.  This model was also the best on the precision-recall curve.  

![Screenshot 2022-05-17 165018](https://user-images.githubusercontent.com/90923213/168915960-714cf766-75dc-44fc-b68c-94824ea2f91c.png) <br/>
Precision/Recall/F1 of best model
- Precision: 96% 
- Recall: 85.7% 
- F1 score: 90.73 

## Interpretation Of Best Model
The biggest worry of our clients is correctly identifying customers who are going to churn. Therefore, we chose to look at precision and recall for our evaluation methods. We were able to predict the customers who will churn with 86% recall, which is especially important to our client because this measure is what they are concerned with the most.  

This is especially useful for our clients because if they can predict 86% of customers will churn, they can reach out to them before they churn to try to better meet their needs and get them to remain a customer. In our model, we were able to predict 6 out of every 7 customers who will churn. Keeping existing customers is much more important than finding new customers because it is a lot more expensive to attempt to find new customers Our model helps to figure out what customers have a higher chance of churning and allows the company to reach out to those customers before they decide to churn, giving them a chance to retain more customers and increase profits. 

## Conclusion and Recommendations 
After interpreting the results of our model and knowing which variables affect the churn rate the most, we have produced recommendations that the company can implement to address these variables and improve the churn rate of their business.  

1. **Reward customers with higher cashback rewards when customers reach a certain number of transactions per month.** Based on our model, we believe this will help the company because individuals who make more monthly transactions are significantly less likely to leave the company’s services.  

2. **Offer different incentives such as travel amenities, credit card reward points, gas-purchase rewards, etc., for individuals who spend above their average credit balance.** According to our model, individuals who spend a higher dollar amount are much more likely to stay with the company since the transaction amount is the second most important variable for our model. 

3. **Offer incentives such as increased rewards for customers who have more than one company product.** Our model shows us that the more products a customer has through your company, the less likely they are to churn. This goes along with creating loyal customers who open multiple credit cards through your company. These customers are less likely to churn than a customer who has just one credit card opened.  

## Contact
Created by [@cadekeenan] <br>
Created by [@immcsorley] <br>
Created by [@timcookk] <br>
