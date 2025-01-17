# Lab4 - Mushroom Classification

## Goal

The goal of this lab is to become familiar with a classification workflow. Models are trained and fine-tuned to predict if a mushroom is edible or poisonous based on mushroom features.

Using edible as the negative and poisonous as the positive class, we require a classifier that has very high recall score while maintaining precision at an acceptable level. 

Therefore, using cross-validation, models are first trained/tuned to maximize f1 score: The harmonic mean of precision and recall.

The best model obtained from grid search is evaluated on the test dataset, and classification report and confusion matrix are produced.

## What to do

### Datasets
yellowbrick mushroom  
https://www.scikit-yb.org/en/latest/api/datasets/mushroom.html


### Classifiers
- `LogisticRegression()`
- `SVC()`
- `BernoulliNB()`
- `RandomForestClassifier(random_state=55)` 
- `GradientBoostingClassifier(random_state=56)` 

### Steps

1. Load data.
2. Inspect data with pandas and seaborn as directed
3. Preprocessing using OneHotEncoder and LabelEncoder
4. Create training and test sets with `train_test_split()`, `random_state=37`, `test_size=0.2`
5. Compare classification models using 7-fold cross-validation.
6. Hyperparameter tuning using grid search with 7-fold cross-validation.
7. Retrain the best model.
8. Evaluate best model on test data including precision, recall and confusion matrix.

### Specifications
Write the following functions: 
- `get_classifier_cv_score()`

Additional functions provided for use:
- `print_grid_search_result()`
- `plot_grid_search_results()`
- `plot_confusion_matrix()`

Function headers and documentation are included in `lab4.ipynb`. Implement the function body accordingly.

Use these functions to implement the tasks as directed.

### Ideas for optional investigations:
1. Could we boost performance using feature engineering?
1. Use a different metric to find the best model
1. Grid search for other classifiers
1. Find a better threshold

## What to hand in
- In the Jupyter notebook `lab4.ipynb` implement the steps above as indicated. 
- Keep code clean and remove any unnecessary cells. 
- Use the results obtained to answer all questions in the notebook. 
- In the section *Reflection*, include a sentence or two about what you liked/disliked, found interesting/confusing/challangeing/motivating while working on this assignment.

During development, checkin progress with git and use descriptive commit messages.
