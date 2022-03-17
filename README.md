# Homework 6

* You can work on this assignment as a group or an individual.
* Do a git clone on this repository into a directory on your computer.
* Once you've done the git clone, a directory called "hw-06-*your-group-name**" was created. Please do all your work inside this directory.
* You must complete the assignment in Python but you do not have to use Jupyter Notebooks.
* You should include your code for each answer AND a written response that answers the question in English.
* Your written answers should be in markdown cells or comments (markdown prefered)
* You will be graded for neatness and ease of reading your code and answers.
* While you are working on this assignment, you should occasionally add and commit your work to your local git repository and the remote repository
* If you did the clone correctly (and have worked in the directory that was created from the clone), the remote should already be set up.
* Please note that if you have trouble directly pushing your work to the remote repo, you can directly upload files to github.

## Part 1

The ["moviereviews.tsv"](https://github.com/stat426-fall2021/hw-06-data) dataset is a subset of movie reviews from a larger dataset
of [25,000 movie reviews](http://ai.stanford.edu/~amaas/data/sentiment/). The goal is to build a classification model that predicts whether or not the review is positive or negative based on the words in the review.

1.  Import the data.  Note that the dataset is tab delimited   
2. Check for and remove missing values and blank strings (if any)   
3. Split the data into a training set and a test set.  Use `test_size=0.4`, and `random_state=713`  
4.  Vectorize the data using Count Vectorizor.  To keep the X matrix from being too large, use min_df = 50 and remove stop words the way we did in class with the SPAM/HAM classification.
   
5.  Build classifiers:  fit models using
     * Multinomial Naive Bayes
     * Logistic Regression
     * Decision Tree
     * Random Forest
     * Gradient Boosting

6. Report the training and testing accuracy, F1 score, and AUC for each model in the previous problem.  What model performs the best?   

7.  What words are most important for distinguishing between positive and negative reviews? Compare the important features for your top two models.


## Part 2

The dataset ["UTfires.csv"](https://github.com/stat426-fall2021/hw-06-data) is a subset of the [1.88 Million US Wildfires Kaggle DataSet](https://www.kaggle.com/rtatman/188-million-us-wildfires) that contains the fire data for the State of UT.  Build a model to predict whether or not the fire was caused by natural or human means.  The target should be "NWCG_CAUSE_CLASSIFICATION" (exclude the "Missing data/not specified/undetermined" category).  Suppose that we are trying to build a model that can predict the cause within days of the fire being detected.  As such, *you are not allowed to use any variable in the dataset that **would not generally be available at the start** of the fire*.  See the [Kaggle](https://www.kaggle.com/rtatman/188-million-us-wildfires) page for information about the variables.   

Use your model to predict the the cause of the fires in the ["UT2016-2018.csv"](https://github.com/stat426-fall2021/hw-06-data) dataset (this contains info on Utah wildfires from 2016 - 2018).  Submit your predictions in a CSV file that is named "*your-group-name*-fire-predictions.csv" with the following columns:  FOD_ID, Prediction = Prediction (use 0 for natural and 1 for human), PProb = Predicted Probability of being in class 1.  
