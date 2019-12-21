---
layout: post
title:  "资源导入设置"
date:   2019-12-19
excerpt: "项目中模型、纹理、音频资源导入设置方案记录"
tag:
- mmorpg
- 手游
comments: false
---
## 概要

虽然现在手机内存普遍都非常大了，但因为项目需要面向中低端机，且ios内存比较小，所以对内存优化管理需要谨小慎微的进行。在项目中，针对不同的平台，在资源导入的时候做了差异化设置，在这里做下记录。

## 模型

* `meshCompression`：压缩比越高模型文件越小。地形模型设置为`Low`，其他像是人物、怪物、特效的模型设为`Hight`。
* `Read/Write Enable`：不需要运行时修改模型的统一**关闭**，像是地形模型需要进行静态合批的需要开启。
* `Optimize Mesh`：**开启**，可提升GPU性能。
* `Normals`：不需要法线信息，设置为`None`，减小模型大小。
* `Optimize Game Objects`：**启用**。将暴露在Hierarchy的子节点移除。
* `Anim. Compression`：使用`Optimal`,会比`Keyframe Reduction`节省约50%大小。
* `Import Lights`：项目中并不需要，**关闭**。
* `Index Format`：Mesh Index buffer 的大小，项目中使用`16bit`(最多65535个顶点)

## 纹理

* `Read/Write Enable`：不需要运行时读取图片像素信息则**禁用**。开启会增加一倍的内存消耗。
* `Generate Mip Maps`：如果不是3D模型贴图，则禁用，否则会多出约33%的内存开销。Mipmaps主要为远处的物件生成较为清晰的小贴图，减少渲染导致的画质损失。像UI贴图，则完全用不到。在项目中全部关闭了。
* `Max Size`：统一设为**2048**。
* `Format`：
   * `Android`：透明贴图`ETC2_RBGA8`，不透明贴图`ETC2_RGB`，高质量贴图`RGBA 16`。
   * `IOS`：ui贴图`ASTC_RGBA_6x6`，透明贴图`PVRTC_RGBA4`，不透明贴图`PVRTC_RGB4`,高质量贴图**RGBA 16**
* `Compression Quality`：视贴图需求的质量来定。品质越高则贴图越大。

## 音频

* `Force To Mono`：启用。
* `Load Type`：使用`Compressed In Memory`,边播边解压。
* `Compression Format`：使用`Vorbis`，压缩比较高。

## 资料

[Unity性能优化 – 设置篇](https://wuzhiwei.net/unity-settings-optimization/)  

[unity贴图格式](https://blog.csdn.net/studyinroom/article/details/90479419)  

## 项目地址

github地址：[场景编辑器](https://github.com/V1nChy/Game-Scene-Editor)