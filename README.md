# Credit_Risk_Analysis

## Overview of the analysis: 

Credit risk is very tough to predict. In this project we want to take a look at how all the factors in our loan_stats csv help predict whether someone is low or high risk status. One method that data scientists use for this type of issue is creating a model and then evaluate and train the models that they create. In this specific project we are using imbalanced-learn and scikit-learn libraries to build models and evalute them using a resampling method. In the first couple of models I oversampled the data using randomoversampler and smote algorithms and undersample the data with the clustercentroid algorithm. In the remaining models I used a combination approach to over and undersample the data using smoteenn. Finally, I compared two machine learning models that minimize bias, balancedrandomforestclassifier and easyensembleclassifier.

## Results: 

- Naive Random Oversampling results: Our balanced accuracy test it 67%, the precision for the high_risk has a very low positivity at 1% and the recall is 74%
<img width="1382" alt="naive" src="https://user-images.githubusercontent.com/67278193/99189208-2bb20d00-272e-11eb-8616-de6011dece3b.png">

- SMOTE oversampling results: the accuracy score is 66.2%, the precision for the high_risk loans has a low positvity again at 1% and recall is 69% overall
<img width="1286" alt="smote" src="https://user-images.githubusercontent.com/67278193/99189213-2e146700-272e-11eb-87e1-3d7f80ba662a.png">

- Undersampling results: balanced accuracy score is 66.2% overall, the precision is at 99% and the recall is 41%
<img width="1315" alt="undersampling" src="https://user-images.githubusercontent.com/67278193/99189216-31a7ee00-272e-11eb-88d0-de8b0acb1411.png">

- Combination(over and undersampling) results: balanced accuracy score is 54.7% the precision is 99% and the recall is 57% overall
<img width="1355" alt="combination" src="https://user-images.githubusercontent.com/67278193/99189223-34a2de80-272e-11eb-8044-b988f1a57823.png">

- Balanced Random Forest Classifier results: the accuracy score is 77.2% the precision is 99% and the recall is 88%
<img width="1293" alt="random forest" src="https://user-images.githubusercontent.com/67278193/99189228-366ca200-272e-11eb-8f97-78bdacff4a43.png">

- Easy Ensemble AdaBoost Classifier results: the accuracy score is 91.7% the precision is 99% and the recall is 94%
<img width="1353" alt="ensemble" src="https://user-images.githubusercontent.com/67278193/99189232-3a002900-272e-11eb-8077-9695c40fcc83.png">

## Summary: 

In the first four models we undersampled, oversampled and did a combination of both to try and determine which model is best at predicting which loans are the highest risk. The next two models we resampled the data using ensemble classifiers to try and predict which which loans are high or low risk. In our first four models our accuracy score is not as high as the ensemble classifiers and the recall in the oversampling/undersampling/mixed models is low as well. Typically in your models you want a good balance of recall and precision which is why I recommend the ensemble classifiers over the first four models. It appears that the Easy Ensemble had the best balance of all the models because of it's high accuracy score and good balance of precision and recall scores.
