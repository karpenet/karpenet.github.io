---
layout: project
title: Segformer
desc: Semantic Segmentation with Transformers
favicon: "../img/segformer.gif"
order: 9
---

## Building the SegFormer Model Architecture
Instead of using a pre-built model, I decided to implement the SegFormer architecture from scratch to gain a deeper understanding of its inner workings. Here’s a brief outline of the architecture:

1. Backbone (Transformer Encoder): The core of SegFormer is based on a transformer encoder that processes image patches. The input image is split into patches, each of which is embedded and passed through the transformer layers.
2. Multi-scale Features: The model extracts features at multiple scales, allowing it to capture both fine and coarse details within an image.
3. Lightweight Decoder: The output of the transformer is passed through a lightweight decoder that up-samples the features to generate the final segmentation mask.

<iframe src="https://wandb.ai/karpenet-uofpenn/Segformer-B0/reports/Segformer-B0-Training-Run--Vmlldzo5NTU4OTIw?accessToken=70zinxzi3m6f7qyktsj9zzk6rwdqdkti4xzdfu1c8c40qdx4u3bz6loq5uqsmgl9" style="border:none;height:1024px;width:100%">

