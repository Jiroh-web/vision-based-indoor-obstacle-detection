# Vision-Based Indoor Obstacle Detection System

## Overview
This project demonstrates a real-time computer vision system for indoor obstacle detection.
The system uses a YOLOv11n object detection model to identify common indoor objects such as chairs, tables, and people. By combining object detection with distance estimation, the system determines whether obstacles are within a predefined safety threshold.
The purpose of this project is to explore how computer vision can improve environmental awareness and support navigation in indoor spaces.
This repository focuses on the AI-based obstacle detection and decision logic used to determine when navigation guidance should be triggered.

## System Concept
The system performs the following steps:
1. Capture RGB images from a depth camera
2. Detect indoor obstacles using a YOLOv11n model
3. Estimate the distance to detected objects
4. Determine whether the obstacle is within a safety threshold
5. Trigger navigation guidance logic (left / center / right)

The audio output module is handled by an external microcontroller and is not included in this repository.

## Model
Model: YOLOv11n  
Training platform: Google Colab  
Training dataset: Custom indoor obstacle dataset from roboflow

Classes:
- Chair - Table - Person

Images:
- All: 7686
- Chair: 2572
- Table: 2689
- Person: 2749

Instances:
- All: 14216
- Chair: 6243
- Person: 4801
- Table: 3172
  
The model is optimized for real-time indoor obstacle detection.

## Results
The trained model achieved strong performance
- Precision: 91%
- Recall: 82%
- mAP@50: 88%

The system runs in real time and can continuously monitor the surrounding environment for potential obstacles.

## Repository Scope

This repository includes only the computer vision and obstacle detection components of the assistive walker prototype.
Hardware integration, audio output, and microcontroller code are not included.

## Future Work
Future improvements include:

- Improving detection accuracy in crowded environments
- Expanding detectable object categories
- Optimizing performance for embedded devices
- Enhancing navigation decision logic

## Acknowledgment
This work was developed as part of a collaborative student project.  
This repository contains only the computer vision components implemented by the author.
