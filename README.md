#  GeoHeat-CME 🌍 🌡️🌡
**Spatiotemporal Analysis and Prediction of Land Surface Temperature over CME Region using Remote Sensing and Machine Learning**

![Status](https://img.shields.io/badge/status-Ongoing-blue)
![Python](https://img.shields.io/badge/python-3.8%2B-yellow)
![GEE](https://img.shields.io/badge/Google%20Earth%20Engine-enabled-green)
![License](https://img.shields.io/badge/license-MIT-lightgrey)

## 📌 Project Overview
**GeoHeat-CME** is a remote sensing and machine learning project focused on understanding and predicting **Land Surface Temperature (LST)** patterns across the **College of Military Engineering (CME)** campus located in Pune, India. The project emphasizes the spatiotemporal behavior of LST across three sub-regions — **Solar Panel Areas, Built-Up Zones, and Water Bodies** — using **satellite data**, **indices** (NDVI, NDBI), and advanced ML models.

## 🎯 Objectives
- 🛰️ Extract and preprocess LST from MODIS & Landsat data (2000–2024)
- 📍 Define and analyze LST over solar, built-up, and water regions within CME
- 🌱 Compute NDVI, NDBI, and emissivity
- 🤖 Predict LST up to 2041 using ML models (SVM, ANN, LSTM, RF)
- 📊 Evaluate performance using R², RMSE, and MAE
- 🗺️ Generate heatmaps and export-ready CSVs for future research & planning

## 🧪 Methodology
- **Data Sources:** MODIS (MOD11A2), Landsat 8/9, Dynamic World (GOOGLE/DYNAMICWORLD/V1)
- **Preprocessing:** Cloud masking, temperature conversion, NDVI/NDBI computation, seasonal filtering (Mar–Jun, 10am–5pm)
- **Region Focus:** Sub-regions manually digitized from CME shapefile
- **Prediction:** Models trained on 2000–2020, tested on 2021–2024, predicted up to 2041
- **Export:** Cleaned CSVs for each region + interactive maps


## 📍 Study Area

The study focuses on the **College of Military Engineering (CME)**, located near Dapodi in **Pune, Maharashtra, India**. The CME campus is characterized by a diverse mix of urban, vegetative, and water bodies, making it an ideal site for analyzing **heat stress patterns**. The study area includes:

- **Water bodies** (marked in red): Representing natural and artificial lakes within CME.
- **Solar Panel Region** (marked in green): An energy-sensitive zone of interest for temperature forecasting.
- **Built-up Area** (marked in blue): Densely constructed zones prone to urban heat island effects.


<p align="center">
  <img src="https://github.com/ishitak12/GeoHeat-CME/blob/main/cme_image1.jpg" alt="Study Area Map" width="600"/>
</p>
<p align="center"><b>Figure 1: Study Area Map</b></p>
The first image presents the geographical context of the **College of Military Engineering (CME)**, which is located near Dapodi in the Pune district of Maharashtra, India. The map on the top left highlights the location of Maharashtra within the national boundary of India, while the bottom left inset zooms in on the Pune district. The right portion of the image shows a **high-resolution satellite view** of the CME region, clearly demarcating its extensive infrastructure, vegetation cover, internal road networks, and surrounding urban areas.

![LULC Zones](https://github.com/ishitak12/GeoHeat-CME/blob/main/cme_image2.jpg)  
**Figure 2: Annotated Subregions - Water, Solar, Built-up**
The second image delineates three specific sub-regions within the CME boundary that form the core of this study’s analysis: Water Bodies, Solar Panel Zone, and Built-up Area. These are represented in red, green, and blue respectively.

**Water** (Red): Represents natural or artificial water bodies located inside the campus. These areas are critical for analyzing thermal cooling patterns due to their lower heat retention and higher latent heat exchange.

**Solar** (Green): Denotes the region with solar infrastructure. This area is vital to assess how renewable energy installations interact thermally with their surroundings.

**Built-up** (Blue): Covers infrastructure-dense zones including buildings, roads, and paved areas which typically exhibit elevated surface temperatures due to the Urban Heat Island (UHI) effect.

These selected zones enable targeted analysis of Land Surface Temperature (LST) and other indices like NDVI and NDBI, helping in understanding microclimate behavior and supporting prediction modeling for future years.
---

## 🛰️ Data Sources

| Source        | Product / Collection              | Resolution | Period        |
|---------------|-----------------------------------|------------|---------------|
| **Landsat 8/9** | LC08/LC09 Tier 1 Level 2         | 30m        | 2013–2024     |
| **MODIS**     | MOD11A2 (LST 1km, 8-day avg)       | 1km        | 2000–2024     |
| **Dynamic World** | GOOGLE/DYNAMICWORLD/V1 (LULC)  | 10m        | 2020–2024     |
| **AWS/IMD**   | Ground-based weather station data | -          | 2000–2024     |

---

## ⚙️ Tech Stack

- **Google Earth Engine (GEE)**: Data extraction, preprocessing, satellite imagery.
- **Python**: Data analysis, ML modeling.
- **Libraries**: pandas, scikit-learn, matplotlib, seaborn, keras (for LSTM), xgboost.
- **QGIS** & **Google Earth Pro**: For digitization, visualization, and shapefile creation.
- **GitHub & Streamlit** *(future scope)*: Web-based deployment of prediction models.

---

## 📊 Machine Learning Models Used

| Model           | Type               | Usage                      |
|----------------|--------------------|----------------------------|
| Random Forest   | Ensemble, Tree     | Feature importance & robust baseline |
| SVM             | Supervised         | Non-linear classification |
| ANN             | Neural Network     | Non-linear LST regression |
| LSTM            | Deep Learning (RNN)| Time-series LST prediction |

---



