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
### Dataset
Here is the dataset link: https://www.kaggle.com/datasets/paultimothymooney/blood-cells.

The row dataset containing 410 images for 5 classes:
![Show 5 classes](/uploads/images/project_resnet_1.png)

We clean the data by:
>1. Delete 10% of the Neutrophil
>2. Training the less-amount class multi-time
>3. Drop the Basophil class
>4. Drop the double class
>5. Drop the null class
![The comparison](/uploads/images/project_resnet_2.png "Dataset distribution after cleaning")

Also, I do the data exploration by drawing the pixel distribution and average images.

| ![Average](/uploads/images/project_resnet_3.png "average images for each class") | ![Distribution](/uploads/images/project_resnet_4.png "Pixel distribution") |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------|



### Model selection
#### ResNet
This model solved the degradation problem: As the network became deeper and deeper, the error begin to increase - hard to converge.
- Not caused by overfitting, because the training error is also increase
- Not caused by gradients vanishing/exploding, because this problem has been largely addressed by normalization layers.

Core concept - the residual block
- The target weight is near the identity.
- A identity map adding the block-beginning layer feature to the block-ending layer.
- Solve the degradation problem.

![The Resisual block](/uploads/images/project_resnet_5.png "Residual learning: a building block.")

#### EfficientNet
The author of the EfficientNet firstly using neural architecture search to find the baseline network, which ensures the whole architecture to be smaller and more accurate. And then he proposes a compound scaling method, uniform scale network width, depth and resolution using a composite factor φ. He scaled up the baseline model by this composite factor and come up with the EfficientNet.

To test the robustness of the scaling method, the author applies the scaling method to MobileNets and Resnets, showing that the composite scaling method improves the accuracy of all these models.
![Scaling](/uploads/images/project_resnet_6.png "Model Scaling.")


#### AlexNet
Traditional CNN, just as a control group to evaluate the performance of the EfficientNet and the ResNet.


## Results
We evaluate the model by the training loss/accuracy graph, confusion matrix and the statistic information.

### The result of the EfficientNet
| ![EfficientNet loss graph](/uploads/images/project_resnet_7.png "The loss decreasing graph of the EfficientNet.")            | ![EfficientNet accuracy graph](/uploads/images/project_resnet_8.png "The accuracy increasing graph of the EfficientNet.") |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|

| ![The statistic information](/uploads/images/project_resnet_9.png "The statistic information of the EfficientNet") | ![EfficientNet loss graph](/uploads/images/project_resnet_10.png "The confusion matrix of the EfficientNet."){:height="50%" width="50%"} |
|--------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|

<table rules="none" align="center">
	<tr>
		<td>
			<center>
				<img src="/uploads/images/project_resnet_9.png" width="60%" />
				<font color="AAAAAA">001.jpg</font>
			</center>
		</td>
		<td>
			<center>
				<img src="/uploads/images/project_resnet_9.png" width="60%" />
				<font color="AAAAAA">002.jpg</font>
			</center>
		</td>
	</tr>
</table>

### The result of the ResNet
