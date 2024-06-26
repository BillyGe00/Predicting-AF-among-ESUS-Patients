# Stage One (abstract submission)

* we have 468 patients up until March, 2023
* exclusion criteria (1. patients with afib prior to index stroke; 2. patients with no follow-up hospital visits after index stroke)
* we extracted features including demographic data (age and gender), medical comorbidities (history of hypertension, history of heart failure, history of diabetes, etc.), lab records (cholesterol, hemoglobin, glucose, red and white blood cell count, etc.), radiographic reports (electrocardiogram and echocardiogram), and other common risk factors (smoking and obesity)
* we performed external validation of HAVOC and Brown ESUS-AF risk scores
* we built machine learning tree-based models including random forest classifier, extremely randomized trees classifier, gradient boosting classifier, and histogram gradient boosting classifier

# Stage Two

* we have 510 patients up until December, 2023
* study period: from 2010-01-01 to 2023-12-13 (earliest and latest index stroke event is 2015-11-01 and 2023-08-25; earliest and latest afib event is 2016-09-22 and 2023-11-14) 
* exclusion criteria (1. patients with afib prior to index stroke; 2. patients with other stroke history within five years prior to index stroke identified in the study period)
* we extracted features including demographic data (age, gender), physical characteristics (height, weight), lab records (cholesterol, hemoglobin, glucose, red and white blood cell count, etc.), radiographic reports (electrocardiogram and echocardiogram), and other common risk factors (obesity, smoking)
* we also extracted medical comorbidities features (history of hypertension, diabetes, congestive heart failure, etc.) to build baseline ML models without embedding vector
* we extracted dummy variables from medical comorbidities history (990, 2742) and prescribed medicines history (365) (different from stage one)
* we converted those dummy variables into dimension = 32 or 64 embedding vector via unsupervised deepwalk and autoencoder methods
* we converted those dummy variables into dimension = 32 or 64 embedding vector via supervised hypergraph model (pre-trained on a larger PSCI patient cohort and transfer learning + fine-tuning to/on this AF project)
* we performed external validation of HAVOC, Brown ESUS-AF, CHA2DS2-VASc, and C2HEST risk scores (similar to stage one)
* we plan to build machine learning tree-based models (similar to stage one)

# Progress Update

* we are currently in stage two
* feature extraction is complete
* external validation is complete
* modeling is in progress
