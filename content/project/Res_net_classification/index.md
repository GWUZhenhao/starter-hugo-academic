---
title: Blood cell classification
summary: A deep-learning based medical image classification project.
tags:
  - Deep Learning
date: '2022-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

authors:
  - Zhenhao Zhao

image:
  caption: 
  focal_point: Smart

# links:
#   - icon: twitter
#     icon_pack: fab
#     name: Follow
#     url: https://twitter.com/georgecushen
url_code: ''
url_pdf: ''
url_slides: ''
url_video: ''

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
# slides: example
---

## Project overview

This project using deep learning method to do the classification for the blood smear images. 
We test and compared three classic classification model here: ResNet, EfficientNet and the AlexNet.

## Methods
### Dataset:
Here is the dataset link: https://www.kaggle.com/datasets/paultimothymooney/blood-cells.

The row dataset containing 410 images for 5 classes:
![Show 5 classes](/uploads/UAS_project/5_class.png)

We clean the data by:
>1. Delete 10% of the Neutrophil
>2. Training the less-amount class multi-time
>3. Drop the Basophil class
>4. Drop the double class
>5. Drop the null class
![The comparison](/uploads/UAS_project/data_clean_compare.png "Try the title")

<figure class="half">
    <img src="/uploads/UAS_project/data_clean_compare.png">
    <img src="/uploads/UAS_project/data_clean_compare.png">
</figure>

<div style="text-align: center;">
    <img style="border-radius: 0.3125em;
    box-shadow: 0 2px 4px 0 rgba(34,36,38,.12),0 2px 10px 0 rgba(34,36,38,.08);" 
    src="/uploads/UAS_project/data_clean_compare.png" alt="average picture">
    <br>
    <div style="color:orange; border-bottom: 1px solid #d9d9d9;
    display: inline-block;
    color: #999;
    padding: 2px;">Try the caption</div>
</div>





### Model selection:




## Results
