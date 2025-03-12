## 📂 Processed Data

### **`pv_8kW_5minresample_concat`,`pv_8kW_15minresample_concat`**  
- **Sampling Rate**: 5, 15 min 
- **Columns**:  

  | Column Name             | Description                   | Unit  |  
  |-------------------------|-------------------------------|-------|  
  | `datetime`              | Timestamp                     | -     |  
  | `PVtot (kW)`            | Total solar power output      | kW    |  
  | `Irradiance (W/m2)`     | Measured solar irradiance     | W/m²  |
  | `alpha (m2)`            | solar efficiency              | m²    | 
  | `k`                     | Correction factor             | -     | 
  | `PVtot_correct (kW)`    | Corrected solar power         | kW    | 

### **`pv_8kW_5minresample_concat_impute`,`pv_8kW_15minresample_concat_impute`**  
- **Sampling Rate**: 5, 15 min 
- **Columns**:  

  | Column Name                          | Description                                                  | Unit             |
  |--------------------------------------|--------------------------------------------------------------|------------------|
  | `Datetime`                           | Timestamp                                                    | -                |
  | `PVtot (kW)`                         | Total solar power output                                     | kW               |
  | `Irradiance (W/m²)`                  | Measured solar irradiance                                    | W/m²             |
  | `alpha (m²)`                         | solar efficiency                                             | m²               |
  | `k`                                  | Correction factor                                            | -                |
  | `PVtot_correct (kW)`                 | Corrected total solar power output                           | kW               |
  | `Temp (°C)`                          | Measured ambient temperature                                 | °C               |
  | `Inwp`                               | Numerical weather prediction (irradiance)                    | W/m²             |
  | `Tnwp`                               | Numerical weather prediction (temperature)                   | °C               |
  | `Iclr`                               | Clear-sky irradiance                                         | W/m²             |
  | `CI_CM`                              | Cloud index from CM method (grayscale)                       | -                |
  | `CI_RGB`                             | Cloud index from RGB method (RGB red channel)                | -                |
  | `PVtot (kW)_imputed`                 | Imputed total solar power output                             | kW               |
  | `Irradiance (W/m²)_imputed`          | Imputed measured solar irradiance                            | W/m²             |
  | `alpha (m²)_imputed`                 | Imputed solar efficiency                                     | m²               |
  | `k_imputed`                          | Imputed correction factor                                    | -                |
  | `PVtot_correct (kW)_imputed`         | Imputed corrected total solar power output                   | kW               |
  | `Temp (°C)_imputed`                  | Imputed ambient temperature                                  | °C               |
  | `Inwp_imputed`                       | Imputed numerical weather prediction (irradiance)            | W/m²             |
  | `Tnwp_imputed`                       | Imputed numerical weather prediction (temperature)           | °C               |
  | `Iclr_imputed`                       | Imputed clear-sky irradiance                                 | W/m²             |
  | `CI_CM_imputed`                      | Imputed cloud index from CM method (grayscale)               | -                |
  | `CI_RGB_imputed`                     | Imputed cloud index from RGB method (RGB red channel)        | -                |
