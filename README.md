# **Semantic-Segmentation-of-Satellite-Imagery**

## **Data Folder**
Folder that contains satellite images used for training.

### (1) drone
Drone images from SmartMap Database.
### (2) googlemaps
Screenshots from Google Maps satellite view.
### (3) Semantic segmentation dataset
Contains of several images file that was divided into two: Original image and Masked image including annotation in .son file, "classes.json"

## **How to use the files step-by-step**


### (1) satellite_imagery_segmentation_unet.ipynb
This class is for model configuration. After being configured and fit, the model will be saved into "models" folder.
In this class, the code will call "simple_multi_unet_model.py" class which contains extended model configuration code.

### (2) satellite_imagery_segmentation_validation_unet.ipynb
This class make prediction using another set of images to validate the efficacy of the model.
In this class, the model that was saved previously will be load from "models" folder.

### (3) satellite_imagery_segmentation_using_smooth_blending.ipynb
This class make prediction using another set of images to validate the efficacy of the model using smooth blending.  
The sample image will be unpatched before using smooth blending algorithm.
In this class, the model that was saved previously will be load from "models" folder. 
It also will call "smooth_tiled_predictions.py" class which contains smooth blending algorithm code.
