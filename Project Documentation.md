# Project Documentation

## Scripts

* ESUS_AFIB_latest_data_20231213.ipynb (where I defined patient cohort and extracted features accordingly)
* descriptive_statistics.ipynb (where I made the baseline characteristics table in ESUS-AF google doc page 3-4)
* external_validation.ipynb (where I validated HAVOC, Brown ESUS-AF, CHA2DS2-VASc, and C2HEST risk scores in our patient cohort)
* McNemar.ipynb (where I compared performance between two models in a single train/test split)
* lr_rf.ipynb (logistic regression and random forest model performance evaluation)
* gb.ipynb (gradient boosting model performance evaluation)
* "fine-tuning scripts" folder (where I fine-tuned all of the random forest and gradient boosting models)
* "hyperparameter_tuning_results" folder (where I stored all of the random forest and gradient boosting hyperparameter tuning results)

## Data

* 510_ESUS_AF_feat.csv
* billy_updated_PROMOTE_feat_icd3.csv
* billy_updated_PROMOTE_feat_icd4.csv
* hypergraph_input_af_icd4.csv
* hypergraph_input_af_icd3.csv

## Feature Extraction

### patient cohort definition

### demographics (race, ethnicity, gender, age)

### ICD

### prescribed med

### ECHO

### ECG

### labs

### physical characteristics (height, weight)

### other common risk factors (smoking, obesity)


