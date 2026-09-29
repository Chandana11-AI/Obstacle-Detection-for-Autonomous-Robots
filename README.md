# Obstacle Detection for Autonomous Robots

Real-time computer vision project for detecting and classifying obstacles in autonomous navigation scenarios using RGB-D data.

## Project Overview

This capstone project explored how modern object-detection models can support autonomous robots operating in dynamic environments. The system was designed around RGB-D inputs, combining standard RGB imagery with depth information so that detected objects could be interpreted with additional spatial context.

The project compared deep-learning approaches including YOLOv11 and RT-DETR, with a focus on practical obstacle detection, model behaviour, and suitability for near-real-time robotic perception.

## Problem Statement

Autonomous robots need to identify obstacles quickly and reliably in order to navigate safely. A useful perception system must do more than recognize objects in an image; it should also support decisions about where objects are located and whether they may interfere with the robot's path.

This project focused on building a perception pipeline that could:

- detect relevant objects in RGB images
- incorporate depth information from RGB-D inputs
- compare multiple object-detection architectures
- evaluate model outputs for autonomous-navigation use cases
- provide a foundation for downstream path-planning or collision-avoidance logic

## Technical Approach

The project followed a typical computer-vision workflow:

1. Prepare RGB-D image data for model input.
2. Train or evaluate object-detection models on obstacle classes.
3. Compare detections produced by YOLOv11 and RT-DETR.
4. Examine detection quality and practical inference behaviour.
5. Use depth information to add spatial context to detected obstacles.
6. Assess how the pipeline could support robotic navigation.

## Models Explored

### YOLOv11

YOLOv11 was considered for its suitability for fast object detection and its potential for real-time inference. In a robotics setting, low-latency detection is important because the environment can change continuously while the robot is moving.

### RT-DETR

RT-DETR was explored as a transformer-based real-time detector. It provides a different architectural approach from YOLO-style detectors and was useful for comparing detection quality and inference characteristics.

## RGB-D Perception

Unlike conventional RGB-only vision systems, RGB-D data includes depth information in addition to colour imagery.

This makes it possible to move beyond simply answering:

> What object is present?

and begin answering:

> How far away is the detected object?

That additional spatial information is especially useful for obstacle avoidance, proximity estimation, and autonomous navigation.

## Tools and Technologies

- Python
- PyTorch
- YOLOv11
- RT-DETR
- OpenCV
- RGB-D image processing
- Computer vision
- Object detection
- Deep learning

## Project Contribution

My work on the capstone focused on the computer-vision component of the autonomous-robotics problem, including:

- researching and comparing modern object-detection architectures
- working with RGB-D data for obstacle perception
- evaluating YOLOv11 and RT-DETR for the use case
- examining how detection outputs could be incorporated into a robotic perception pipeline
- documenting the model-development and evaluation process

The project was completed as part of a capstone collaboration with Kevares Automation Solutions.

## Evaluation

The project was designed to compare models using metrics commonly used in object detection, including:

- precision
- recall
- mean Average Precision (mAP)
- inference latency
- detection consistency across object classes

Performance values are not published in this repository because the current public version does not yet include the original experimental notebooks, evaluation logs, or result files required to reproduce those measurements.

## Practical Application

A system like this can support autonomous mobile robots in environments such as:

- warehouses
- industrial facilities
- indoor service environments
- research robotics platforms

The object detector acts as one component of a larger autonomy stack. Its outputs can be combined with depth estimation, localization, path planning, and control systems to help a robot respond to obstacles in its surroundings.

## Repository Status

This repository currently documents the project architecture and technical approach.

A future revision can include:

- training and evaluation notebooks
- sample RGB-D data
- model configuration files
- quantitative model-comparison results
- detection visualizations
- inference examples

## Key Skills Demonstrated

Computer Vision | Object Detection | Deep Learning | PyTorch | OpenCV | YOLOv11 | RT-DETR | RGB-D Processing | Model Evaluation | Autonomous Robotics
