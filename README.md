# 三维重建论文收藏

本文档由 CatDesk 自动维护，收录每日三维重建方向顶会/顶刊论文推荐（来源：CVPR、ICCV、ECCV、SIGGRAPH、NeurIPS、TPAMI、IJCV 等）。

重点子方向：3D Gaussian Splatting、多视图立体重建（MVS）、SLAM / 实时三维重建。

---

## 论文分类大纲

按研究方向分类索引，快速定位感兴趣的论文。

### 🔷 一、前馈式 3D Gaussian Splatting（Feed-Forward 3DGS）

研究如何用前馈网络直接预测高斯基元，无需逐场景优化，追求泛化能力与推理速度。

- **AnchorSplat**（2026-04-13）— 以三维几何先验（稀疏点云/体素）为锚点生成高斯基元，打破像素对齐范式 · [CVPR 2026](https://arxiv.org/abs/2604.07053)
- **SparseSplat**（2026-04-14）— 基于熵的自适应高斯密度采样，仅用 22% 高斯基元达 SOTA 渲染质量 · [CVPR 2026](https://arxiv.org/abs/2604.03069)
- **UniSplat**（2026-04-15）— 从无位姿稀疏多视图图像学习统一三维表示，支持场景理解与具身 AI · [CVPR 2026](https://arxiv.org/abs/2604.10573)
- **IDESplat**（2026-04-17）— 迭代深度概率估计精准预测高斯球中心，以 10.7% 参数量超越 DepthSplat · [CVPR 2026](https://arxiv.org/abs/2601.03824)
- **C3G**（2026-04-21）— 仅用 2K 个紧凑高斯完成无位姿场景重建与三维开放词汇分割 · [CVPR 2026](https://arxiv.org/abs/2512.04021)
- **Uni3R**（2026-04-29）— 前馈框架统一三维重建与开放词汇语义理解，0.15 秒完成场景重建，RE10K PSNR 25.07 · [CVPR 2026 Highlight](https://arxiv.org/abs/2508.03643)

### 🔶 二、3DGS 渲染加速与结构优化

研究如何提升 3DGS 的渲染效率，通过遮挡剔除、结构化表示等手段降低冗余计算。

- **Proxy-GS**（2026-04-22）— 代理网格引入统一遮挡先验，推理加速 2.5×，获 CVPR 2026 Oral · [CVPR 2026 Oral](https://arxiv.org/abs/2509.24421)
- **Stochastic Ray Tracing for 3DGS**（2026-05-06）— 首个无排序可微随机光线追踪框架，支持可重光照与非针孔相机 · [CVPR 2026](https://arxiv.org/abs/2603.23637)

### 🌧️ 三、3DGS 场景鲁棒性（恶劣条件重建）

研究在恶劣天气、动态城市等复杂条件下保持高质量三维重建的方法。

- **NimbusGS**（2026-04-23）— 统一框架处理雾/雨/雪混合天气退化，双分量分解 + 几何引导梯度缩放 · [CVPR 2026](https://arxiv.org/abs/2603.27228)
- **VAD-GS**（2026-04-24）— 可见性感知致密化修复动态城市场景几何空洞，在 Waymo/nuScenes 超越 SOTA · [CVPR 2026](https://arxiv.org/abs/2510.09364)

### 🧠 四、大规模三维重建基础模型（LRM）

研究具备长上下文处理能力的大规模三维重建模型，探索测试时训练、自回归重建等新范式。

- **tttLRM**（2026-04-16）— 将测试时训练（TTT）层引入三维重建，线性复杂度支持任意数量视角输入 · [CVPR 2026](https://arxiv.org/abs/2602.20160)

### 🔬 五、视觉几何基础模型（Visual Geometry Foundation Models）

研究端到端几何预测架构，无需迭代优化即可从任意数量视图直接推理相机参数、深度图、点云等全部三维属性。

- **VGGT**（2026-04-27）— CVPR 2025 最佳论文，纯前馈 Transformer 从任意视图直接推理全部三维属性，无需几何后处理 · [CVPR 2025 Best Paper](https://arxiv.org/abs/2503.11651)
- **MoRE**（2026-05-07）— MoE 架构驱动的稠密三维视觉基础模型，动态路由特征至任务专家，置信度深度精炼 + 语义融合，多基准 SOTA · [CVPR 2026](https://arxiv.org/abs/2510.27234)

### 🎬 六、4D 动态场景重建（4D Dynamic Scene Reconstruction）

研究将三维高斯表示扩展到时间维度，实现动态场景的连续时间重建与任意时刻渲染，解决时间混叠、鬼影等核心挑战。

- **RetimeGS**（2026-04-28）— 连续时间 4DGS 表示，光流引导初始化 + 三重渲染监督，任意时刻无鬼影重建 · [CVPR 2026 Oral](https://arxiv.org/abs/2603.13783)
- **L4DRotorGS**（2026-05-08）— 分层 4D 旋转体高斯泼溅，22.3× 压缩率支持长时动态场景（>10s），RTX 3090 实现 500+ FPS · [CVPR 2026](https://cvpr.thecvf.com/virtual/2026/poster/36256)

### 📡 七、SLAM / 实时三维重建（SLAM / Real-Time 3D Reconstruction）

研究实时同步定位与建图系统，探索在动态真实场景中鲁棒跟踪与高质量稠密重建的方法。

- **DROID-W**（2026-04-30）— 基于动态不确定性感知可微 BA 的 RGB SLAM，无需类别先验即可鲁棒处理真实动态场景，ETH Zürich + 微软 · [CVPR 2026](https://arxiv.org/abs/2603.19076)

### 🎨 八、三维生成（3D Generation）

研究从文本、图像等条件生成高质量三维资产的方法，涵盖原生三维表示学习、扩散/流匹配生成模型、PBR 材质建模等核心技术。

- **TRELLIS.2**（2026-05-01）— 原生紧凑结构化隐空间 + 40亿参数流匹配模型，数秒内生成高分辨率 PBR 材质三维资产，微软研究院 · [CVPR 2026 Oral](https://arxiv.org/abs/2512.14692)

### 🪟 九、3DGS 透明表面建模（Transparent Surface Modeling）

研究如何在 3D Gaussian Splatting 框架中建模玻璃、水面等透明/半透明界面，通过辐射传输分解实现物理一致的反射与透射渲染。

- **GLINT**（2026-05-04）— 分解高斯辐射传输建模场景级透明表面，无需显式分割 mask 即可自动定位透明区域，NAVER LABS · [CVPR 2026 Oral](https://arxiv.org/abs/2603.26181)

### 🔍 十、多视图稠密匹配与三维重建（MVS / Dense Matching）

研究从多张图像建立稠密、一致的像素级对应关系，为 SfM 和三维重建提供高精度轨迹，突破成对匹配范式，追求全局几何一致性。

- **MV-RoMa**（2026-05-05）— 首个多视图稠密匹配模型，Track-Guided 多视图编码器 + 像素对齐精炼器，SfM 全面超越稀疏/稠密匹配基线 · [CVPR 2026](https://arxiv.org/abs/2603.27542)

---

## 论文列表

### 2026-04-13

**AnchorSplat: Feed-Forward 3D Gaussian Splatting with 3D Geometric Priors**
**基于三维几何先验的前馈式三维高斯泼溅**

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
**面向实用的前馈式三维高斯泼溅：像素非对齐预测**

- **来源**：CVPR 2026
- **作者**：Zicheng Zhang, Xiangting Meng, Ke Wu, Wenchao Ding
- **链接**：https://arxiv.org/abs/2604.03069

**核心内容**：提出 SparseSplat，首个能根据场景结构和局部区域信息丰富度自适应调整高斯密度的前馈式 3DGS 模型。通过基于熵的概率采样策略，在纹理稀少区域生成大而稀疏的高斯基元，在信息丰富区域分配小而密集的高斯基元，生成高度紧凑的 3DGS 地图。实验表明，SparseSplat 仅用 22% 的高斯基元即可达到 SOTA 渲染质量，仅用 1.5% 的高斯基元仍能保持合理渲染质量。

**亮点**：

1. 首创基于熵的自适应高斯密度采样，打破像素对齐范式，仅用 22% 高斯基元即达 SOTA 渲染质量，极大降低存储与计算开销
2. 专用点云网络解决感受野不匹配问题，局部上下文编码更精准，属性回归更高效，适合 AR/VR 和机器人等下游任务
3. 极致压缩潜力突出：仅保留 1.5% 高斯基元仍可维持合理渲染质量，为实时三维重建在资源受限设备上的部署提供新思路

---

### 2026-04-15

**UniSplat: Learning 3D Representations for Spatial Intelligence from Unposed Multi-View Images**
**UniSplat：从无位姿多视图图像学习空间智能三维表示**

- **来源**：CVPR 2026
- **作者**：Bo Zhou, Qiuxia Lai, Zeren Sun, Xiangbo Shu, Yazhou Yao, Wenguan Wang
- **链接**：https://arxiv.org/abs/2604.10573

**核心内容**：提出 UniSplat，一种前馈式框架，旨在从无位姿（unposed）稀疏多视图图像中学习统一的三维表示，为空间智能（场景理解、具身 AI）提供感知基础。框架包含三大核心组件：① 双重掩码策略（dual-masking），迫使模型从不完整视觉线索中推断结构信息；② 由粗到细的高斯泼溅策略（coarse-to-fine Gaussian splatting），通过逐步精细化辐射场来减少外观与语义之间的不一致；③ 位姿条件重校准机制（pose-conditioned recalibration），确保几何-语义跨任务一致性。

**亮点**：

1. 无位姿输入下的几何感知学习：双重掩码策略强制模型从不完整视觉线索中推断三维结构，无需相机位姿即可获得高质量几何感知表示，大幅降低数据采集门槛
2. 几何-语义跨任务一致性保障：位姿条件重校准机制通过重投影对齐，解决了多任务头之间的几何-语义不匹配问题，实现外观、几何、语义的统一三维表示
3. 空间智能基础模型潜力：UniSplat 生成的统一三维表示在稀疏视图、无位姿等挑战性条件下具有强泛化能力，可直接服务于场景理解和具身 AI 等下游任务

---

### 2026-04-16

**tttLRM: Test-Time Training for Long Context and Autoregressive 3D Reconstruction**
**tttLRM：面向长上下文自回归三维重建的测试时训练**

- **来源**：CVPR 2026
- **作者**：Chen Wang, Hao Tan, Wang Yifan, Zhiqin Chen, Yuheng Liu, Kalyan Sunkavalli, Sai Bi, Lingjie Liu, Yiwei Hu（University of Pennsylvania / Adobe Research / UCI）
- **链接**：https://arxiv.org/abs/2602.20160

**核心内容**：提出 tttLRM，一种新型大规模三维重建模型，将测试时训练（Test-Time Training, TTT）层引入三维重建任务，实现具有线性计算复杂度的长上下文自回归三维重建。其核心思想是将多幅图像观测压缩到 TTT 层的"快速权重"（fast weights）中，形成隐空间中的隐式三维表示，可解码为高斯泼溅（Gaussian Splats）等显式格式用于下游应用。在线学习变体支持从流式观测中进行渐进式三维重建与精细化。

**亮点**：

1. TTT 层赋能长上下文重建：将多视图观测压缩为快速权重隐式表示，以线性复杂度支持任意数量视角输入，突破以往前馈重建模型视角数量受限的瓶颈
2. 在线渐进式重建能力：在线学习变体支持从流式观测中逐步积累和精细化三维场景，天然适配 SLAM 和机器人实时感知等在线应用场景
3. 跨任务预训练迁移：在新视角合成任务上预训练后有效迁移到显式三维重建（高斯泼溅），在物体级与场景级重建基准上均超越现有 SOTA，验证了预训练策略的通用性

---

### 2026-04-17

**IDESplat: Iterative Depth Probability Estimation for Generalizable 3D Gaussian Splatting**
**IDESplat：面向可泛化三维高斯泼溅的迭代深度概率估计**

- **来源**：CVPR 2026
- **作者**：Wei Long, Haifeng Wu, Shiyin Jiang, Jinhua Zhang, Xinchun Ji, Shuhang Gu
- **链接**：https://arxiv.org/abs/2601.03824

**核心内容**：提出 IDESplat，一种可泛化前馈式 3DGS 框架，通过迭代深度概率估计来精准预测高斯球中心（Gaussian means）。IDESplat 引入深度概率增强单元（DPBU），通过级联 warp 操作生成极线注意力图并以乘法方式融合，消除单次 warp 的固有不稳定性；再通过堆叠多个 DPBU 构建迭代深度估计流程，逐步筛选高置信度深度候选。在 RE10K 上以仅 10.7% 的参数量和 70% 的显存，PSNR 超越 DepthSplat 0.33 dB；在跨数据集 DTU 实验中 PSNR 提升 2.95 dB。

**亮点**：

1. 迭代深度概率增强（DPBU）：通过级联 warp 操作的极线注意力图乘法融合，彻底消除单次 warp 的不稳定性，逐步精炼深度候选，使高斯球中心预测更精准，在 RE10K 上仅用 10.7% 参数量即超越 DepthSplat
2. 极强跨数据集泛化能力：在 DTU 跨数据集实验中 PSNR 提升 2.95 dB，证明迭代深度估计策略能有效捕获跨视角几何一致性，泛化到未见场景
3. 轻量高效实时推理：以 70% 显存占用实现实时渲染效率，兼顾重建质量与计算资源，适合在资源受限设备上部署可泛化三维重建系统

---

### 2026-04-21

**C3G: Learning Compact 3D Representations with 2K Gaussians**
**C3G：基于 2K 高斯的紧凑三维表示学习**

- **来源**：CVPR 2026
- **作者**：Honggyu An, Jaewoo Jung, Mungyeom Kim, Sunghwan Hong, Chaehyun Kim, Kazumi Fukuda, Minkyeong Jeon, Jisang Han, Takuya Narihira, Hyuna Ko, Junsu Kim, Yuki Mitsufuji, Seungryong Kim（KAIST / Sony AI）
- **链接**：https://arxiv.org/abs/2512.04021

**核心内容**：提出 C3G，一种新型前馈式三维重建框架，通过仅在关键空间位置估计约 2K 个紧凑高斯（3D Gaussians）来完成无位姿稀疏视图的三维场景重建与理解。其核心创新在于引入可学习 token，通过自注意力机制聚合多视图特征，指导高斯基元的空间分配，确保每个高斯基元都整合了跨视角的相关视觉特征。在无位姿新视角合成、三维开放词汇分割和视角不变特征聚合等任务上均达到 SOTA。

**亮点**：

1. 极致紧凑的高斯表示：仅用 2K 个高斯基元完成场景重建，打破了以往前馈重建方法按像素密集分配高斯导致冗余爆炸的范式，在大幅降低内存开销的同时保持高质量重建效果
2. 可学习 token 驱动的特征聚合：通过自注意力机制让每个高斯 token 自适应地整合多视角特征，解决了稀疏视图下多视图特征聚合次优的问题，同时注意力模式可直接复用于 feature lifting，无需额外模块
3. 重建与理解统一框架：同一紧凑表示同时支持新视角合成（重建）和三维开放词汇分割（理解），在两类任务上均超越现有方法，验证了紧凑几何表示作为通用三维特征载体的潜力

---

### 2026-04-22

**Proxy-GS: Unified Occlusion Priors for Training and Inference in Structured 3D Gaussian Splatting**
**Proxy-GS：面向结构化三维高斯泼溅训练与推理的统一遮挡先验**

- **来源**：CVPR 2026 Oral（满分论文）
- **作者**：Yuanyuan Gao, Yuning Gong, Yifei Liu, Li Jingfeng, Dingwen Zhang, Yanci Zhang, Dan Xu, Xiao Sun, Zhihang Zhong（上海交通大学 / 上海人工智能实验室 / 西北工业大学 / 四川大学 / 香港科技大学）
- **链接**：https://arxiv.org/abs/2509.24421

**核心内容**：Proxy-GS 提出利用轻量级代理网格（proxy mesh）引入统一的遮挡先验，在推理阶段通过代理系统以不到 1ms 的速度生成 1000×1000 分辨率的精确遮挡深度图，用于剔除被遮挡的锚点和高斯基元以加速渲染；在训练阶段引导高斯增密沿代理表面生长，避免遮挡区域的无效增密。在 MatrixCity Streets 等遮挡密集数据集上，Proxy-GS 相比 Octree-GS 实现了超过 2.5 倍的渲染加速，同时显著提升渲染质量。

**亮点**：

1. 统一遮挡先验框架：首次将代理网格引入结构化 3DGS 的训练与推理两个阶段，用同一套遮挡深度图同时指导推理时的高斯剔除（加速渲染）和训练时的增密策略（提升质量），实现了训练-推理一致的遮挡感知优化
2. 极速代理系统：核心代理系统可在 1ms 内生成 1000×1000 分辨率的精确遮挡深度图，计算开销极低，在遮挡密集的大规模城市场景（MatrixCity Streets）中实现超过 2.5 倍渲染加速
3. 即插即用的通用性：Proxy-GS 作为插件式模块可与多种 MLP-based 3DGS 渲染器（Scaffold-GS、Octree-GS 等）无缝集成，无需修改底层渲染架构，且获得 CVPR 2026 满分 Oral 认可

---

### 2026-04-23

**NimbusGS: Unified 3D Scene Reconstruction under Hybrid Weather**
**恶劣混合天气下的统一三维场景重建**

- **来源**：CVPR 2026
- **作者**：Yanying Li, Jinyang Li, Shengfeng He, Yangyang Xu, Junyu Dong, Yong Du（中国海洋大学 / 华南理工大学）
- **链接**：https://arxiv.org/abs/2603.27228

**核心内容**：NimbusGS 提出了一个统一框架，用于从多视图退化图像（雾、雨、雪及其混合天气）中重建高质量三维场景。NimbusGS 将天气退化分解为两类：一是跨视图一致的连续介质（如大气散射、光线衰减），用全局传输场（global transmission field）建模；二是每帧独立的动态粒子（如雨滴、雪花），用逐视图粒子残差（per-view particulate residuals）建模。还引入了几何引导的梯度缩放机制（geometry-guided gradient scaling），缓解严重能见度退化时的梯度失衡问题。

**亮点**：

1. 双分量天气退化分解：首次将复杂的混合天气退化系统地分解为全局传输场（静态大气效应，跨视图一致）和逐视图粒子残差（动态瞬态扰动，每帧独立）两部分，物理建模清晰，可同时处理雾、雨、雪及任意组合天气
2. 几何引导梯度缩放：针对强退化（低能见度）场景下三维高斯自监督优化中梯度失衡导致几何学习不稳定的痛点，提出几何引导的梯度缩放机制，有效稳定训练过程并显著提升几何重建精度
3. 统一框架泛化能力强：NimbusGS 无需为每种天气单独训练或调参，单一模型即可处理多种及混合天气输入，为自动驾驶、机器人导航等恶劣天气下的三维感知重建提供了全新解决方案

---

### 2026-04-24

**VAD-GS: Visibility-Aware Densification for 3D Gaussian Splatting in Dynamic Urban Scenes**
**动态城市场景中3D高斯泼溅的可见性感知致密化**

- **来源**：CVPR 2026
- **作者**：Yikang Zhang, Rui Fan（同济大学）
- **链接**：https://arxiv.org/abs/2510.09364

**核心内容**：VAD-GS 针对动态、无界城市场景中 3D 高斯泼溅（3DGS）几何重建质量不足的问题，提出了一种可见性感知的致密化框架。VAD-GS 通过基于体素的可见性推理识别不可靠几何结构，利用多样性感知视图选择挑选最具信息量的支撑视图，再以块匹配多视图立体（patch matching MVS）重建缺失结构，为无初始点区域生成基于可靠几何先验的新高斯基元。在 Waymo 和 nuScenes 数据集上的实验表明，VAD-GS 在渲染质量和几何重建精度上均超越当前最优 3DGS 方法。

**亮点**：

1. 可见性感知的几何修复：首次将基于体素的可见性分析引入 3DGS 致密化流程，精准定位因视锥不重叠而缺失的几何区域，并通过多视图立体重建（patch matching MVS）主动填补空洞，彻底突破传统克隆/分裂策略仅能在已有点附近扩展的局限
2. 多样性感知视图选择：设计了专门的多样性感知视图选择策略，为每个缺失区域自动筛选覆盖最全面、信息最丰富的支撑视图组合，有效保证后续 MVS 重建的精度
3. 动态与静态对象几何双提升：VAD-GS 在 Waymo 和 nuScenes 上全面优于现有 3DGS 方法，不仅静态背景几何更完整准确，动态前景对象（如车辆、行人）的深度图和法线图质量也显著提升

---

### 2026-04-27

**VGGT: Visual Geometry Grounded Transformer**
**视觉几何基础 Transformer**

- **来源**：CVPR 2025 Best Paper Award（最佳论文）
- **作者**：Jianyuan Wang, Minghao Chen, Nikita Karaev, Andrea Vedaldi, Christian Rupprecht, David Novotny（牛津大学 & Meta AI）
- **链接**：https://arxiv.org/abs/2503.11651

**核心内容**：VGGT 是一个纯前馈神经网络，能够直接从一张、几张乃至数百张输入视图中推理出场景的所有关键三维属性，包括相机参数、点图（point maps）、深度图以及三维点轨迹（3D point tracks）。传统三维重建方法依赖捆绑调整（Bundle Adjustment）等迭代优化手段，而 VGGT 完全摒弃了几何后处理步骤，实现了真正意义上的端到端三维几何推理。单张图像重建仅需不到 1 秒，却在相机参数估计、多视图深度估计、稠密点云重建和三维点跟踪等多个任务上超越了需要几何优化的竞争方法。

**亮点**：

1. 端到端统一三维推理：VGGT 首次以单一前馈网络统一处理相机估计、深度预测、点云重建和三维点跟踪四大核心任务，彻底消除了对 Bundle Adjustment 等迭代几何优化的依赖，推理速度极快（<1秒/帧），同时在所有任务上均达到或超越 SOTA
2. 视图数量无关的泛化能力：模型设计上对输入视图数量无约束，从单视图到数百视图均可直接处理，体现了 Transformer 架构在多视图几何理解上的强大泛化能力
3. 强大的下游迁移能力：预训练 VGGT 作为特征骨干可显著提升非刚性点跟踪和前馈式新视角合成等下游任务，证明其学到的几何表征具有高度通用性，荣获 CVPR 2025 最佳论文奖

---

### 2026-04-28

**RetimeGS: Continuous-Time Reconstruction of 4D Gaussian Splatting**
**RetimeGS：4D 高斯泼溅的连续时间重建**

- **来源**：CVPR 2026 Oral
- **作者**：Xuezhen Wang, Li Ma, Yulin Shen, Zeyu Wang, Pedro V. Sander（香港科技大学广州）
- **链接**：https://arxiv.org/abs/2603.13783

**核心内容**：RetimeGS 将 4DGS 在时间插值时产生鬼影的根本原因定义为"时间混叠"（temporal aliasing），并提出了一种简洁有效的 4DGS 表示，显式定义三维高斯的时间行为以缓解时间混叠。为实现平滑一致的插值，RetimeGS 引入了光流引导的初始化与监督（optical flow-guided initialization and supervision）、三重渲染监督（triple-rendering supervision）以及其他针对性策略。在包含快速运动、非刚性形变和严重遮挡的数据集上，RetimeGS 在质量和连贯性方面均超越了当前最优方法。

**亮点**：

1. 时间混叠问题的首次系统性解决：RetimeGS 首次将 4DGS 在时间插值时产生鬼影的根本原因定义为"时间混叠"，并通过显式建模高斯基元的时间行为从根本上解决这一问题，为连续时间动态场景重建提供了全新理论框架
2. 光流引导 + 三重渲染监督的协同设计：光流引导初始化为高斯基元提供了准确的运动先验，三重渲染监督强制模型学习时间连续的运动轨迹，两者协同作用使 RetimeGS 在大运动、非刚性形变和严重遮挡等极端场景下仍能保持无鬼影的高质量渲染
3. 广泛的应用价值与 CVPR 2026 Oral 认可：RetimeGS 直接赋能慢动作视频生成、时间编辑和影视后期制作等高价值应用场景，在 PSNR、SSIM、LPIPS 等指标上全面超越现有 4DGS SOTA 方法

---

### 2026-04-29

**Uni3R: Unified 3D Reconstruction and Semantic Understanding via Generalizable Gaussian Splatting from Unposed Multi-View Images**
**Uni3R：从无位姿多视图图像统一三维重建与语义理解**

- **来源**：CVPR 2026 Highlight
- **作者**：Xiangyu Sun, Haoran Jiang, Liyi Liu, Seokhun Nam, Gyeongrok Kang, Xin Wang, Wenbo Sui, Zhizhong Su, Wenyu Liu, Xinggang Wang（地平线机器人 & 华中科技大学）
- **链接**：https://arxiv.org/abs/2508.03643

**核心内容**：Uni3R 提出了一个新颖的前馈框架，能够直接从无位姿（unposed）的多视图图像中联合重建统一的三维场景表示，并同时赋予其开放词汇语义理解能力。方法的核心是跨视图 Transformer（Cross-View Transformer），它能够鲁棒地整合来自任意数量多视图输入的信息，然后回归一组携带语义特征场的三维高斯基元。这种统一表示在单次前馈传递中同时支持三大任务：高保真新视角合成、开放词汇三维语义分割和深度预测。在 RE10K 数据集上达到 25.07 PSNR，在 ScanNet 上达到 55.84 mIoU，整个场景重建仅需约 0.15 秒。

**亮点**：

1. 重建与语义理解的首次统一：Uni3R 首次在单一前馈框架内同时完成三维重建（新视角合成 + 深度预测）和开放词汇语义分割三大任务，无需任何位姿先验，彻底打破了"重建"与"理解"两个任务需要分别建模的传统范式
2. 跨视图 Transformer 实现无位姿泛化：通过跨视图注意力机制鲁棒整合任意数量无位姿多视图输入，无需相机标定或 SfM 预处理，直接回归带语义特征场的三维高斯基元，在 RE10K（PSNR 25.07）和 ScanNet（mIoU 55.84）等多个基准上全面超越现有方法
3. 开放词汇语义场的创新设计：将语义特征场直接嵌入三维高斯基元，支持任意文本查询的开放词汇三维语义分割，无需针对特定类别重新训练，获得 CVPR 2026 Highlight 认可

---

### 2026-04-30

**DROID-SLAM in the Wild**
**野外动态场景下的 DROID-SLAM**

- **来源**：CVPR 2026
- **作者**：Moyang Li, Zihan Zhu, Marc Pollefeys, Daniel Barath（苏黎世联邦理工学院 ETH Zürich & 微软）
- **链接**：https://arxiv.org/abs/2603.19076

**核心内容**：DROID-W 提出了一套面向真实野外动态场景的鲁棒实时 RGB SLAM 系统。DROID-W 的核心创新是将动态不确定性（dynamic uncertainty）显式建模为逐像素连续值，通过多视角 DINO 特征一致性来检测视觉不一致区域，并将其无缝嵌入可微 Bundle Adjustment（BA）优化框架：不确定性高的区域残差被连续软抑制（soft suppression），而非硬性 mask 丢弃。系统在 RTX 5090 上可达约 30 FPS 实时性能。在 DROID-W 数据集上平均轨迹误差仅 23cm，而原始 DROID-SLAM 误差高达 1.46m，提升显著。

**亮点**：

1. 无类别先验的动态感知：DROID-W 彻底摆脱对语义分割等预定义动态类别先验的依赖，利用 DINO 特征的跨视角一致性自动发现任意未知动态干扰，采用连续逐像素不确定性表达替代二值化 mask，支持"软抑制"策略，真正实现面向真实世界"随手拍"视频的通用动态 SLAM
2. 不确定性与可微 BA 深度融合：将动态不确定性直接嵌入 DROID-SLAM 可微 Bundle Adjustment 核心优化框架，通过交替迭代优化位姿/深度与不确定性估计，保持实时性能（约 30 FPS @ RTX 5090），该不确定性感知模块具备即插即用特性
3. 高难度真实场景基准贡献：提出 DROID-W 数据集，包含 7 段室外城市高动态场景序列，涵盖过曝、镜面反射、太阳光晕等极端拍摄条件，配备 RTK 支持的厘米级精度真值轨迹

---

### 2026-05-01

**TRELLIS.2: Native and Compact Structured Latents for 3D Generation**
**原生紧凑结构化隐空间三维生成（TRELLIS.2）**

- **来源**：CVPR 2026 Oral
- **作者**：Jianfeng Xiang, Xiaoxue Chen, Sicheng Xu, Ruicheng Wang, Zelong Lv, Yu Deng, Hongyuan Zhu, Yue Dong, Hao Zhao, Nicholas Jing Yuan, Jiaolong Yang（清华大学 & 微软研究院 & 中国科学技术大学）
- **链接**：https://arxiv.org/abs/2512.14692 | 项目页：https://microsoft.github.io/TRELLIS.2/

**核心内容**：TRELLIS.2 是微软研究院提出的新一代三维生成框架，其核心创新是 O-Voxel（Omni-Voxel，全能体素）——一种新型稀疏体素结构，通过灵活的对偶网格（Flexible Dual Grids）同时编码几何与外观信息，能够鲁棒处理任意拓扑，并支持完整的 PBR 材质属性。基于 O-Voxel，作者设计了稀疏压缩变分自编码器（SC-VAE），实现 16 倍空间下采样，将 1024³ 分辨率的全纹理资产压缩至约 9.6K 隐变量。在此紧凑隐空间上，作者训练了 40 亿参数的流匹配（Flow Matching）生成模型，可在 3 秒（512³）至 60 秒（1536³）内高效生成高分辨率 PBR 材质三维资产。

**亮点**：

1. 原生三维表示突破拓扑瓶颈：O-Voxel 彻底摆脱等值面（iso-surface）场的拓扑约束，通过稀疏体素 + 灵活对偶网格统一编码几何与 PBR 材质，支持开放曲面、非流形几何和封闭内部结构，是首个在单一表示中同时解决任意拓扑与丰富材质建模的三维生成框架
2. 极致压缩与高效生成的完美平衡：SC-VAE 实现 16 倍空间下采样，将百万级体素压缩至约 9.6K 隐变量，压缩率远超现有三维 VAE 方案；在此超紧凑隐空间上训练的 40 亿参数流匹配模型，推理效率极高（512³ 仅需 3 秒）
3. 即插即用的极简数据处理流程：O-Voxel 支持与标准纹理网格的即时双向无损转换（CPU 单核 < 10 秒完成网格→O-Voxel，CUDA 加速 < 100ms 完成 O-Voxel→网格），无需任何优化迭代或可微渲染

---

### 2026-05-04

**GLINT: Modeling Scene-Scale Transparency via Gaussian Radiance Transport**
**通过高斯辐射传输建模场景级透明表面（GLINT）**

- **来源**：CVPR 2026 Oral
- **作者**：Youngju Na, Jaeseong Yun, Soohyun Ryu, Hyunsu Kim, Sung-Eui Yoon, Suyong Yeon（KAIST & NAVER LABS）
- **链接**：https://arxiv.org/abs/2603.26181 | 项目页：https://youngju-na.github.io/GLINT/ | 代码：https://github.com/youngju-na/GLINT

**核心内容**：GLINT 是首个在 3D Gaussian Splatting 框架下系统解决场景级透明表面建模问题的方法，获 CVPR 2026 Oral。GLINT 提出了分解高斯辐射传输（Decomposed Gaussian Radiance Transport）框架：将场景中的透明界面显式建模为独立的界面高斯层，并将出射辐射分解为界面自身辐射、反射辐射和透射辐射三个物理分量，通过混合渲染管线（光栅化处理界面层 + 光线追踪处理反射/透射路径）实现物理一致的辐射传输。在优化阶段，GLINT 利用几何分离线索（geometry separation cues）自举透明区域定位，无需任何显式分割 mask 监督即可自动发现并精确建模透明区域。

**亮点**：

1. 物理驱动的辐射传输分解：GLINT 将透明界面的出射辐射显式分解为界面辐射、反射辐射和透射辐射三个物理分量，通过混合渲染管线（光栅化 + 光线追踪）实现物理一致的高斯辐射传输，从根本上解决了 3DGS 在透明表面上几何错误与渲染伪影并存的核心难题
2. 无监督透明区域自举定位：GLINT 利用分解表示中自然涌现的几何分离线索，结合预训练视频重光照模型的几何与材质先验，在无需任何显式透明区域分割 mask 的情况下自动完成透明界面定位与解耦
3. 场景级透明建模能力：GLINT 支持玻璃幕墙、展示柜、落地窗等大尺度场景级透明结构的高质量重建，在合成与真实数据集上均达到 SOTA 性能，为室内场景重建、AR/VR 内容制作等提供坚实的技术基础

---

### 2026-05-05

**MV-RoMa: From Pairwise Matching into Multi-View Track Reconstruction**
**从成对匹配到多视图轨迹重建（MV-RoMa）**

- **来源**：CVPR 2026
- **作者**：JongMin Lee, Seungyeop Kang, Sungjoo Yoo（首尔大学）
- **链接**：https://arxiv.org/abs/2603.27542 | 项目页：https://icetea-cv.github.io/mv-roma/

**核心内容**：MV-RoMa 是首个多视图稠密匹配模型，解决了现有方法在成对匹配范式下链式传播时产生碎片化、几何不一致轨迹的核心问题。MV-RoMa 提出从源图像到多个共视目标图同时联合估计稠密对应关系的新范式：（1）多视图编码器以成对匹配结果为几何先验，通过高效的多视图特征交互建立全局一致的特征表示；（2）像素对齐多视图精炼器利用像素级注意力精细化对应关系，产生高度一致的跨视图匹配轨迹；（3）后处理策略将模型输出的多视图一致对应关系作为高质量轨迹直接馈入 SfM 管线。

**亮点**：

1. 首个多视图稠密匹配范式：MV-RoMa 打破了"成对匹配后拼接"的传统范式，首次实现了从一张源图像到多个共视目标图的联合稠密对应估计，通过多视图编码器引入成对匹配几何先验，从根本上消除了逐对处理带来的几何不一致性问题
2. 端到端高质量 SfM 轨迹生成：MV-RoMa 的后处理策略将多视图一致对应关系直接作为高质量轨迹注入 SfM 管线，在 ETH3D、IMC Photo Tourism 等标准三维重建基准上，三维重建的轨迹稠密度和精度均大幅超越现有最优的稀疏（SuperGlue、LightGlue）和稠密（RoMa、DKM）匹配方法
3. 高效多视图架构设计：针对多视图场景下全注意力机制的计算代价随视图数呈二次方增长的瓶颈，MV-RoMa 设计了层次化的多视图编码-精炼架构，使整体计算复杂度接近线性，在保证多视图一致性的同时具备良好的可扩展性

---

### 2026-05-06

**Stochastic Ray Tracing for the Reconstruction of 3D Gaussian Splatting**
**用于三维高斯泼溅重建的随机光线追踪**

- **来源**：CVPR 2026
- **作者**：Peiyu Xu, Xin Sun, Krishna Mullia, Raymond Fei, Iliyan Georgiev, Shuang Zhao（UC Irvine & Adobe Research & NVIDIA）
- **链接**：https://arxiv.org/abs/2603.23637 | 项目页：https://xupaya.github.io/stoch3DGS/

**核心内容**：本文提出首个面向标准与可重光照 3DGS 的无排序可微随机光线追踪框架。核心贡献是基于无偏蒙特卡洛估计器的像素颜色梯度计算——每条光线仅对随机采样的少量高斯子集求值，完全规避排序需求。对于标准 3DGS 重建，该方法在重建质量和速度上与基于光栅化的 3DGS 持平，同时大幅超越基于排序的光线追踪方法。对于可重光照 3DGS，同一随机估计器驱动逐高斯着色与全光线追踪阴影光线计算，重建保真度显著超越现有方法。

**亮点**：

1. 首个无排序可微随机光线追踪框架：通过无偏蒙特卡洛估计器对像素颜色梯度进行随机近似，每条光线仅评估少量随机子集高斯，彻底绕过 3D Gaussian 光线追踪中成本最高的全局排序操作，同时保持梯度估计的无偏性
2. 重建与渲染的统一物理一致框架：对于可重光照场景，同一随机估计器同时驱动逐高斯 PBR 着色与全光线追踪阴影光线（shadow rays），完全抛弃了现有方法依赖的阴影贴图近似，首次在 3DGS 框架内实现了重建阶段与渲染阶段的全光线追踪统一
3. 支持非针孔相机与复杂光学效应：光线追踪框架天然支持鱼眼、全景等非针孔相机模型及反射、折射等复杂光学传输效应，为自动驾驶、医疗成像等依赖特种相机的场景重建提供了更通用的 3DGS 方案

---

### 2026-05-07

**MoRE: 3D Visual Geometry Reconstruction Meets Mixture-of-Experts**
**MoRE：三维视觉几何重建遇见混合专家模型**

- **来源**：CVPR 2026
- **作者**：Jingnan Gao, Zhe Wang, Xianze Fang, Xingyu Ren, Zhuo Chen, Shengqi Liu, Yuhao Cheng, Jiangjing Lyu, Xiaokang Yang, Yichao Yan（上海交通大学 & 阿里巴巴集团）
- **链接**：https://arxiv.org/abs/2510.27234 | 项目页：https://g-1nonly.github.io/MoRE_Website/ | 代码：https://github.com/alibaba/Taobao3D

**核心内容**：本文提出 MoRE——一种基于混合专家（MoE）架构的稠密三维视觉基础模型。MoRE 将特征动态路由至任务专属专家，使各专家专注于互补的数据特征，从而同时提升模型的可扩展性与适应性。为增强真实场景下的鲁棒性，MoRE 引入了基于置信度的深度精炼模块，稳定并优化几何估计结果。此外，模型将稠密语义特征与全局对齐的三维骨干表示相融合，实现高保真表面法线预测。大量实验表明，MoRE 在多个基准测试上达到最先进性能。

**亮点**：

1. 首个将混合专家（MoE）架构引入三维视觉几何基础模型：MoRE 通过动态路由机制将特征分配给任务专属专家（深度估计、表面法线预测、点图估计等），突破了单一密集网络在多任务几何学习中的容量瓶颈，在保持推理效率的同时实现了模型容量的高效扩展
2. 置信度引导的深度精炼模块：针对真实场景中深度估计不稳定的问题，MoRE 设计了基于置信度的深度精炼模块，通过预测每个像素的置信度权重来动态调整深度估计，有效过滤低置信度区域的噪声预测
3. 语义与几何的深度融合：MoRE 将稠密语义特征与全局对齐的三维骨干表示相结合，用于高保真表面法线预测，实现了语义理解与几何重建的协同增强；配合针对多任务几何学习设计的定制化损失函数，模型在深度估计、表面法线预测、多视图三维重建等多个基准上均达到最先进水平

---

### 2026-05-08

**Layered 4D-Rotor Gaussian Splatting: A Compressed Representation for Long Dynamic Scenes**
**分层四维旋转体高斯泼溅：长时动态场景的压缩表示**

- **来源**：CVPR 2026
- **作者**：Hanjie Xu*, Yuanxing Duan*, Qiyu Dai*, Ge Li†, Baoquan Chen†, He Wang†（北京大学前沿计算研究中心）
- **链接**：https://cvpr.thecvf.com/virtual/2026/poster/36256 | 项目页：https://m1sak1-mei.github.io/layered-4d-rotor/

**核心内容**：本文提出 L4DRotorGS（Layered 4D-Rotor Gaussian Splatting），一种专为长时动态场景设计的统一压缩表示框架。核心设计是将 4D 高斯按时间跨度组织成分层结构，再将每层划分为离散的时间桶（temporal buckets），实现对必要子集的按需访问与渲染，大幅降低 GPU 显存需求。在压缩方面，结合三种互补技术：因式协方差量化（Factorized Covariance Quantization）、分层压缩（Layered Compression）和残差码本量化（Residual Codebook Quantization），实现高达 22.3× 的压缩比，同时保持高视觉保真度。作者还设计了高度优化的 C++/CUDA 框架，实现了超过 500 FPS 的实时渲染速度（RTX 3090）。

**亮点**：

1. 首个专为长时动态场景设计的压缩 4DGS 框架：L4DRotorGS 突破了现有 4DGS 方法局限于短时（<10秒）场景的瓶颈，通过分层时间组织结构（按时间跨度分层 + 离散时间桶划分），实现对长时动态场景的高效编码与按需渲染；分层结构不仅使 GPU 显存消耗与场景时长解耦，还为后续基于时间局部性的压缩和渲染优化提供了天然的结构基础
2. 三重量化压缩协同实现 22.3× 极致压缩：通过因式协方差量化、分层压缩和残差码本量化三种技术的有机结合，在极大压缩存储占用的同时保持高视觉保真度；相比现有 4DGS 方法，存储占用减少超过 20 倍，使移动端或边缘设备部署长时动态场景渲染成为可能
3. 高度优化的 C++/CUDA 实现支持 500+ FPS 实时渲染：区别于仅关注重建质量的学术工作，L4DRotorGS 还设计了高度工程化的 C++/CUDA 训练-压缩-渲染一体化框架，在 RTX 3090 上实现超过 500 FPS 的实时渲染速度，远超现有 4DGS 方法

---

*最后更新：2026-05-08*
