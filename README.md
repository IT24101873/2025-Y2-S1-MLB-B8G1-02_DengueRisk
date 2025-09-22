# 2025-Y2-S1-MLB-B8G1-02_DengueRisk

Project Overview
This project focuses on classifying dengue risk levels in Sri Lankan districts as "High Risk" or "Low Risk" based on weekly dengue cases and weather data. The goal is to predict high-risk weeks for each district to enable proactive mosquito control and healthcare planning, supporting public health surveillance and prevention efforts by hospitals, health authorities, and communities.
Dataset Details

Source/Origin: The dataset is combined from two main sources:

National Dengue Control Unit, Ministry of Health, Sri Lanka: Weekly dengue case reports extracted from PDFs (2022–2025).
Open-Meteo API: Historical weather data for Sri Lankan districts, including parameters like temperature, rainfall, wind speed, sunshine duration, daylight duration, and evapotranspiration.


Format: Ministry data was extracted from PDFs into tabular form; Open-Meteo data was downloaded as CSV files.
Key Statistics:

Type: Tabular (structured).
Size: 4,367 rows covering the period from 2022 to August 8, 2025.
Main Features: District, WeekStartDate, Cases (weekly dengue cases), temperature_mean (°C), temperature_max (°C), temperature_min (°C), precipitation_sum (mm), rain_sum (mm), sunshine_duration (s), daylight_duration (s), wind_speed_10m_max (km/h), et0_fao_evapotranspiration (mm).
Target Variable: Binary classification into "High Risk" (weekly cases ≥ 75th percentile for that district) or "Low Risk" (below the threshold), adjusted for population and baseline differences across districts.


External Datasets: No additional external reference datasets were used.

Group Member Roles
The group consists of 6 members, each responsible for one preprocessing technique as part of the Progress Review I on Data Preprocessing & EDA:

IT24101873 - Jesmeen M.B.A: Handling Missing Data
IT24101952 - Senevirathna U.K.J.: Encoding Categorical Variables
IT24101927 - Liyanage J.L.K.L.: Outlier Removal
IT24101972 - Nethsara K.P.S.: Normalization/Scaling
IT24101829 - Ranasinghe R.P.V.K.: Feature Engineering (Feature Selection and Dimension Reduction)
IT24103815 - Fernando W.P.S.: Data Cleaning (Renaming Columns, Date Conversion, etc.)

How to Run the Code
Prerequisites

Python version: 3.10 or higher.
Key libraries: pandas, numpy, scikit-learn, matplotlib, seaborn (for data manipulation, preprocessing, and visualizations).
Install dependencies: Create a requirements.txt file with the above libraries and run pip install -r requirements.txt.

Steps

Clone the repository: git clone <repository-url>.
Place the raw dataset (DengueRiskCombined_Final.csv) in the data/raw/ folder.
Open the project in Jupyter Notebook or JupyterLab: Navigate to the repository folder and run jupyter notebook or jupyter lab.
Run individual notebooks: Execute IT_Number_Preprocessing_technique.ipynb for each member's contribution.
Run the group pipeline: Execute group_pipeline.ipynb to see the integrated preprocessing flow.
Outputs: EDA visualizations will be saved in results/eda_visualizations/ (as PNG/JPEG), and the final processed dataset in results/outputs/. Logs (if any) in results/logs/.
