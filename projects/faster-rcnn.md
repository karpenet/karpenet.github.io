---
layout: project
title: Faster-RCNN
desc: Towards Real-Time Object Detection with Region Proposal Networks
favicon: "../img/faster-rcnn.png"
order: 8
---

## Github Repository
[https://github.com/kedarkarpe/Faster-RCNN](https://github.com/kedarkarpe/Faster-RCNN)

## Introduction
In this project we will implement some of the components of MaskRCNN, an algorithm that addresses the task of instance segmentation, which combines object detection and semantic segmentation into a per-pixel object detection framework.

The full implementation of Faster-RCNN would take many days to train, so we will implement a simpler version of the Region Proposal Network that keeps all the necessary components. However, these simplifications affect the performance of the algorithm. In the second parts of the project, we will use pretrained parts to boost the performance.

![Object Detection - State of the Art.](img/faster-rcnn/obj-det.png)

## Model Architecture
The architecture for the RPN and the later refinement of the proposals is shown below:
![Model Architecture.](img/faster-rcnn/arch.png)

## Part 1 - Region Proposal Networks
Region Proposal Networks (RPNs) are ”attention mechanisms” for the object detection task, performing a crude but inexpensive first estimation of where the bounding boxes of the objects should be. They were first proposed as a way to address the issue of expensive greedy algorithms like Selective Search, opening new avenues to end-to-end object detection tasks. They work through classifying the initial anchor boxes into object/background and refine the coordinates for the boxes with objects. Later, these boxes will be further refined and tightened by the instance segmentation heads as well as classified in their corresponding classes.

![Architecture of the Region Proposal Network.](img/faster-rcnn/rpn-arch.png)

### 1. Ground Truth Creation
![Ground Truth Proposal Regions.](img/faster-rcnn/gt-prop.png)
![Top 20 Ground Truth proposals.](img/faster-rcnn/top-20.png)

### 2. Training and Loss Plots
![Fire test of the inkjet cartridge driver.](img/faster-rcnn/trainloss.png)
![First power-on test of the robot.](img/faster-rcnn/classloss.png)
![First power-on test of the robot.](img/faster-rcnn/regloss.png)

### 3. Predicted Outputs
![Pre-NMS Predicted Proposals.](img/faster-rcnn/pre-nms.png)
![Post-NMS Predicted Proposals.](img/faster-rcnn/nms.png)

## Part 2 - Object Detection
### Hi

## References
1. Original YOLO paper: [https://arxiv.org/pdf/1506.02640.pdf](https://arxiv.org/pdf/1506.02640.pdf)
2. Intuitive Explanation: [https://towardsdatascience.com/yolo-you-only-look-once-real-time-object-detection-explained-492dc9230006](https://towardsdatascience.com/yolo-you-only-look-once-real-time-object-detection-explained-492dc9230006)
3. YOLO Video Tutorial: [https://www.youtube.com/watch?v=9s_FpMpdYW8&list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF&index=30](https://www.youtube.com/watch?v=9s_FpMpdYW8&list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF&index=30)
4. mean Average Precision: [https://medium.com/@jonathan_hui/map-mean-average-precision-for-object-detection-45c121a31173](https://medium.com/@jonathan_hui/map-mean-average-precision-for-object-detection-45c121a31173)
5. Intersection over Union: [https://www.pyimagesearch.com/2016/11/07/intersection-over-union-iou-for-object-detection](https://www.pyimagesearch.com/2016/11/07/intersection-over-union-iou-for-object-detection)