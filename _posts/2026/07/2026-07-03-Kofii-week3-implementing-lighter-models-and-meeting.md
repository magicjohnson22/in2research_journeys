---
title: Week 3- Implementation of lighter weight models, training and validation
date: 2026-07-03
time: "15:00:00"
author: kofii
categories: ["Linux", "Git", "Python", "Learning", "Torchvision", "deeplab", "Model training", "Mobilenetv3_large", "LLRASP"]
layout: post
---



### Highlights
- This week, I started to train the actual datasets (Mobious and openEDS data) on the local CPU device. Miguel Xochicale had requested the full dataset of MOBIOUS for the research so I moved from training the model with the sample data from Github to training it with the lighter-weight model(DEEPLAB).
- The segmentation fault issue I encountered last week was resolved after discussing it in a meeting with my supervisors. I implemented a line of code into the training script where this simply made use of one processor to train the model whereas in reality, multiple process will be used on the GPU
- I researched a a seconf lightweight model (LRASPP) to be able to handle training large datasets on the local CPU device as I did with DEEPLAB last week. The implementation of several models is to perform accurate benchmarking and have enough models for implementing Federated Learning to the Models to maintain data privacy
- After downloading the datasets we were given access to, there seemed to be some inconsistencies in the data files. Everyy image in Mobious is meant to have an associated mask to effectively train the model, however, this wasn't so in the dataset. I met up with Ruaridh and has a pair programming session to by writing code to group images without a mask into a different folder not used by the model in training


### Setbacks
- Regardless of implemmeting two lighter-weight models to train these datasets on a CPU, it still took a huge amount of time; days, to train the model with one dataset. Will raise this up during the project meeting next week to derive a solution to this
- Segmentation fault trying to derive graphs for the difference in validation and training metrics between models and datasets. Will likely work on a GPU machine.   


### Next Week's Plan
- Meet up with my supervisors to discuss my setbacks from earlier and derive a solution
- TI Planning meeting next week; a full day conference were all colleagues from ARC meet up to share and tackle projects amongst each other. Will be a nice experience
- Code review and presentation to our supervisors during our scheduled 1:1 meetings
- Gained access to Myriad and will hopefully train all models on it.