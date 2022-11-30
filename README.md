# Financial Inclusion
This project was undertaken with the goal of finding out individuals with access to bank accounts and the different factors that influence them. This project could be used by government, financial institutions and Community enabler organizations(NGOs) to plan and roll out initiatives that would ultimately favour individuals gain access to banking institutions promoting a saving culture across East Africa.

## Business Understanding


## Problem Statement
Access to banks and banking services can help households better manage their financial decisions. Yet households may be reluctant to use these services if they do not trust the institutions, quality of service is poor or if the services disrupt local financial relationships. In East Africa, the banking sector plays a mojor role in the driving the economy forward through investment and providing loans to entrepreneurs and business players.

## Success metrics
Final model evaluation will be judged based on the Mean Absolute Error and the model precision, with a minimum of 80% true positive in the minority class.

## Data Understanding
The data used from in this project was obtained from Zindi Africa platform (https://zindi.africa/competitions/financial-inclusion-in-africa/data). There are two datasets provided, train.csv and test.csv.
1. **Train.csv**

The dataset contains 13 columns with 23524 entries. Each row is an entry pertaining an individual. Below there are brief descriptions of the different columns.
 - ***country*** : This column contains the name of country locations where the individuals are located.
 - ***year*** : This column contains the year the entry was recorded.
 - ***uniqueid*** : This column is a unique identifier to each record in the dataset.
 - ***bank_account*** : This is the target column with entries showing whether one has a bank account or not.
 - ***location_type*** : This column contains the type of location an individual is ie. urban, rural etc.
 - ***cellphone_access*** : This column contains information wether an individual has access to a cellphone or not.
 - ***household_size*** : This column contains information about the size of the household of an individual.
 - ***age_of_respondent*** :The column contains information about the age of the individual.
 - ***gender_of_respondent*** : This column contains the biological gender identification of the individual.
 - ***relationship_with_head*** : This column contains information about the nature of relationship with the head of the household to an individual.
 - ***marital_status*** : This column contains information about the marital status of the individual.
 - ***education_level*** : This column contains information about the educational level of the individual.

2. **Test.csv**

The columns are similar as those of the train set with the exception of the bank_account column which is missing.

## Exploratory Data Analysis
In this stage

## Model Selection
The modelling process entailed testing a total of five models these are:
- Logistic Regression Model
- KNN Model
- Decision Tree Classifier Model
- XGBoost Classifier Model
- Random Forest Model

### First Iteration
All the models were fitted and evaluated using the validation set. Afterwards, model tuning was performed to see if there could be any significant improvement in performance from base models. It was observed that performance of the models was getting worse as they were tuned. The models seemed to perform better on the train sets, however, the results were underwhelming in the validation set. The most promising models were base models of Random Forest Classifier and Decision Tree Classifier models, with both models capturing about 39% of the minority class.

### Second Iteration
####  Dealing with Class imbalance
The SMOTE technique from sklearn was used to solve the class imbalance in the trainset. Afterwards the models were fitted, validated and tuned to optimize them. The best performing model was the KNN classifier model with an ability to distungish the minority class 84% of the time. The MAE of the model was 0.0241 and precision score of 99% in the minority class.

## Conclusions
The best model so far is the Xgboost classifier. Overall there is lack of access to bank accounts among the population in the region. There maybe multiple factors to these eg.

- Lack of trust on banking institutions.
- Emergence of mobile banking across the region.
- Lack of education to the population about banking institutions.
Further investment in these department will go along way in trying to enable the population save more and have more faith in banking services.

## Reccommendations
These are the recommendations from this analysis:
- Increase microfinance initiatives to boost knowledge of financial institutions.
- Active Campaigns should be carried out to target people in informal employment to increase their access to bank accounts.
- Further research should be carried out to find out why most household heads have no access to bank accounts.