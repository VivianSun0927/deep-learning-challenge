# Deep Learning Challenge - Module 22

![deeplearning](https://home.sophos.com/sites/default/files/2021-09/ai-article-pic8.jpeg)

## Introduction
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization, such as:

- EIN and NAME—Identification columns
- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested
- IS_SUCCESSFUL—Was the money used effectively

## Data Preprocessing

## Compiling, Training, and Evaluating the Model
In my pursuit of achieving a 75% accuracy score for the model, I made several attempts but unfortunately fell short. The first optimization attempt yielded a 70% accuracy score, which was the closest I came to the target. However, subsequent tries resulted in decreasing scores of 62% and 53%. Among all my attempts, the combination that showed the most success was using "relu" activation for the first and second hidden layers, and "sigmoid" activation for the output layer. For the first hidden layer, I set the number of units to 50, and for the second layer, I used 30 units. Initially, I trained the model for 50 epochs, which resulted in the 70% accuracy score. However, when I experimented with adding a third hidden layer, reducing the number of epochs, or changing the activation method for the hidden layers, the accuracy scores declined.
