# Supervised Classification of the Camp Fire 2018 with Random Forest 
## Classification based on Remote Sensing Imagery in Python 2.7

This [python script](https://github.com/joanneroll/python-classification-randomforest/blob/master/python-classification-randomforest.ipynb) shows the workflow of how to implement a supervised classification based on remote sensing data. It consists of certain preprocessing steps including a cloud mask, the classification based on random forest and postprocessing steps. The code is the result of an university assignment on which I worked together with [Laura](https://github.com/lanbra).

This project aims to analyze the extent of the burned area following the Camp Fire 2018 in Paradise. To execute this task, two Landsat 8 scenes were compared, a prefire and a postfire scene.

**Note:** This script for processing raster data is built on the classic modules gdal, numpy and matplotlib. Without doubt, there is room from improvement, e.g. using rasterio, especially for plotting. Also, being new to machine learning, it has to be noted that this is a very simple application in which some methodological approaches (e.g. the resampling strategy) probably can be questioned. As it is known from Random Forest models, also this application most likely is suffering from overfitting. 

**Modules and dependencies:**
* Python 2.7.17 
* gdal 3.0.2
* os 
* glob2 0.7
* numpy 1.15.1
* re 
* matplotlib 2.2.4
* scikit-learn 0.20.0
* imbalanced-learn 0.4.2
* scipy 1.2.3

**Data download and preparation:**
* Download of the Landsat 8 scenes from the [USGS Earth Explorer](https://earthexplorer.usgs.gov/): 16.10. (Prefire) and 10.12.2018 (Postfire)
* Cropping the extent of both scenes to the area of interest
* Renaming the files following the pattern "LC08_Prefire_Paradise_B*.tif" respectively "LC08_Postfire_Paradise_B*.tif"
* Collecting of training data in the Postfire scene 
* 8 classes: bare ground, masked cloud, water, shadow, vegetation, agriculture, sealed surfaces, burned area

**Links and tutorials:**
* [Scikit-learn (Random Forest Classifier)](https://scikit-learn.org/stable/modules/generated/sklearn.ensemble.RandomForestClassifier.html)
* [Classification tutorial by Chris Holden](https://ceholden.github.io/open-geo-tutorial/python/chapter_5_classification.html)
* [Quality Assessment Layer of Landsat 8](https://www.usgs.gov/land-resources/nli/landsat/landsat-collection-1-level-1-quality-assessment-band?qt-science_support_page_related_con=0#qt-science_support_page_related_con)