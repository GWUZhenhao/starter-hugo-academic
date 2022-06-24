---
title: The aneurysm and vessel segmentation for 3D digital subtraction angiography images
summary: A deep-learning based medical image processing algorithm.
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
For this project, the No New U-Net (nnUNet) was used for accurate segmentation of 3D digital subtraction angiography images. The dice coefficient was taken as the evaluation standard, and the accuracy had reached above 90 percent. 

<div class="table">

| Disk 0 | Disk 1 | Disk 2 | Disk 3 |
|:------:|:------:|:------:|:-------:|
|   A1   |   A2   |   A3   | Ap(1-3) |
|   A4   |   A5   |   A6   | Ap(4-6) |
|   B1   |   B2   |   B3   | Bp(1-3) |
|   B4   |   B5   |   B6   | Bp(4-6) |

</div>
