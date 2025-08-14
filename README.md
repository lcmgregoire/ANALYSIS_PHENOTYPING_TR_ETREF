# 📊 ANALYSIS_PHENOTYPING_TR_ETREF

R scripts for analyzing transpiration response (TR) to reference evapotranspiration (ETref) in **pearl millet** (*Cenchrus americanus*) and **sorghum** (*Sorghum bicolor*), based on data from multi-platform phenotyping experiments.

This repository contains the analysis workflows used in the article:  
> *New large-scale protocols to measure transpiration response to high evaporative demand reveal large genetic variation in pearl millet and sorghum*  
> (DOI pending)

---

## 📖 Project Overview

This repository implements the statistical and data processing steps for **three complementary phenotyping platforms** 
For each experiment:
- Transpiration (or evapotranspiration) is normalized by leaf area  
- Reference evapotranspiration (ETref) is computed from meteorological data (calculated with Penman–Monteith equation)  
- Transpiration response (Tr- ETref) is modeled using 4 models : linear, affine, polynomial 2, or segmented.
   T
The 3 phenotyping platforms to measure the transpiration response : 

1. **Low-Throughput Pot Weighing (LTP)** with sorghum (2024) and pearl millet (2025) panels, in Thièes, Senegal. 
   – Transpiration response  (Tr- ETref) with pot-level transpiration manual measurements normalized by leaf area , repeated multiple times per day (4 times a day, during four days)
   - measure of root area at harvest
   - measure of root /shoot ratio
   
2. **High-Throughput LeasyScan (HTP)** with sorghum panel (2023)
   – Transpiration response  (Tr- ETref) with automated transpiration and leaf area estimation using  load cells and 3D scanning.
   
3. **Lysimeter Platform** with sorghum (2024) and pearl millet (2025) panels
  -  measure TEplant = dry biomass at harvest / water transpirat
   – Extended time-interval measurements for transpiration efficiency (TEplant) and TR-ETref relationships.



---

## ✨ Features

- **Data Import & Cleaning**  
  Handles raw data from multiple platforms, removes outliers, and normalizes for plant size.
- **ETref Computation**  
  Implements the Penman–Monteith equation for 15- and 30-min intervals.
- **Model Fitting**  
  Fits linear, affine, polynomial, and segmented regression (breakpoint) models.
- **Trait Extraction**  
  Automatically derives TR model parameters, root traits, and TEplant.
- **Statistical Analysis**  
  Uses linear mixed models for heritability estimation and trait correlation.
- **Visualization**  
  Generates histograms, correlation plots, and TR vs. ETref curves.

---
