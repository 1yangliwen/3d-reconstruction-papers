# 三维重建论文收藏

收录三维重建方向顶会/顶刊论文推荐（来源：CVPR、ICCV、ECCV、SIGGRAPH、NeurIPS、TPAMI、IJCV 等），由 CatDesk 自动维护。

## 论文分类大纲

按研究方向分类索引，快速定位感兴趣的论文。

### 🔷 一、前馈式 3D Gaussian Splatting（Feed-Forward 3DGS）

研究如何用前馈网络直接预测高斯基元，无需逐场景优化，追求泛化能力与推理速度。

- **AnchorSplat**（2026-04-13）— 以三维几何先验（稀疏点云/体素）为锚点生成高斯基元，打破像素对齐范式 · [CVPR 2026](https://arxiv.org/abs/2604.07053)
- **SparseSplat**（2026-04-14）— 基于熵的自适应高斯密度采样，仅用 22% 高斯基元达 SOTA 渲染质量 · [CVPR 2026](https://arxiv.org/abs/2604.03069)
- **UniSplat**（2026-04-15）— 从无位姿稀疏多视图图像学习统一三维表示，支持场景理解与具身 AI · [CVPR 2026](https://arxiv.org/abs/2604.10573)
- **IDESplat**（2026-04-17）— 迭代深度概率估计精准预测高斯球中心，以 10.7% 参数量超越 DepthSplat · [CVPR 2026](https://arxiv.org/abs/2601.03824)
- **C3G**（2026-04-21）— 仅用 2K 个紧凑高斯完成无位姿场景重建与三维开放词汇分割 · [CVPR 2026](https://arxiv.org/abs/2512.04021)

### 🔶 二、3DGS 渲染加速与结构优化

研究如何提升 3DGS 的渲染效率，通过遮挡剔除、结构化表示等手段降低冗余计算。

- **Proxy-GS**（2026-04-22）— 代理网格引入统一遮挡先验，推理加速 2.5×，获 CVPR 2026 Oral · [CVPR 2026 Oral](https://arxiv.org/abs/2509.24421)

### 🌧️ 三、3DGS 场景鲁棒性（恶劣条件重建）

研究在恶劣天气、动态城市等复杂条件下保持高质量三维重建的方法。

- **NimbusGS**（2026-04-23）— 统一框架处理雾/雨/雪混合天气退化，双分量分解 + 几何引导梯度缩放 · [CVPR 2026](https://arxiv.org/abs/2603.27228)
- **VAD-GS**（2026-04-24）— 可见性感知致密化修复动态城市场景几何空洞，在 Waymo/nuScenes 超越 SOTA · [CVPR 2026](https://arxiv.org/abs/2510.09364)

### 🧠 四、大规模三维重建基础模型（LRM）

研究具备长上下文处理能力的大规模三维重建模型，探索测试时训练、自回归重建等新范式。

- **tttLRM**（2026-04-16）— 将测试时训练（TTT）层引入三维重建，线性复杂度支持任意数量视角输入 · [CVPR 2026](https://arxiv.org/abs/2602.20160)

---

## 论文详情

### 2026-04-13

**AnchorSplat: Feed-Forward 3D Gaussian Splatting with 3D Geometric Priors**
基于三维几何先验的前馈式三维高斯泼溅

- **来源**：CVPR 2026
- **作者**：Xiaoxue Zhang, Xiaoxu Zheng, Yixuan Yin, Tiao Zhao, Kaihua Tang, Michael Bi Mi, Zhan Xu, Dave Zhenyu Chen
- **链接**：https://arxiv.org/abs/2604.07053

**核心内容**：提出 AnchorSplat，一种前馈式 3DGS 框架，以三维几何先验（稀疏点云/体素/RGB-D 点云）为锚点，直接在 3D 空间中生成高斯基元，打破了传统像素对齐范式。引入 Gaussian Refiner 模块进行轻量级精细化，在 ScanNet++ v2 NVS 基准上达到 SOTA。

**亮点**：
1. 锚点对齐高斯表示，不依赖图像分辨率和视角数量，视角一致性显著提升
2. 大幅减少高斯基元数量，兼顾计算效率与重建保真度
3. Gaussian Refiner 仅需少量前向传播即可精细化，部署灵活

---

### 2026-04-14

**SparseSplat: Towards Applicable Feed-Forward 3D Gaussian Splatting with Pixel-Unaligned Prediction**
面向实用的前馈式三维高斯泼溅：像素非对齐预测

- **来源**：CVPR 2026
- **作者**：Zicheng Zhang, Xiangting Meng, Ke Wu, Wenchao Ding
- **链接**：https://arxiv.org/abs/2604.03069

**核心内容**：提出 SparseSplat，首个能根据场景结构和局部区域信息丰富度自适应调整高斯密度的前馈式 3DGS 模型。通过基于熵的概率采样策略，在纹理稀少区域生成大而稀疏的高斯基元，在信息丰富区域分配小而密集的高斯基元，生成高度紧凑的 3DGS 地图。

**亮点**：
1. 首创基于熵的自适应高斯密度采样，打破像素对齐范式，仅用 22% 高斯基元即达 SOTA 渲染质量
2. 专用点云网络解决感受野不匹配问题，局部上下文编码更精准
3. 极致压缩潜力：仅保留 1.5% 高斯基元仍可维持合理渲染质量

---

### 2026-04-15

**UniSplat: Learning 3D Representations for Spatial Intelligence from Unposed Multi-View Images**
UniSplat：从无位姿多视图图像学习空间智能三维表示

- **来源**：CVPR 2026
- **作者**：Bo Zhou, Qiuxia Lai, Zeren Sun, Xiangbo Shu, Yazhou Yao, Wenguan Wang
- **链接**：https://arxiv.org/abs/2604.10573

**核心内容**：提出 UniSplat，一种前馈式框架，旨在从无位姿稀疏多视图图像中学习统一的三维表示。框架包含三大核心组件：双重掩码策略、由粗到细的高斯泼溅策略、位姿条件重校准机制。

**亮点**：
1. 无位姿输入下的几何感知学习，大幅降低数据采集门槛
2. 几何-语义跨任务一致性保障，实现外观、几何、语义的统一三维表示
3. 空间智能基础模型潜力，可直接服务于场景理解和具身 AI 等下游任务

---

### 2026-04-16

**tttLRM: Test-Time Training for Long Context and Autoregressive 3D Reconstruction**
tttLRM：面向长上下文自回归三维重建的测试时训练

- **来源**：CVPR 2026
- **作者**：Chen Wang, Hao Tan, Wang Yifan, Zhiqin Chen, Yuheng Liu, Kalyan Sunkavalli, Sai Bi, Lingjie Liu, Yiwei Hu（University of Pennsylvania / Adobe Research / UCI）
- **链接**：https://arxiv.org/abs/2602.20160

**核心内容**：提出 tttLRM，将测试时训练（TTT）层引入三维重建任务，实现具有线性计算复杂度的长上下文自回归三维重建。在线学习变体支持从流式观测中进行渐进式三维重建与精细化。

**亮点**：
1. TTT 层赋能长上下文重建，以线性复杂度支持任意数量视角输入
2. 在线渐进式重建能力，天然适配 SLAM 和机器人实时感知等在线应用场景
3. 跨任务预训练迁移，在物体级与场景级重建基准上均超越现有 SOTA

---

### 2026-04-17

**IDESplat: Iterative Depth Probability Estimation for Generalizable 3D Gaussian Splatting**
IDESplat：面向可泛化三维高斯泼溅的迭代深度概率估计

- **来源**：CVPR 2026
- **作者**：Wei Long, Haifeng Wu, Shiyin Jiang, Jinhua Zhang, Xinchun Ji, Shuhang Gu
- **链接**：https://arxiv.org/abs/2601.03824

**核心内容**：提出 IDESplat，通过迭代深度概率估计来精准预测高斯球中心。引入深度概率增强单元（DPBU），通过级联 warp 操作消除单次 warp 的固有不稳定性。在 RE10K 上以仅 10.7% 的参数量和 70% 的显存，PSNR 超越 DepthSplat 0.33 dB。

**亮点**：
1. 迭代深度概率增强（DPBU），仅用 10.7% 参数量即超越 DepthSplat
2. 极强跨数据集泛化能力，在 DTU 跨数据集实验中 PSNR 提升 2.95 dB
3. 轻量高效实时推理，以 70% 显存占用实现实时渲染效率

---

### 2026-04-21

**C3G: Learning Compact 3D Representations with 2K Gaussians**
C3G：基于 2K 高斯的紧凑三维表示学习

- **来源**：CVPR 2026
- **作者**：Honggyu An, Jaewoo Jung, Mungyeom Kim, Sunghwan Hong, Chaehyun Kim, Kazumi Fukuda, Minkyeong Jeon, Jisang Han, Takuya Narihira, Hyuna Ko, Junsu Kim, Yuki Mitsufuji, Seungryong Kim（KAIST / Sony AI）
- **链接**：https://arxiv.org/abs/2512.04021

**核心内容**：提出 C3G，通过仅在关键空间位置估计约 2K 个紧凑高斯来完成无位姿稀疏视图的三维场景重建与理解。引入可学习 token 通过自注意力机制聚合多视图特征。

**亮点**：
1. 极致紧凑：仅用 2K 个高斯基元完成场景重建，大幅降低内存开销
2. 可学习 token 驱动的特征聚合，自适应整合多视角特征
3. 重建与理解统一框架，同时支持新视角合成和三维开放词汇分割

---

### 2026-04-22

**Proxy-GS: Unified Occlusion Priors for Training and Inference in Structured 3D Gaussian Splatting**
Proxy-GS：面向结构化三维高斯泼溅训练与推理的统一遮挡先验

- **来源**：CVPR 2026 Oral
- **作者**：Yuanyuan Gao, Yuning Gong, Yifei Liu, Li Jingfeng, Dingwen Zhang, Yanci Zhang, Dan Xu, Xiao Sun, Zhihang Zhong（上海交通大学 / 上海人工智能实验室 / 西北工业大学 / 四川大学 / 香港科技大学）
- **链接**：https://arxiv.org/abs/2509.24421

**核心内容**：Proxy-GS 提出利用轻量级代理网格引入统一的遮挡先验，在推理阶段以不到 1ms 生成精确遮挡深度图剔除被遮挡的高斯基元，在训练阶段引导增密沿代理表面生长。在 MatrixCity Streets 上实现超过 2.5 倍渲染加速。

**亮点**：
1. 统一遮挡先验框架：首次将代理网格引入 3DGS 训练与推理两个阶段
2. 极速代理系统：1ms 内生成遮挡深度图，实现 2.5× 渲染加速
3. 即插即用的通用性，可与多种 MLP-based 3DGS 渲染器无缝集成

---

### 2026-04-23

**NimbusGS: Unified 3D Scene Reconstruction under Hybrid Weather**
恶劣混合天气下的统一三维场景重建

- **来源**：CVPR 2026
- **作者**：Yanying Li, Jinyang Li, Shengfeng He, Yangyang Xu, Junyu Dong, Yong Du（中国海洋大学 / 华南理工大学）
- **链接**：https://arxiv.org/abs/2603.27228

**核心内容**：NimbusGS 将天气退化分解为两类：跨视图一致的连续介质（全局传输场）和每帧独立的动态粒子（逐视图粒子残差），并引入几何引导梯度缩放机制缓解梯度失衡问题。

**亮点**：
1. 双分量天气退化分解，可同时处理雾、雨、雪及任意组合天气
2. 几何引导梯度缩放，有效稳定训练过程并提升几何重建精度
3. 统一框架，单一模型即可处理多种及混合天气输入

---

### 2026-04-24

**VAD-GS: Visibility-Aware Densification for 3D Gaussian Splatting in Dynamic Urban Scenes**
动态城市场景中3D高斯泼溅的可见性感知致密化

- **来源**：CVPR 2026
- **作者**：Yikang Zhang, Rui Fan（同济大学）
- **链接**：https://arxiv.org/abs/2510.09364

**核心内容**：VAD-GS 通过基于体素的可见性推理识别不可靠几何结构，利用多样性感知视图选择挑选最具信息量的支撑视图，再以块匹配 MVS 重建缺失结构。在 Waymo 和 nuScenes 数据集上均超越当前最优方法。

**亮点**：
1. 可见性感知的几何修复，精准定位并主动填补因视锥不重叠而缺失的几何区域
2. 多样性感知视图选择，自动筛选覆盖最全面的支撑视图组合
3. 动态与静态对象几何双提升，对自动驾驶感知系统具有重要实用价值
