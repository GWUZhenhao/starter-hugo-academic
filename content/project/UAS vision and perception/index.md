---
title: Camera Vision based Perception for UAS Autonomous Landing
summary: A deep-learning based UAS perception algorithm.
tags:
  - Deep Learning
date: '2022-04-27T00:00:00Z'

# Optional external URL for project (replaces project detail page).
external_link: ''

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

The use of small Unmanned Aircraft Systems (UAS) is promising for last-mile package delivery. Commercial small
UASs have become more and more automated in executing a pre-defined flight plan and landing in a well-clear landing
pad. However, to achieve higher level autonomy during an off-nominal landing, a UAS needs to recognize landing scene
reconfiguration such as moving or static obstacles near/on the designated landing pad. These obstacles often include
people, pets, cars, and bikes. We explore the feasibility of using camera vision based perception to (1) identify the
landing pad, and (2) detect the obstacles near or on the landing pad. An accurate, fast and reliable perception module is
a key component for a fully autonomous landing stack, together with a prediction module and planning/control module.
In this project, we focus on implementing and evaluating two state-of-the-art deep learning models for UAS perception,
RetinaNet and YOLOv5. We compare the two models’ object detection accuracy and the computation speed with
real-world landing videos. 

# Result
