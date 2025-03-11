# CUEE Solar Data  

## 📌 Overview  
This repository contains preprocessed solar energy and weather-related datasets. The raw data is collected from various sources, solar meters, weather forecasting models, and satellite images. Below is a detailed explanation of both raw and processed data, including all column names.  

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


## 📂 Raw Data  

### ☀ **Solar Data (`raw_PV`)**  
- **Source**: CUBEMS Solar Meter (8 kWp meter)
- **Sampling Rate**: 670 ms  
- **Missing Data**: April 4-5, 2023 
- **Columns**:  

  | Column Name | Description | Unit |  
  |-------------|------------|------|  
  | `Time(s)`   | Timestamp  | Seconds |  
  | `Ia, Ib, Ic, Iavg` | Phase currents | A |  
  | `Pa, Pb, Pc, Ptot` | Active power | W |  
  | `VAa, VAb, VAc, VAtot` | Apparent power | VA |  


### ⚡ **Solar EE Data (`raw_EE_Station1`)**  
- **Source**: CUEE Platform (8 kWp Solar Meter)  
- **Sampling Rate**: 1 min  
- **Columns**:  

  | Column Name | Description | Unit |  
  |-------------|------------|------|  
  | `Datetime`  | Timestamp  | UTC |  
  | `Generated power_28` | Generated power | kW |  
  | `Ambient temperature_29` | Temperature | °C |  
  | `Irradiance_30` | Solar irradiance | W/m² |  
  | `Relative humidity_31` | Humidity | % |  
  | `PySolar Irradiance_121` | Modeled irradiance | W/m² |  
  | `PySolar Azimuth angle_122` | Sun azimuth angle | ° |  
  | `NCEP Ambient temperature_123` | Forecast temperature | °C |  
  | `PVwatts Diffuse irradiance_128` | Diffuse radiation | W/m² |  
  | `NCEP Short-wave irradiance_126` | Short-wave radiation | W/m² |  
  | `PVwatts AC system output_134` | AC power output | W |  
  | `PVwatts Cell temperature_133` | PV cell temperature | °C |  
  | `PVwatts DC array output_132` | DC power output | W |  
  | `PVwatts PoA irradiance_131` | Plane-of-array irradiance | W/m² |  
  | `PVwatts Wind speed_130` | Wind speed | m/s |  

### 🌦 **NWP Forecast Data (`raw_NWP`)**  
- **Source**: Numerical Weather Prediction (NWP) Model  
- **Sampling Rate**: 10-15 min  
- **Columns**:  

  | Column Name | Description | Unit |  
  |-------------|------------|------|  
  | `Date`  | Date | - |  
  | `UT time` | Universal Time | - |  
  | `Temperature` | Forecast temperature | K |  
  | `Relative Humidity` | Humidity | % |  
  | `Pressure` | Atmospheric pressure | hPa |  
  | `Wind speed` | Wind speed | m/s |  
  | `Wind direction` | Wind direction | ° |  
  | `Rainfall` | Precipitation | kg/m² |  
  | `Snowfall` | Snowfall | kg/m² |  
  | `Snow depth` | Snow depth | m |  
  | `Short-wave irradiation` | Solar radiation | Wh/m² |  


### ☁ **Cloud Index Data (`raw_cloudindex`)**  
- **Source**: Himawari Satellite Images  
- **Sampling Rate**: 10 min  
- **Columns**:  

  | Column Name | Description |  
  |-------------|------------|  
  | `site_name` | Site name |  
  | `lat, lng` | Latitude & Longitude |  
  | `row_idx_TIFF, col_idx_TIFF` | Pixel row & column index |  
  | `lat_TIFF, lng_TIFF` | Latitude & Longitude in TIFF |  
  | `Datetime` | Timestamp |  
  | `CI_CM` | Cloud index (grayscale) |  
  | `CI_RGB` | Cloud index (RGB red channel) |  


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


   
