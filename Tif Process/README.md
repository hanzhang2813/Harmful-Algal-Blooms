# GeoTIFF Utilities

This repository contains simple Jupyter notebooks for basic GeoTIFF operations using **GDAL** and **NumPy**.  
The code is minimal and easy to adapt for different projects in remote sensing and geospatial analysis.

---

## 📂 Notebooks

### 1. `read_tif.ipynb`
- Read a GeoTIFF file with GDAL.
- Return:
  - raster array (as NumPy array)
  - raster size (width, height)
  - geotransform (affine parameters)
  - projection (WKT)
  - band count

### 2. `write_tif.ipynb`
- Save a NumPy array as a GeoTIFF file.
- Supports single-band and multi-band images.
- Invalid values (`NaN`, `inf`, `-inf`) are replaced with `-999` as NoData.

### 3. `Group_tif_by_year.ipynb`
- Group `.tif` files into subfolders based on year extracted from the filename.
- Example:
- input/
  - 2020_image1.tif
  - 2021_image2.tif
- output/
  - 2020/2020_image1.tif
  - 2021/2021_image2.tif


### 4. `clip_tif.ipynb`
- Clip GeoTIFF files by a shapefile boundary.
- Uses `gdal.Warp` with `cutlineDSName` and `cropToCutline`.
- Supports batch processing of a folder of `.tif` files.

---

## 🔧 Requirements
Install via conda (recommended):
```bash

conda install -c conda-forge gdal numpy
