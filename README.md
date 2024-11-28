# Healthcare Data Pipeline

This repository implements a healthcare data pipeline that processes and analyzes datasets related to patient demographics, symptoms, medications, and encounters. The pipeline cleans, structures, and analyzes the data to provide insights into patient information, medication trends, and symptom analysis. The project also includes a series of data transformations and analysis steps to ensure high-quality, actionable data.


# Project Structure

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


# Installation

To run the pipeline, clone this repository and install the necessary dependencies:


git clone https://github.com/Aadi-stack/Data-Engineering.git

cd healthcare_pipeline

pip install -r requirements.txt

