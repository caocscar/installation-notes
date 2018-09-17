# Python 3.6 Installation Notes on Windows 10

## Table of Contents
- [Anaconda](#anaconda3-v5_1_0-windows-64-bit)
- [Geopandas](#geopandas-v0_4_0)
- [Instagram](#instagramapi-v1_0_2)
- [igraph](#igraph-v0_7_1)
- [openCV](#opencv-v3_4_2)
- [pdf2image](#pdf2image-v0_1_14)
- [PyTesseract](#pytesseract-v0_2_2)
- [Selenium](#selenium-v3_13_0)
---
## Anaconda3 v5_1_0 Windows 64-bit
**Problem:** `conda` and `pip` commands not recognized in the command window  
**Solution:** Add `C:\Users\caoa\AppData\Local\Continuum\anaconda3\Scripts` to the PATH environment variable to your local account for a local user installation

**Problem:** Can not install packages with `conda` or `pip` because it can not find the following file `C:\Users\caoa\AppData\Local\Continuum\anaconda3\Lib\site-packages\certifi\weak.pem`  
**Solution:** Copied `cacert.pem` and renamed to `weak.pem`

## Geopandas v0_4_0
**Problem:** `conda install -c conda-forge geopandas` asks to uninstall anaconda
**Solution:** Use `pip install` binary wheels (gdal, pyproj, fiona, shapely, rtree, geopandas). No need for setting PATH. Reference: https://geoffboeing.com/2014/09/using-geopandas-windows/

## igraph v0_7_1
**Problem:** Plots in Jupyter Notebook don't work  
**Solution:** Copy this modified igraph drawing [\_\_init\_\_.py](https://github.com/epmarie/network_workshop/blob/master/__init__.py) file to `..\Anaconda3\Lib\site-packages\igraph\drawing` folder

## InstagramApi v1_0_2
**Problem:** Need ffmpeg  
**Solution:** Install ffmpeg from https://www.ffmpeg.org/

**Problem:** Issue with making requests  
**Solution:** `requests` package has to be v2.11.1 [See Source](https://github.com/LevPasha/Instagram-API-python/blob/master/requirements.txt)

## OpenCV v3_4_2
1. Download binary wheel from http://www.lfd.uci.edu/~gohlke/pythonlibs/ and `pip install`
2. Update `numpy` if `import cv2` does not work

## pdf2image v0_1_14
1. Install Poppler for Windows http://blog.alivate.com.au/poppler-windows/ 
2. Add `poppler-0.51` folder to your PATH or move it to a PATH directory
3. `pip install pdf2image`
4. `pip install -U pillow`
5. Restart Spyder if necessary

## PyTesseract v0_2_2
1. Install Google's Tesseract-OCR Engine (v3_05_01) via [pre-built binary package for Windows](https://github.com/UB-Mannheim/tesseract/wiki) for all users on PC
2. Add `Tesseract-OCR` folder to your PATH
3. `pip install pytesseract`
4. `pip install -U pillow`
5. Restart Spyder if necessary

## Selenium v3_13_0
1. `pip install selenium`
2. Download latest chromedriver from https://sites.google.com/a/chromium.org/chromedriver/downloads
3. Put chromedriver.exe in the PATH or specify it directly in the line of code
`webdriver.Chrome(r'C:\Users\caoa\AppData\Local\Continuum\anaconda3\chromedriver.exe', chrome_options = options)`
