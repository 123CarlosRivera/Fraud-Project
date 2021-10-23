# Capstone Project - GA Data Engineering Consultants
#### Carlos Benito Rivera
#### *DSIR82-E Capstone, Presented 10.22.21*

# Problem Statement
At this point every person has probably recieved a call from a scammer telling you that you've ordered an iphone and that your payment had to be returned because they ran out of phones. To return the money they'll need the credit card number to credit the account. This is is a very popular scam. Credit card fraud in the USA is a major issue that can affect anyone and have very bad consequences debt consequences. This project aims to analyze credit card data for insight, and train a classifying model optimized for type 2 errors. Given the enormous amount of online transactions, an online tool will be developed on the final model to assist field partners with additional resource for classifying whether or not a given purchase is fraudulent. My most of my models performed well with high accuracy, but my final model was able to decrease type 2 errors by more than 75%. An executive summary of my methodology and workflow can be found [here](https://github.com/123CarlosRivera/Fraud-Project/blob/main/EXEC_SUM.md).
# Content
- app_model: contains the model used for the streamlit app
- Code: contains all syntax notebooks where data science flow was done
- presentation: contains my powerpoint presentation
- smaller_data: contains all the subsets of the data used in eda and modeling
- visual: contains all the images used in the presentation

# Software packages
- Pandas for data ingestion and cleaning
- scikitlearn for model preprocessing, selection, and training
- numpy for general mathematical operations
- classifier_copy, a personal .py script that trains multiple models for comparisons

# Data
Due to the size of the file I needed to break down the dataset for different phases of my workflow. The inital EDA and modeling in notebook **modeling_A** was done with a smaller dataset called SmallBalancedData.csv. After identifying my best models, I gridsearched over the hyperparameters and retrained those models. In **modeling_B**. I used a bigger dataset called final_model.csv that was too large to store on github. It was composed of credit card fraud data from the top 5 states: NY,PA,CA,TX,OH. The last dataset dt_misclass.csv is composed of the misclassifications from the NY model in notebook **modeling_C**. Alink to the original dataset can be found [here](https://www.kaggle.com/kartik2112/fraud-detection).

# Data Dictionary
|Feature|Type|Dataset|Description|
|---|---|---|---|
|trans_date_trans_time|datetime64|SmallBalancedClasses.csv|Transaction Date Time| 
|cc_num|int64|SmallBalancedClasses.csv|Credit Card Number| 
|merchant|object|SmallBalancedClasses.csv|Merchant Name| 
|category|object|SmallBalancedClasses.csv|Category of purchase|
|amt|float64|SmallBalancedClasses.csv|Amount of purchase| 
|first|object|SmallBalancedClasses.csv|First name on credit card| 
|last|object|SmallBalancedClasses.csv|Last name on credit card| 
|gender|object|SmallBalancedClasses.csv|Gender of credit card owner|
|street|object|SmallBalancedClasses.csv|Street of credit card owner| 
|city|object|SmallBalancedClasses.csv|City of credit card owner| 
|state|object|SmallBalancedClasses.csv|State of credit card owner| 
|zip|int64|SmallBalancedClasses.csv|Zip code of credit card owner| 
|lat|float64|SmallBalancedClasses.csv|Latitude of credit card owner| 
|long|float64|SmallBalancedClasses.csv|Longitude of credit card owner| 
|city_pop|int64|SmallBalancedClasses.csv|City population of credit card owner| 
|job|object|SmallBalancedClasses.csv|Job of credit card owner| 
|dob|object|SmallBalancedClasses.csv|Date of birth of credit card owner| 
|trans_num|float64|SmallBalancedClasses.csv|Transaction number| 
|unix_time|int64|SmallBalancedClasses.csv|Digital time| 
|merch_lat|float64|SmallBalancedClasses.csv|Merchant latitude| 
|merch_long|float64|SmallBalancedClasses.csv|Merchant longitude| 
|is_fraud|int64|SmallBalancedClasses.csv|Whether transaction is fraud or not| 
|hour|int64|SmallBalancedClasses.csv|Hour of transaction| 

# Areas for Further Research/Study:
- Cloud Computing for better models
- Tunning the decision tree model on the decision threshold

