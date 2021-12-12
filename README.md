# Credit-Card-Default-Payments-Detection
This is the final project for the course of Artificial Intelligence(Fall-2021) and it is implemented by Siva Bandaru and Keerthan Malagam.

This project implements prediction of credit card defaulters by training data set with different machine learning algorithms and comparing performance of each model.

## Table of Contents:
+ [Data Set](#Data_Set) </br>
+ [Machine Learning models used](#Machine_Learning_models_used) </br>
+ [How we used these models in project](#How_we_used_these_models_in_project) </br>
+ [Performance](#Performance) </br>

## <a name="Data_Set"></a> Data Set 

This dataset contains information on default payments, demographic factors, credit data, payment history, and bill statements of credit card clients from April to September of 2005.
 
There are 24 features:
 
**Demographic Information**
- ID: ID of each client
- LIMIT_BAL: Amount of given credit in NT dollars (includes individual and family / supplementary credit)
- SEX: Gender (1=male, 2=female)
- EDUCATION: (1=graduate school, 2=university, 3=high school, 4=others, 5=unknown, 6=unknown)
- MARRIAGE: Marital status (1=married, 2=single, 3=others)
- AGE: Age in years

**Repayment Status for past 6 months**

**(-1 = pay duly, 1 = payment delay for one month, 2 = payment delay for two months, ..., 9 = payment delay for nine months and above)**
- PAY_0: Repayment status in September, 2005 
- PAY_2: Repayment status in August, 2005 (scale same as above)
- PAY_3: Repayment status in July, 2005 (scale same as above)
- PAY_4: Repayment status in June, 2005 (scale same as above) 
- PAY_5: Repayment status in May, 2005 (scale same as above)
- PAY_6: Repayment status in April, 2005 (scale same as above)


**Amount of bill statement for past 6 months**
- BILL_AMT1: Amount of bill statement in September, 2005 (NT dollar)
- BILL_AMT2: Amount of bill statement in August, 2005 (NT dollar)
- BILL_AMT3: Amount of bill statement in July, 2005 (NT dollar)
- BILL_AMT4: Amount of bill statement in June, 2005 (NT dollar)
- BILL_AMT5: Amount of bill statement in May, 2005 (NT dollar)
- BILL_AMT6: Amount of bill statement in April, 2005 (NT dollar)

**Amount of previous payment for past 6 months**
- PAY_AMT1: Amount of previous payment in September, 2005 (NT dollar)
- PAY_AMT2: Amount of previous payment in August, 2005 (NT dollar)
- PAY_AMT3: Amount of previous payment in July, 2005 (NT dollar)
- PAY_AMT4: Amount of previous payment in June, 2005 (NT dollar)
- PAY_AMT5: Amount of previous payment in May, 2005 (NT dollar)
- PAY_AMT6: Amount of previous payment in April, 2005 (NT dollar)

**Target Variable**
- default payment next month: Default payment (1=yes, 0=no)
***

## <a name="Machine_Learning_models_used"> </a> Machine Learning models used 
**SVM**

A support vector machine "(SVM) is a supervised machine learning algorithm that can be used for both classification as a regression task. However, it is mainly used in classification problems. In the SVM algorithm, each of the values ​​at a particular coordinate. Draw each data element as a point in the n-dimensional space (n is the number of features) that is the value of  the feature. Next, find a superplane that very well distinguishes the two classes and perform the classification.

**How it works**

A simple linear SVM classifier works by drawing a straight line between two classes. That is, all data points on one side of the line represent categories, and data points on the other side of the line are placed into other categories. This means you can choose from an infinite number of lines. What makes the linear SVM algorithm better than other algorithms like nearest neighbour is that it picks the best line for classifying data points. Pick the line that separates the data and keep it as far away as possible from the cabinet data points. 2D examples will help you understand all machine learning jargon. A grid usually has multiple data points. You want to categorize these data points, but you don't want your data to fall into the wrong category. This means that we are trying to find the line between the two nearest points that separates the other data points. Therefore, the two nearest data points give the reference vector to use to find this line. This line is called the decision boundary.

**Logistic Regression**

Logistic regression — also known as logit regression, binary logit, or binary logistic regression. The statistical method of logistic regression is used to predict the outcome of a dependent variable based on previous observations. It's a type of regression analysis that's frequently used to solve binary classification problems.

The approach used by logistic regression is to model the log of the odds ratio of the outcomes.A logistic regression model is fit by estimating the coefficients using maximum likelihood estimation. This is because no closed-form solution exists, unlike for linear regression.If you're unfamiliar with regression analysis, it's a type of predictive modeling technique that's used to determine the relationship between a dependent variable and one or more independent variables.

**How it works**

In Logistic regression, instead of fitting a regression line, we fit an "S" shaped logistic function, which predicts two maximum values (0 or 1).
The curve from the logistic function indicates the likelihood of something such as whether the cells are cancerous or not, a mouse is obese or not based on its weight, etc.
Logistic Regression is a significant machine learning algorithm because it has the ability to provide probabilities and classify new data using continuous and discrete datasets.
Logistic Regression can be used to classify the observations using different types of data and can easily determine the most effective variables used for the classification

**Naive bayes**

A Naive Bayes classifier is a probabilistic machine learning model that’s used for classification task. The crux of the classifier is based on the Bayes theorem.

**How it works**

Using Bayes theorem, we can find the probability of A happening, given that B has occurred. Here, B is the evidence and A is the hypothesis. The assumption made here is that the predictors/features are independent. That is presence of one particular feature does not affect the other. Hence it is called naive.

**Random Forest**

Random forest is a supervised learning algorithm. The "forest" it builds, is an ensemble of decision trees, usually trained with the “bagging” method. The general idea of the bagging method is that a combination of learning models increases the overall result.

**How it works**

Random forest is a supervised learning algorithm. The "forest" it builds, is an ensemble of decision trees, usually trained with the “bagging” method. The general idea of the bagging method is that a combination of learning models increases the overall result.

One big advantage of random forest is that it can be used for both classification and regression problems, which form the majority of current machine learning systems. Let's look at random forest in classification, since classification is sometimes considered the building block of machine learning. Below you can see how a random forest would look like with two trees:

Random forest has nearly the same hyperparameters as a decision tree or a bagging classifier. Fortunately, there's no need to combine a decision tree with a bagging classifier because you can easily use the classifier-class of random forest. With random forest, you can also deal with regression tasks by using the algorithm's regressor.

Random forest adds additional randomness to the model, while growing the trees. Instead of searching for the most important feature while splitting a node, it searches for the best feature among a random subset of features. This results in a wide diversity that generally results in a better model.

Therefore, in random forest, only a random subset of the features is taken into consideration by the algorithm for splitting a node. You can even make trees more random by additionally using random thresholds for each feature rather than searching for the best possible thresholds (like a normal decision tree does).
 
 ## <a name="How_we_used_these_models_in_project"> </a> How we used these models in project
 
- Performed training on data set.
- Predicting the model by using test data set.
- Evaluated the model by using F1 score,K Fold Cross validation and confusion matrix.
- Testing the trained model with new dataset

## <a name="Performance"> </a> Performance
**Following is the performance of each models used.**
![image](https://user-images.githubusercontent.com/95928967/145607620-8f56e6bf-5f14-4886-a5ff-6506d5abd7b8.png)

![image](https://user-images.githubusercontent.com/95928967/145636792-b7e5e418-02c6-4583-999e-9d0701a92992.png)


