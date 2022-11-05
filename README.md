# Neural_Network_Charity_Analysis
## Overview of the loan prediction risk analysis:

The purpose of this analysisis to help Beks create a binary classifier to predict whether applicants will be successful if funded by Alphabet Soup.
We will use knowledge of machine learning and neural networks to conduct the analysis.

Dataset used:
A CSV file containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. 

Within this dataset are a number of columns that capture metadata about each organization, such as the following:

EIN and NAME—Identification columns

APPLICATION_TYPE—Alphabet Soup application type

AFFILIATION—Affiliated sector of industry

CLASSIFICATION—Government organization classification

USE_CASE—Use case for funding

ORGANIZATION—Organization type

STATUS—Active status

INCOME_AMT—Income classification

SPECIAL_CONSIDERATIONS—Special consideration for application

ASK_AMT—Funding amount requested

IS_SUCCESSFUL—Was the money used effectively

##  Results:

### Data Preprocessing
What variable(s) are considered the target(s) for your model?
- We considered the column "IS SUCCESSFUL" as the target, this is the identifier for whether the donation to charity was used effectively.

What variable(s) are considered to be the features for your model?
- ['APPLICATION_TYPE',
 'AFFILIATION',
 'CLASSIFICATION',
 'USE_CASE',
 'ORGANIZATION',
 'INCOME_AMT',
 'SPECIAL_CONSIDERATIONS']
These variables are the features of the model.

What variable(s) are neither targets nor features, and should be removed from the input data?
- We removed columns "EIN" and "NAME", they are just index information which will not affect the data evaluation.

### Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
- In the nerual network model, we selected two hidden layers with 80 and 30 neurons. 
- Activation function 'relu' was used to speed up the process. 'Sigmoid' was chosen because we are performing a binary classification on the outer layer.
- The model was trained with 100 epochs.
- Accuracy was used to measure the model.

Were you able to achieve the target model performance?
- Our accuracy score was only 72.4, indicating not sufficient to help predicting the performance.

What steps did you take to try and increase model performance?
- To help increase the accuracy, we tried 2 different methods:
1. Adding 1 more layer to the model, using 100, 80, 30 nerons for each layer repectively, this gave us the same accuracy score.
2. Changing the activation from 'relu' to 'tanh', with two hidden layers of 80 and 30 neurons, but we still got the same accuracy score.

##  Summary:
The overall results of the deep learning model was not as promising as expected, despite the fact we tried different layers and activations. 
However, it is recommended that we use a different machine learning model to solve this classification problem, such as supervised machine learning. Since we did all the data manipulation and merging, we could have chosen 2 metrics such as INCOME_AMT and IS SUCCESSFUL for different sampling methods to predict the accuracy score.
