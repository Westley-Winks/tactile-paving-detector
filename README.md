# Tactile Paving Mapper: Project Overview
---
- Scraped over 12,000 images and iterated through several CNN architectures to classify whether or not an image contained tactile paving
- Due to messy crowd-sourced data, models did no better than guessing.
- I messaged the authors of [this](https://doras.dcu.ie/26261/) paper and they were kind enough to send me 2,119 annotated images. Huge shout out to them!

## Problem
---
This project had many inspirations: [this](https://99percentinvisible.org/episode/curb-cuts/) 99 Percent Invisible podcast, [this](https://medium.com/towards-data-science/garbage-route-optimization-using-computer-vision-object-detection-17a217d5582d) trash mapping article, and [this](https://doras.dcu.ie/26261/) research paper.

People with vision problems need resources in the built world to help them navigate it. One of these resources are known as tactile paving: the usually yellow mats of raised bumps found at intersections. When someone using a cane feels this tactile paving, they know that they are at an intersection and should proceed with caution before walking across the intersection.

Cities should be built around the people that live there. But how do we know if our cities are, in fact, accessible and inclusive? What if we could push images of our cities through a machine learning model and produce a heatmap of where infrastructure building should be prioritized?

That is the goal of this project. A machine learning model with be trained to detect tactile paving in an image. EXIF data will be pulled from the images to get a approximate location for generating a heat map. This can be used by city government and citizens alike to get a better understanding of the accessibility landscape of their built environment, wherever that may be.

## Tools
---
**Packages:** requests, matplotlib, tensorflow, keras

**Environment:** conda, Jupyter, VSCode

## Data
---
- All the data is from the kind folks at the [Crowd4Access Project!](https://crowd4access.insight-centre.org/)
- Data was crowd sourced by citizens in Ireland generating photos of streets and footpaths
- Over 2,000 of these images were annotated by hand to create a bounding box around the tactile paving in those images

## Model
---
- Will try a transformer model using Hugging Face
- Will try a YOLO model

## Future Work
---
- Try other base models (YOLO, etc.)
- Try DETR with a different convolutional backbone
- Once sufficiently accurate: Map Bend, OR!

## References
---
- Venkatesh G M, Bianca Pereira, and Suzanne Little. Urban Footpath Image Dataset to Assess Pedestrian Mobility. *UrbanMM ’21, October 20–24, 2021, Virtual Event, China*
- Rodrigo Fuentes. Garbage Route Optimization Using Computer Vision Object Detection
- Francois Chollet. Deep Learning with Python. ISBN 9781617294433
- NielsRogge. Tutorial notebook using balloons. https://github.com/NielsRogge/Transformers-Tutorials/blob/master/DETR/Fine_tuning_DetrForObjectDetection_on_custom_dataset_(balloon).ipynb
- https://huggingface.co/docs/transformers/training#finetuning-in-native-pytorch