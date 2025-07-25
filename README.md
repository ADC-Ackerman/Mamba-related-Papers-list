# Mamba相关文献整理

本贴旨在整理我们阅读到的Mamba相关文献，后续会对文献、目录和其他内容持续优化，欢迎大家与我们一起学习交流！
<br><br>
## 相关论文

### Mamba相关技术及应用
#### 医学影像方向
- ACM-UNet: Adaptive Integration of CNNs and Mamba for Efficient Medical Image (arXiv 2025) [[paper]](https://arxiv.org/abs/2505.24481) [[code]](https://github.com/zyklcode/ACM-UNet)  
  **介绍**：提出CNN与Mamba的自适应融合架构，通过参数共享机制提升医学图像分割效率，在脑肿瘤分割任务中实现20%推理加速。

- DGFE-Mamba: Mamba-Based 2D Image Segmentation (JBE 2025) [[paper]](https://doi.org/10.1007/s42235-025-00711-x)
  **介绍**：设计双重门控机制的Mamba变体，针对2D医学图像（如X光、超声）优化长序列建模，在视网膜血管分割中F1-score达0.89。

- Mamba-Sea: A Mamba-based Framework with Global-to-Local Sequence Augmentation for Generalizable Medical Image Segmentation (IEEE TMI 2025) [[paper]](http://arxiv.org/abs/2504.17515) [[code]](https://github.com/orange-czh/Mamba-Sea)  
  **介绍**：提出"全局-局部"注意力机制，通过多尺度特征融合提升跨模态（CT/MRI）医学图像泛化能力，在ISBI 2025挑战赛中排名前三。

- MSVM-UNet: Multi-Scale Vision Mamba UNet for Medical Image (arXiv 2024) [[paper]](http://arxiv.org/abs/2408.13735) [[code]](https://github.com/gndlwch2w/msvm-unet)  
  **介绍**：将Mamba与U-Net结合，设计多尺度视觉模块处理不同大小的医学目标，在肝脏分割任务中实现92.7%的Dice系数。

- U-Mamba: Enhancing Long-range Dependency for Biomedical Image (arXiv 2024) [[paper]](http://arxiv.org/abs/2401.04722) [[code]](https://github.com/bowang-lab/U-Mamba)  
  **介绍**：通过引入酉变换改进Mamba，增强生物医学图像中的长距离依赖建模，在病理切片细胞核分割中减少15%的假阴性。

- VMamba: Visual State Space Model (NeurIPS 2024) [[paper]](https://arxiv.org/abs/2401.10166) [[code]](https://github.com/MzeroMiko/VMamba)
  **介绍**：首次将 Mamba 的状态空间模型（SSM）扩展到视觉领域，提出视觉状态空间建模框架。通过引入位置感知门控机制，VMamba 在病理切片细胞核分割中实现了比传统 Transformer 快 3 倍的推理速度，同时保持 91.2% 的 Dice 系数。

- LightM-UNet: Mamba Assists in Lightweight UNet for Medical Image Segmentation (arXiv 2024) [[paper]](https://arxiv.org/abs/2403.05246) [[code]](https://github.com/MrBlankness/LightM-UNet)
   **介绍**：设计轻量化 Mamba 模块替代传统 UNet 的卷积层，在保持模型参数量低于 5MB 的同时，显著提升小目标（如乳腺微钙化）的检测精度。在 INbreast 数据集上，LightM-UNet 的 AUC-ROC 达 0.94，较基线提升 7%。

- Swin-UMamba: Mamba-based UNet with ImageNet-based pretraining (arXiv 2024) [[paper]](https://arxiv.org/abs/2402.03302) [[code]](https://github.com/JiarunLiu/Swin-UMamba)  
   **介绍**：结合 Swin Transformer 的层次化结构与 Mamba 的长序列建模能力，通过 ImageNet 预训练初始化 Mamba 参数。在腹部 CT 多器官分割任务中，Swin-UMamba 的平均 Dice 系数达 0.89，较纯 CNN 模型提升 5.3%。

- GroupMamba: Parameter-Efficient and Accurate Group Visual State Space Model (CVPR 2025) [[paper]](https://arxiv.org/abs/2407.13772v1) [[code]](https://github.com/Amshaker/GroupMamba)  
  **介绍**：提出分组参数化Mamba，在保持模型精度的同时减少50%参数量，在ChestX-ray14数据集上实现82.3%的AUC。

- JamMa: Ultra-lightweight Local Feature Matching with Joint Mamba (CVPR 2025) [[paper]](https://arxiv.org/abs/2503.03437) [[code]](https://github.com/leoluxxx/JamMa)  
  **介绍**：设计轻量级Mamba架构用于医学图像特征匹配，在肺部CT配准任务中实现0.8mm的平均误差，模型仅1.2MB。

- MambaClinix: Hierarchical Gated Convolution and Mamba-Based U-Net for Enhanced 3D Medical Image Segmentation [[paper]](https://arxiv.org/abs/2409.12533) [[code]](https://github.com/CYB08/MambaClinix-PyTorch)  
  **介绍**：结合门控卷积与Mamba构建3D分割网络，在脑部MRI体积分割中比传统U-Net减少30%训练时间。

- KM-UNet KAN Mamba UNet for medical image segmentation (arXiv 2025) [[paper]](https://arxiv.org/abs/2501.02559) [[code]](https://github.com/2760613195/KM_UNet)  
  **介绍**：提出知识感知Mamba（KAN）模块，通过整合先验解剖知识提升分割精度，在胰腺分割任务中超越SOTA方法。

- Multi-Scale VMamba: Hierarchy in Hierarchy Visual State Space Model (arXiv 2025) [[paper]](https://arxiv.org/abs/2405.14174) [[code]](https://github.com/YuHengsss/MSVMamba)
  **介绍**：构建多层级 Mamba 架构，通过跨尺度状态交互增强多分辨率特征融合。在眼底血管分割任务中，Multi-Scale VMamba 的 F1-score 达 0.91，尤其对直径 < 50μm 的微血管检测率提升 12%。

- MSM-UNet: A medical image segmentation method based on wavelet transform and multi-scale Mamba-UNet (ESWA 2025) [[paper]](https://www.sciencedirect.com/science/article/pii/S0957417425018603?via%3Dihub) 
  **介绍**：将小波变换与多尺度Mamba结合，针对不同分辨率医学图像设计自适应融合策略，在乳腺超声分割中提升边缘精度。

- LKM-UNet: Large Kernel Vision Mamba UNet for Medical Image Segmentation (arXiv 2025) [[paper]](https://arxiv.org/abs/2403.07332) [[code]](https://github.com/wjh892521292/LKM-UNet)  
  **介绍**：引入大核卷积增强Mamba的全局感知能力，在COVID-19肺部病变分割中对小病灶的检测率提升18%。

### 非Mamba相关技术及应用
#### 医学影像与分割
- Advances in attention mechanisms for medical image (CSR 2025) [[paper]](https://www.sciencedirect.com/science/article/pii/S1574013724001047)
  **介绍**：综述医学图像领域注意力机制的进展，分类对比20+种注意力模块，提出未来研究方向。

- Generalized Source-Free Domain-adaptive Segmentation via Reliable Knowledge Propagation (ACM MM 2024) [[paper]](https://dl.acm.org/doi/10.1145/3664647.3680567)
  **介绍**：提出无源域自适应分割框架，通过知识蒸馏和一致性正则化，在跨扫描仪前列腺分割中提升12%性能。

- Interactive Medical Image Segmentation: A Benchmark Dataset and Baseline (arXiv 2024) [[paper]](https://arxiv.org/pdf/2411.12814)
  **介绍**：提出IMIS 基线网络，支持通过点击、边界框、文本提示及其组合等交互式输入生成高质量掩码
  
#### 通用视觉与多任务
- Perceive Anything: Recognize, Explain, Caption, and Segment Anything in Images and (arXiv 2025) [[paper]](http://arxiv.org/abs/2506.05302) 
  **介绍**：构建统一视觉基础模型，支持图像识别、解释、描述和分割多任务，在COCO数据集上实现78.3%的泛化能力。

#### 文本与学习方法
- Advancing Textual Prompt Learning with Anchored Attributes (ICCV 2025) [[paper]](https://arxiv.org/abs/2412.09442) [[code]](https://github.com/zhengli97/ATPrompt)  
  **介绍**：提出锚定属性的文本提示学习方法，通过语义约束提升医学报告生成的准确性，在PubMed数据集上BLEU-4提升5.2。

#### 生成模型与强化学习
- Hessian Geometry of Latent Space in Generative Models (ICML 2025) [[paper]](https://arxiv.org/abs/2506.10632) [[code]](https://github.com/alobashev/hessian-geometry-of-diffusion-models)  
  **介绍**：从Hessian矩阵角度分析生成模型潜在空间的几何特性，提出基于曲率的采样策略，在医学图像生成中提升25%多样性。

- A survey on physics informed reinforcement learning: Review and open problems (ESWA 2025) [[review]](https://www.sciencedirect.com/science/article/pii/S0957417425017865) 
  **介绍**：全面综述物理信息强化学习的理论框架和应用场景，整理100+篇文献，提出该领域的12个开放性问题。
