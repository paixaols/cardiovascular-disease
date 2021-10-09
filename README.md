# Cardiovascular disease detection

Dataset from kaggle:

https://www.kaggle.com/sulianova/cardiovascular-disease-dataset

# 1. The problem
Predict whether a person has cardiovascular disease (CVD) based on health and lifestyle conditions. The dataset contains objective information (gender, age, height, and weight), examination results (blood pressure, glucose and cholesterol levels), and information provided by the patient (smoking, alcohol intake, and physical activity).

# 2. Solution strategy
**1 Data description:** prepare dataset to perform subsequent analysis, eg, convert data types.

**2 Feature engineering:** derive new attributes based on the original data to better describe the phenomenon to be modeled.

**3 Data filtering:** filter data that may not be relevant or available during production.

**4 Exploratory data analysis:** explore the data to gain insights that may be relevant later during machine learning modeling.

**5 Data preparation:** prepare the data to apply machine learning models.

**6 Feature selection:** select the most relevant features for training the model.

**7 Machine learning modeling:** train machine learning models.

**8 Hyperparameter fine tuning:** fine tune the model parameters.

**9 Understand model performance:** characterize the model performance with statistical metrics.

# 3. Top 3 data insights
**Hypothesis 1:** smoking increases the chance of developing CVD.

**False.** Occurrence of CVD is higher among non smoking people.

**hypothesis 2:** alcohol intake increases the chance of developing CVD.

**False.** Occurrence of CVD is slightly lower among people who consume alcohol.

**hypothesis 3:** physical activity reduces the chance of developing CVD.

**True.** Active people have lower, however slight, chance of developing CVD.

# 4. Machine learning model applied
Tests were performed using logistic Regression, Random Forest Classifier, CatBoost Classifier, and XGBoost Classifier.

# 5. ML performance
CatBoost Classifier and XGBoost Classifier presented equivalent performance, XGBoost Classifier was chosen due to its lower execution time.

## Performance metrics
Below are the metrics found after 10-fold cross-validation.

| Accuracy  | Precision | Recall    | f1-score  | ROC-AUC      |
| --------- | --------- | --------- | --------- | ------------ |
| 73% +- 1% | 76% +- 1% | 65% +- 1% | 70% +- 1% | 0.72 +- 0.01 |

## Test dataset
Running the final model with the test dataset yielded the following metrics:

| Accuracy | Precision | Recall | f1-score | ROC-AUC |
| -------- | --------- | ------ | -------- | ------- |
| 72%      | 76%       | 65%    | 70%      | 0.72    |

| Diagnosis      | Occurrence |
| -------------- | ---------- |
| True           | 72%        |
| False negative | 18%        |
| False positive | 10%        |
