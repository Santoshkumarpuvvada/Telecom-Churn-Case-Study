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

## Recommendations:
1. Local Incoming Minutes for 8th Month,Volume based cost for 3G , Average Recharge Amount for Data for 8th Month ,Special Incoming Calls for 8th Month,Local Incoming Minutes for 7th Month are the top 5 influencing factors of churn
2. For the customers who might churn in future as per the model prediction,using customer service we should first understand issues they are facing. This will also help us in preventing rolling out unnecessary promotional plans if customer is happy( Remember that accuracy of model is around 81%),
3. Once we understand the issues faced by customer, we can take redressal steps like rolling out attractive plans, cashback offers, loyalty programs, freebies to retain them instead of letting them go.
4. If many customers in same area are facing network issues, we may even consider installation of additional towers near by provided that its profitable for the company.

