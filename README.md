**#Rossmann Sales Prediction**

**Predicting sales of a major store chain Rossmann**
 
**Problem Description**
Rossmann operates over 3,000 drug stores in 7 European countries. Currently, Rossmann store managers are tasked with predicting their daily sales for up to six weeks in advance. Store sales are influenced by many factors, including promotions, competition, school and state holidays, seasonality, and locality. With thousands of individual managers predicting sales based on their unique circumstances, the accuracy of results can be quite varied.
You are provided with historical sales data for 1,115 Rossmann stores. The task is to forecast the "Sales" column for the test set. Note that some stores in the dataset were temporarily closed for refurbishment.

**Data Description**
Rossmann Stores Data.csv - historical data including Sales

store.csv - supplemental information about the stores


**Steps involved:**
**Exploratory Data Analysis:**
After loading the datasets, various analysis was performed by comparing our target variable sales with other independent variables. We performed various analysis like feature engineering, feature transformation, handling outliers, analyzing categorical and numerical data, Understanding important features, etc.

**Feature Engineering:**

1)Handling missing values:
While exploring our project we keep in mind to handle missing values and fill them with their respective mean and modes.


2)Null values treatment:
Our dataset contains a large number of null values which might tend to disturb our accuracy hence we dropped them at the beginning of our project in order to get a better result.

3)Outliers:
Outliers in regression are observations that fall far from the “cloud” of points. These points are especially important because they can have a strong inﬂuence on the least squares line. We have used this specific technique on columns like “sales” and “customers” to remove the outliers for them.

**Feature Transformation:**
Feature transformation is performed on two columns: -

StateHoliday: In the StateHoliday a=public holiday, b=Easter holiday, c=Christmas holiday,0=State Holiday. Hence, we considered a, b, c as holiday and input them with 1.
Date: We simply converted it into a datetime object and categorized it into year, month and day format.

**EDA Visualization:**

EDA Visualization is performed by using seaborn libraries with various plots like histogram, violinplot, barplot, etc. We have used these plots for describing correlations, For relationship of promo and sales, Effect of StateHoliday and SchoolHoliday. 

**One Hot Encoding:**
Machine Learning is performed only on numerical values, so there might be some columns which do not have numerical values. One Hot Encoding is a method which converts data types of values into numerical values. We have performed this technique where it was necessary.


**Feature Selection:**
There are various factors while performing feature selection. Our project is based on regression which is a parametric approach, So there are various things to keep in mind like there should be a linear and additive relationship between dependent and independent variables. There should be no correlation between residual terms, etc.
 
 
**ALGORITHMS:**

1) Linear Regression Model
2) Elastic Net Model
3) Ridge Regression Model	 
4) Lasso Regression Model
5) Decision Tree 
6) Random Forest

**Linear Regression Model**
Linear regression is a linear model, e.g., a model that assumes a linear relationship between the input variables (x) and the single output variable (y). More specifically, that y can be calculated from a linear combination of the input variables (x).

**Elastic Net Model**
Elastic net is a penalized linear regression model that includes both the L1 and L2 penalties during training. Using the terminology from “The Elements of Statistical Learning,” a hyperparameter “alpha” is provided to assign how much weight is given to each of the L1 and L2 penalties.

**Ridge Regression Model**
Ridge regression is a model tuning method that is used to analyse any data that suffers from multicollinearity. This method performs L2 regularization. When the issue of multicollinearity occurs, least-squares are unbiased, and variances are large, this results in predicted values being far away from the actual values.

**Lasso Regression Model**
In statistics and machine learning, lasso (least absolute shrinkage and selection operator; also Lasso or LASSO) is a regression analysis method that performs both variable selection and regularization in order to enhance the prediction accuracy and interpretability of the resulting statistical model.

**Decision Tree**
Decision tree algorithm falls under the category of supervised learning. They can be used to solve both regression and classification problems.
Decision tree uses the tree representation to solve the problem in which each leaf node corresponds to a class label and attributes are represented on the internal node of the tree.

**Random Forest**
Random forests or random decision forests is an ensemble learning method for classification, regression and other tasks that operates by constructing a multitude of decision trees at training time.


**Model Performance:**

 Linear Regression Model with Cross Validation: - 
 
1.Our Data set is not perfectly suitable for the linear regression model.It is giving accuracy of 83 with test data and accuracy of 84 with training data.

2.We tried cross validation with linear regression but the model still improved by 0.01 percent.

3.Lasso and Ridge Regression with Cross validation & Hyperparameter: -        
They are both also unable to improve the accuracy of our model even after Hyperparameter tuning giving accuracy of 83 with test data and 84 with training data.

4.Decision Tree Regression: -
It works Excellent on our Data set. Giving accuracy of 93 with test data and accuracy of 99 with training data. We can also say the model has overfitted our dataset for the Decision Tree Regression.

5.Random Forest Regression: -
It also works great on our Data set. Giving accuracy of 70 with test data and accuracy of 70 with test data which is consider as ideal solution of the model.

**Conclusion:**
1.	Sundays have negligible sales records. Monday (1) and Friday (5) have the highest sales. Fridays have maximum sales records. Customer features also follow the same trend.
2.	Lots of zero sales is disturbing our Target Variable. When stores are closed the sales value is zero hence, we have to deal with the zero sales.
3.	During State Holidays there are negligible sales records. But we have some Sales records even during School Holidays.
4.	Sales have declined in 2015 compared to previous years.
5.	We Tried to fit our dataset into a regression assumption but we failed to fit most of the features due to their nature.
6.	From the model Comparison we can say our dataset is not performing well in linear Regression even after Cross validation, Hyperparameter tuning with L1 & L2 does not help the model to improve its accuracy.  
7.	Decision Tree and Random Forest both work well. It should be due to the nature of features which are mostly categorical in nature.
8.	But it also seems that they are overfitting.
9.	From the Model we come to know that the customer feature is one of the most important features as it should be in case of sales prediction.
10. Competition Distance, Competition Since year, Days of week all these features are also important for the sales prediction.



