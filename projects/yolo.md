---
layout: project
title: YOLO
desc: Object Detection using Deep Convolutional Networks
favicon: "../img/yolo.png"
order: 7
---

## Github Repository
[https://github.com/kedarkarpe/YouOnlyLookOnce-SmPl](https://github.com/kedarkarpe/YouOnlyLookOnce-SmPl)

## Introduction
Object detection is a fundamental task in computer vision. The problem of object recognition essentially consists of first localizing the object and then classifying it with a semantic label. In recent deep learning based methods, YOLO is an extremely fast real time multi object detection algorithm.

![YOLO Predicted Classes.](../img/yolo/yolo_strip.png)

## Model Architecture
<div style="text-align:center">
    <img src="../img/yolo/model_arch.png" width="75%">
    <figcaption>Fig: YOLO model layer details</figcaption>
</div>

## Implementation
<div style="text-align:center">
    <img src="../img/yolo/yolo_arch.png" width="75%">
    <figcaption>Fig: Training pipeline for YOLO</figcaption>
</div>

## Results
<div style="text-align:center">
    <img src="../img/yolo/yolo_pred.png" width="75%">
    <figcaption>Fig: Original and Predicted bounding boxes by the model</figcaption>
</div>

## References
1. Original YOLO paper: [https://arxiv.org/pdf/1506.02640.pdf](https://arxiv.org/pdf/1506.02640.pdf)
2. Intuitive Explanation: [https://towardsdatascience.com/yolo-you-only-look-once-real-time-object-detection-explained-492dc9230006](https://towardsdatascience.com/yolo-you-only-look-once-real-time-object-detection-explained-492dc9230006)
3. YOLO Video Tutorial: [https://www.youtube.com/watch?v=9s_FpMpdYW8&list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF&index=30](https://www.youtube.com/watch?v=9s_FpMpdYW8&list=PLkDaE6sCZn6Gl29AoE31iwdVwSG-KnDzF&index=30)
4. mean Average Precision: [https://medium.com/@jonathan_hui/map-mean-average-precision-for-object-detection-45c121a31173](https://medium.com/@jonathan_hui/map-mean-average-precision-for-object-detection-45c121a31173)
5. Intersection over Union: [https://www.pyimagesearch.com/2016/11/07/intersection-over-union-iou-for-object-detection](https://www.pyimagesearch.com/2016/11/07/intersection-over-union-iou-for-object-detection)