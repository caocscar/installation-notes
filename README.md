# Python 3.6 Installation Notes on Windows 7

**Table of Contents**
- [Anaconda](#anaconda3-5.1.0-windows-64bit)
- [Geopandas](#geopandas-0.3.0)
- [Instagram](#instagramapi-1.0.2)


## Anaconda3 5.1.0 Windows 64bit
**Problem:** `conda` and `pip` commands not recognized in the command window  
**Solution:** Add `C:\Users\caoa\AppData\Local\Continuum\anaconda3\Scripts` to the PATH environment variable to your local account for a local user installation

**Problem:** Can not install packages with `conda` or `pip` because it can not find the following file `C:\Users\caoa\AppData\Local\Continuum\anaconda3\Lib\site-packages\certifi\weak.pem`  
**Solution:** Copied `cacert.pem` and renamed to `weak.pem`

## Geopandas 0.3.0
**Problem:** Can not `pip install` geopandas binary wheel  
**Solution:** Used `conda install -c conda-forge geopandas` instead

## InstagramApi 1.0.2
**Problem:** Need ffmpeg  
**Solution:** Install ffmpeg


