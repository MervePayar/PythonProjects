# Somatus Machine Learning Challenge: Predicting Acute Kidney Injury

## Purpose

The purpose of this challenge is for you to demonstrate your ability to frame and solve a problem using your skills as a Machine Learning Engineer.

**Your submission for this exercise will not be evaluated on the complexity of the model that you choose or the performance of the model that you train.** We are interested in learning how you think about the problem and apply and evaluate a model more than your ability to implement a specific model type or optimize a specific performance metric.

## Task Details

### Summary

In this challenge, you will build a model to predict the occurrence of a hospitalization related to Acute Kidney Injury.

"Acute kidney injury (AKI), also known as acute renal failure (ARF), is a sudden episode of kidney failure or kidney damage that happens within a few hours or a few days. AKI causes a build-up of waste products in your blood and makes it hard for your kidneys to keep the right balance of fluid in your body. AKI can also affect other organs such as the brain, heart, and lungs. Acute kidney injury is common in patients who are in the hospital, in intensive care units, and especially in older adults."

*Source: https://www.kidney.org/atoz/content/AcuteKidneyInjury*

### Submission

Your submission for this challenge should include your Python code and any other artifacts that you feel are relevant for showing your work. Notebooks are acceptable if you wish to use them.

Where applicable, including the following items in your submission will help us to understand and assess your work:

* Description of selected modeling approach and any assumptions you made
* Notes on important data or feature-related decisions you made
* Clear, documented, and well-formatted code
* Any specific instructions needed to execute your code

## Data

### Source

The datasets for this challenge are publicly available datasets from the Centers for Medicare and Medicaid Services and contain synthesized claims data for Medicare members.

*Source: https://www.cms.gov/Research-Statistics-Data-and-Systems/Downloadable-Public-Use-Files/SynPUFs/DE_Syn_PUF*

### Data Model and Dictionaries

Attached you will find two files:

* **176541_DE1_0_2008_Beneficiary_Summary_File_Sample_1.csv**: contains data for Medicare insurance beneficiaries
* **176549_DE1_0_2008_to_2010_Inpatient_Claims_Sample_1.csv**: contains data for inpatient hospital claims submitted to Medicare for beneficiaries

These files can be joined together using the Beneficiary Code field ("DESYNPUF_ID").

For more detailed information on these files, including data dictionaries and other reference material, see pages 9 through 11 of Section 4 ("Summary of Variables of the CMS Linkable 2008–2010 Medicare DE-SynPUF") in the attached PDF document called "SynPUF_DUG."

You can also visit the link found in the "Source" section above for more reference material.

### Labels

A label for an AKI hospitalization can be constructed by examining the diagnoses associated with an inpatient hospital claim. For the purposes of this exercise, these diagnoses are encoded using the ICD-9-CM coding system.

The ICD-9 codes associated with a particular inpatient hospital claim can be found in the following fields:

* ADMTNG_ICD9_DGNS_CD
* ICD9_DGNS_CD_1
* ICD9_DGNS_CD_2
* ICD9_DGNS_CD_3
* ICD9_DGNS_CD_4
* ICD9_DGNS_CD_5
* ICD9_DGNS_CD_6
* ICD9_DGNS_CD_7
* ICD9_DGNS_CD_8
* ICD9_DGNS_CD_9
* ICD9_DGNS_CD_10

The following five ICD-9 code values are used to specify Acute Kidney Injury:

* **584.5**: Acute kidney failure with lesion of tubular necrosis
* **584.6**: Acute kidney failure with lesion of renal cortical necrosis
* **584.7**: Acute kidney failure with lesion of renal medullary [papillary] necrosis
* **584.8**: Acute kidney failure with other specified pathological lesion in kidney
* **584.9**: Acute kidney failure, unspecified

*Source: http://www.icd9data.com/2014/Volume1/580-629/580-589/584/default.htm*
