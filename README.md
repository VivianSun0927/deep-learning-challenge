# Deep Learning Challenge - Module 22

![deeplearning](https://home.sophos.com/sites/default/files/2021-09/ai-article-pic8.jpeg)

## Introduction
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization.



## Data Preprocessing
In the process of preparing the data for our model, we performed several preprocessing steps. This report provides an overview of the data preprocessing steps undertaken.

### Target Variable:

The target variable for our model is "IS_SUCCESSFUL", which indicates whether a charitable organization was successful or not.
Features:

The features considered for our model are as follows:

- APPLICATION_TYPE—Alphabet Soup application type
- AFFILIATION—Affiliated sector of industry
- CLASSIFICATION—Government organization classification
- USE_CASE—Use case for funding
- ORGANIZATION—Organization type
- STATUS—Active status
- INCOME_AMT—Income classification
- SPECIAL_CONSIDERATIONS—Special considerations for application
- ASK_AMT—Funding amount requested

### Irrelevant Variables:

The variables "EIN" and "NAME" were identified as irrelevant for our model and were removed from the input data as they neither served as targets nor features.
Preprocessing Steps:

### Binning of "APPLICATION_TYPE":

To address the imbalance and reduce the number of unique values in the "APPLICATION_TYPE" column, we performed binning.
Application types with fewer occurrences than a specified cutoff value (set at 500) were grouped together as "Other".
This helped in reducing the number of unique values and simplifying the categorical variable.

### Binning of "CLASSIFICATION":

Similar to the "APPLICATION_TYPE" column, we performed binning on the "CLASSIFICATION" column.
Classification codes with occurrences lower than a cutoff value (set at 1000) were grouped as "Other".
This consolidation helped in managing the dimensionality of the categorical variable.

### Conversion of Categorical Data:

To utilize the categorical variables in our model, we used the "pd.get_dummies" function to convert them into numeric form.
This process created separate columns for each unique value within the categorical variables, representing their presence or absence.
The original categorical columns were replaced with these new binary columns in the dataset.

### Data Splitting:

After preprocessing, the dataset was split into training and testing datasets using the "train_test_split" function.
The features (X) and the target (y) were separated into respective arrays.

### Standardization:

To ensure consistency and comparability of the feature variables, we applied standardization using the "StandardScaler".
The scaler was fit on the training data, and the same transformation was applied to both the training and testing datasets.
This process scaled the feature values to have zero mean and unit variance, allowing for better model performance.
By performing these preprocessing steps, we have prepared the data for our model, ensuring that the target variable, features, and irrelevant variables have been appropriately handled. The dataset is now ready for further analysis and model training.

## Compiling, Training, and Evaluating the Model
In my pursuit of achieving a 75% accuracy score for the model, I made several attempts but unfortunately fell short. The first optimization attempt yielded a 70% accuracy score, which was the closest I came to the target. However, subsequent tries resulted in decreasing scores of 62% and 53%. Among all my attempts, the combination that showed the most success was using "relu" activation for the first and second hidden layers, and "sigmoid" activation for the output layer. For the first hidden layer, I set the number of units to 50, and for the second layer, I used 30 units. Initially, I trained the model for 50 epochs, which resulted in the 70% accuracy score. However, when I experimented with adding a third hidden layer, reducing the number of epochs, or changing the activation method for the hidden layers, the accuracy scores declined.
