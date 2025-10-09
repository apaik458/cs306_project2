# COMPSYS 306 Project 2

## Directory Guide

```dataset``` - Collected and augmented sign classification dataset

```models``` - Trained models

```scripts``` - Python scripts/notebooks

## Running Model on Jetbot

In progress

## Model Description

Model input: 224x224x3 tensor
- 224x224 RGB image

Model output: enumeration (probability distribution)
- [NOTHING, STOP, SLOW, GREEN, YELLOW, SHEEP]

Multinomial logistic regression
- Multi-class classification model that outputs probabilities of input belonging to each class (use threshold values to make prediction)

## Dataset Collection

**Dataset Gathering**
- Take 36 photos at detection range and 36 photos out of detection range for each sign
- Distances: 0cm (detection), 5cm, 10cm, 15cm
- At each out of detection range, take photos at 3 horizontal and 3 vertical angles (total 9)
- At each detection range, take photos at 4 horizontal and 4 vertical angles (total 16)

**Dataset Augmentation**

Orientation/position transformations
- Rotation
- Shear (to simulate different angles of view)
- Blur (to simulate movement)

Colour/lighting transformations
- Brightness
