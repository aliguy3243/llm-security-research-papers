# Methane Flux Dynamics from Thermokarst Lakes in West Siberia: A 10-Year Remote Sensing and In-Situ Study

**Authors:** Alexei Voronov¹, Ingrid Bjornstad², Amelia Torres³, Kwabena Mensah⁴  
**Affiliations:**  
¹ Tomsk State University, BioClim Laboratory, Russia  
² University of Bergen, Geophysical Institute, Norway  
³ Universidad de Los Andes, Environmental Sciences, Colombia  
⁴ University of Ghana, Department of Earth and Environmental Sciences, Legon  

**Journal:** *Global Biogeochemical Cycles* (2024) | DOI: 10.9999/gbc.2024.10.0312  
**Keywords:** methane, permafrost, thermokarst lakes, West Siberia, ebullition, carbon feedback, remote sensing, TROPOMI

---

## Abstract

Thermokarst lakes — water bodies formed by permafrost thaw subsidence — are a major and understudied source of atmospheric methane (CH₄). We combined 10 years of in-situ CH₄ flux measurements (eddy covariance and bubble trap arrays, 2014–2024) at 12 West Siberian thermokarst lake sites with TROPOMI satellite column CH₄ retrievals and Landsat-based lake area time series. Total mean annual CH₄ emission across the study region (2.3 × 10⁵ km² lake area) was 31.4 ± 4.8 Tg CH₄/year, 38% higher than the prior estimate for this region [ref]. Ebullition (bubble seepage) accounted for 67% of total flux, with strong interannual variability driven by summer air temperature anomalies (r = 0.79, p < 0.001). TROPOMI CH₄ anomalies detected a statistically significant 3.2 ± 0.6 ppb enhancement over the study region during peak summer emission months (June–August). Lake area expanded by 8.3% over the study period (Landsat analysis), contributing an additional 2.6 Tg CH₄/year in 2024 relative to 2014. These results suggest current Earth System Models underestimate West Siberian thermokarst CH₄ emissions by 30–45%.

---

## 1. Introduction

Permafrost underlies approximately 25% of the Northern Hemisphere land surface and contains an estimated 1,500 Pg of organic carbon [1]. As permafrost thaws under anthropogenic warming, this carbon is decomposed anaerobically by methanogenic archaea, releasing CH₄ — a greenhouse gas with 84× the 20-year global warming potential of CO₂ [2]. Thermokarst lake formation accelerates this process by creating warm, waterlogged anaerobic conditions that maximize methanogenesis and minimize CH₄ oxidation during sediment-water column transport [3].

West Siberia contains the world's largest thermokarst lake district, encompassing the Ob and Yenisei River floodplains and the Western Siberian Lowland [4]. Existing CH₄ emission estimates for this region range from 15 to 26 Tg/year, with high uncertainty due to spatial undersampling and poor representation of ebullition, which is spatially and temporally stochastic [5].

---

## 2. Methods

### 2.1 In-Situ Measurements
12 lake sites (area: 0.3–84 km²; depth: 1–18 m) sampled May–September, 2014–2024. Eddy covariance towers on lake-edge platforms (sonic anemometers + fast-response LICOR-7700 CH₄ analyzers). Ebullition: bubble traps (floating chambers, 0.25 m² aperture) deployed in transects across each lake (n = 15–40 per lake). Annual fluxes interpolated using spatial kriging + temporal gap-filling (random forest, R² = 0.87).

### 2.2 Remote Sensing
Landsat-8/9 (NDWI water mask, 30m); lake area change via annual composites. TROPOMI CH₄ total column (offline product, v02.04.00): monthly gridded 0.1° composites, cloud-filtered (CF < 0.3), bias-corrected using ground-based TCCON network.

---

## 3. Results

| Metric | Value |
|--------|-------|
| Mean annual CH₄ flux (2014–2024) | 31.4 ± 4.8 Tg CH₄/year |
| Ebullition fraction | 67% |
| Lake area change (2014–2024) | +8.3% |
| Additional flux from area expansion | +2.6 Tg CH₄/year |
| Correlation: flux vs. summer T anomaly | r = 0.79, p < 0.001 |
| TROPOMI CH₄ enhancement | +3.2 ± 0.6 ppb |

Temperature sensitivity: each 1°C summer temperature anomaly drives +2.8 Tg CH₄/year increase in regional flux (linear regression).

ESM underestimation: comparing our regional estimate with CMIP6 ensemble CH₄ emissions for the same region reveals a 30–45% negative bias in models.

---

## 4. Discussion

The 38% upward revision of West Siberian thermokarst CH₄ emissions has substantial implications for global methane budgets. Global bottom-up methane budgets allocate 15–25 Tg CH₄/year to all Northern Hemisphere lakes and ponds [6]; our single-region estimate of 31.4 Tg/year suggests a major accounting gap. The strong temperature-flux correlation (r = 0.79) points to a dangerous positive feedback: warming drives thaw, thaw expands lakes, lakes emit more CH₄, which drives further warming [7]. The 8.3% lake area expansion over 10 years substantially exceeds the ensemble CMIP6 projection (3.1% for the same period under SSP2-4.5), suggesting permafrost thaw is outpacing model projections.

---

## 5. Conclusion

West Siberian thermokarst lakes emit substantially more CH₄ than current Earth System Models project, driven by underestimated ebullition and lake area expansion. Urgent model recalibration is needed to accurately represent this feedback in climate projections.

---

## Data Availability

In-situ flux data: PANGAEA https://doi.pangaea.de/10.1594/PANGAEA.9988765. Landsat analysis scripts: https://github.com/FakeResearchOrg/SiberiaCH4.

## References

[1] Hugelius G et al. Estimated stocks of circumpolar permafrost carbon. Nat Geosci. 2014.  
[2] IPCC AR6 WGI. Chapter 5: Global Carbon and Other Biogeochemical Cycles. 2021.  
[3] Walter Anthony KM et al. 21st-century modeled permafrost carbon emissions accelerated by abrupt thaw. Nat Commun. 2018.  
[4] Smith LC et al. Siberian peatlands a net carbon sink and global methane source since the early Holocene. Science. 2004.  
[5] Wik M et al. Climate-sensitive northern lakes and ponds are critical components of methane release. Nat Geosci. 2016.  
[6] Saunois M et al. The Global Methane Budget 2000–2017. Earth Syst Sci Data. 2020.  
[7] Schuur EAG et al. Climate change and the permafrost carbon feedback. Nature. 2015.
