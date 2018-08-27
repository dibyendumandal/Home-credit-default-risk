# Home credit default risk @ Kaggle
*My Jupyter notebooks associated with the Kaggle competition [Home credit default risk](https://www.kaggle.com/c/home-credit-default-risk).  We scored 0.742 (out of 1)*

In these notebooks I describe some of our attempts at the [Home credit default risk](https://www.kaggle.com/c/home-credit-default-risk) organized at Kaggle using the [Scikit-Learn library](http://scikit-learn.org/stable/).  By "we", I mean a tem of a biology graduate student, a physics postdocdoctoral scholar (me), and a software professional.  It was the first Kaggle competition for all of us, and an enriching experience!

## Competiton description

The [description](https://www.kaggle.com/c/home-credit-default-risk#description) of the competion on Kaggle reads "Many people struggle to get loans due to insufficient or non-existent credit histories. And, unfortunately, this population is often taken advantage of by untrustworthy lenders. [Home Credit](http://www.homecredit.net/) strives to broaden financial inclusion for the unbanked population by providing a positive and safe borrowing experience. ... While Home Credit is currently using various statistical and machine learning methods to make these predictions, they're challenging Kagglers to help them unlock the full potential of their data."  We took on this challenge! 

## Notebooks

This was a great exercise in [supervised learning](https://en.wikipedia.org/wiki/Supervised_learning), in particular [classification](https://en.wikipedia.org/wiki/Statistical_classification).  The [data](https://www.kaggle.com/c/home-credit-default-risk/data) consisted of 7 tables, one for the main application data and six more. 

We approached the problem in three steps: 
** (1) ** To keep things simple we started with just the application data.  Even there, we first played with only a few features that displyed strong correlations with the output, found in our exploratory data analysis (EDA).  Because the dataset is skewed (very few people defaulted), we had to subsample the data for non-defaulters.  This substantially improved our prediction.  We also utilized [multiple imputation](https://en.wikipedia.org/wiki/Imputation_(statistics)#Multiple_imputation) strategy to fill in the missing values.  Follwoing are the related notebooks.  
* **[application_data_only_EDA.ipynb](https://github.com/dibyendumandal/Home-credit-default-risk/blob/master/application_data_only_EDA.ipynb)**. Here we explored the correlations among the variables. 
* **[application_data_only_with_top_features.ipynb](https://github.com/dibyendumandal/Home-credit-default-risk/blob/master/application_data_only_with_top_features.ipynb)**. Analysis with top features.  Utilizes oneHotEncoding, imputation by mean value, and subsampling.  The following standard algorithms for statistical classification (i) Gaussian Naive Bayes, (ii) Logistic Regression, (iii) Random Forest, (iv) AdaBoost Classifier, and (v) Gradient Bossting Classifier.  We also performed hyperparameter tuning using grid search. 
* **[application_data_only_with_top_features_and_multiple_imputations.ipynb](https://github.com/dibyendumandal/Home-credit-default-risk/blob/master/application_data_only_with_top_features_and_multiple_imputations.ipynb)**. Used multiple imputaton instead of imputation by mean. 

** (2) ** Next, we moved on the complete application table.  

* **[application_data_only_with_all_features.ipynb](https://github.com/dibyendumandal/Home-credit-default-risk/blob/master/application_data_only_with_all_features.ipynb)**. Analysis with all the features

** (3) ** Finally, we played with the combined data from all the tables utilizing various kernels posted in the competition site.

* **[combined_data.ipynb](https://github.com/dibyendumandal/Home-credit-default-risk/blob/master/combined_data.ipynb)**
* **[combined_data_with_missing_entries_removed.ipynb](https://github.com/dibyendumandal/Home-credit-default-risk/blob/master/combined_data_with_missing_entries_removed.ipynb)**
* **[combined_data_with_subsampling.ipynb.](https://github.com/dibyendumandal/Home-credit-default-risk/blob/master/Combined_data_with_subsampling.ipynb)**



