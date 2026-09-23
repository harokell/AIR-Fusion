# AIR-Fusion

### Interactive All-in-One Image Restoration and Fusion · IJCAI 2026

Bing Cao, **Qiang Zhang**†, Xingxin Xu, Pengfei Zhu  
† First student author

[Project page](https://qiangzhang-dev.github.io/air-fusion/) · [Paper](https://www.ijcai.org/proceedings/2026/105) · [PDF](https://www.ijcai.org/proceedings/2026/0105.pdf) · [BibTeX](https://www.ijcai.org/proceedings/2026/bibtex/105) · [中文解读](https://qiangzhang-dev.github.io/notes/air-fusion/) · [中文介绍](README.zh-CN.md) · [Qiang's homepage](https://qiangzhang-dev.github.io/)

> **Repository status:** Paper overview, original figures, a Chinese research note and citation are available. Implementation and model weights are not publicly available.

## Overview

AIR-Fusion studies how to restore degraded images while combining infrared and visible information. It adapts a frozen, restoration-capable latent diffusion model using infrared cues and text instructions, rather than fully fine-tuning the backbone.

The method addresses image fusion under challenging conditions such as rain, haze, low light, noise and blur.

## Method at a glance

- **Frozen restoration backbone:** preserves the restoration priors of a pretrained latent diffusion model.
- **Cross-Modal Bridging Adapter (CMBA):** aligns infrared cues and text instructions with the backbone's conditioning space and injects them into multi-scale denoising features.
- **Trajectory-Constrained Rectifier (TCR):** uses source-image structure in a pixel–latent loop to constrain sampling and recover fine detail.

![AIR-Fusion overall framework — original Figure 2 from the paper](air-fusion-framework.png)

**Figure 2. Overall framework of AIR-Fusion.** Original figure from the [published paper (page 3)](https://www.ijcai.org/proceedings/2026/0105.pdf#page=3), showing text interaction, the unified core architecture and the restoration–fusion process. Click the image to view it at full resolution.

## Results and further reading

The paper reports experiments across multiple datasets and degradation settings. Refer to the published tables and figures for quantitative results, comparison protocols and limitations.

The [project page](https://qiangzhang-dev.github.io/air-fusion/) presents the published comparisons and limitations. The [Chinese research note](https://qiangzhang-dev.github.io/notes/air-fusion/) explains the motivation, CMBA and TCR, and how to interpret the experiments.

## Citation

```bibtex
@inproceedings{ijcai2026p105,
  title     = {Interactive All-in-One Image Restoration and Fusion},
  author    = {Cao, Bing and Zhang, Qiang and Xu, Xingxin and Zhu, Pengfei},
  booktitle = {Proceedings of the Thirty-Fifth International Joint Conference on Artificial Intelligence, {IJCAI-26}},
  publisher = {International Joint Conferences on Artificial Intelligence Organization},
  editor    = {Diego Calvanese},
  pages     = {935--943},
  year      = {2026},
  month     = {8},
  note      = {Main Track},
  doi       = {10.24963/ijcai.2026/105},
  url       = {https://doi.org/10.24963/ijcai.2026/105}
}
```

## Contact

Maintained by **Qiang (Nate) Zhang**. For questions about the paper, open an issue or email [zhangqiang_c@outlook.com](mailto:zhangqiang_c@outlook.com).
