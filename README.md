# nlp-predict-tweets-about-real-disasters

## Problem Statement:

Twitter has become an important communication channel in times of emergency. The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies). But, it’s not always clear whether a person’s words are actually announcing a disaster. In this competition, you’re challenged to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t. You’ll have access to a dataset of 10,000 tweets that were hand classified. 

Competition details and dataset can be found in kaggle: https://www.kaggle.com/c/nlp-getting-started

## Approach Taken:
1. Performed text pre-processing and replaced constactions (e.g. wouldn't to would not) in dataset.
2. Used BERT pre-trainted model **bert-base-uncased** with maxlength 512.
3. Identified optimal learning rate (3e-5) and fine-tuned using one cycle policy and the optimal learning rate.
5. Evaluated on Test dataset. Confusion matrix is as below:


              precision    recall  f1-score   support

           0       0.83      0.88      0.85       863
           1       0.83      0.76      0.80       660

    accuracy                           0.83      1523
   macro avg       0.83      0.82      0.82      1523
weighted avg       0.83      0.83      0.83      1523



5. Performed prediction on final dataset and submitted. Got Public Score: 0.81428
