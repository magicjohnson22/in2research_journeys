---
title: Week 4 - Finalising preprocessing package 
date: 2026-07-10
time: "15:00"
author: mmohamoud
categories: ["Shutil", "python", "openEDS","data-wrangling","RIT-eyes","npy","conversion" , ] # This is optional, list of categories that you want to add
layout: post
---

### Highlights

* On Monday this week, I attended the TI planning at Bidsborough House. This was a really interesting experience as I was able to see how the different projects were planned and divided. I also had the chance to meet all my supervisors, Zakaria, Ruaridh and Miguel, in person and speak about my project progress.

* I was also able to update my mask-matching script for OpenEDS and fully sort the dataset, with the images in `.png` format and the masks in `.npy` format, into separate folders. I then produced a `.npy` to `.png` conversion script to convert all 27,431 `.npy` masks into `.png`.

* After having issues with storage over the previous weeks, I was able to free up 100 GB of space, which allowed me to download the third dataset, RIT-Eyes, and begin sorting the data.

* This week, I also continued working on my preprocessing package and successfully trialled producing augmentations from all 3 datasets. I mainly worked on fixing and producing separate scripts for sorting the OpenEDS and RIT-Eyes datasets. Since all 3 datasets have different folder structures, I decided to produce separate sorting and data-wrangling scripts for each one.

### Challenges

* The RIT-Eyes dataset has a different folder structure compared with the MOBIUS and OpenEDS datasets, so I had to produce a separate sorting script. The images and masks also have the same stem and are both in `.tif` format, so my mask-matching script needs to be updated again.

* I implemented `shutil` to help move and organise files within my sorting scripts. This was useful for automating the data-wrangling process, but it also meant I had to be careful with the selected file paths and checking that images and masks were moved correctly as I run prematurely and had to redownload dataset due to having partial sorting.

#### Goals for Following Week

* Complete the preprocessing package and merge, or be ready to merge, my work with the original repo and Kofi’s work.

* Begin training U-Net on augmented images and familiarise myself with at least 1 other model from the research, so I can work towards benchmarking 3 models against each other.

* ![Bring it Home](123.png)
