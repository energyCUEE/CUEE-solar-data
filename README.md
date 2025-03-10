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

# Process data
   
