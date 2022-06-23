# Telecom-Churn-Case-Study
## Business Problem:
Understanding customer behaviour during churn & recommend strategies to manage them
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business goal.
To reduce customer churn, telecom companies need to predict which customers are at high risk of churn.
In this project, we will analyse customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn and identify the main indicators of churn of the high value customers.

## Data:
Data for the case study can be found at https://drive.google.com/file/d/1UcPpB0sr3qjDKpMhQAM8H4_0uy-le5Z1/view?usp=sharing

## Methodology adopted:
For tackling 2 objectives in this case study, 2 different approaches are adopted
1) predict the customers who are likely to churn: For this, PCA was perfomed as no. of dimensions in the data was very high( 178 attributes) & then XG boost & Random Forest were used as predictors for the churn.
2) Understanding why the customers churn - Both the above models have poor interpretability although prediction power is robust. Hence we built a seperate model - Logistic regression so as to understand the impact of the various attributes on the churn

## Results & Recommendations:
1. Since the primary objective of the business is to  prevent the churn,we should chose a model which identifies the churn customers better.
2. As the data set is highly imbalanced (92% Non churn & 8% churn), accuracy will be a poor measure to assess performance of the model
3. Instead **Recall/Sensitivity** will be a very good measure. A model with 81% sensitivity will identify 81% of churned customers and will only miss 19% of churned customers. A highly sensitive model can be useful for rolling out targeted plans & Schemes to potential churn customers & retain them

Model	                        	  Accuracy	Sensitivity	Specificity	Precision
a)	Logistic Regression with RFE	0.814771	0.811620	  0.815026  	0.262528
b)	Random Forest with PCA	    	0.852556	0.765845	  0.859591	  0.306770
c)  XGBoost with PCA	            0.860748	0.792254	  0.866305	  0.324675

From the above  results table, it looks like the Logistic Regression with RFE gives better model performance when comparing Random Forest with PCA and XGBoost with PCA for the following reasons:
1. Sensitivity is best among all models (81%)
2. Accuracy is around 81% which is in an acceptable range
3. Model interpretation is much better using Logistic Regression

Hence, we propose following **recommendations** based on output of Logistic Regression:
1. Local Incoming Minutes for 8th Month,Volume based cost for 3G , Average Recharge Amount for Data for 8th Month ,Special Incoming Calls for 8th Month,Local Incoming Minutes for 7th Month are the top 5 influencing factors of churn
2. For the customers who might churn in future as per the model prediction,using customer service we should first understand issues they are facing. This will also help us in preventing rolling out unnecessary promotional plans if customer is happy( Remember that accuracy of model is around 81%),
3. Once we understand the issues faced by customer, we can take redressal steps like rolling out attractive plans, cashback offers, loyalty programs, freebies to retain them instead of letting them go.
4. If many customers in same area are facing network issues, we may even consider installation of additional towers near by provided that its profitable for the company.

Note: Due to computational constraints, limited hyper parameters were used in XG boost method.More hyperparmeters in grid search CV may result in better performance. 
