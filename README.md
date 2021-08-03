# Overview
This repository provides the source code and models used in the paper "Overfitting Measurement of Deep Neural Networks Using No Data" published in the 8th IEEE International Conference on Data Science and Advanced Analytics.<BR>
It includes four Jupyter notebooks. 
* makeModelCIFAR10.ipynb
* makeModelSVHN.ipynb
* makeModelTinyImageNet.ipynb
* drawDiagram.ipynb

The "sampleModels" folder contains all the models used in the paper.

### makeModelCIFAR10.ipynb, makeModelSVHN.ipynb, makeModelTinyImageNet.ipynb
These notebooks train models on the CIFAR10, SVHN, and Tiny ImageNet data sets.<BR>
They store models to "models" directory.<BR>
The makeModelSVHN.ipynb requires data sets (train_32x32.mat, test_32x32.mat) that can be downloaded from the website
http://ufldl.stanford.edu/housenumbers/. <BR>
The makeModelTinyImageNet.ipynb requires Tiny ImageNet data sets that can be downloaded from the website http://cs231n.stanford.edu/tiny-imagenet-200.zip.<BR>

### drawDiagram.ipynb
This notebook draws persistent homology diagrams of trained models using Dionysus library.<BR>

# Usage

## Paramenters in the notebooks 

### makeModelCIFAR10.ipynb, makeModelSVHN.ipynb, makeModelTinyImageNet.ipynb

They have one parameter for specifing the dropout ratio.<BR>
In the paper, it was set to 0.0, 0.2, 0.4, and 0.6.<BR>

### drawDiagram.ipynb

This notebook has three parameters.<BR>
* target group
* dropout ratio
* model directory

The parameter of target group specifies the layers to calculate the persistent homology.<BR>
It can be set to 1 or 2 for CIFAR10 and SVHN data sets, which correspond to the 1st and 2nd group in the paper, respectively.<BR>
It can be set to 3 for Tiny ImageNet data set, which correspond to the 3rd group in the paper.<BR><BR> 

The parameter of dropout ratio specifies the ratio used in the makeModelCIFAR10.ipynb, makeModelSVHN.ipynb, and makeModelTinyImageNet.ipynb.<BR><BR>

# Sample

## sample models

The drawDiagram.ipynb illustrates the PH diagrams of the trained models in the "sampleModels" folder by setting the model directory to "sampleModels."<BR>

![tinyImagenet1000Dropout0 6-2-0-1](https://user-images.githubusercontent.com/61130343/127968734-08e08268-7fd2-4326-841d-0dfbe4ecd76d.png)


