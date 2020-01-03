# Credit Cards Default Project Summary

## Why am I conducting this project?

Using the dataset on credit card default with a variety of variables relating to the demographics of the individuals and their payment history between April 2005 - September 2005, the task is to predict whether an individual defaults in the following month.

This is important for a credit card company to understand the risk level of different customers and whether there is a high risk customer type that the company could conduct further screening for before offering their services.

## Hypotheses & Metric choices

The following list will present hypotheses which I believe will have an impact on credit card default and hence why I will be adding them to the model (INITIAL ASSUMPTIONS WITH NO RELATION TO RESULTS)
 - Individuals who are more educated are likely to have better paying jobs/understand the long term implications of default and are hence less likely to default
 - Older individuals (maybe more financially mature) are less likely to default than younger individuals
 - Individuals with a higher balance limit are more likely to default (more scope for financial recklessness) - Quite weak hypothesis
 - Single individuals are more likely to default than married individuals (reduced income security)
 - Individuals who pay duly each month are less likely to default than those who do not
 - Default rate between men and women is equal
 
## Model Scores

- Evaluation metric choice: ROC_AUC score - explained <a href = '#roc_auc'> here </a>
- **Baseline model: Logisitic regression - Model cross validated score = [0.58632406 0.631525   0.62611891]**
- First iteration - Random forest classifier - Model cross validated score = [0.5677343 , 0.56818185, 0.56545654]
- First iteration - Random forest classifier (with model hypertuning) - Model cross validated score = [0.5989066 , 0.62402006, 0.62082581]
- **Second iteration - Random forest classifier (with addition payment delay variables) - Model cross validated score = [0.71882929, 0.75468678, 0.75359391]**

## Results - Business intuition

- The purpose of this project was to not only create a model which can predict default likelihood of a customer, it was also to understand the demographics and risk factors for individuals that are high risk.
- As shown by the feature importance bar chart, the top 3 most importance factors that influence whether the individual is likely to default in the next month (from the given variables), is whether they delayed payment in September by over 2+ months, whether they delayed payment in August by over 2+ months and whether they delayed payment in July by over 2+ months - This seems rather intuitive
- Individuals with higher credit balances are less likely to default
- Although age, marriage, education and sex all have lower feature importance, they are all still significant in the logistic regression (5% level of significance). 
    - There is a negative association between age and default
    - There is a positive association between marriage and default
    - There is a negative association between education and default
    - There is a positive association between being male and default
    

## Note: Further feature engineering will still be conducted to improve this project and model performance in the future.
