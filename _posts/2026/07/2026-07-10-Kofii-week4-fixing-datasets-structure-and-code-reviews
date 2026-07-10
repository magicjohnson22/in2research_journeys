---
title: Week 4 - Fixing datasets, Code reviews, Access to Myriad GPU, Code Merging and TI Planning
date: 2026-07-10
time: "16:30:00"
author: kofii
categories: ["Linux", "Git", "Python", "Learning", "Torchvision", "deeplab", "UNet", "Model training", "OpenEDS", "Mobious", ]
layout: post
---



### Highlights
- I am halfway through the placement now, met various colleagues at ARC, have gotten used to the office and ARC culture. Our supervisors have been really helpful, they pretend like we don't know anything and guide as from scratch which has been really beneficial to me. I have learnt so much more in these past few weeks than I have learnt in University. The exposure to this project, these tools being used has widened my knowledge horizon and I have to thank everyone who has helped me in this journey. I am only halfway through and there is still more to learn and I am looking forward to it
- I attended my first TI Planning with ARC colleagues. This is where the people at ARC meet up once every 3 months to share projects amongst themselves. It was really insightful and eye opening to see all these projects people have to wor on within the next 3 months. This helped me gain even more experience getting into the ARC culture. All of the projects I heard about are really important and can't wait to see the outcomes
- The segmentation fault issue I encountered last week has been resolved. We know have access to Myriad GPU which can run all models (UNet, Deeplabv3 and LRASPP) with the full datasets (Mobious, openEDS and RTI-eyes) and not just the sample data on Github. I am currently reading the documentation regarding Myriad, installing the VPNs needed and will start training latest by next week
- During our 1:1 meetings, I had a code review with 3 of my Ruaridh and Zakaria. This was basically them tracking what I have been getting on with for the past weeks, reviewing the code and suggesting what I could have done better. My code run without any major concerns, I showed them the output of my new model being trained and it produced really impressive results with hardly any overfitting. I also compared the UNet model with Deeplab and did abrief benchmarking of their capacities.
- Now that I have two fully functional models that effectively train at least 2 datasets, will be 3 by next week. I was given a brief introduction to the implementation of Federated Learning during our 1:1s. Will hopefully start with that next week

### Setbacks
- Once again, inconsistency in openEDS dataset. Takes more time to give a structure that the model can easily access and train. I will tweak the data wrangling code Ruaridh and I wrote during our pair programming session to accomodate that, hopefully it works!

### Next Week's Plan
- Meet up with my Mohammed(also working on this project) and try to merge our codes so his augmented data can run on both models and try to fix any merging conflicts 
- Start training all models and datasets (both augmented and raw data) with Myriad GPU and benchmark all results
- After first two points above are completed, I shall get started on Federated Learning