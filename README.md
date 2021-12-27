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

## Results

### Target variables
- The column `IS_SUCCESSFUL` contains binary data refering to weither or not the charity donation was used effectively. This variable is then considered as the target for our deep learning neural network analysis.

### Feaute Variables
- The following columns are the features for our model: 
- APPLICATION_TYPE
- AFFILIATION
- CLASSIFICATION
- USE_CASE
- ORGANIZATION
- STATUS
- INCOME_AMT
- SPECIAL_CONSIDERATIONS
- ASK_AMT
### Model Compilation
We tried different model compilation scenarios including :
- Changing different number of hidden layers
- choosing different nodes for each hidden layer
- changing the activation function
but at the end, the last model that we used and generated the maximum accuracy compared to other models is as follows:
![image](https://user-images.githubusercontent.com/86033316/147513392-c92ea183-fd00-4724-ae71-d180a58975ac.png)

- We used 3 hidden layers and in each layer we selected 140 nodes. We selected 140 since our model has 49 input variables and 140 is in the ballpark of 2-3 times input variables. 
- We used "Relu" activation function for 1st and 2nd hidden layer, and used "Tanh" for 3rd hidden layer.
- Our model reach the maximum accuracy of 0.7485 which is very close to our target of 75%.
### Additional step taken in preprocessing
After analyzing value_counts for our ASK_AMT column, we realized that the majority of the ask amount fo loan is for $5,000. 
![image](https://user-images.githubusercontent.com/86033316/147513874-f32d9449-5c2a-4892-a993-b662e94a89ab.png)
![image](https://user-images.githubusercontent.com/86033316/147513910-9e3ad95e-e265-444b-9669-b83658d234f0.png)

Then we decided to modify our binning for ASK_AMT and changed it to below classifications:
![image](https://user-images.githubusercontent.com/86033316/147513969-248c3667-ee30-4653-afdc-ad3bb4026268.png)
This resulted in a less complex model and slightly increase accuracy.
## Summary
After performing numerous preprocessing techniques and also trying various different Neural Network Models, we were still not able to generate results with accuracy above 75% and we can conclude that our model is not outperforming.
We highly recommend further steps in pre-processing and also elliminating some features that has less corrolation to our target value. For instance, we believe that "Special COnsideration" can be elliminated from our calculations to increase our model's simplicity.






