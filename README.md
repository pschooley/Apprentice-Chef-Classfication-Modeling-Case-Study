# Apprentice-Chef-Classfication-Modeling-Case-Study

## About / Synopsis

This repo contains a business case written by Professor Chase Kusterer at Hult International Business School for his Machine Learning students. The business case is based on Apprentice Chef, Inc. – a fictitious meal kit delivery company targets busy professionals with little to no skills in the kitchen. All meals take at most 30 minutes to make and there are a wide variety of daily-prepared gourmet meals which are delivered to the customers doors along with award-winning disposable cookware. 

Recently, Apprentice Chef Inc. has launched a cross-selling promotion where subscribers receive a half bottle of wine from a local California vineyard every Wednesday. I was tasked with analyzing the data set provided by Professor Chase Kusterer with approximately 2000 customers. The data dictionary is provided within this repository for your reference. The goal of this project was perform an exploratory data analysis and provide the top insights to answer the following question: which customers will subscribe to Apprentice Chef's cross-sell promotion?

After performing an exploratory analysis in Jupyter Notebook and feature engineering, a machine learning classification model was built to predict cross-sell success. 

## Table of contents

1. Title / Repository Name: #Apprentice-Chef-Classfication-Modeling-Case-Study
2. About / Synopsis
3. Table of contents
4. Technical Information/Packages Used
5. Summary of EDA/Feature Engineering Process
6. Repository Files Included
7. Resources/Contributers (Documentation and other links)

## Technical Information/Packages Used

**Built with** [Jupyter Notebook](https://jupyter.org/install)

### Libraries 
-	random as rand 
-	pandas as pd                       
-	matplotlib.pyplot as plt                      
-	seaborn as sns                      
-	from sklearn.model_selection train_test_split 
-	from sklearn.linear_model LogisticRegression  
-	from sklearn.metrics  confusion_matrix        
-	from sklearn.metrics  roc_auc_score            
-	from sklearn.neighbors  KNeighborsClassifier   
-	from sklearn.neighbors  KNeighborsRegressor    
-	from sklearn.preprocessing  StandardScaler    

### Libraries for Classification Trees
-	from sklearn.tree  DecisionTreeClassifier      
-	from sklearn.tree  export_graphviz             
-	from sklearn.externals.six  StringIO           
-	from IPython.display  Image                                         

### Hyperparameters
-	from sklearn.model_selection  GridSearchCV     
-	from sklearn.metrics  make_scorer         


## Summary of EDA/Feature Engineering Process
It should be noted that a feature was added to the initial dataset using external research. After confirming all values were duplicates in the name and first_name columns, a column was added indicating if the person was a male or female (1=male, and 0=female). The source of this additional variable can be found following this link: https://www.kaggle.com/mylesoneill/game-of-thrones#character-predictions.csv and navigating to the character-predictions.csv.

1. Importing all necessary packages and user defined functions created by Professor Chase Kusterer
2. Checking the head, type of each variable, and for null values: 47 null values were detected in the Family_Name column
3. Created a feature to classify by Apprentice Chef's email domain categories by splitting the emails from their domain and classifying as: personal, professional, junk.
4. Created a feature called Total_Logins, which is the sum of PC_logins and Mobile_logins
5. Dropped the following non-numerical columns: FAMILY_NAME, NAME, FIRST_NAME, EMAIL, personal_email_domain, domain_group and junk (to avoid dummy variable trap).
6. Checked for missing values again and confirmed none are present
7. Took counts of categorical variable groups to confirm n > 75 for each category
8. Proceed with EDA by generating histograms and boxplots for each variable to observe outliers
9. Created outlier thresholds with necessary variables as either a low or high threshold
10. Created feature columns for each outlier threshold
11. Dataframes with variables and list of labels were created for both the target variable and explanatory variables

## Repository Files Included

- Apprentice Chef Data Dictionary (created by Professor Chase Kusterer)
- ELIZABETH_SCHOOLEY_A2_ANALYSIS (EDA, feature engineering, all classification models and Markdown process descriptions)
- ELIZABETH_SCHOOLEY_A2_MODEL.py (timed final best performing model by AUC score)

## Resources (Documentation and other links)

- All case study materials were created and provided by Professor Chase Kusterer
- All user-defined functions following imported libraries section were created and provided by Professor Chase Kusterer and the majority can be referenced here https://github.com/chase-kusterer/machine_learning_trinkets
- External feature described in the Summary section: https://www.kaggle.com/mylesoneill/game-of-thrones#character-predictions.csv

