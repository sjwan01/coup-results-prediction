# Coup Results Prediction

## Background

Coups are sudden and violent events that unlawfully seize power from governments. They often entail violence and are hugely impactful on people’s lives, not only in the country where the coup takes place but also in countries that are closely connected to it.

Hence, predicting coup results becomes an important task, as it could help stakeholders and entities make decisions in advance to get ready for the upcoming risks or crises. For instance, government officials could prepare ahead of time to respond to the new geopolitical environment, and investors could make plans to avoid losing their local economic interests.

Qualitative methods for this type of problems are commonly based on critical analysis of articles and archives from various sources. As a data scientist, however, I wonder if predictions can be made using solely data methods - whether there exists some data models that can accurately tell if a coup will succeed, and whether they could inform us which features are the most crucial in determining the result.

## Data

Our analysis mainly makes use of datasets from the following sources:
- [**_Coup d'État Project_ (CDP)**](https://clinecenter.illinois.edu/project/research-themes/democracy-and-development/coup-detat-project)
- [**_Rulers, Elections, and Irregular Governance dataset_ (REIGN)**](https://oefdatascience.github.io/REIGN.github.io/menu/reign_current.html)

The _**CDP**_ dataset contains coup types, results, etc. of 943 coup instances from 1945 to 2022, and the _**REIGN**_ dataset provides thorough information about leadership and regime of countries across time. While the datasets can also be found in this repository, it is highly recommended to check out their websites. The codebooks provide comprehensive description about the datasets. Supplementary datasets from _**Oxford University**_ and _**World Bank**_ are also used to construct additional features that are deemed relevant to our problem.

The `realized` variable in the _**CDP**_ dataset is the target feature to be predicted.

## Goals

I aim to answer the following two questions through [__data analysis__](https://github.com/sjwan01/coup-results-prediction-with-classification-models/blob/main/Coup%20Results%20Prediction.ipynb):
- __*Which factors are the most influential in determining whether a result will succeed?*__
- __*How accurate can our predictions be with only selected information?*__

## Models

The following two classification models are implemented and evaluated in this project:
- __Decision Tree__
- __Random Forest__

They are deemed appropriate as they are __(1)__ robust to outliers and __(2)__ embedded with feature selection methods. Their performance are evaluated and discussed across a range of metrics: accuracy score, precision score, recall score, F1 score, and ROC curve.
