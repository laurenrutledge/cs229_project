Predicting Female Swimmers' Specialization with Machine Learning

Overview: 

This project investigates whether machine learning can predict a female swimmer’s specialization before the age of 18 using historical race data from USA Swimming. By leveraging exploratory data analysis (EDA), ARIMA time-series forecasting, and multi-output regression, this study explores patterns in youth swim performance to determine optimal stroke specialization.


Repository Structure: 
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


