# Project Documentation

## Scripts

1. ESUS_AFIB_latest_data_20231213.ipynb (where I defined patient cohort and extracted features accordingly)
2. descriptive_statistics.ipynb (where I made the baseline characteristics table in ESUS-AF google doc page 3-4)
3. external_validation.ipynb (where I validated HAVOC, Brown ESUS-AF, CHA2DS2-VASc, and C2HEST risk scores in our patient cohort)
4. McNemar.ipynb (where I compared performance between two models in a single train/test split)
5. lr_rf.ipynb (logistic regression and random forest model performance evaluation)
6. gb.ipynb (gradient boosting model performance evaluation)
7. "fine-tuning scripts" folder (where I fine-tuned all of the random forest and gradient boosting models)
8. "hyperparameter_tuning_results" folder (where I stored all of the random forest and gradient boosting hyperparameter tuning results)

## Data

1. 510_ESUS_AF_feat.csv
2. billy_updated_PROMOTE_feat_icd3.csv
3. billy_updated_PROMOTE_feat_icd4.csv
4. hypergraph_input_af_icd4.csv
5. hypergraph_input_af_icd3.csv

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


