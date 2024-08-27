# NVDRS-social-isolation
This repository contains the code to conduct NLP-based topic modeling, annotation, and supervised classification of NVDRS law enforcement and coroner/medical examiner narratives for chronic social isolation and loneliness and related events.

## Data

Access to the NVDRS Restricted Access Database requires approval from the NVDRS RAD review committee, consisting of scientific and data analysis experts within CDC's National Center for Injury Prevention and Control. More information on application procedures can be fuound here: 
https://www.cdc.gov/nvdrs/about/nvdrs-data-access.html

## Code

1) nvdrs_circmustance_topic_models.ipynb : The first step in our NLP pipeline utilized this code to assess topics within the "Circumstance" summary fields, for both law enforcement and coroner medical examiner. Topics were selected by suicide and CDC Injury Prevention experts after applying BERTOpic on the circumstance summary fields. This code also creates samples used for annotation/supervised classifier model training.

2) nvdrs_social_isolation_events_reliability_coding.Rmd: This file is used to calculate interrater agreement across all topics prior to supervised learning model training.
  
4) nvdrs_circumstance_rf_svm_classifiers.ipynb and nvdrs_roberta_classification.ipynb: These python notebooks include the code used to train and optimize hyperparameters for the supervised classifiers. rf/svm includes bag-of-words bigram classifiers, while roberta file contains the RoBERTa model classifier code.

5)  nvdrs_predictions_code.ipynb: This code is used to classify all full-length narratives in the NVDRS sample, which can be used for downstream analysis.'

6)  nvdrs_prediction_exploration_distributions.Rmd : This code is used to conduct exploratory data analysis and assessment of predictors of social isolation related events using generalized linear modeling. 

