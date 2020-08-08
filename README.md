# FoodImageClassifier
Did this for my Deep Learning Module Assignment 1. Based off the food-101 dataset on Kaggle, which was used in a DL competition.

Achieved an 'A' grade / 4.0 GPA for this assignment. (Models, Presentation which is not included and Final Report).

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
* A NVIDIA GPU with 2GB NVRAM (or equivalent)
* NvMe SSD for unzipping the large (food-101) dataset

## Software Packages
* Anaconda
   * Tensorflow (which includes Keras) and Tensorflow-Base
   * Tensorboard
   * Tensorflow GPU (optional)
   
```
conda install tensorflow
conda install tensorflow-gpu
```


## Preprocessing Steps
1) Download food-101 zip from this [website](https://www.kaggle.com/dansbecker/food-101). Make sure you download the `.zip` file and **NOT** the `.zip.zip` file. 
***Warning: If you have a non-NVMe SSD, this could take up to 8 hours to unzip***

2) Place Image_Preprocessing.ipynb, 40.txt (or any other specified .txt file from the `Food_List.zip`) and the extracted image file (food-101/food-101/food-101/images) into the same base directory of choice. An example is given below:

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
For all my models, I chose an image size of 150 x 150 and used data augmentation for all models, which aided in increasing the diversity of the relatively small dataset of 1000 images per food category. For most models, I used a standard set of augmentation parameters, which can be found in the notebook (base models).

## Results
| Model Number:  | Description/Type:                     |Test Accuracy (%):|
| -------------  | ------------------------------------- | ---------------- |
| 0              | Non-PT RMSProp Base                   | 64.2             |
| 1              | Non-PT RMSProp Lower LR               | 68               |
| 2              | Non-PT RMSProp Change Steps Per Epoch | 57               |
| 3              | Non-PT RMSProp Higher LR              | 59.8             |
| 4              | Non-PT Adam Lower LR                  | 55.8             |
| 5              | Non-PT Adam Base                      | 71.2             |
| 6              | Non-PT SGD+Momentum Base              | 67.4             |
| 7              | Non-PT SGD+Momentum Lower Momentum    | 64.4             |
| 8              | Non-PT Adam Regularization            | 69.6             |
| 9              | PT VGG16 Fine Tuning 2                | 74.6             |
| 10             | PT VGG16 Base*                        | 67.8             |
| 11             | PT VGG16 Fine Tuning 1                | 73.2             |
| 12             | PT ResNet50 Base                      | 75.4             |
| 13             | PT ResNet50 Fine Tuning 1             | 79.6             |
| 14             | PT ResNet50 Fine Tuning 2             | 78.8             |
| 15             | PT ResNet50 Fine Tuning 3             | 83.4             |

*underfitted.
