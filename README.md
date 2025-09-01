# Remote Sensing Utilities

This repository provides a minimal toolkit for **GeoTIFF processing, spectral indices calculation, and machine learning classification**.  
It is designed for water color remote sensing and algal bloom detection, but the functions can be easily adapted to other remote sensing tasks.

---

## 📂 Structure

- **Tif Process/**
  - Basic utilities for reading, writing, grouping, reprojecting, and clipping GeoTIFF files.

- **Band_indices.ipynb**
  - Functions to compute common spectral indices (NDVI, NDWI, EVI, etc.).
  - Can be extended to water indices (MNDWI, AWEI, GNDVI).

- **Machine_learning.ipynb**
  - Machine learning pipeline for training classifiers (RF, XGBoost, SVM).
  - Includes feature normalization, model training, evaluation (Accuracy, Precision, Recall, F1, Kappa), and saving models.

- **predict_tif.ipynb**
  - Apply trained ML models to GeoTIFF images.
  - Save prediction results as new GeoTIFF maps.

---

## 🔧 Requirements

- Python 3.8+
- numpy, pandas, matplotlib
- scikit-learn
- xgboost
- joblib
- GDAL

Install with conda (recommended):

```bash
conda install -c conda-forge gdal numpy pandas scikit-learn xgboost matplotlib joblib
