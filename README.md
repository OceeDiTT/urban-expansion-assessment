<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f2027,50:203a43,100:2c5364&height=200&section=header&text=Urban%20Expansion%20Assessment&fontSize=30&fontColor=ffffff&animation=fadeIn" />

  ### Spatio-Temporal Assessment of Urban Expansion in Lahore (2000–2025)

  <img src="https://img.shields.io/badge/Tools-ArcGIS%20Pro-blue" />
  <img src="https://img.shields.io/badge/Data-Landsat-green" />
  <img src="https://img.shields.io/badge/Method-Remote%20Sensing-orange" />
  <img src="https://img.shields.io/badge/Analysis-LULC%20Change-critical" />
</div>

## Overview
This project analyzes **urban expansion dynamics in Lahore District, Pakistan** over a 25-year period (2000–2025) using **Remote Sensing (RS)** and **Geographic Information Systems (GIS)** techniques.

The study leverages Landsat satellite imagery and classification methods to quantify land use/land cover (LULC) changes and assess how urban growth has transformed the landscape.

---

## Objectives
- Generate LULC maps for **2000 and 2025**
- Compare **unsupervised vs supervised classification methods**
- Evaluate classification accuracy
- Quantify **urban expansion patterns**
- Analyze land conversion into built-up areas

---

## Study Area
- **Location:** Lahore District, Pakistan  
- **Coordinates:** 31°13′N – 31°43′N, 74°00′E – 74°39.5′E  
- **Area:** ~1,772 km²  
- **Population (2025):** ~14.8 million  

Lahore is one of the fastest-growing cities globally, making it an ideal case study for urban expansion analysis.

---

## Data Sources
### Satellite Data:
- Landsat 5 TM (2000)
- Landsat 8 OLI/TIRS (2025)
- Spatial Resolution: 30m  
- Path/Row: 149/038  
- Source: USGS Earth Explorer  

### Ancillary Data:
- Administrative boundaries  
- High-resolution Google Earth imagery  

---

## Methodology

### 1. Preprocessing
- Images used as **standard corrected products**
- Same seasonal window (**April**) selected for consistency  

### 2. Feature Enhancement
- **NDVI** → Vegetation detection  
- **NDBI** → Built-up areas  
- **MNDWI** → Water bodies  

### 3. Classification Approach
A hybrid strategy combining:
- **Unsupervised Classification (ISO Cluster)**
- **Supervised Classification**
  - Random Forest  
  - Support Vector Machine  
  - Maximum Likelihood *(selected for final output)*  

### 4. Accuracy Assessment
- 200 random reference points per year  
- Confusion matrix used to compute:
  - Overall Accuracy  
  - User’s Accuracy  
  - Producer’s Accuracy  

### 5. Change Detection
- Post-classification comparison  
- Raster → Vector conversion  
- Quantification of land transitions  

---

## Key Results

### Classification Accuracy
| Method | Year | Accuracy |
|-------|------|---------|
| Unsupervised | 2000 | 56.5% |
| Unsupervised | 2025 | 54.0% |
| Supervised | 2000 | 71.5% |
| Supervised | 2025 | **79.5%** |

Supervised classification significantly outperformed unsupervised methods.

---

### Urban Expansion
- Built-up area increased from **275 km² (2000)** to **1022 km² (2025)**
- Total increase: **+43.23%**

---

### Land Cover Changes (2000–2025)

| Land Cover | Change |
|-----------|--------|
| Built-up | **+43.23%** |
| Vegetation | -16.90% |
| Barren Land | -25.57% |
| Water Bodies | -0.74% |

---

### Land Conversion
- Vegetation → Built-up: **~292 km²**
- Barren → Built-up: **~442 km²**

---

## Key Insights
- Urban growth follows **road networks and peri-urban expansion**
- Significant **loss of vegetation and agricultural land**
- Increased **environmental risks**:
  - Urban Heat Island (UHI)
  - Air pollution (smog)
- Expansion concentrated in:
  - Southeast  
  - South  
  - Southwest regions  

---

## Tools & Technologies
- ArcGIS Pro  
- Landsat Satellite Imagery  
- Remote Sensing Indices (NDVI, NDBI, MNDWI)  
- Machine Learning Classifiers  

---

## Implications
This study supports:
- Sustainable urban planning  
- Smart city development  
- Policy alignment with **SDG 11 (Sustainable Cities and Communities)**  

---

## How to Use This Project
1. Acquire Landsat imagery from USGS  
2. Preprocess and subset study area  
3. Apply classification workflows in ArcGIS Pro  
4. Perform accuracy assessment  
5. Run post-classification change detection  

---

## Collaborators
- Christian Oluoma  
- Adebola Adedayo  
- Saba Fatima  
