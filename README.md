# Healthcare Data Pipeline

This repository implements a healthcare data pipeline that processes and analyzes datasets related to patient demographics, symptoms, medications, and encounters. The pipeline cleans, structures, and analyzes the data to provide insights into patient information, medication trends, and symptom analysis. The project also includes a series of data transformations and analysis steps to ensure high-quality, actionable data.


# Project Structure


```markdown
healthcare_data_pipeline/
│
├── data/                        # Raw datasets, including links or examples
│   ├── patients_data.csv
│   ├── encounters_data.csv
│   ├── symptoms_data.csv
│   ├── medications_data.csv
│   ├── conditions_data.csv
│   └── gender_data.csv          # If bonus dataset is used
│
├── src/                         # Main pipeline and code
│   ├── __init__.py
│   ├── connect.py               # Logic for connecting to datasets
│   ├── clean.py                 # Data cleaning functions
│   ├── structure.py             # Data structure and standardization
│   ├── merge.py                 # Logic for merging datasets
│   ├── analysis.py              # Code for Data Analysis tasks
│   └── visualize.py             # Code for visualizations (graphs, charts)
│
├── notebooks/                   # Jupyter notebooks for exploration
│   └── data_assessment.ipynb     # Data Assessment notebook
│
├── tests/                       # Unit tests for pipeline code
│   ├── test_clean.py
│   ├── test_merge.py
│   ├── test_analysis.py
│   └── test_visualizations.py
│
├── requirements.txt             # Python dependencies
├── pipeline.py                  # Script to run the pipeline end-to-end
├── README.md                    # Project documentation and instructions
└── LICENSE                      # License file (optional)

# Project Overview

This project focuses on healthcare data management, with a focus on patient demographic information, medication records, symptoms, and other clinical data. The pipeline is designed to:

Ingest data from multiple sources such as CSV and Parquet files.
Clean the data by addressing missing values, fixing data quality issues, and standardizing formats.
Structure the data into standardized columns as per the Tuva Data Model Input Layer.
Analyze the data to uncover insights, such as medication trends, racial distribution of patients, and symptom severity.
Merge datasets to create a master table for reporting and further analysis.
The main tasks in this pipeline include:

Data Cleaning: Removing duplicates, fixing inconsistencies, and handling missing data.
Data Structuring: Mapping raw data to a standardized format based on the Tuva Data Model.
Analysis: Analyzing patient demographics, medication trends, and symptoms over time.



# Requirements
* Python 3.10
 
## Required libraries:
* pandas
* matplotlib
* seaborn
* kedro (for pipelining)
* numpy
* great_expectations (for data validation)
* pytest (for testing)
* dbt (for database transformation, if Tuva model is applied)


# Install dependencies with the following command:

'''bash
pip install -r requirements.txt
'''



Dataset Description
Patients Dataset: Contains patient information including ID, age, gender, and race.
Encounters Dataset: Contains details about each medical encounter including date and associated patient ID.
Symptoms Dataset: Captures patient symptoms with categories and severity.
Medications Dataset: Lists prescribed medications for patients including drug, dosage, and date.
Conditions Dataset: Information about diagnosed conditions including patient ID and diagnosis.
Bonus Dataset (Gender): A separate dataset to update missing gender information.



How to Run the Pipeline
Step 1: Prepare the datasets. Place the datasets in the data/ directory. Ensure that the file names match the ones in the structure.
Step 2: Install dependencies by running:
bash
Copy code
pip install -r requirements.txt
Step 3: Run the pipeline. This will load, clean, structure, and analyze the data.
Using Kedro:
bash
Copy code
kedro run
This will execute all steps of the pipeline from data loading to analysis.
Pipeline Steps
Connect:

Load all datasets into the pipeline.
Bonus: Load data into a free database if required.
Clean:

Handle missing values, duplicates, and any data quality issues.
Standardize column names and correct data formats.
Structure:

Standardize column names according to the Tuva Data Model.
Extract individual symptoms from the Symptoms column.
Merge:

Merge all datasets into a single "master table" for analysis.
Analysis:

Conduct data analysis as specified in the Data Analysis task.
Generate visualizations like pie charts and time-series plots.
Running Tests
To ensure the code works as expected, run the unit tests using pytest:

bash
Copy code
pytest tests/
Project Outcomes
Data Assessment: Overview of data quality issues found across datasets.
Data Analysis:
Number of distinct patients.
Medication trends over time.
Pie charts of patient distributions by race and gender.
Percentage of patients with all symptoms ≥ 30.


