The Sorghum-100 dataset is a curated subset of the RGB imagery captured during the TERRA-REF experiments, labeled by cultivar. This data could be used to develop and assess a variety of plant phenotyping models which seek to answer questions relating to the presence or absence of desirable traits (e.g., "does this plant exhibit signs of water stress?''). In this contest, we focus on the question: ``What cultivar is shown in this image?''

<img src="https://terraref.org/sites/terraref.org/files/TERRA-REF-Scanner.jpg" width="550px"/>

Predicting the cultivar in an image is an especially good challenge problem for familiarizing the machine learning community with the TERRA-REF data. At first blush, the task of predicting the cultivar from an image of a plant may not seem to be the most biologically compelling question to answer -- in the context of plant breeding, the cultivar, or parental lines are typically known. A high accuracy machine learning predictor of the species captured by the sensor data, however, can be used to determine where errors in the planting process may have occurred. For example, seed may be mislabeled prior to planting, or planters may get jammed, depositing seeds non-uniformly in a field. Both types of errors are surprisingly common and can cause major problems when processing data from large-scale field experiments with hundreds of cultivars and complex field planting layouts.

# Data

Check back!

# Baseline

Check back!

# FGVC-9 Kaggle Competition
The original Sorghum-100 dataset paper was published in the 8th Fine-Grained Visual Categorization Workshop (FGVC) at CVPR 2021. We then hosted a FGVC competition on Sorghum-100 through FGVC in 2022. That competition has closed, but can still be accessed at https://www.kaggle.com/c/sorghum-100.

# Citation
If you use this code for your research, please cite the following work:
```
@inproceedings{sorghum100,
author = {Dulay, Justin and Chao, Ren and Rolwes, Greg and Stylianou, Abby},
year = {2021},
month = {June},
title = {{The Sorghum-100 Dataset - FGVC8}},
booktitle = {IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR) Fine-Grained Visual Categorization Workshop}
}
```
