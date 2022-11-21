# How can StumbleUpon avoid surfacing stale content?
For full Power Point presentation, click [here.](https://github.com/riwasabri/Classification/blob/master/Classification%20-%20Presentation.pdf)
## **Design**

The goal of this project is to build a classification model for identifying evergreen vs
ephemeral articles. The practical application of this model would be to help
StumbleUpon - a user-curated web content discovery engine - improve on the quality of
articles recommended by systematically determining if an article is valuable to its users
or not.

Given the classes are balanced, the model will be optimized by looking at accuracy. It is
also particularly important to have high precision in order to avoid misclassifying articles
as evergreen when they are not.

## **Data** 

The data is gathered from Kaggle and consists of 7000+ rows, with one row
corresponding to one URL that StumpleUpon recommended to their users. Each URL in
the dataset is labeled as evergreen (1) or not (0) - this is the target.
Initial cleaning consisted of checking for duplicates, imputing null values where needed,
renaming columns for clarity.

## **Algorithm**

**Metrics and Hyperparameter Tuning:**
* Metrics: Accuracy, Precision as metrics of main interest
* Tuning: RandomizedGridSearchCV, GridSearchCV.

**Baseline Models:**

* Initial Baseline model on numerical features using Logistic Regression
* Feature selection with L2 Penalty
* Improvement on Baseline by trying models of varying complexity (KNN, Naive
Bayes, Random Forest,XGBoost)

**Feature Engineering:**

* Categorical Feature extraction: alchemy category, publisher
* Feature Engineering based on industry insights; for example: how-to’s, lists are
most likely to be evergreen while industries like fashion or business have
relatively high ephemeral articles.

**Improved Models:**

* Using engineered features to compare several models: Log Reg, KNN,
XGBoost,Random Forest
* Trying Ensembling

**Towards next step: TF-IDF**
* Experimented with baseline LogReg with TF-IDF.

## **Tools**
* Data Analysis: Pandas,Numpy.
* Modeling: Scikit learn.
* Data Visualization: Matplotlib,Seaborn
