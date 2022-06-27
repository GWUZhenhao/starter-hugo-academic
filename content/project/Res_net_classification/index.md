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
>Delete 10% of the Neutrophil
>Training the less-amount class multi-time
>Drop the Basophil class
>Drop the double class
>Drop the null class
![The comparison](/uploads/UAS_project/data_clean_compare.png)




### Model selection:




## Results
