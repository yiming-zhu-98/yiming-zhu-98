---
id: research-2
emoji: 
image: "images/research/dynamixer.jpg"
date: 2022-12-15
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

# DynaMixer:具有动态编码功能的 Vision MLP 架构

## 摘要

这项工作提出了一种纯粹的**MLP架构**，从数学角度来看，它能够与注意力机制相媲美，并在相同的参数下实现最佳性能。

## 方法论

```python
算法 1 DynaMixer Block的伪代码   (PyTorch风格)
###### 初始化投影矩阵 #######
proj_c = nn.Linear(D, D)
proj_o = nn.Linear(D, D)
###### forward函数代码 ######
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

## [项目主页 🔗](https://github.com/ziyuwwang/DynaMixer)

