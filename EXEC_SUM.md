# Executive Summary
---
# Methodology
---
Detecting fraud is a serious issue in the USA, so our data science workflow had to match the seriousness. First step was to create two smaller datasets: SmallBalancedData.csv and final_model.csv. Since the original dataset was too large to store on github I created a smaller one for EDA and initial modeling purposes. The second dataset was created to train the final model on a larger datatset with more fraud cases. Second step was to explore the data for any patters or trends, features that stood out, and any features that I could possibly engineer. Third step would be to start training a variety of classifying models to select 3 for hyper-tunning. After selecting those models I performed gridsearch over their parameters to optimize those models. To finish off I chose my final model and performed EDA on the misclassifications to investigate any possible trends.

# Results
---
The gridsearchCV revealed that the DecisionTree model had the highest accuracy with the lowest amount of type 2 errors compared to the null model. Our focus was to minimize the amount of type 2 erros; never classifying a purchase as noFraud when in realiy it is fraudulant purchase. The null model had 511 type 2 erros, and our final model had 124 cases. This is a significant improvement over the null model.
- Null Model (Logistic Regression Model)

> Train Acc: 0.99

> Test Acc: 0.99

> Type 2 Errors: 511

- Decision Tree Classifier Model

> Train Acc: 1.0

> Test Acc: 0.99

> Type 2 Errors: 124
# Conclusions and Recommendations
---
Although my final model function really well, they're only tools to be used for more professional input. To build stronger models cloud computing would need to be used to train models on more data.

# Web App
---
New York is the leading credit card fraud state with over 500 cases a year that account for over 350K in damages. Built on machine learning models trained on fraud purchase data from the state of New York, this online tool can be used to assist credit card companies in classifying whether or not a purchase is fradulent.

The app functions on a decision tree classifier model that was pretrained on a dataset of 85K fraud cases only in New York. Below are the results.

- Decision Tree Classifier Model 

> Train Acc: 0.99

> Test Acc: 0.99

> Type 2 Errors: 56