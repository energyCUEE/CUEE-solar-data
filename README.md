# CUEE Solar Data  

## 📌 Overview  
This repository contains preprocessed solar energy and weather-related datasets. The raw data is collected from various sources, solar meters, weather forecasting models, and satellite images. Below is a detailed explanation of both raw and processed data, including all column names.  

[📄 View Plot (PDF)](https://github.com/energyCUEE/CUEE-solar-data/master/graph/timeseries_CI.pdf)

## 🔄 Data Processing Steps

The raw data has been processed into **1-minute, 5-minute, 15-minute, and daily** samples. The preprocessing steps include: 

1. **Data Cleaning**:  
   - Removed missing values, incorrect timestamps, and duplicate records.  
   - Standardized timestamp formats.  

2. **Data Resampling**:  
   - Adjusted time intervals to **1-min, 5-min, 15-min, and daily** formats.  
   - Ensured consistency across datasets.  

3. **Feature Engineering**:  
   - Calculated new features (e.g., efficiency solar, imputed data).


## 📂 Preprocessed Data  

This folder contains cleaned and structured datasets with different time resolutions. Each dataset has been resampled to ensure consistency.  

### Folder Contents:  

- **`data_Cloudindex_5minresample/`** → Cloud index data, resampled every **5 minutes**.  
- **`data_Irradiance_1minresample/`** → Solar irradiance data, resampled every **1 minute**.  
- **`data_NWP_15minresample/`** → Numerical Weather Prediction (NWP) data, resampled every **15 minutes**.  
- **`data_PV_5minresample/`** → Solar PV power generation data, resampled every **5 minutes**.  
- **`data_Temperature_15minresample/`** → Temperature data, resampled every **15 minutes**.  
- **`... (other datasets)`** → Additional preprocessed datasets following the same structure.  

Each file inside this folder represents a cleaned and structured version of the raw data, with resampled time intervals

## 📂 Processed Data  

This folder contains the **final datasets**, created by merging and concatenating all **preprocessed data** from **2023-2024**. These datasets are structured and ready for analysis or modeling.  

### 🔄 Processing Steps:  

1. **Merged Data** → Combined all preprocessed datasets from **2023-2024**.  
2. **Concatenation** → Unified different time intervals into a single structured dataset.  
3. **Final Formatting** → Ensured consistent column names, time alignment, and missing value handling.

### Folder Contents:  


## ✅ Conclusion  
This dataset has been carefully cleaned and processed to ensure accuracy and reliability. It is now ready for further analysis, modeling, and forecasting applications.


   
