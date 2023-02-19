# Sampling-Assignment
This repo contains a python notebook which explores various sampling methods and test them on different classification models to determine which sampling works better for given imbalanced dataset.
As the given dataset is imbalanced, two sampling methods have been used to overcome this i.e. undersampling majority class and oversampling minority class.

---
## Sampling Techniques

The sampling techniques used for the data are :

### 1. Under Sampling
This reduces the majority class to be of equal count as the minority class. E.g. in the given dataset the minority class has 9 records so the majority class is sampled to have only 9 records also.

### 2. Over Sampling

This increases the number of records of minority class to match majority class occurances. In other words the minority class is continously sampled with replacement to make its occurances equal to majority class.

This results in replication of records.

### 3. Simple Random Sampling

This is the most simple sampling method. Size of the sample has been calculated using the formula for the given population size. The data is randomly selected from the dataset without replacement. The minority class may be selected, may not be.

### 4. Disproportionate Stratified Sampling

The sample obtained as a result of this stratified sampling method doesn't represent the population in its distribution. This is used to sample equal number of samples from each class. It is different from undersampling as here the number of samples from each class can be different from minumim number of occurances of any class. 

E.g. In the code we have choosen 7 samples from each class but undersampling keeps samples to maximum number of minority class occurance i.e. 9 here.

### 5. Proportionate Stratified Sampling

The sample obtained from this method represents population in its distribution. Minority class is in minority in samples also.

---

### Classification Models

Models used for this data:

1. Logistic Regression
2. Naive Bayes Classifier
3. KNearest Neighbors Classifier
4. Support Vector Machine
5. Decision Tree Classifier

The models were trained on the samples and then their performance was evaluated using test data which was sampled from data such that it contains atleast 2 records from minority class for purpose of testing.

---

### Result

OverSampling Performed best overall for all the models.

Simple Random Sampling and Proportionate Stratified Sampling also performed well.

Mean Score of the accuracy of models for the samples is:

UnderSample | OverSample | SimpleSample | DispropStratSample | PropStratSample
--- | --- | --- | --- | ---
0.620 | 0.953 | 0.933 | 0.640 | 0.920

### KNN Classifier gave the best overall score for all samples with mean accuracy score of 0.94 which is better than most of the rest as some gave 1.0 accuracy for some samples but not for all.

#### Note:

I've taken mean of score as all were of the same scale and all have to be maximised.
