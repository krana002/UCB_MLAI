## Overview: 
In this practical application, our goal is to compare the performance of the different classifiers using Portuguese bank's direct phone call marketing campaigns, which aim to promote term deposits among existing customers. The classifiers used are K Nearest Neighbor, Logistic Regression, Decision Trees, and Support Vector Machines. 

### Getting Started:
Our dataset comes from the UCI Machine Learning repository link. The data is from a Portugese banking institution and is a collection of the results of multiple marketing campaigns. We will make use of the article accompanying the dataset here for more information on the data and features. Here is the link to the Jupyter Notebook.
### Business Understanding:
The main objective is to build multiple classifier methods that will predict whether a customer contact over the phone will result in a sale of banking deposit products. The features used to train the classifier methods is from a Portugal dataset of bank customers including the demographic details of the customers contacted, age and duration of contact. The goal is to examine the performance of multiple classifier methods based on a set of metrics so as to increase the effectiveness of the bank's telemarketing campaign. 
### Exploratory Data Analysis:
EDA was done to see the correlation among the various numerical data values. Then various representations were done like the histogram of bank customers by age, scatter plot of campaign contacts by age, duration of contact was used to arrive at the most optimal dataset (removing outliers). It was also observed that there were no null data values.


### Feature Engineering: 
2 levels of analysis was done using the engineering features. In the first instance, 7 key features (identified as part of EDA) like age, education, job, marital, default, housing, loan etc was used and simple models of Logistic Regression, KNN, Decision Tree, SVM was used arrive at the Performance and Accuracy of the models. Decision Tree showed the highest accuracy while Logistic Regression and Decision Tree came up with comparable train time.

![alt text](https://ibb.co/DzGXZzG)

Further analysis was done to extend the model with additional features and measure the performance using ROC AUC. In this situation, Logistic Regression with Hyperparameters, KNN with GridSearchCV and Decision Trees with GridSearchCV was used and summarized as below.

![alt text](https://ibb.co/LnG3yfY)

After hyperparameter tuning, Logistic Regression and Decision Trees showed the highest ROC AUC scores but Logistic Regression took much less time than Decision Tree (with 6 depth). 
### Findings:
Both the base analysis and detailed analysis pointed to Decision Tree and Logistic Regression having best ROC AUC (that helps maximize true positives so that there are no missed opportunities). 
Logistic Regression is the most efficient, providing the analysis in the shortest time. So, when the dataset is large, Logistic Regression could be used to quickly arrive at the accuracy values.
