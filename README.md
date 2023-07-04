# telecom-churn-case-study
> Predict churning customers for a Telecom company based on temporal behaviour


## Table of Contents
* [General Information](#general-information)
* [Technologies Used](#technologies-used)
* [Conclusions](#conclusions)


## General Information
### Problem Statement
In the telecom industry, customers are able to choose from multiple service providers and actively switch from one operator to another. In this highly competitive market, the telecommunications industry experiences an average of 15-25% annual churn rate. Given the fact that it costs 5-10 times more to acquire a new customer than to retain an existing one, customer retention has now become even more important than customer acquisition.

For many incumbent operators, retaining high profitable customers is the number one business goal. To reduce customer churn, telecom companies need to predict which customers are at high risk of churn. In this project, you will analyze customer-level data of a leading telecom firm, build predictive models to identify customers at high risk of churn.

In this competition, your goal is to build a machine learning model that is able to predict churning customers based on the features provided for their usage.


### Business Goal:
The main goal of the case study is to build ML models to predict churn. The predictive model that we’re going to build will have the following purposes:
1. It will be used to predict whether a high-value customer will churn or not, in near future (i.e. churn phase). By knowing this, the company can take action steps such as providing special plans, discounts on recharge etc.
2. It will be used to identify important variables that are strong predictors of churn. These variables may also indicate why customers choose to switch to other networks.
3. Even though overall accuracy will be our primary evaluation metric, we should also mention other metrics like precision, recall, etc. for the different models that can be used for evaluation purposes based on different business objectives. For example, in this problem statement, one business goal can be to build an ML model that identifies customers who'll definitely churn with more accuracy as compared to the ones who'll not churn. We have to mention which metric can be used in such scenarios.
4. Recommend strategies to manage customer churn based on our observations.

Note that it's highly likely that we'll need to build multiple models to fulfil the objectives mentioned in Points 1 and 2. Since here, we have a large number of attributes, and thus we should try using a dimensionality reduction technique such as PCA and then build a predictive model. After PCA, we can use any classification model.

The above model will only be able to achieve one of the two goals - to predict customers who will churn. We can’t use the above model to identify the important features for churn. That’s because PCA usually creates components that are not easy to interpret.

Therefore, we have to build another model with the main objective of identifying important predictor attributes which help the business understand indicators of churn. A good choice to identify important variables is a logistic regression model or a model from the tree family.


### Data set
A train.csv was provided that has telecom data for June, July and August with churn probability already calculated. Another unseen dataset test.csv was also provided for which we have to predict churn probability based on the best model we select.

A data dictionary was also provided that described the meaning of the variables in train and test dataset.


### Data Definitions
The definitions are also listed down below:

CIRCLE_ID : Telecom circle area to which the customer belongs to
LOC : Local calls - within same telecom circle
STD : STD calls - outside the calling circle
IC : Incoming calls
OG : Outgoing calls
T2T : Operator T to T, i.e. within same operator (mobile to mobile)
T2M : Operator T to other operator mobile
T2O : Operator T to other operator fixed line
T2F : Operator T to fixed lines of T
T2C : Operator T to it’s own call center
ARPU : Average revenue per user
MOU : Minutes of usage - voice calls
AON : Age on network - number of days the customer is using the operator T network
ONNET : All kind of calls within the same operator network
OFFNET : All kind of calls outside the operator T network
ROAM : Indicates that customer is in roaming zone during the call
SPL : Special calls
ISD : ISD calls
RECH : Recharge
NUM : Number
AMT : Amount in local currency
MAX : Maximum
DATA : Mobile internet
3G : 3G network
AV : Average
VOL : Mobile internet usage volume (in MB)
2G : 2G network
PCK : Prepaid service schemes called - PACKS
NIGHT : Scheme to use during specific night hours only
MONTHLY : Service schemes with validity equivalent to a month
SACHET : Service schemes with validity smaller than a month
*.6 : KPI for the month of June
*.7 : KPI for the month of July
*.8 : KPI for the month of August
FB_USER : Service scheme to avail services of Facebook and similar social networking sites
VBC : Volume based cost - when no specific scheme is not purchased and paid as per usage


## Technologies Used
- pandas - version 1.4.4
- numpy - version 1.21.5
- seaborn - version 0.11.2
- matplotlib - version 3.5.2
- statsmodels - version 0.13.2
- sci-kit learn - version 1.0.2


## Contact
Created by [@varunsharma8898] - feel free to contact me!