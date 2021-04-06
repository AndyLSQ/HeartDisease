# HeartDisease
Supervised learning project

# Introduction
According to the Center for Disease Control, heart disease is the leading cause of mortality in the United States, accounting for nearly a quarter of all deaths*. By understanding which diagnostics and symptoms are most indicative of disease, we may be able to accelerate diagnosis and treatment.
*https://www.cdc.gov/heartdisease/facts.htm

# Hypothesis
With the selected supervised machine learning models, we'll be able to predict heart disease with higher accuracy based on the features provided in this dataset.

# Conclusion
*Heart disease can be predicted based on these models*

Based on the results of this experiment, the use of supervised machine learning is an effective tool in predicting heart disease based on the key diagnostic measures included in this dataset. In particular, 3 models- Random Forest, Gradient Boosting, and Logistic Regression- were extremely effective after minor tweaks to the feature set.

## Note on Overfitting

For the Random Forest, Gradient Boosting, and Logistic regression models, I performed an importance analysis on the feature set to assess if removing the less important features would result in improvements to the respective models.

This ended up causing drastic improvements in these models, bringing them near 100% accuracy with a 20% test split. Such high accuracy made me suspicious that the models could be overfitting.

To further assess this risk I performed the following steps:
- Increased test split. I was able to increase the split up to 80% for Random Forest and up to 95% for Logistic Regression, while still maintaining accuracy scores near 1.00.
- I performed 5-fold cross validation and accuracy remained high across all folds for these models.

Based on the consistently high evaluation scores across all folds, and when using very small training splits, I feel comfortable that the model is not overfitting. I think there are some clear indicators of heart disease in this dataset which are allowing for such high effectiveness of these models. This particular dataset is also relatively small so I would like to expand testing to a larger dataset in the future.

## The best model is...
In balancing explanatory versus predictive power, I must weigh the ease of interpretation of the chosen model against it's predictive accuracy. A simpler model such as regression is more easily explainable to a broader audience, but not all data fits this type of model. More complex models such as gradient boosting may in many cases be more powerful, but the tradeoff is that they are more difficult to understand and explain without getting overly technical.

The practical application of this project is to facilitate earlier detection of heart disease in order to accelerate treatment. Therefore the primary goal is to use these variables to generate an accurate prediction so I would prioritize predictive accuracy for this use case.

However, in this instance we have 3 models that perform very well- Random Forest, Gradient Boosting and Logistic Regression. Given that there is not a significant drop in predictive power between the models, I would opt for the most interpretable of the 3, which is Logistic Regression.
