---
title: UGUICanvasScaler
date: 2023-11-12 09:25:00
author: Mrqe
cover: true
summary: UGUICanvasScaler的三种模式
categories: UGUI
tags:
  - unity
  - UGUI
---

# UGUI

## CanvasScaler——恒定物理模式

**Constant Physical Size (恒定物理模式)∶**无论屏幕大小和分辨率如何，UII元素始终保持相同物理大小

**DPI**：( Dots Per Inch，每英寸点数)图像每英寸长度内的像素点数

unity面板：

![unity面板、](https://mrqe-note.oss-cn-chengdu.aliyuncs.com/PicGo/PicGoPicGoPicGoimage-20231113201132615.png)

**Physical Unit:**物理单位，使用的物理单位种类
**Fallback Screen DPI:**备用DPI，当找不到设备DPI时，使用此值

**Default Sprite DPI:**默认图片DPI

### Constant Physical Size

![image-20231113201733148](https://mrqe-note.oss-cn-chengdu.aliyuncs.com/PicGo/image-20231113201733148.png)

Reference Pixels Per Unit(单位参考像素)

新单位参考像素=单位参考像素*Physical Unit / Default Sprite DPI
再使用模式一:恒定像素模式的公式进行计算
原始尺寸=图片大小（像素)/(Pixels Per Unit/新单位参考像素)

#### 恒定像素模式和恒定物理模式区别
相同点:他们都不会进行缩放，图片有多大显示多大，使用他们不会进行分辨率大小自适应

不同点:恒定像素模式相同尺寸不同DPI设备像素点区别，像素点越多细节越多
同样为5像素，DPI较低的设备上看起来的尺寸可能会大于DPI较高的设备