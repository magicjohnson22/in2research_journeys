---
title: Week 3 - Preprocessing on the mobious dataset 
date: 2026-07-03
time: "17:30"
author: mmohamoud
categories: ["Augmentation", "python", "Preprocessing","MOBIOUS","Pillow","Image","mask"] # This is optional, list of categories that you want to add
layout: post
---

### Highlights

* This week, I began by testing my code on the MOBIUS dataset and was successful in producing augmented images. I currently have around 8 augmentations in my preprocessing package: 5 geometric transformations, including rotations by 90, 180 and 270 degrees, as well as horizontal and vertical flips. These geometric transformations are applied to both the image and the mask.
* I also added 3 image-only, non-geometric augmentations: brightness and contrast with ability for adjustment and grayscale conversion. These are only applied to the images, as applying them to the masks would change the mask labels incorrectly and cause issues down the line when training the model on.
* I also added an image-mask pair matching script to check whether each image in a dataset has a corresponding mask. This is an important step before augmentation because the image and mask pairs need to match correctly for segmentation training.

### Challenges

* My image-mask pair matching script is showing that all images have matching masks within the dataset however this is incorrect as the number of images is greater than the number of masks.
* My code does not currently work on the openEDS dataset as the folder structures are different as well as both the image and mask being in .png format whereas my code currently only supports jpg,jpeg.
* Non-geometric augmentations also keep getting applied to the mask need to ensure that this it only applies the transforms to the mask upon applying geometric transformations only.

#### Goals for Following Week

* Add support for datasets that use non-JPEG formats, such as .png and .tif.
* Fix the image-mask pair matching script so it works correctly.
* Add further image-only augmentations, including CLAHE, blur, gamma correction and histogram equalisation.
* Successfully demonstrate augmentations on the OpenEDS and RIT-Eyes datasets.
