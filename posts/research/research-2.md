---
id: research-2
emoji: 
image: "images/research/dynamixer.jpg"
date: 2023-03-15
title: DynaMixer:A Vision MLP Architecture with Dynamic Mixing
title_zh: DynaMixer:具有动态编码功能的 Vision MLP 架构
excerpt: ICML2022
excerpt_zh: ICML2022
---

# [DynaMixer:A Vision MLP Architecture with Dynamic Mixing](https://arxiv.org/pdf/2201.12083)

## Abstract

This work proposes a pure **MLP architecture** that rivals the attention mechanism from a mathematical perspective, achieving optimal performance with the same parameters.

## Methodology
```python
Algorithm 1 Pseudo-code for DynaMixer Block (PyTorchlike)
###### initializaiton #######
proj_c = nn.Linear(D, D)
proj_o = nn.Linear(D, D)
###### code in forward ######
def dyna_mixer_block(self, X):
H, W, D = X.shape
# row mixing
for h = 1:H
Y_h[h,:,:] = DynaMixerOp_h(X[h,:,:])
# column mixing
for w = 1:W
Y_w[:,w,:] = DynaMixerOp_w(X[:,w,:])
# channel mixing
Y_c = proj_c(X)
Y_out = Y_h + Y_w + Y_c
return proj_o(Y_out)
```

## [Project WebPage 🔗](https://github.com/ziyuwwang/DynaMixer)


---zh---

# 通过几何与遮挡感知构建3D GAN反演编码器

## 摘要

这是一项**开源**工作，它仅需单张图像输入即可同时实现高保真度的重建和合理的3D几何形状。我们的工作可应用于新视角合成和3D一致性编辑。

## 方法论

我们的框架可以分为两部分：

- W 空间反转。我们设计了一个编码器 E，将输入图像 I 反转为 w+ 个潜在编码。

- F 空间补全。我们计算输入图像与其重建图像之间的图像残差 △I，并提出 AFA 模块来优化 F 潜在映射。

## [项目主页 🔗](https://github.com/ziyuwwang/DynaMixer)

