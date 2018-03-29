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

## igraph v0_7_1
**Problem:** Plots in Jupyter Notebook don't work  
**Solution:** Copy this modified igraph drawing [\_\_init\_\_.py](https://github.com/epmarie/network_workshop/blob/master/__init__.py) file to `..\Anaconda3\Lib\site-packages\igraph\drawing` folder

## InstagramApi v1_0_2
**Problem:** Need ffmpeg  
**Solution:** Install ffmpeg from https://www.ffmpeg.org/

**Problem:** Issue with making requests  
**Solution:** `requests` package has to be v2.11.1 [See Source](https://github.com/LevPasha/Instagram-API-python/blob/master/requirements.txt)

