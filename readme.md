Dementia Model Validation Study
=============
<img src="https://img.shields.io/badge/Study%20Status-Design%20Finalized-brightgreen.svg" alt="Study Status: Design Finalized">

- Analytics use case(s): **Patient-Level Prediction**
- Study type: **Clinical Application**
- Tags: **EHDEN, OHDSI**
- Study lead: **Henrik John**
- Study lead forums tag: **[EHDEN:lhjohn](https://forum.ehden.eu/u/lhjohn), [ODSI:lhjohn](https://forums.ohdsi.org/u/lhjohn)**
- Study start date: **2020-10-01**
- Study end date: **2021-03-31**
- Protocol: **[mi-erasmusmc/EmcDementiaModelValidation](https://github.com/mi-erasmusmc/EmcDementiaModelValidation)**
- Publications: **Coming Soon**
- Results explorer: **Coming Soon**

This study externally validates three existing dementia prediction models that are proposed in clinical prediction model literature. We will assess the models’ performance in real-world settings and discuss the quality of model reporting.

The three clinical prediction models (CPMs) that will be examined are Walters’ Dementia Risk Score, Mehta’s RxDx-Dementia Risk Index and Nori’s ADRD dementia prediction model. Walters predicts 5-year risk of first recorded dementia diagnosis among patients aged 60–79 using a cox proportional hazard model. Mehta predicts risk of incident dementia among patients diagnosed with type 2 diabetes mellitus and hypertension using a cox proportional hazard model. Nori predicts Alzheimer’s disease and related dementias (ADRD) among patients aged 45 and older using a logistic regression model.

We will conduct the study using data from observational databases across the European Health Data & Evidence Network (EHDEN) and the Observational Health Data Sciences and Informatics (OHDSI) network and perform analyses using the OHDSI Patient Level Prediction (PLP) package framework.

Instructions To Install and Run Package From Github
===================

- Make sure you have PatientLevelPrediction installed (this requires having Java and the OHDSI FeatureExtraction R package installed):

```r
  # get the latest PatientLevelPrediction
  install.packages("devtools")
  devtools::install_github("OHDSI/PatientLevelPrediction", ref = 'development')
  # check the package
  PatientLevelPrediction::checkPlpInstallation()
```

- Download the study package through your shell. Note, this repository includes the replicated models as submodules. Submodules need to be initialised and updated, before they can be build and executed.
```shell
  git clone https://github.com/mi-erasmusmc/EmcDementiaModelValidation.git
  git submodule init
  git submodule update
```
- The three analyses can now be found in the subfolders of the cloned repository. Execute each of the three analyses by running the code in (extras/CodeToRun.R). Refer to their individual readme files for more information.

- **Alternative approach:** If you have problems getting the submodules to work, you can also directly download the study packages of the three analyses as follows

```
git clone https://github.com/mi-erasmusmc/EmcWaltersDementiaModel.git
git clone https://github.com/mi-erasmusmc/EmcMehtaDementiaModel.git
git clone https://github.com/mi-erasmusmc/EmcNoriDementiaModel.git
```
