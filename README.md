# Neural_Network_Charity_Analysis

## Overview of the analysis
The purpose of this analysis was to use deep learning models to vet donation applicants for AlphabetSoup, a philanthropic organization dedicated to donating funds to other organizations. The deep learning models would aid AlphabetSoup in their decision to donate by predicting if an organization would be successful if they were given funding. The dataset includes more than 34,000 organizations that have received funding from AlphabetSoup over the years.

## Results

Data Preprocessing
- We inspected the data and dropped two columns that were not needed, "EIN" and "NAME". These neither targets nor features.

![application_df](resources/images/drop.png)

- The variable considered as the target for the model is the IS_SUCCESSFUL column.
- The variable(s) considered to be the features for the model are:

    APPLICATION_TYPE—Alphabet Soup application type  
    AFFILIATION—Affiliated sector of industry  
    CLASSIFICATION—Government organization classification  
    USE_CASE—Use case for funding  
    ORGANIZATION—Organization type  
    STATUS—Active status  
    INCOME_AMT—Income classification  
    SPECIAL_CONSIDERATIONS—Special consideration for application  
    ASK_AMT—Funding amount requested

- We inspected the number of unique values and identified columns that had more than 10 unique values. We would need bucketing to reduce the number of dummy columns. This would be indicated by the "other" column.

![application_df](resources/images/unique_values.png)

- We looked at the APPLICATION_TYPE value counts for binning and generated a density plot.

![application_df](resources/images/valuecounts.png)

![application_df](resources/images/visualvaluecounts.png)

- To further reduce the unique values, we filtered the list of value counts that occured less than 500 times in the column. We used the replace method to replace all of those values with "other". The same procedure was used for the CLASSIFICATION column.

![application_df](resources/images/replace.png)

- We generated categorical variables

![application_df](resources/images/categorical.png)


Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
- Were you able to achieve the target model performance?
- What steps did you take to try and increase model performance?

## Summary
