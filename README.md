# Pre-Published Protocol for the Study: "Association of cataract surgery with cosmetic surgery: A retrospective cohort comparative studyrocedures"

---

## Table of Contents

1. [Introduction](#introduction)
2. [Objectives](#objectives)
3. [Methods](#methods)
   - [Data Source](#data-source)
   - [Dataset Construction and Linkage](#dataset-construction-and-linkage)
   - [Data Fit for Purpose](#data-fit-for-purpose)
   - [Disease and Outcome Definitions](#disease-and-outcome-definitions)
   - [Statistical Analysis](#statistical-analysis)
   - [Ethics and Governance](#ethics-and-governance)
4. [References](#references)

---

## Introduction

Cataract surgery is one of the most commonly performed surgical procedures worldwide, primarily aimed at restoring vision impaired by lens opacity. Improved visual acuity following cataract surgery may influence patients' perceptions of their appearance and could potentially increase the likelihood of undergoing cosmetic procedures. This study aims to investigate the association between cataract surgery and the subsequent uptake of cosmetic surgeries, specifically facial aesthetic and body contouring procedures.

---

## Objectives

- **Primary Objective:**
  - To evaluate whether patients who have undergone cataract surgery are more likely to receive cosmetic surgery compared to those who have not undergone cataract surgery.
  
- **Secondary Objectives:**
  - To classify the types of cosmetic procedures most commonly performed after cataract surgery.
  - To assess the incidence of adverse events following cosmetic surgery in patients with a history of cataract surgery.
  - To explore whether demographic factors such as age and sex modify the association between cataract surgery and subsequent cosmetic procedures.

---

## Methods

### Data Source

The study will utilize data from the **TriNetX US Collaborative Network**, a federated database providing access to de-identified electronic health records (EHRs) from approximately 66 million patients across 116 healthcare organizations (HCOs) in the United States, as of August 2024. The TriNetX platform allows researchers to conduct large-scale retrospective cohort studies by aggregating and harmonizing data from participating HCOs.

### Dataset Construction and Linkage

#### Cohort Selection

Two cohorts will be established:

1. **Cataract with Surgery (CWS) Cohort:**
   - **Inclusion Criteria:**
     - Patients aged **≥18 years**.
     - Diagnosis of cataract identified by **ICD-10-CM codes H25** (Age-related cataract) or **H26** (Other cataract).
     - Underwent cataract extraction surgery, indicated by **ICD-10-CM code Z98.4** (Cataract extraction status).

2. **Cataract No Surgery (CNS) Cohort:**
   - **Inclusion Criteria:**
     - Patients aged **≥18 years**.
     - Diagnosis of cataract identified by **ICD-10-CM codes H25** or **H26**.
     - **No record** of cataract extraction surgery during the study period.

#### Data Linkage and Quality Assurance

- **Linkage Process:**
  - Patient records will be linked across various data domains (demographics, diagnoses, procedures, laboratory measurements, and healthcare utilization) using unique de-identified patient identifiers within the TriNetX platform.
  - The linkage is unidirectional, from patient demographics to clinical outcomes.

- **Handling Missing Data:**
  - Variables with missing data will be assessed for patterns of missingness.
  - If data are missing completely at random, multiple imputation methods will be employed.
  - The proportion of observed data for each variable will be documented.

- **Completeness of Follow-Up:**
  - Follow-up time will be calculated from the date of cataract diagnosis to the date of the first cosmetic procedure, loss to follow-up, or end of the study period (August 2024).
  - Completeness of follow-up will be assessed by calculating the median follow-up time and attrition rates.

### Data Fit for Purpose

#### Data Origin and Clinical Processes

- The TriNetX database compiles EHR data collected during routine clinical care, including inpatient and outpatient encounters.
- The data are originally recorded for clinical management, billing, and administrative purposes.

#### Coding Systems and Data Manipulation

- **Diagnoses:** Coded using the **International Classification of Diseases, Tenth Revision, Clinical Modification (ICD-10-CM)**.
- **Procedures:** Coded using the **Current Procedural Terminology (CPT)** codes and **ICD-10 Procedure Coding System (ICD-10-PCS)**.
- **Laboratory Measurements:** Coded using the **Logical Observation Identifiers Names and Codes (LOINC)** system.

#### Data Quality Assessment

- Data quality will be assessed by examining consistency, completeness, and plausibility of values.
- Outlier detection methods will be used to identify and address improbable values.
- Validation checks will be performed to ensure the accuracy of coded data.

#### Potential Sources of Bias

- **Selection Bias:** Due to the retrospective design and reliance on available EHR data.
- **Information Bias:** Misclassification of exposures or outcomes due to coding errors or omissions.
- **Confounding:** Potential confounders will be addressed through propensity score matching and multivariable analyses.

### Disease and Outcome Definitions

#### Exposures

- **Cataract Diagnosis:**
  - Identified using **ICD-10-CM codes:**
    - **H25:** Age-related cataract.
    - **H26:** Other cataract.

- **Cataract Surgery:**
  - Identified using **ICD-10-CM code: Z98.4** (Cataract extraction status).

#### Outcomes

- **Primary Outcome:**
  - Receipt of **cosmetic surgery**, classified into facial aesthetic procedures and body contouring procedures.

- **Facial Aesthetic Procedures:**
  - **Rhinoplasty:**
    - **CPT codes:**
      - **30400**–**30420** (Surgical repair of nasal deformity).
  - **Blepharoplasty:**
    - **CPT codes:**
      - **15820**–**15823** (Eyelid surgery).
  - **Rhytidectomy:**
    - **CPT code:**
      - **15824**–**15829** (Facelift procedures).

- **Body Contouring Procedures:**
  - **Breast Reconstruction:**
    - **CPT codes:**
      - **19357**–**19369** (Breast reconstruction procedures).
  - **Liposuction:**
    - **CPT codes:**
      - **15876**–**15879** (Suction-assisted lipectomy).

#### Adverse Events

- **Dry Eye Syndrome:**
  - **ICD-10-CM code: H04.12** (Dry eye syndrome).
- **Visual Disturbances and Low Vision:**
  - **ICD-10-CM codes:**
    - **H53** (Visual disturbances).
    - **H54** (Blindness and low vision).
- **Corneal Scars and Opacities:**
  - **ICD-10-CM code: H17** (Corneal scars and opacities).

#### Definitions and Implementation Logic

- Patients will be considered to have undergone a specific procedure if the relevant CPT code is recorded **after** the date of cataract diagnosis or surgery.
- Temporal relationships will be established to ensure proper sequencing of exposures and outcomes.

#### Validation of Coding Schemes

- The coding schemes are based on standardized coding manuals published by the **American Medical Association (AMA)** and the **World Health Organization (WHO)**.
- Clinical experts in ophthalmology and plastic surgery have reviewed the code lists to ensure accuracy and relevance.
- Cross-referencing with prior published studies will be conducted to validate the definitions used.

### Statistical Analysis

#### Software and Tools

- Analyses will be performed using the **TriNetX analytics platform**.
- Additional statistical analyses may be conducted using **R software (version 4.0 or later)**.

#### Descriptive Statistics

- Continuous variables will be summarized using means and standard deviations.
- Categorical variables will be summarized using frequencies and percentages.
- Baseline characteristics will be compared using:
  - **Independent-samples t-tests** for continuous variables.
  - **Chi-square tests** for categorical variables.

#### Propensity Score Matching (PSM)

- **Matching Method:**
  - One-to-one matching using the **greedy nearest neighbor** algorithm without replacement.
- **Covariates for Matching:**
  - **Demographics:** Age, sex, race, ethnicity.
  - **Clinical Factors:** Body Mass Index (BMI).
  - **Socioeconomic Factors:** Extreme poverty, low income, financial insecurity, problems related to housing and economic circumstances.
  - **Employment Status.**
  - **Education and Literacy Problems.**
  - **Homelessness.**
  - **Psychiatric Conditions:** Body dysmorphic disorder (BDD), anxiety disorders.

#### Risk Analysis

- **Relative Risks (RRs):**
  - Calculated for the occurrence of cosmetic procedures in the CWS cohort compared to the CNS cohort.
- **Confidence Intervals:**
  - 95% confidence intervals will be computed for all estimates.
- **Statistical Significance:**
  - A two-sided p-value of **<0.05** will be considered statistically significant.

#### Survival Analysis

- **Kaplan–Meier Survival Analysis:**
  - Used to estimate the cumulative incidence of cosmetic procedures over time.
- **Log-Rank Test:**
  - Employed to compare survival curves between cohorts.
- **Assumption Checks:**
  - Proportional hazards assumption will be tested using Schoenfeld residuals.

#### Analysis of Adverse Events

- A secondary analysis will be conducted within the CWS cohort to compare adverse events between patients who underwent blepharoplasty and those who did not.
- **Multivariable Regression:**
  - Adjusted for potential confounders identified in the propensity score matching.
- **Risk Estimates:**
  - Relative risks and hazard ratios will be calculated for adverse events.

#### Sensitivity Analyses

- Stratified analyses will be performed to assess the effect modification by:
  - **Sex:** Male vs. Female.
  - **Age Groups:** Younger (<65 years) vs. Older (≥65 years).
- Interaction terms will be included in regression models to test for statistical significance.

#### Assumptions and Model Validation

- Model assumptions will be verified through diagnostic plots and statistical tests.
- Model fit will be assessed using measures such as the **Akaike Information Criterion (AIC)**.
- Internal validation will be performed using bootstrapping methods.

#### Generalizability

- The study population is representative of adults with cataract diagnoses in the United States.
- Findings may be generalizable to similar healthcare settings and populations.

### Ethics and Governance

#### Informed Consent and Data Governance

- The study will use de-identified EHR data; therefore, individual informed consent is not required.
- The research will adhere to the **Health Insurance Portability and Accountability Act (HIPAA)** regulations and ethical principles outlined in the **Declaration of Helsinki**.

#### Data Privacy and Protection

- All data accessed will be de-identified in compliance with HIPAA Safe Harbor standards.
- Data storage and analysis will occur within the secure environment of the TriNetX platform, which employs encryption and access controls.

#### Patient and Public Involvement

- Although patients will not be directly involved in the study design or conduct, the research question is informed by clinical observations and prior patient feedback regarding post-cataract surgery experiences.

#### Data Sharing and Transparency

- Due to data use agreements with TriNetX, individual-level data cannot be shared externally.
- Aggregated data and statistical code (where permissible) will be made available upon reasonable request to facilitate transparency and reproducibility.

---

## References

1. **TriNetX:** A global health research network that provides access to EHR data for clinical research.
2. **American Medical Association (AMA):** Publisher of the CPT coding manual.
3. **World Health Organization (WHO):** Publisher of the ICD-10-CM coding manual.
4. **Health Insurance Portability and Accountability Act (HIPAA):** U.S. legislation that provides data privacy and security provisions for safeguarding medical information.
5. **Declaration of Helsinki:** A set of ethical principles for medical research involving human subjects.

---

**Note:** This protocol is intended to provide a comprehensive and transparent plan for the proposed research study, ensuring adherence to high standards of scientific rigor and ethical conduct. All analyses will be conducted as specified, and any deviations from the protocol will be documented and justified in the final research report.
