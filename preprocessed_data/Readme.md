## 📂 Preprocessed Data

### ☁ **`data_Cloudindex`**  
- **Source**: Himawari Satellite Images
- **Sampling Rate**: 5, 15 min 
- **Columns**:  

  | Column Name | Description                                   | Unit  |  
  |-------------|-----------------------------------------------|-------|  
  | `Datetime`  | Timestamp                                     | -     |  
  | `CI_CM`     | Cloud index from CM method (grayscale)        | -     |  
  | `CI_RGB`    | Cloud index from RGB method (RGB red channel) | -     |  

### 🌞 **`data_Iclr`**  
- **Source**: Calculate irradiance clear sky
- **Sampling Rate**: 5, 15 min 
- **Columns**:  

  | Column Name | Description           | Unit  |  
  |-------------|-----------------------|-------|  
  | `Datetime`  | Timestamp             | -     |  
  | `Iclr`      | Clear-sky irradiance  | W/m²  |  

### ⚡ **`data_Irradiance`**  
- **Source**: CUEE Platform (8 kWp Solar Meter)
- **Sampling Rate**: 1, 5, 15 min 
- **Columns**:  

  | Column Name             | Description                   | Unit  |  
  |-------------------------|-------------------------------|-------|  
  | `Datetime`              | Timestamp                     | -     |  
  | `Irradiance (W/m2)`     | Measured solar irradiance     | W/m²  |  

### 🌦 **`data_NWP`**  
- **Source**: Numerical Weather Prediction (NWP) Model
- **Sampling Rate**: 5, 15 min 
- **Columns**:  

  | Column Name | Description                                   | Unit  |  
  |-------------|-----------------------------------------------|-------|  
  | `Datetime`  | Timestamp                                     | -     |  
  | `Inwp`      | Numerical weather prediction (irradiance)     | W/m²  | 
  | `Tnwp`      | Numerical weather prediction (temperature)    | °C    | 

### ☀ ** `data_PV`**  
- **Source**: CUBEMS Solar Meter (8 kWp meter)
- **Sampling Rate**: 1, 5, 15 min 
- **Columns**:  

  | Column Name | Description               | Unit  |  
  |-------------|---------------------------|-------|  
  | `datetime`  | Timestamp                 | -     |  
  | `Ptot (kW)` | Total solar power output  | kW    | 

### 🌡️ **`data_Temperature`**  
- **Source**: CUEE Platform (8 kWp Solar Meter)
- **Sampling Rate**: 1, 5, 15 min 
- **Columns**:  

  | Column Name         | Description                   | Unit  |  
  |---------------------|-------------------------------|-------|  
  | `Datetime`          | Timestamp                     | -     |  
  | `Temp (degree C)`   | Measured ambient temperature  | °C    |

   