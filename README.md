# CUEE-solar-data

# Raw data
  - **ข้อมูลโหลด (raw_GWSQ_load)**
    - CUBEMS คอลัมน์ 2 จะเป็นข้อมูลพลังงาน (Wh)
    - ข้อมูลจากมิเตอร์เก่า (มีนาคม 2023 - พฤษภาคม 2023) โดยมี sampling rate 670 ms และมีทั้งหมด 12 คอลัมน์ ข้อมูลจะเรียงตามลำดับดังนี้: time(s), la, Ib, Ic, Pa, Pb, Pc, Ptot, VAa, VAb, VAc, VAtot (ข้อมูล P หน่วย W)
    - ข้อมูลจากมิเตอร์ใหม่ (7 พฤษภาคม 2023 เป็นต้นไป) โดยมี sampling rate 420 ms และมีทั้งหมด 30 คอลัมน์ ข้อมูลจะเรียงตามลำดับดังนี้: Time(s), Ia, Ib, Ic, In, Iavg, Va, Vb, Vc, Vavg, Pa, Pb, Pc, Ptot, VARa, VARb, VARc, VARtot, VAa, VAb, VAc, VAtot, PFa, PFb, PFc, PFtot, DFa, DFb, DFc, DFtot (ข้อมูล P หน่วย kW, Q หน่วย KVAR, S หน่วย KVA)
    - ไม่มีข้อมูลวันที่ 4, 5, 12 เมษายน 2023 และวันที่ 2, 6, 10 พฤษภาคม 2023 รวมถึงวันที่ 15 มิถุนายน 2023 เนื่องจากความผิดพลาดของระบบที่เก็บข้อมูล ทำให้ข้อมูลไม่ครบในบางวัน

  - **ข้อมูลโซลาร์ (raw_PV)**
    - CUBEMS คอลัมน์ 2 จะเป็นข้อมูลพลังงาน (Wh)
    - ข้อมูลจากมิเตอร์โซลาร์ 15 kWp (มีนาคม 2023 เป็นต้นไป) โดยมี sampling rate 670 ms และมีทั้งหมด 12 คอลัมน์ ข้อมูลจะเรียงตามลำดับดังนี้: Time(s), Ia, Ib, Ic, Iavg, Pa, Pb, Pc, Ptot, VAa, VAb, VAc, VAtot (ข้อมูล P หน่วย W)
    - ข้อมูลจากมิเตอร์โซลาร์ 8 kWp จะไม่มีข้อมูลในวันที่ 4 และ 5 เมษายน 2023

  - **ข้อมูลโซลาร์ EE (raw_EE_Station1)**
    - ข้อมูลจากมิเตอร์โซลาร์ 8 kWp จาก CUEEplatform (มกราคม 2023 เป็นต้นไป) โดยมี sampling rate 1 min และมีทั้งหมด 19 คอลัมน์
    - ข้อมูลจะเรียงตามลำดับดังนี้: Datetime,	Generated power_28 (kW),	Ambient temperature_29 (degree C),	Irradiance_30 (W/m2), Relative humidity_31 (%),	PySolar Irradiance_121 (W/m2),	PySolar Azimuth angle_122 (Degree),	NCEP Ambient temperature_123 (C), PVwatts Diffuse irradiance_128 (W/m2),	NCEP Short-wave irradiance_126 (W/m2),	NCEP Release time_125 (Percent), NCEP Relative humidity_124 (Percent),	PVwatts Beam irradiance_127 (W/m2),	PVwatts AC system output_134 (W), PVwatts Cell temperature_133 (C),	PVwatts DC array output_132 (W),	PVwatts PoA irradiance_131 (W/m2), PVwatts Wind speed_130 (m/s),	PVwatts Ambient temperature_129 (C)
  
  - **ข้อมูล NWP (raw_NWP)**
    - ข้อมูลพยากรณ์จาก NWP (มกราคม 2023 เป็นต้นไป) โดยมี sampling rate 10, 15 min และมีทั้งหมด 11 คอลัมน์
    - ข้อมูลจะเรียงตามลำดับดังนี้: Date;	UT time;	Temperature;	Relative Humidity;	Pressure;	Wind speed;	Wind direction;	Rainfall;	Snowfall; Snow depth;	Short-wave irradiation
    - ข้อมูล Temperature หน่วย K,	ข้อมูล Short-wave irradiation หน่วย W/m^2

  - **ข้อมูล cloud index (raw_cloudindex)**
    - CI_CM (ขาวดำ)
      - ข้อมูล CI ที่สกัดมาจากรูป himawari (มกราคม 2023 เป็นต้นไป) โดยมี sampling rate 10 min และมีทั้งหมด 9 คอลัมน์
      - ข้อมูลจะเรียงตามลำดับดังนี้: site_name,	lat, lng, row_idx_TIFF, col_idx_TIFF, lat_TIFF, lng_TIFF, Datetime, CI_CM
    - CI_RGB (R channel)
      - ข้อมูล CI ที่สกัดมาจากรูป himawari (มกราคม 2023 เป็นต้นไป) โดยมี sampling rate 10 min และมีทั้งหมด 9 คอลัมน์
      - ข้อมูลจะเรียงตามลำดับดังนี้: site_name,	lat, lng, row_idx_TIFF, col_idx_TIFF, lat_TIFF, lng_TIFF, Datetime, CI_RGB

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


   
