# Neural_Network_Charity_Analysis

## Overview
The objective was to create, train and optimize a neural network model for determining the success or failure rate of charities using a CSV file containing attributes on over 34,000 organizations. The following parameters were used to optimize the model accuracy:
1. Hidden layers
2. Neurons in each layer (i.e. layer architecture)
3. Activation functions (relu, tanh & sigmoid)
4. Input features (show/hide columns)
5. Number of training iterations (epochs)

The goal to achieve 75% accuracy for the optimized model was not reached from the various iterations ran. The final trained model reached an accuracy of 74% after experimentation with the different inputs.

## Results

### Data Preprocessing
From the charity_data.csv file, the following target, feature and identification variables are considered:
1. Target Variable
IS_SUCCESSFUL

2. Feature Variables
APPLICATION_TYPE—Alphabet Soup application type
AFFILIATION—Affiliated sector of industry
CLASSIFICATION—Government organization classification
USE_CASE—Use case for funding
ORGANIZATION—Organization type
STATUS—Active status
INCOME_AMT—Income classification
SPECIAL_CONSIDERATIONS—Special consideration for application
ASK_AMT—Funding amount requested

3. ID Variables
EIN
NAME

The ID variables are removed from the dataset, and the categorical variables are encoded and bucketized into unique numeric values. After the encoding step is finished, the dataset is split into training and testing and scaled.

### Compiling, Training and Evaluating the Model
Model inputs for the **tensorflow.keras.models.**:

| Parameter | Original Run | Optimized Run | 
|:---|:---|:---|
| Number of Epochs | 100 | 140 | 
| Hidden Layers | 2 | 3 |
| Output Layer | 1 | 1 |
| Layer architecture | 120 / 40 / 1 | 120 / 60 / 3 / 1 |
| Activation | relu / relu / sigmoid | relu relu sigmoid sigmoid |
| Model Accuracy | 0.7244 | 0.7257 |
| Loss | 0.5856 | 0.5618 | 

## Summary
No significant increase in the model accuracy by changing the above parameters. At best the neural network model can predict the success or failure rate of the charity dataset with 73% accuracy, and the initial model parameters are balanced in their performance run time and accuracy (less epochs and decent accuracy). Steps taken included an incremental approach to changing each model parameter in order to compare to the previous results, however the expected result was not always consistent with previous runs. It was difficult to gauge which factors mattered more for the model accuracy as sometimes the changes to the factors yielded a neglible change. The factors that made the most significance was the number of epochs, and layer architecture. 

It is highly suggested that other modeling approaches be taken to help better predict the charity success rate for the provided dataset, since the performance on the neural network model does not meet the criteria. 
