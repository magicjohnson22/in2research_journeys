---
title: Week 6 - U-Net Model training (Cont.)  
date: 2026-07-24
time: "17:00"
author: mmohamoud
categories: ["U-Net", "myriad", "Model","deep learning","training",] # This is optional, list of categories that you want to add
layout: post
---

### Highlights

* Set up my Myriad environment and ran my first successful training after loads of trial and error with modules, paths, and dependencies

* Succesfully trained U-NET on full MOBIUS and OpenEDS datasets , acheiving 86 and 92% model accuracy resepctively.
 
* Found an extra model (SegFormer) which I can possibly utilise down the line which may be more useful.

### Challenges

* RDSS turned out to be really slow throughout the day so I had to copy my dataset over to Scratch storage first before training would actually run as I couldn't train on the RDSS project folder's path.

* Had a frustrating back and forth with modules loading the wrong pytorch version clashed with old CUDA modules still loaded, and even once that was sorted torch kept saying it was unavailable as well as also other modules so I had to add directly into my job script so it could set up the environment (torch, CUDA, etc.) fresh every time it ran

* Kept having all errors along with other small config mistakes like wrong file paths and folder names that only showed up after a job had already been queued and run,despite no errors when running as .py so a lot of  submitting a job, waiting , find a tiny error, fixing and then resubmitting job. 

#### Goals for Following Week

* Train U-Net on RIT-eyes dataset and look to begin benchmarking. 
* Begin training the next model either deeplab or RITnet on all 3 datasets.
* Organise RDSS project folder properly as well as merging and organising git repo.