# FoodImageClassifier
Did this for my Deep Learning Module Assignment 1. Based of the food-101 dataset on Kaggle.

Assigned 10 types of food.
* caprese_salad
* hamburger
* creme_brulee
* baklava
* omelette
* paella
* peking_duck
* cheesecake
* sushi
* beef_carpaccio

## Recommended Hardware
* At least 16GB RAM
* An i7 Intel Processor (or equivalent)
* A NVIDIA GPU

## Software Packages
* Anaconda
   * Tensorflow (which includes Keras) and Tensorflow-Base
   * Tensorboard
   * Tensorflow GPU (optional)


## Preprocessing Steps
1) Download food-101 zip from this [website](https://www.kaggle.com/dansbecker/food-101). Make sure you download the `.zip` file and **NOT** the `.zip.zip` file. 
***Warning: If you have a non-NVMe SSD, this could take up to 8 hours to unzip***

2) Place Image_Preprocessing.ipynb, 40.txt and the extracted image file (food-101/food-101/food-101/images) into the same base directory of choice. An example is given below:

```
DL Assignment 1
|- Image_Preprocessing.ipynb
|- 40.txt
|- Assignment_1.ipynb
|- images (102 items)
   |- apple_pie (1000 images)
      |-
   |- baby_back_ribs
   |- baklava
   ...
   |- tiramisu
   |- tuna_tartare
   |- waffles
   |- .DS Store (can ignore)
```
3) Run Image_Preprocessing.ipynb with 40.txt and your path of the images folder specified. The folder structure should be modified slightly
as shown below.
```
DL Assignment 1
|- Image_Preprocessing.ipynb
|- 40.txt
|- train
|- test
|- validate
|- Assignment_1.ipynb
|- images (102 items)
   |- apple_pie (1000 images)
      |-
   |- baby_back_ribs
   |- baklava
   ...
   |- tiramisu
   |- tuna_tartare
   |- waffles
   |- .DS Store (can ignore)
```

4) Create a new folder named `Assigned_Images` and move the `train`, `test` and `validate` folders to this folder. The reultant directory structure is shown below.
```
DL Assignment 1
|- Image_Preprocessing.ipynb
|- 40.txt
|- Assigned_Images
   |- train
   |- test
   |- validate
|- Assignment_1.ipynb
|- images (102 items)
   |- apple_pie (1000 images)
      |-
   |- baby_back_ribs
   |- baklava
   ...
   |- tiramisu
   |- tuna_tartare
   |- waffles
   |- .DS Store (can ignore)
```

## Building the Model
To be updated...
