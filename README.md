# Evaluation of various machine learning methods on lithological facies prediction for reservoir characterization

## Introduction
Three machine learning methods are applied to evaluate the accuracy on lithological facies classification and prediction for reservoir characterization. The public well logging dataset provided by [SEG](http://www.seg.org) are used in this project. The training dataset have ten wells with a set of nine variables as the predictors and one variable rock facies as the outcome. The validation dataset consist two wells that have the same predictors as the training dataset.

## Model Training
Three supervised learning models ([K-Nearest Neighbors (KNN)](knn.ipynb), [Support Vector Machine (SVM)](svm.ipynb), and [Random Forest (RF)](kfc.ipynb)) are to be trained on data to perform the facies classification. First, the data preparation step includes reading raw data from disk, QC, cleanning up missing data and creating the clean dataset for use. There are 917 missing values in PE variable. Those incomplete data can be either removed from the training data or filled by training a regressor to imputate those missing values. The first option is used in this project. Second, the training data and blind test data from the clean dataset are created and conditioned. Next, the training data are split into training and test set, and the learning models are trained and optimized by using cross validation. Finally, the trained models are applied to validation dataset to predict lithological facies in two wells that do not have outcome lables.

<p align="center">
 <img src="https://user-images.githubusercontent.com/110936252/184397187-ce785945-eb01-4905-a10d-e7f45325363d.png" alt="Figure 1" width="700"/>
</p>

## Model Evaluation


![fig3](https://user-images.githubusercontent.com/110936252/184400741-f619029a-b752-483c-affe-ada6a642d0b0.png)
![fig4](https://user-images.githubusercontent.com/110936252/184400755-3dbd2cc9-e9b6-4c68-b911-0127fe30c362.png)
