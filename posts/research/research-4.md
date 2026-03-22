---
id: research-4
emoji: 
image: "images/research/flowfill.jpg"
date: 2022-06-03
title: Diverse Image Inpainting with Normalizing Flow
title_zh: 基于流模型等多样性图片补全
excerpt: ECCV2022
excerpt_zh: ECCV2022
---

# [Diverse Image Inpainting with Normalizing Flow](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136830053.pdf)

## Abstract

We propose Flow-Fill an inpainting framework that utilizes a conditional normalizing flow model to generate diverse structural priors. Flow-Fill achieves a real-time inference speed that is approximately **87 times** faster than autoregressive-based models and **142 times** faster than diffusion-based models.

## Methodology
- Learn Structural Priors. We use a conditional normalizing flow to model diverse structural priors.
- Guided Texture Generation. The structural priors obtained in the first stage are low-resolution and have no texture details. In the second stage, we upsample the image and generate texture.

## [Project WebPage 🔗](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136830053.pdf)

---zh---

# [基于流模型等多样性图片补全](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136830053.pdf)

## 摘要
我们提出了一种名为 Flow-Fill 的图像修复框架，它利用条件归一化流模型生成多样化的结构先验。Flow-Fill 的实时推理速度比基于自回归的模型快约 **87 倍**，比基于扩散的模型快约 **142 倍**。

## 方法论

- 学习结构先验。我们使用条件归一化流来建模不同的结构先验。

- 引导纹理生成。第一阶段获得的结构先验分辨率较低，缺乏纹理细节。在第二阶段，我们对图像进行上采样并生成纹理。

## [项目主页 🔗](https://www.ecva.net/papers/eccv_2022/papers_ECCV/papers/136830053.pdf)

