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
![The comparison](/uploads/UAS_project/data_clean_compare.png "Dataset distribution after cleaning")

Also, I do the data exploration by drawing the pixel distribution and average images.

| ![Average](/uploads/UAS_project/average_image.png "average images for each class") | ![Distribution](/uploads/UAS_project/pixel_distribution.png "Pixel distribution") |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|



### Model selection:
#### ResNet:
This model solved the degradation problem: As the network became deeper and deeper, the error begin to increase - hard to converge.
- Not caused by overfitting, because the training error is also increase
- Not caused by gradients vanishing/exploding, because this problem has been largely addressed by normalization layers.

Core concept - the residual block
- The target weight is near the identity.
- A identity map adding the block-beginning layer feature to the block-ending layer.
- Solve the degradation problem.

![The Resisual block](/uploads/UAS_project/res_block.png "Residual learning: a building block.")

#### EfficientNet:
The author of the EfficientNet firstly using neural architecture search to find the baseline network, which ensures the whole architecture to be smaller and more accurate. And then he proposes a compound scaling method, uniform scale network width, depth and resolution using a composite factor φ. He scaled up the baseline model by this composite factor and come up with the EfficientNet.

To test the robustness of the scaling method, the author applies the scaling method to MobileNets and Resnets, showing that the composite scaling method improves the accuracy of all these models.
![Scaling](/uploads/UAS_project/scale.png "Model Scaling.")


#### AlexNet:
Traditional CNN, just as a control group to evaluate the performance of the EfficientNet and the ResNet.


## Results
We evaluate the model by the training loss/accuracy graph, confusion matrix and the
![Scaling](/uploads/UAS_project/EfficientNet_performance.JPG "Result of EfficientNet.")
