📂 Structure

Tif Process/

Basic utilities for reading, writing, grouping, reprojecting, and clipping GeoTIFF files.

Band_indices.ipynb

Functions to compute common spectral indices (NDVI, NDWI, EVI, etc.).

Can be extended to water indices (MNDWI, AWEI, GNDVI).

Machine_learning.ipynb

Machine learning pipeline for training classifiers (RF, XGBoost, SVM).

Includes feature normalization, model training, evaluation (Accuracy, Precision, Recall, F1, Kappa), and saving models.

predict_tif.ipynb

Apply trained ML models to GeoTIFF images.

Save prediction results as new GeoTIFF maps.

Google_earth_Engine.ipynb / .py

Use Google Earth Engine (GEE) for remote sensing image processing and downloading (e.g., Landsat/Sentinel imagery).

Support advanced operations such as monthly/annual average composites, cloud masking, spectral index calculation, etc.

🔧 Requirements

Python 3.8+

numpy, pandas, matplotlib

scikit-learn

xgboost

joblib

GDAL

geemap (for Google Earth Engine support)

Install with conda (recommended):

conda install -c conda-forge gdal numpy pandas scikit-learn xgboost matplotlib joblib geemap

🌍 Google Earth Engine (GEE) Integration

This repository includes tools for downloading and processing satellite imagery directly via Google Earth Engine
, using the Python-based geemap API.

Typical supported workflows:

Filtering by date and region

Cloud/snow masking

Computing monthly or annual composites

Deriving spectral indices (NDVI, FAI, etc.)

Exporting GeoTIFFs with specific projection and scale

📘 For installation and detailed GEE usage in Python, refer to the official geemap documentation
.
