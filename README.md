# Obstacle Detection for Autonomous Robots

Real-time computer vision project for detecting, segmenting, and interpreting obstacles in autonomous navigation scenarios using RGB-D data.

## Project Overview

This capstone project explored how modern computer-vision models can support autonomous robots operating in dynamic environments. The system was designed around RGB-D inputs, combining standard RGB imagery with depth information so that detected objects could be interpreted with additional spatial context.

The project explored and compared three deep-learning approaches: YOLOv11, RT-DETR, and Mask R-CNN. Together, these models provided different perspectives on the trade-offs between fast object detection, transformer-based detection, and instance segmentation for robotic perception.

## Problem Statement

Autonomous robots need to identify obstacles quickly and reliably in order to navigate safely. A useful perception system must do more than recognize objects in an image; it should also support decisions about where objects are located, how they are shaped, and whether they may interfere with the robot's path.

This project focused on building a perception pipeline that could:

- detect relevant objects in RGB images
- incorporate depth information from RGB-D inputs
- explore both object detection and instance segmentation
- compare multiple deep-learning architectures
- evaluate model outputs for autonomous-navigation use cases
- provide a foundation for downstream path-planning or collision-avoidance logic

## Technical Approach

The project followed a computer-vision workflow centered on model comparison and robotic perception:

1. Prepare RGB-D image data for model input.
2. Train or evaluate models on obstacle classes.
3. Compare detections produced by YOLOv11 and RT-DETR.
4. Explore Mask R-CNN for instance-level segmentation and more detailed object boundaries.
5. Examine detection quality, segmentation behaviour, and practical inference characteristics.
6. Use depth information to add spatial context to detected obstacles.
7. Assess how the perception outputs could support robotic navigation.

## Models Explored

### YOLOv11

YOLOv11 was considered for its suitability for fast object detection and its potential for real-time inference. In a robotics setting, low-latency detection is important because the environment can change continuously while the robot is moving.

### RT-DETR

RT-DETR was explored as a transformer-based real-time detector. It provides a different architectural approach from YOLO-style detectors and was useful for comparing detection quality and inference characteristics.

### Mask R-CNN

Mask R-CNN was explored for instance segmentation in addition to object detection. Unlike bounding-box-only detectors, Mask R-CNN can generate a pixel-level mask for each detected object, making it useful for understanding object shape and spatial boundaries.

For autonomous robotics, this richer segmentation output can be valuable when the system needs more precise information about where an obstacle begins and ends rather than relying only on rectangular bounding boxes.

## RGB-D Perception

Unlike conventional RGB-only vision systems, RGB-D data includes depth information in addition to colour imagery.

This makes it possible to move beyond simply answering:

> What object is present?

and begin answering:

> How far away is the detected object, and where does it occupy space?

That additional spatial information is especially useful for obstacle avoidance, proximity estimation, and autonomous navigation.

## Tools and Technologies

- Python
- PyTorch
- YOLOv11
- RT-DETR
- Mask R-CNN
- OpenCV
- RGB-D image processing
- Computer vision
- Object detection
- Instance segmentation
- Deep learning

## Project Contribution

My work on the capstone focused on the computer-vision component of the autonomous-robotics problem, including:

- researching and comparing modern object-detection and segmentation architectures
- working with RGB-D data for obstacle perception
- exploring YOLOv11, RT-DETR, and Mask R-CNN for the use case
- comparing bounding-box detection with instance-level segmentation
- examining how model outputs could be incorporated into a robotic perception pipeline
- documenting the model-development and evaluation process

The project was completed as part of a capstone collaboration with Kevares Automation Solutions.

## Evaluation

The project was designed to compare models using metrics commonly used in object detection and segmentation, including:

- precision
- recall
- mean Average Precision (mAP)
- inference latency
- detection consistency across object classes
- segmentation quality for Mask R-CNN outputs

Performance values are not published in this repository because the current public version does not yet include the original experimental notebooks, evaluation logs, or result files required to reproduce those measurements.

## Practical Application

A system like this can support autonomous mobile robots in environments such as:

- warehouses
- industrial facilities
- indoor service environments
- research robotics platforms

The perception component can feed information into a larger autonomy stack containing localization, path planning, collision avoidance, and control systems. Detection outputs provide object identity and location, while segmentation and depth information can provide more precise spatial context for navigation decisions.

## Repository Status

This repository currently documents the project architecture and technical approach.

A future revision can include:

- training and evaluation notebooks
- sample RGB-D data
- model configuration files
- quantitative model-comparison results
- detection and segmentation visualizations
- inference examples

## Key Skills Demonstrated

Computer Vision | Object Detection | Instance Segmentation | Deep Learning | PyTorch | OpenCV | YOLOv11 | RT-DETR | Mask R-CNN | RGB-D Processing | Model Evaluation | Autonomous Robotics
