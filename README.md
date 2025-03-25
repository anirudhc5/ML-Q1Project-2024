# Pedicting Median Doctors' Incomes Before Tax

The purpose of this project was to gain an understanding of how useful machine learning models using WEKA can be in predicting general practitioners’ salaries, as well as the wider applications of predicting these salaries based on demographics. These demographics include, but are not limited to: GP type, contract type, country of residence within the UK, rurality, region, and working hours. We were able to train and test twenty different machine learning models, all of which are capable of predicting GP salaries using demographic data with at least 66% accuracy. Our best-performing model was our Random Forest model with Correlation attribute selection, achieving an accuracy of 97.5728% on testing, as well as TPR, FPR, and ROC values of 0.951, 0.077, and 0.987 respectively. A major limitation of our project was the lack of representation with our labels, with just three out of 1070 instances belonging to the highest income tax bracket, negatively affecting predictability and artificially inflating accuracies without actually learning from it. Future directions for this project include gathering more data from high-income general practitioners, or even oversampling to make the bracket represented. Also, future non-machine-learning studies can make use of this demographic data to further investigate the root causes of discrepancies in GP salaries, rather than just correlation as our models suggest. As such, investigating the root causes is what will enable policy-makers to further develop and improve quality of life.

Steps to reproduce our model: Random Forest with Info Gain attribute selection:

1. Open Weka and load training.arff in the Train-Test-Datasets/Original-Dataset.
2. Go to the Select Attributes tab and choose the class - Median Income Before Tax.
3. Select InfoGainAttributeEval as the attribute evaluator and Ranker as the search method and hit Start.
4. Remove all features with a ratio of less than 0.05 and keep the remaining features and the class in the dataset.
5. Save this dataset as an arff.
6. Repeat steps 1-5 for testing.arff.
7. The above files can be found under Train-Test-Datasets/Info-Gain
8. Open Weka and load the training set.
9. Click on the classify tab and click “Supplied test set” under Test Options.
10. Load the testing dataset and select the correct class - Median Income Before Tax.
11. Select Random Forest as the classifier algorithm. This is under the trees folder.
12. Click Start. 
13. The model can be be found here: Model_Performance_Data/Best_model_RandomForest.model
