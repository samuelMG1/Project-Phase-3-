## Dimension Data Customer Attrition Prediction 
## Overview
Dimension Data is a leading African born technology provider operating in the Middle East and Africa, offering a portfolio of services including systems integration, managed services infrastructure, cloud solutions, business applications, customer experience, and intelligent security solutions.Founded in 1983.
Dimension Data is faced with a challenge where there is a high churn rate with most of its customers abandoning their services and switching to their competitors.
 The company has identified this problem and is now seeking to build a classifier that will help them predict whether a customer will soon stop doing business with them. 
This will be done by proper analysis using their dataset to gain insights on what factors result in a high churning rate. A prediction model will be developed and this will provide insights and recommendations to the telecommunication company that will help them retain customers and avoid Account Cancellations.
# Problem statement
To develop a machine learning model that can be used to predict and determine the probability of Loss of Customers on the  service and what factors result in this.
# Objectives
•	To identify the features that are likely to cause a customer to drop off.
•	To develop a machine learning model that will accurately predict the customers that are at a high risk of Account Cancellations.
•	To come up with measures to prevent customers who are at high risk from  Droping-off.
## Business Understanding.
Customer attrition, the loss of clients or customers, is a significant issue for industries like telecommunications and Communication Technology. Effectively managing and reducing attrition is essential for businesses operating in these sectors.
The primary objective of this project is to enhance customer retention by investigating the key factors associated with customers unsubscribing from a service, specifically within the telecommunication sector. The focus is on identifying patterns that may predict customer churn and devising strategies to address this phenomenon.
 The overarching goal is to minimize financial losses attributed to customers who discontinue their services. The project seeks to uncover discernible patterns in customer behavior leading to dropping off.
## Data Understanding.
The data used has been sourced from their database. The dataset contains a record of 4250 rows and 21 columns containing different features. Out of the 21 columns, 3 are categorical and 15 are numerical. The categorical features include:
1.	State -This is where the customer resides
3.  customer id- This is the customer Id on the services
2.	Area code - The area code associated with the customer's phone number.
2.	Account length - The number of days the customer has been an account holder.
3.	Number of v-mail messages - The number of voice mail messages received by the customer.
4.	Total day minutes - The total number of minutes the customer used during the day.
5.	Total day calls - The total number of calls made by the customer during the day.
6.	Total day charge - The total charges incurred by the customer for daytime usage.
7.	Total evening minutes - The total number of minutes the customer used during the evening.
8.	Total evening calls - The total number of calls the customer used during the evening.
9.	Total evening charge - The total charges incurred by the customer during the evening.
10.	Total night minutes - The total number of minutes the customer used during the night.
11.	Total night calls - The total number of minutes the customer used during the night.
12.	Total night charge - The total charges incurred by the customer for nighttime usage.
13.	Total international minutes - The total number of international minutes used by the customer.
14.	Total international calls - The total number of international calls used by the customer.
15.	Total international charge - The total charges incurred by the customer for international usage.
16.	number Customer service calls - The number of customer service calls made by the customer.
17.	Churn – This is the target variable its binary (1 which means loss of client and 0 meaning loss of client).
## Data Preparation
# Data Cleaning
We went through the dataset and inspected if there were missing values and null values. From this process there were no missing values and null values This shows the dataset we are working with to be complete. There were no duplicates in the dataset. 
# Data Analysis
In the Exploratory Data Analysis process, we looked into the dataset by visually and statistically examining and understanding the data before further splitting it for more analysis and modelling.
![alt text](image.png)
From the visualization above the observations on the distribution of the numerical features can be seen
 1. The distribution in the Account length is evenly skewed, indicating that the majority of customers have shorter account lengths. This suggests potential inaccuracies in predicting customer dropping off, as longer account lengths might be a more accurate predictor.

 2. The distribution of the Number of Voice Mail Messages is relatively even, indicating that the number of voicemail messages is not a particularly strong predictor of customer churn.
 ![alt text](image-2.png)
 3. Total Day Minutes, Total Day Calls, and Total Day Charge: These features show a significant amount of potential noise in the data, as the distribution is positively skewed and there is a significant amount of overlap between the classes.
 ![alt text](image-3.png)

4. Total Evening Minutes, Calls, and Charge: These features show a similar pattern to the Total Day features, indicating potential noise and overlap between classes.
![alt text](image-4.png)

5. Total Nighttime Minutes, Calls, and Charge: The distribution of these features is negatively skewed, indicating that the majority of customers have less activity at night. This suggests potential inaccuracies in predicting customer churn, as higher activity at night might be a more accurate predictor.
## Modeling
The dataset we are working on is an example of a binary classification problem that predicts churn (whether a customer will churn or not). This will use a basic logistic regression model.

To accomplish the outlined objectives specified in the project proposal, we plan to leverage a combination of diverse machine learning algorithms. The selected algorithms, each offering unique advantages, are tailored to address specific aspects of the project requirements. The following algorithms will be employed:
1. Logistic Regression
2. Decision Tree
3. Random Forest

In the assessment of our model performances, the ROC_AUC metric will be employed as a key evaluation measure. The ROC_AUC is a comprehensive metric particularly well-suited for binary classification problems. It considers both sensitivity and specificity across various threshold levels, providing a robust indication of a model's ability to discriminate between classes.


# Logistic Regression
The logistic regression model Despite its foundational nature, the model demonstrates effectiveness in capturing instances of interest, making it a valuable component of the predictive framework.
# Decision Trees
The recall score of the decision tree model stands at 0.71, a commendable performance that falls slightly short of surpassing our baseline model. This score implies that the model proficiently identifies approximately 71% of actual positive instances. While not an improvement over the baseline, the model's ability to capture a substantial portion of positive instances indicates its effectiveness in identifying potential cases of interest.
# Random Forest
The random forest classifier model exhibits an improved recall score of 0.73, showcasing a notable enhancement over its predecessor. This implies that the model accurately identifies approximately 73% of the actual positive instances.

Upon evaluation through the confusion matrix, it becomes evident that the model achieves a higher count of true positives and true negatives in comparison to false positives and false negatives. This suggests a robust performance, emphasizing the model's ability to make correct predictions more frequently than incorrect ones, indicative of its avoidance of overfitting.

As per the model's analysis, the top three most influential features are identified as total day charge, total international calls, and total evening charge.

# Model Comparison
# Model Tuning
The tuned Random Forest model demonstrates strong performance in discerning between positive (churned) and negative (non-churned) customer classes, particularly in accurately identifying churned customers.Indicating its ability to correctly capture 76% of the actual churned customers.

## conclusion
The Random Forest classifier has a recall score of 73% for predicting customer churn, effectively identifying many actual churners. While this is a good start, further feature engineering could enhance the model's performance. Improving recall is crucial for reducing misclassifications and better retaining at-risk customers. Continuous refinement through feature engineering is recommended to boost the model's accuracy and effectiveness.

## Recommendations
To address higher churn rates, it is recommended to implement targeted promotional strategies, such as offering exclusive discounts to customers in specific regions. Improving customer service by enhancing training programs for representatives is also proposed to boost satisfaction and reduce churn. Additionally, reviewing the pricing structure for various charges and introducing discounted packages can make offerings more competitive. Lastly, enhancing the voicemail plan's value through new features or discounts aims to increase customer adoption and retention.
