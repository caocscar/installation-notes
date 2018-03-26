# Python 3.6 Installation Notes on Windows 7

## Table of Contents
- [Anaconda](#anaconda3-v5_1_0-windows-64-bit)
- [Geopandas](#geopandas-v0_3_0)
- [Instagram](#instagramapi-v1_0_2)
---
## Anaconda3 v5_1_0 Windows 64-bit
**Problem:** `conda` and `pip` commands not recognized in the command window  
**Solution:** Add `C:\Users\caoa\AppData\Local\Continuum\anaconda3\Scripts` to the PATH environment variable to your local account for a local user installation

**Problem:** Can not install packages with `conda` or `pip` because it can not find the following file `C:\Users\caoa\AppData\Local\Continuum\anaconda3\Lib\site-packages\certifi\weak.pem`  
**Solution:** Copied `cacert.pem` and renamed to `weak.pem`

## Geopandas v0_3_0
**Problem:** Can not `pip install` geopandas binary wheel  
**Solution:** Used `conda install -c conda-forge geopandas` instead

## InstagramApi v1_0_2
**Problem:** Need ffmpeg  
**Solution:** Install ffmpeg


