# Project Documentation

## Scripts

* ESUS_AFIB_latest_data_20231213.ipynb (where I defined patient cohort and extracted features accordingly)
* descriptive_statistics.ipynb (where I made the baseline characteristics table in ESUS-AF google doc page 3-4)
* external_validation.ipynb (where I validated HAVOC, Brown ESUS-AF, CHA2DS2-VASc, and C2HEST risk scores in our patient cohort)
* McNemar.ipynb (where I compared performance between two models in a single train/test split)
* lr_rf.ipynb (logistic regression and random forest model performance evaluation)
* gb.ipynb (gradient boosting model performance evaluation)
* "fine-tuning scripts" folder (where I fine-tuned all of the random forest and gradient boosting models)
* cleaned_PROMOTE_Yuzhang.ipynb (where I put together ICD and prescribed med dummy data for PROMOTE in order for Yuzhang to conduct transfer learning)
* ESUS_AFIB_embedding_generation.ipynb (where I put together ICD and prescribed med dummy data for ESUS-AF in order to for Yuzhang to generate embedding vectors)

## Data

* 510_ESUS_AF_feat.csv
* billy_updated_PROMOTE_feat_icd3.csv
* billy_updated_PROMOTE_feat_icd4.csv
* hypergraph_input_af_icd4.csv
* hypergraph_input_af_icd3.csv
* "embeddings_20240520" folder
*  "hyperparameter_tuning_results" folder (where I stored all of the random forest and gradient boosting hyperparameter tuning results)

## Feature Extraction

### patient cohort definition

* “dr_nahab” folder
* "DELTA" folder
* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_DX_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_DX_20231213.csv

Key Notes in Data Cleaning
* Chart reviews of encounter type (TEC Visit, Inpatient, etc.) and diagnosis scope (billing diagnosis, discharge diagnosis, etc.) is important in deciding what filtering criteria to use.
* Always confirm the ICD codes associated with the specific disease you are referring to, here is the website I find to accurately understand each ICD10 code: https://www.icd10data.com/.
* We can also compare our exlcusion criteria to existing literatures similar to our project. I found problems in our previous patient cohort after reading this literature: https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6891883/. Then I followed their practice in setting a 5-year pre-observation period and corerected our stroke-related ICD codes.

Other Key Notes
* Communicate with Dr. Nahab and Rob regarding how to expand our existing ESUS patient cohort efficiently.

### demographics (race, ethnicity, gender, age)

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_DEMO_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_EPIC_DEMO_20231213.csv

Key Notes in Data Cleaning
* According to US Census Bureau, ethnicity has two categories: Hispanic or Latino and Not Hispanic or Latino.
* According to US Census Bureau, race has six categories: White, Black or African American, American Indian or Alaska Native, Asian, Native Hawaiian or Other Pacific Islander, and More Than One Race.

### ICD comorbidities

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_DX_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_DX_20231213.csv

Key Notes in Data Cleaning
* Always convert orginal, raw ICD codes to a standard format. I recommend the ICD-Mappings API: https://github.com/snovaisg/ICD-Mappings.
* Always confirm the ICD codes associated with the specific disease you are referring to, here is the website I find to accurately understand each ICD10 code: https://www.icd10data.com/.

### prescribed med

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_PRESCR_MED_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_Prescr_Meds_20231213.csv

Key Notes in Data Cleaning
* The difference in prescribed med data record between CDW and EPIC is huge. It was difficult for me to find a method to standardize them.
* The current approach I employed is to take into consideration those drugs with only one main ingredient.

Other Key Notes
* I have tried but failed the RxNorm API by standardizing both CDW and EPIC prescribed med to a medical ID based on the drug ingredient, dosage, etc. The wesbite of this API is: https://lhncbc.nlm.nih.gov/RxNav/APIs/api-RxNorm.findRxcuiById.html. The problem is that the medical ID is different given very minor difference between two prescribed med names, whether the difference is caused by inaccurate data records, manufacture companies, dosages, etc.
* Hence this problem is yet to be completely solved, even though I have found my current approach to be fairly robust (there is low noise in data outcome) and complete (there is few data missing in the process of excluding drugs with more than one main ingredients).

### ECHO

### ECG

### labs

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_LABS_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_Labs_20231213.csv

### other common risk factors (height, weight, smoking, obesity)

* Latest_data_Billy_20231213/CDW_Output/DS3465_CDW_Flowsheet_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_Flowsheet_20231213.csv
* Latest_data_Billy_20231213/Epic_Caboodle_Output/DS3465_Epic_Smoking_History_20240402.csv

