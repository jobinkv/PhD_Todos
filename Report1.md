
## Table of condent
* **[Introduction](#introduction)**
* **[Problem statement](#problem-statement)**
* **[Dataset](#dataset)**
* **[The Deep-filter bank features](#the-Deep-filter-bank-features)**
* **[Experiments](#experiments)**
* **[Reference](#reference)**


## Indroduction
This work focus on document image segmentation and layout analysis. 
## Problem statement
 We consider the segmentation as a pixel classification problem.
Each pixel is represented by a feature vector. By training a classifier with the features, we classify each pixel into one of the four classes: Text, Graphics and Background
We are experimenting to find the appropriate feature for document images.

## Dataset
In this work, we run our experiment on technical document image. 
Sample image of our dataset and it’s corresponding annotations are 
shown in the figure 1.  The red, blue and green regions in the annotated 
image represent background, text and graphics regions respectively. 
Our dataset contains 100 technical images. We randomly choose 50 images for 
training, 20 images for validation and 30 images for testing. 

## The deep-filter bank features


In the experiment section, we extract two types of deep 
features namely FC-CNN and FV-CNN, which are explained in [1]. 

Both descriptors are based on the same CNN features [2] 
obtained from an off-the-shelf CNN pre-trained on the ImageNet ILSVRC 2012 data.
The architecture of the CNN can be found **[here](#https://www.google.com/url?q=http%3A%2F%2Fwww.vlfeat.org%2Fmatconvnet%2Fmodels%2Fimagenet-vgg-m.svg)**.
### The FC-CNN features
The FC-CNN descriptor is obtained by extracting as features the output of the penultimate Fully-Connected (FC) layer of a CNN, including the non-linear gating function, 
applied to the input image. The feature dimension is 4096.

### The FV-CNN features
The FV-CNN is the fisher vector encoded on the output of a single (last) 
convolutional layer of the CNN. Differently from FC-CNN, FV pools local features densely 
within the described regions removing global spatial information, and is therefore more
apt at describing textures. The convolution layer output size will change according to 
the input image size. The convolutional feature size can be represent as 512XK, where K 
is an positive integer varies according to the image size. In the FV encoding stage, we 
randomly choose a constant number N features from the K.

## Experiments

### Patch classification task
In the first stage of the experiment, we segment our document images into patches 
and assigned the label of it’s center pixel.  Extract the FV-CNN and FC-CNN from 
the document image patch and trained a 1 vs rest linear SVM classifier and report the 
precision of classification by varying the patch size.
