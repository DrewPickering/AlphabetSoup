# Challenge – Alphabet Soup

## Overview
Build a machine learning model that will be able to predict the success of a venture paid by Alphabet Soup. The trained model will be used to determine the future funding decisions.  Only projects predicted by the model to be a success will receive any future funding from Alphabet Soup.

## Resources
Alphabet Soup’s business team provided a CSV containing more than 34,000 organizations that have received various amounts of funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization such as the following:
•	EIN and NAME—Identification columns
•	APPLICATION_TYPE—Alphabet Soup application type
•	AFFILIATION—Affiliated sector of industry
•	CLASSIFICATION—Government organization classification
•	USE_CASE—Use case for funding
•	ORGANIZATION—Organization type
•	STATUS—Active status
•	INCOME_AMT—Income classification
•	SPECIAL_CONSIDERATIONS—Special consideration for application
•	ASK_AMT—Funding amount requested
•	IS_SUCCESSFUL—Was the money used effectively

## Objectives
Import, analyze, clean, and preprocess a “real-world” classification dataset.
Select, design, and train a binary classification model of your choosing.
Optimize model training and input data to achieve model performance as close to 0.75 as possible or better.

## Data Preprocessing
1.	Determine target variable; “IS_SUCCESSFUL”
2.	Determine variables to be features of the model
3.	Remove unnecessary data columns; “NAME” and “EIN”
4.	Combine rare categorical data into buckets; “CLASSIFICATION” and “APPLICATION_TYPE”
5.	Encode categorical data
6.	Standardize numerical values

## Review of final model
### Benchmark models:
    Logistic Regression = 0.467 accuracy
    Random Forest = 0.710 accuracy

The final Deep Neural Network model achieved 0.7271 accuracy and 0.5533 loss.  It utilized 2 layers; layer 1 - 32 neurons and layer 2 - 12 neurons.  The standard guidance is to use two to three times the number of neurons as input variables.  This was steadily increased to optimize.  Ranges between 8:5 neurons per layer to the final 32:12 were tested with minimal impact on model accuracy.

I was not able to achieve the target 75% accuracy.  Multiple changes to the dataset were tested, binning of certain categories, and differing cut-off points for “Other” were attempted.  These had modest to no effect on the model.  Multiple changes to neurons, a third layer was tested but seem ed to make results worse.  Epochs were varied from 25 up to 500, very minimal changes were achieved.

If a different model were to be used, I would first seek to find new data inputs that may provide some greater insight into success or failure.  Investing should consider the experience of the people running the charity and whether they have had past success or failures.  Perhaps, a new Deep Neural Network model with the inclusion of charity personnel data such as charity “CEO years of experience” or “CEO previous charities led”.
