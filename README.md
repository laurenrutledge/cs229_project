# Predicting Female Swimmers' Specialization with Machine Learning

## Overview: 
This project investigates whether machine learning can predict a female swimmer’s specialization before the age of 18 using historical race data from USA Swimming. By leveraging exploratory data analysis (EDA), ARIMA time-series forecasting, and multi-output regression, this study explores patterns in youth swim performance to determine optimal stroke specialization.

-----

## Repository Structure: 
```plaintext
pythonProject/
│── arima/                                            # Directory containing ARIMA modeling for swim time prediction
│   ├── swim_analysis_results/                        # Results of ARIMA analysis seen in report
│   ├── arima_for_all_events.ipynb
│   ├── calculate_mean_time_per_event_specialized_vs_non_specialized.ipynb  # Notebook used to produce results for ARIMA analysis
│
│── drafts/                                           # Drafts and experimental code, not included in report 
│   ├── datasets/                                     # Raw data files and drafts of processed data samples 
│   ├── multi_output_regression/                      # Work-in-progress regression models, not included in the final report 
│
│── eda_mean_time_per_swim_event_vs_age_of_swimmer/   # Directory containing scripts used for eda analyses
│
│── feature_engineering/                              # Directory containing feature engineering scripts and processed datasets used in final report
│   ├── adding_features_to_dataset.ipynb              # Script to incorporate feature engineering in final report
│   ├── processed_swim_features.csv                   # dataset used for multi-output-regression that incorporates feature engineering results, used in final report
│
│── multi_output_regression/                          # Directory containing the machine learning model for multi-output regression
│   ├── multi_output_regression.ipynb                 # Directory containing the machine learning model for multi-output regression, v0
│   ├── multi_output_regression_v1.ipynb              # Directory containing the machine learning model for multi-output regression, v1
│   ├── multi_output_regression_v2.ipynb              # Directory containing the machine learning model for multi-output regression, v2 - this version was used in final report
│   ├── predictions_vs_actual_specialties.csv         # csv containing results from implementing multi-output-regression, used in final report
│
│── usaa_swim_data/                                   # Directory containing cleaned dataset files, all used ihn final report 
│── .gitignore                                        # Files to exclude from Git
│── data_cleanup.ipynb                                # Script used to clean up original dataset. results are found in usaa_swim_data directory that are used in final report
│── README.md                                         # Project documentation

```

---

## Methodology:
### Data Preprocessing: 
- Used USA Swimming records to filter and clean historical race data
- Removed non-relevant metadata to focus on performance-based attributes
- Converted swim times into a numerical scoring system based on USA Swimming time standards

### Exploratory Data Analysis (EDA):
- Visualized performance progression across different strokes and distances
- Analyzed variability and specialization trends in youth swim times

### Predictive Modeling:
- Baseline Model: ARIMA for time-series forecasting of swim times
- Machine Learning Model: Multi-output regression to predict event specialization

---

## Key Findings:
- ARIMA provides a reasonable statistical baseline but struggles with sprint events
- Multi-output regression improves predictive accuracy for short- and mid-distance races
- Long-distance events show more variability, requiring additional feature engineering

___

## How to Run the Code to Replicate Project 

### 1. Set Up the Environment
- First, activate the Conda environment and install the required dependencies:

```sh
conda create --name cs229_project_env python=3.10
conda activate cs229_project_env
pip install -r requirements.txt
```

### 2. Obtain the Data
- Ensure you have the cleaned dataset ready:
- Use swimmers_cleaned.csv located in the usaa_swim_data/ directory

### 3. Run Feature Engineering
- Execute the feature engineering script to generate additional features:
```sh
jupyter notebook feature_engineering/adding_features_to_dataset.ipynb
```
### 4. Run Exploratory Data Analysis (EDA)
- To analyze swim event performance as a function of age, run: 
```sh
jupyter notebook eda_mean_time_per_swim_event_vs_age_of_swimmer/calculating_mean_time_per_swim_event_as_function_of_age.ipynb
```
### 5. Run ARIMA Model
- To compute ARIMA-based predictions for event specialization, execute:
```sh
jupyter notebook arima/calculate_mean_time_per_event_specialized_vs_non_specialized.ipynb
```
### 6. Run Multi-Output Regression
- To train and evaluate the multi-output regression model:
```sh
jupyter notebook multi_output_regression/multi_output_regression_v2.ipynb
```




