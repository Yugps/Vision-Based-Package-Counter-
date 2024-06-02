# Object Detection Tracker and Counter for Conveyor Belt Packages


## Overview

This project implements an object detection tracker and counter specifically designed for conveyor belt packages in a logistics environment. The system detects packages, tracks their movement, and accurately counts them as they exit the frame. By leveraging YOLOv8, custom datasets, and tracking libraries, this solution addresses the challenge of monitoring package flow in large logistics factories.

- **Before**:
  !first_frame.png

## Features

- **Object Detection with YOLOv8**:
  - YOLOv8 (You Only Look Once) is used for real-time object detection. It efficiently identifies packages (cartons, boxes, etc.) placed on the conveyor belt.
  - The custom dataset, created using Roboflow, ensures that the model is trained specifically for the logistics context.

- **Multi-Directional Flow Tracking**:
  - The conveyor belt handles packages flowing in three directions:
    - **Vertical Downwards (Left)**: Packages move downwards on the left side of the conveyor.
    - **Vertical Upwards (Middle)**: Packages move upwards in the middle section.
    - **Horizontal Towards Right (Exit)**: Packages move horizontally towards the right, exiting the frame.
  - The tracking algorithm ensures continuous monitoring across frames, even when packages change direction.

- **Package Counting and Line Creation**:
  - The system establishes virtual lines or boundaries to count packages as they cross these lines.
  - By integrating the tracking results with the Supervisely library and OpenCV (cv2), the counter accurately tallies the number of packages passing through each section.

## Use Case

In a large logistics factory, manually tracking the number of packages moving around the conveyor belt is nearly impossible. This model provides an automated solution:
- **Theft Prevention**: By analyzing CCTV camera footage, the system detects any irregularities or missing packages, preventing theft.
- **Efficiency Enhancement**: Factory managers can optimize package flow, allocate resources effectively, and identify bottlenecks.
- **Quality Control**: The counter ensures that the expected number of packages reaches the exit, maintaining quality control.

