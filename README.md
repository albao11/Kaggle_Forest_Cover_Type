# Cover Type Prediction of Forests - Kaggle competition

![alt text] (https://github.com/albao11/Kaggle_Forest_Cover_Type/blob/master/oak-hickory.jpg)

## Context
In this competition, I was asked to predict the forest cover type from cartographic variables. The studied data was obtained from the US Geological Survey and US Forest Service. It was in raw form (not scaled) and contained binary columns of data for qualitative independent variables such as wilderness areas and soil types.

Two datasets were provided:
- A training dataset consisting of several features and containing the true cover type labels.
- A test dataset on which I had to predict the cover type labels. I was then evaluated on the accuracy of these predictions.

More details about the competition and the associated final ranking can be found in:
https://www.kaggle.com/c/sd701-cover-type-prediction-of-forests.

## Work overview
I used scikit learn and Jupyter notebook for this competition. In order to test several models, I decided to do not work on the entire training set and to split it into 2 datasets: train_X (80%) and val_X (20%) with their corresponding labels (train_y, val_y). The first set was used for training my models and the second one was used to validate whether the chosen approach was good enough.

After spot-checking the performance of Logistic regression, Decision Tree Classifier and other ensemble learning techniques (Random forest and Extra Trees), I finally decided to spend more time fine tuning the Extra Trees classifier. After examining the feature importance, I adjusted the attributes and finally achieved an accuracy on the competition test set of 96 %. 

A more detailed analysis is given in the jupyter notebook: **Kaggle_clean-OneVSRest.ipynb**.
