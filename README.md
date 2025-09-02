# 🛰️ Remote Sensing Utilities

This repository provides a minimal toolkit for **GeoTIFF processing, spectral indices calculation, and machine learning classification**.  
It is designed for **water color remote sensing and algal bloom detection**, but the functions can be adapted to other remote sensing tasks.

---

## 📁 Project Structure

```
Remote_Sensing_Project/
├── Tif Process/                  # Basic GeoTIFF utilities (read, clip, group, write)
├── Band_indices.ipynb           # NDVI, NDWI, EVI, MNDWI, AWEI, etc.
├── Machine_learning.ipynb       # Classifier training: RF, XGBoost, SVM
├── predict_tif.ipynb            # Predict and export classified GeoTIFF maps
├── GEE_Download.ipynb/.py       # Download data via Google Earth Engine (GEE)
```

---

## ⚙️ Features

- 📦 **GeoTIFF I/O**: Grouping, clipping, reprojection, multi-band write.
- 🌱 **Spectral Indices**: NDVI, NDWI, EVI, MNDWI, AWEI, GNDVI, etc.
- 🤖 **Machine Learning**: Support for RF / XGBoost / SVM with evaluation:
  - Accuracy, Precision, Recall, F1-score, Kappa.
- 🛰 **Prediction Mapping**: Apply trained model to new satellite images.
- 🌍 **GEE Integration**: For time-series image processing & downloading.

---

## 🔧 Requirements

```bash
Python >= 3.8

# Core dependencies
conda install -c conda-forge \
    gdal numpy pandas scikit-learn xgboost matplotlib joblib geemap 
```

---

## 🌍 Google Earth Engine (GEE) Integration

This toolkit supports using **Google Earth Engine (GEE)** via the `geemap` Python API.

Typical remote sensing workflows supported:

- ✅ Query and filter Landsat/Sentinel images
- ✅ Apply cloud and snow masking
- ✅ Compute vegetation and water indices (NDVI, FAI, MNDWI, etc.)
- ✅ Export monthly or annual composites
- ✅ Download as GeoTIFF with projection, resolution control

📘 **Python GEE Setup**: [https://geemap.org/](https://geemap.org/)

---

## 📌 Note

This repository offers a general framework.  
Users can **extend or customize functions** for their own use cases, such as:

- Adding new spectral indices
- Custom preprocessing pipelines
- Annual/monthly statistical compositing
- Cloud/GAP filtering for time series

---

## 📂 Source

Other related code and documentation can be found at:  
🔗 [https://github.com/hanzhang2813/Harmful-Algal-Blooms](https://github.com/hanzhang2813/Harmful-Algal-Blooms)

