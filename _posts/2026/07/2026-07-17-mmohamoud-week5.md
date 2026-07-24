---
title: Week 5 - U-Net Model training  
date: 2026-07-17
time: "17:00"
author: mmohamoud
categories: ["U-Net", "deep learning", "Model","benchmarking","training"] # This is optional, list of categories that you want to add
layout: post
---

### Highlights

This week marks the midpoint of my placement , which has flown by over the course of the past 5 weeks I have gained proficiency in git , VScode and python. I have now completed my preprocessing pipeline , minus a few changes that will be implemented as I continue utilising it in the training of my deep learning models and upon merging with the original repository.I have now moved onto starting my second placement objective of benchmarking 3+ deep learning models and their results/metrics on the 3 datasets;mobious,openEDS and RIT eyes. I began training my U-Net model on the mobious dataset and have achieved a model accuracy of 89.7% which is a big positive but this was only with a smaller sample size to having issues with cluster access so will retrain with the full dataset + added augmenetations from preprocessing pipeline to increase the size on myriad upon sorting out cluster access. I have also began training on openEDS but have had trouble with training openEDS locally due to overheating and laptop crashing. I have also found 1 new model that I will use in the benchmarking but due to its similarity with my current U-Net model I am looking to find another deep learning model to provide a better comparison.


### Challenges

* Pre training on openEDS I spent a day editing code/debugging errors due to many different issues including incorrect inputted image shapes, dimensions errors as the augementations applied to some of the images were rotation by 90 and 270 degrees causing dimension to change from "640x400" to '400x640'. 

* Issues with masks for openEDS as they were in ".png" format whereas the code was expecting ".npy" masks.

* Issues with PC crashing on epoch 4/5 each time looking to retrain on myriad. 

#### Goals for Following Week

* Once cluster access is available train at least 1 model on all 3 datasets so far able to train mobious and openEDS on U-Net as well as mobious on deeplab.
* Clean up git fork ahead of merging with main repo or seperate joint repo.
* Find an extra model as a potential backup/replacement for Attention U-Net