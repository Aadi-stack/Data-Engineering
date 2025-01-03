# Steps to Examine Data Quality

* Load the Data
* Check for Missing Values
* Inspect Data Types
* Check for Duplicates
* Validate Unique Identifiers
* Identify Outliers
* Ensure Consistency Across Datasets
* Analyze Categorical Values
* Review Date Ranges and Formats

## 1. Patients Dataset

### Issues:

* Missing values in fields like `DEATHDATE, DRIVERS, PASSPORT, PREFIX, SUFFIX, MAIDEN, MARITAL, GENDER and FIPS`.

* Inconsistent formatting in columns like `BIRTHPLACE and ADDRESS`.

* Possible invalid or unrealistic `INCOME or HEALTHCARE_EXPENSES`.

* Duplicate '`0`.

## 2. Encounters Dataset

### Issues:

* Missing values in columns such as` REASONCODE and REASON DESCRIPTION`.

* Date inconsistencies in `START and STOP`.

* Potential duplicate entries for the same encounter.

* `PAYER_COVERAGE and BASE_ENCOUNTER_COST` might contain outliers.

## 3. Medications Dataset

### Issues:

* Missing values in `REASONCODE, REASON DESCRIPTION`.

* Unclear BASE_COST values (e.g., zeros or negative values).

* Duplicate records for the same patient and encounter.

## 4. Symptoms Dataset

### Issues:

* Missing values in SYMPTOMS or AGE_END.

* Inconsistencies in `PATHOLOGY and SYMPTOMS` naming conventions.

* `Outliers in NUM_SYMPTOMS` (e.g., too high to be realistic).

## 5. Conditions Dataset

### Issues:

* Missing or invalid values in Diagnosis or Chronicity.

* Duplicate conditions for the same patient.

* Inconsistent use of medical terminology.

