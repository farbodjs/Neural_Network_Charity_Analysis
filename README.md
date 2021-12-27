# Neural_Network_Charity_Analysis
## Overview of the project
From Alphabet Soup’s business team, we have received a CSV containing more than 34,000 organizations that have received funding over the past years
In this project, we used the features in the provided dataset ( https://github.com/farbodjs/Neural_Network_Charity_Analysis/blob/main/charity_data.csv) to a binary classifier that is capable of predicting whether applicants will be successful if funded by our clinet, Alphabet Soup.

## Pre-processing procedure
Within this dataset are a number of columns that capture metadata about each organization, such as the following:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special consideration for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

In our initial pre-processing steps, we decided that in order to decrease model's complexity, it is better to elliminate "EIN" and "Name" from our calculations.

