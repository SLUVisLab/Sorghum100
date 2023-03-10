The Sorghum-100 dataset is a curated subset of the RGB imagery captured during the TERRA-REF experiments, labeled by cultivar. This data could be used to develop and assess a variety of plant phenotyping models which seek to answer questions relating to the presence or absence of desirable traits (e.g., "does this plant exhibit signs of water stress?''). In this contest, we focus on the question: ``What cultivar is shown in this image?''

<p style="text-align: center;"><img src="https://terraref.org/sites/terraref.org/files/TERRA-REF-Scanner.jpg" width="49%"/><img src="https://i.imgur.com/dlOnvRn.png" width="49%"/></p>


Predicting the cultivar in an image is an especially good challenge problem for familiarizing the machine learning community with the TERRA-REF data. At first blush, the task of predicting the cultivar from an image of a plant may not seem to be the most biologically compelling question to answer -- in the context of plant breeding, the cultivar, or parental lines are typically known. A high accuracy machine learning predictor of the species captured by the sensor data, however, can be used to determine where errors in the planting process may have occurred. For example, seed may be mislabeled prior to planting, or planters may get jammed, depositing seeds non-uniformly in a field. Both types of errors are surprisingly common and can cause major problems when processing data from large-scale field experiments with hundreds of cultivars and complex field planting layouts.

# Data

The training and testing dataset (including test data labels) can be downloaded from [https://cs.slu.edu/~astylianou/sorghum100/data.zip](https://cs.slu.edu/~astylianou/sorghum100/data.zip).

# Baseline

To provide a reasonable baseline on the Sorghum-100 dataset, we trained a ResNet-50 model (pre-trained on ImageNet). During training we resize the original images to be 512 pixels on its shortest side, and then take a random 512 × 512 crop (at test time, we take a center crop). We normalize by channel means and standard deviations and perform random horizontal and vertical flips. We use global average pooling and train with cross entropy loss. This baseline approach achieves 72.12% top-1 classification accuracy on the test set. This simple baseline can be found in [this notebook](https://github.com/SLUVisLab/Sorghum100/blob/main/resnet50_baseline.ipynb).

# FGVC-9 Kaggle Competition
The original Sorghum-100 dataset paper was published in the 8th Fine-Grained Visual Categorization Workshop (FGVC) at CVPR 2021. We hosted a FGVC competition on Sorghum-100 through FGVC in 2022. That competition has closed, but can still be accessed at [https://www.kaggle.com/c/sorghum-100](https://www.kaggle.com/c/sorghum-100).

# Citation
If you use this code for your research, please cite the following work:
```
@inproceedings{ren2021multi,
  title={Multi-resolution outlier pooling for sorghum classification},
  author={Ren, Chao and Dulay, Justin and Rolwes, Gregory and Pauli, Duke and Shakoor, Nadia and Stylianou, Abby},
  booktitle={Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
  pages={2931--2939},
  year={2021}
}
```
