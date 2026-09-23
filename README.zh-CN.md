# AIR-Fusion

## 交互式一体化图像恢复与融合 · IJCAI 2026

**论文标题：** Interactive All-in-One Image Restoration and Fusion  
**作者：** Bing Cao、**Qiang Zhang**†、Xingxin Xu、Pengfei Zhu  
† 学生第一作者；作者顺序与正式论文一致。

[项目页](https://qiangzhang-dev.github.io/air-fusion/) · [中文解读](https://qiangzhang-dev.github.io/notes/air-fusion/) · [论文页面](https://www.ijcai.org/proceedings/2026/105) · [论文 PDF](https://www.ijcai.org/proceedings/2026/0105.pdf) · [English](README.md) · [个人主页](https://qiangzhang-dev.github.io/)

> 本仓库提供论文介绍、原始框架图、中文解读与引用信息。代码与模型权重暂未公开。

## 解决什么问题？

红外图像可以突出热目标，可见光图像包含纹理与颜色。但现实中的可见光图像常常受到雨、雾、低照度、噪声或模糊影响：直接融合可能把退化一起带入结果。

AIR-Fusion 探索如何利用预训练扩散模型的恢复能力，在文本指令引导下，同时完成图像恢复与红外–可见光融合。

## 核心思路

1. **保留已有恢复能力。** 冻结具备图像恢复能力的潜空间扩散模型主干。
2. **接入多模态条件。** 通过跨模态桥接适配器 CMBA，将红外信息与文本指令对齐到主干的条件空间。
3. **约束生成过程。** 通过轨迹约束校正器 TCR，在像素与潜空间之间形成闭环，利用源图像结构约束采样并恢复细节。

![AIR-Fusion 整体框架：论文 Figure 2 原图](air-fusion-framework.png)

**图 2：AIR-Fusion 整体框架。** 原图提取自[正式论文第 3 页](https://www.ijcai.org/proceedings/2026/0105.pdf#page=3)，包含文本交互、统一核心架构，以及图像恢复与融合流程。点击图片可查看高清原图。

定量结果、对比设置和局限请以正式论文为准。

## 进一步阅读

[中文论文解读](https://qiangzhang-dev.github.io/notes/air-fusion/)介绍研究动机、CMBA 与 TCR 的设计，以及如何理解实验结果。[项目页](https://qiangzhang-dev.github.io/air-fusion/)提供完整对比表格、原始实验图和局限说明。

## 引用与联系

引用格式见 [英文 README](README.md#citation)，也可以使用 GitHub 的 “Cite this repository” 入口引用论文。

维护者：**Qiang (Nate) Zhang**  
联系邮箱：[zhangqiang_c@outlook.com](mailto:zhangqiang_c@outlook.com)
