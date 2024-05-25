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
* cleaned_PROMOTE_Yuzhang.ipynb (where I put together ICD and prescribed med dummy data for PROMOTE in order for Yuzhang to conduct transfer learning)
* ESUS_AFIB_embedding_generation.ipynb (where I put together ICD and prescribed med dummy data for ESUS-AF in order to for Yuzhang to generate embedding vectors)

## Data

* 510_ESUS_AF_feat.csv
* billy_updated_PROMOTE_feat_icd3.csv
* billy_updated_PROMOTE_feat_icd4.csv
* hypergraph_input_af_icd4.csv
* hypergraph_input_af_icd3.csv
* "embeddings_20240520" folder

## Feature Extraction

### patient cohort definition

* “dr_nahab” folder
* "DELTA" folder
* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_DX_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_DX_20231213.csv

### demographics (race, ethnicity, gender, age)

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_DEMO_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_EPIC_DEMO_20231213.csv

### ICD

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_DX_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_DX_20231213.csv

### prescribed med

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_PRESCR_MED_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_Prescr_Meds_20231213.csv

### ECHO

### ECG

### labs

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_LABS_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_Labs_20231213.csv

### other common risk factors (height, weight, smoking, obesity)

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_Flowsheet_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_Flowsheet_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_Smoking_History_20240402.csv

