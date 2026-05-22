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
- **FastGS**（2026-05-15）— 基于多视角一致性的稠密化与剪枝策略，100 秒完成单场景训练，相比原始 3DGS 加速 15.45×，通用即插即用加速框架 · [CVPR 2026 Highlight](https://arxiv.org/abs/2511.04283)

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
- **Fast3R**（2026-05-13）— DUSt3R 多视图扩展，单次前向传播并行处理 1000+ 张无序无位姿图像，推理速度较 DUSt3R 提升 320 倍 · [CVPR 2025](https://arxiv.org/abs/2501.13928)
- **MUSt3R**（2026-05-12）— DUSt3R 架构对称化扩展至多视图，多层工作记忆机制将复杂度从 O(N²) 降至 O(N)，支持千帧级实时重建与在线 SLAM · [CVPR 2025](https://arxiv.org/abs/2503.01661)

### 🎬 六、4D 动态场景重建（4D Dynamic Scene Reconstruction）

研究将三维高斯表示扩展到时间维度，实现动态场景的连续时间重建与任意时刻渲染，解决时间混叠、鬼影等核心挑战。

- **RetimeGS**（2026-04-28）— 连续时间 4DGS 表示，光流引导初始化 + 三重渲染监督，任意时刻无鬼影重建 · [CVPR 2026 Oral](https://arxiv.org/abs/2603.13783)
- **L4DRotorGS**（2026-05-08）— 分层 4D 旋转体高斯泼溅，22.3× 压缩率支持长时动态场景（>10s），RTX 3090 实现 500+ FPS · [CVPR 2026](https://cvpr.thecvf.com/virtual/2026/poster/36256)

### 📡 七、SLAM / 实时三维重建（SLAM / Real-Time 3D Reconstruction）

研究实时同步定位与建图系统，探索在动态真实场景中鲁棒跟踪与高质量稠密重建的方法。

- **DROID-W**（2026-04-30）— 基于动态不确定性感知可微 BA 的 RGB SLAM，无需类别先验即可鲁棒处理真实动态场景，ETH Zürich + 微软 · [CVPR 2026](https://arxiv.org/abs/2603.19076)
- **SLAM3R**（2026-05-14）— 端到端实时稠密重建，无需显式位姿估计，滑动窗口 + 全局配准网络，20+ FPS 达 SOTA，CVPR 2025 Highlight · [CVPR 2025 Highlight](https://arxiv.org/abs/2412.09401)
- **MASt3R-SLAM**（2026-05-20）— 首个以 MASt3R 三维重建先验为基础的实时单目稠密 SLAM，无需相机标定，15 FPS 实时性能，多基准 SOTA · [CVPR 2025](https://arxiv.org/abs/2412.12392)

### 🎨 八、三维生成（3D Generation）

研究从文本、图像等条件生成高质量三维资产的方法，涵盖原生三维表示学习、扩散/流匹配生成模型、PBR 材质建模等核心技术。

- **TRELLIS.2**（2026-05-01）— 原生紧凑结构化隐空间 + 40亿参数流匹配模型，数秒内生成高分辨率 PBR 材质三维资产，微软研究院 · [CVPR 2026 Oral](https://arxiv.org/abs/2512.14692)
- **CraftsMan3D**（2026-05-22）— 原生三维扩散 + 法线增强几何细化两阶段生成，30 秒内生成工业级高保真网格，支持交互式编辑，CVPR 2025 满分 · [CVPR 2025](https://arxiv.org/abs/2405.14979)

### 🪟 九、3DGS 透明表面建模（Transparent Surface Modeling）

研究如何在 3D Gaussian Splatting 框架中建模玻璃、水面等透明/半透明界面，通过辐射传输分解实现物理一致的反射与透射渲染。

- **GLINT**（2026-05-04）— 分解高斯辐射传输建模场景级透明表面，无需显式分割 mask 即可自动定位透明区域，NAVER LABS · [CVPR 2026 Oral](https://arxiv.org/abs/2603.26181)

### 🔍 十、多视图稠密匹配与三维重建（MVS / Dense Matching）

研究从多张图像建立稠密、一致的像素级对应关系，为 SfM 和三维重建提供高精度轨迹，突破成对匹配范式，追求全局几何一致性。

- **MV-RoMa**（2026-05-05）— 首个多视图稠密匹配模型，Track-Guided 多视图编码器 + 像素对齐精炼器，SfM 全面超越稀疏/稠密匹配基线 · [CVPR 2026](https://arxiv.org/abs/2603.27542)

### 🌐 十一、NeRF / 逆向渲染（NeRF / Inverse Rendering）

研究基于神经辐射场的场景表示与逆向渲染方法，联合估计场景几何、材质与光照，实现物理一致的新视角合成与重光照。

- **PBR-NeRF**（2026-05-11）— 基于物理渲染理论的 NeRF 逆向渲染，两个新颖物理先验约束材质估计，ETH Zürich · [CVPR 2025](https://arxiv.org/abs/2412.09680)
- **DiffusionRenderer**（2026-05-18）— 视频扩散模型驱动的神经逆向与正向渲染统一框架，G-buffer 估计 + 重光照，NVIDIA Research · [CVPR 2025 Oral](https://arxiv.org/abs/2501.18590)

---

## 论文列表

### 2026-04-13 · AnchorSplat

**AnchorSplat: Feed-Forward 3D Gaussian Splatting with 3D Geometric Priors**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2604.07053

提出以三维几何先验（稀疏点云/体素/RGB-D 点云）为锚点，直接在 3D 空间中生成高斯基元，打破了传统像素对齐范式。引入 Gaussian Refiner 模块进行轻量级精细化，在 ScanNet++ v2 NVS 基准上达到 SOTA。锚点对齐高斯表示不依赖图像分辨率和视角数量，视角一致性显著提升，大幅减少高斯基元数量，兼顾计算效率与重建保真度。

---

### 2026-04-14 · SparseSplat

**SparseSplat: Towards Applicable Feed-Forward 3D Gaussian Splatting with Pixel-Unaligned Prediction**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2604.03069

首个能根据场景结构和局部区域信息丰富度自适应调整高斯密度的前馈式 3DGS 模型。通过基于熵的概率采样策略，在纹理稀少区域生成大而稀疏的高斯基元，在信息丰富区域分配小而密集的高斯基元。仅用 22% 的高斯基元即可达到 SOTA 渲染质量，仅用 1.5% 的高斯基元仍能保持合理渲染质量。

---

### 2026-04-15 · UniSplat

**UniSplat: Learning 3D Representations for Spatial Intelligence from Unposed Multi-View Images**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2604.10573

从无位姿（unposed）稀疏多视图图像中学习统一的三维表示，为空间智能（场景理解、具身 AI）提供感知基础。核心组件包括：双重掩码策略（dual-masking）、由粗到细的高斯泼溅策略（coarse-to-fine Gaussian splatting）、位姿条件重校准机制（pose-conditioned recalibration）。无需相机位姿即可获得高质量几何感知表示，大幅降低数据采集门槛。

---

### 2026-04-16 · tttLRM

**tttLRM: Test-Time Training for Long Context and Autoregressive 3D Reconstruction**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2602.20160

将测试时训练（Test-Time Training, TTT）层引入三维重建任务，实现具有线性计算复杂度的长上下文自回归三维重建。将多幅图像观测压缩到 TTT 层的快速权重中，形成隐空间中的隐式三维表示，可解码为高斯泼溅等显式格式。在线学习变体支持从流式观测中进行渐进式三维重建与精细化。

---

### 2026-04-17 · IDESplat

**IDESplat: Iterative Depth Probability Estimation for Generalizable 3D Gaussian Splatting**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2601.03824

通过迭代深度概率估计来精准预测高斯球中心。引入深度概率增强单元（DPBU），通过级联 warp 操作生成极线注意力图并以乘法方式融合，消除单次 warp 的固有不稳定性。在 RE10K 上以仅 10.7% 的参数量和 70% 的显存，PSNR 超越 DepthSplat 0.33 dB；在跨数据集 DTU 实验中 PSNR 提升 2.95 dB。

---

### 2026-04-21 · C3G

**C3G: Learning Compact 3D Representations with 2K Gaussians**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2512.04021

通过仅在关键空间位置估计约 2K 个紧凑高斯来完成无位姿稀疏视图的三维场景重建与理解。引入可学习 token，通过自注意力机制聚合多视图特征，指导高斯基元的空间分配。在无位姿新视角合成、三维开放词汇分割和视角不变特征聚合等任务上均达到 SOTA。

---

### 2026-04-22 · Proxy-GS

**Proxy-GS: Unified Occlusion Priors for Training and Inference in Structured 3D Gaussian Splatting**

- **来源**：CVPR 2026 Oral
- **链接**：https://arxiv.org/abs/2509.24421

利用轻量级代理网格（proxy mesh）引入统一的遮挡先验，在推理阶段以不到 1ms 的速度生成精确遮挡深度图，用于剔除被遮挡的锚点和高斯基元；在训练阶段引导高斯增密沿代理表面生长。在 MatrixCity Streets 等遮挡密集数据集上，相比 Octree-GS 实现超过 2.5 倍的渲染加速，同时显著提升渲染质量。

---

### 2026-04-23 · NimbusGS

**NimbusGS: Unified 3D Scene Reconstruction under Hybrid Weather**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2603.27228

统一框架用于从多视图退化图像（雾、雨、雪及其混合天气）中重建高质量三维场景。将天气退化分解为全局传输场（跨视图一致的连续介质）和逐视图粒子残差（每帧独立的动态粒子）两类，并引入几何引导的梯度缩放机制缓解严重能见度退化时的梯度失衡问题。在多种天气条件下的几何重建质量均超越各类天气专用方法。

---

### 2026-04-24 · VAD-GS

**VAD-GS: Visibility-Aware Densification for 3D Gaussian Splatting in Dynamic Urban Scenes**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2510.09364

针对动态、无界城市场景中 3DGS 几何重建质量不足的问题，提出可见性感知的致密化框架。通过基于体素的可见性推理识别不可靠几何结构，利用多样性感知视图选择挑选最具信息量的支撑视图，再以块匹配多视图立体（patch matching MVS）重建缺失结构。在 Waymo 和 nuScenes 数据集上超越当前最优 3DGS 方法。

---

### 2026-04-27 · VGGT

**VGGT: Visual Geometry Grounded Transformer**

- **来源**：CVPR 2025 Best Paper Award
- **链接**：https://arxiv.org/abs/2503.11651

纯前馈神经网络，能够直接从一张、几张乃至数百张输入视图中推理出场景的所有关键三维属性，包括相机参数、点图、深度图以及三维点轨迹。完全摒弃了几何后处理步骤，实现真正意义上的端到端三维几何推理。单张图像重建仅需不到 1 秒，在相机参数估计、多视图深度估计、稠密点云重建和三维点跟踪等多个任务上超越了需要几何优化的竞争方法。

---

### 2026-04-28 · RetimeGS

**RetimeGS: Continuous-Time Reconstruction of 4D Gaussian Splatting**

- **来源**：CVPR 2026 Oral
- **链接**：https://arxiv.org/abs/2603.13783

将时间混叠（temporal aliasing）定义为 4DGS 在时间插值时产生鬼影的根本原因，并提出连续时间 4DGS 表示，显式定义三维高斯的时间行为以缓解时间混叠。引入光流引导的初始化与监督、三重渲染监督等策略，即使在大运动场景下也能实现无鬼影、时间连贯的渲染。

---

### 2026-04-29 · Uni3R

**Uni3R: Unified 3D Reconstruction and Semantic Understanding via Generalizable Gaussian Splatting**

- **来源**：CVPR 2026 Highlight
- **链接**：https://arxiv.org/abs/2508.03643

从无位姿多视图图像中联合重建统一的三维场景表示，并同时赋予其开放词汇语义理解能力。核心是跨视图 Transformer，回归一组携带语义特征场的三维高斯基元，在单次前馈传递中同时支持高保真新视角合成、开放词汇三维语义分割和深度预测。在 RE10K 达到 25.07 PSNR，在 ScanNet 达到 55.84 mIoU，整个场景重建仅需约 0.15 秒。

---

### 2026-04-30 · DROID-W

**DROID-SLAM in the Wild**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2603.19076

面向真实野外动态场景的鲁棒实时 RGB SLAM 系统。将动态不确定性显式建模为逐像素连续值，通过多视角 DINO 特征一致性检测视觉不一致区域，并将其无缝嵌入可微 Bundle Adjustment 优化框架。在 DROID-W 数据集（7 段室外高动态序列 + RTK 真值轨迹）上平均轨迹误差仅 23cm，而原始 DROID-SLAM 误差高达 1.46m。

---

### 2026-05-01 · TRELLIS.2

**TRELLIS.2: Native and Compact Structured Latents for 3D Generation**

- **来源**：CVPR 2026 Oral
- **链接**：https://arxiv.org/abs/2512.14692

提出 O-Voxel（全能体素）——新型稀疏体素结构，通过灵活的对偶网格同时编码几何与外观信息，支持任意拓扑和完整 PBR 材质属性。基于 O-Voxel 设计稀疏压缩变分自编码器（SC-VAE），实现 16 倍空间下采样。在此紧凑隐空间上训练 40 亿参数的流匹配生成模型，可在 3 秒（512 分辨率）至 60 秒（1536 分辨率）内高效生成高分辨率 PBR 材质三维资产。

---

### 2026-05-04 · GLINT

**GLINT: Modeling Scene-Scale Transparency via Gaussian Radiance Transport**

- **来源**：CVPR 2026 Oral
- **链接**：https://arxiv.org/abs/2603.26181

首个在 3D Gaussian Splatting 框架下系统解决场景级透明表面建模问题的方法。提出分解高斯辐射传输（Decomposed Gaussian Radiance Transport）框架，将出射辐射分解为界面自身辐射、反射辐射和透射辐射三个物理分量，通过混合渲染管线（光栅化 + 光线追踪）实现物理一致的辐射传输。无需任何显式透明区域分割 mask 即可自动完成透明界面定位与解耦。

---

### 2026-05-05 · MV-RoMa

**MV-RoMa: From Pairwise Matching into Multi-View Track Reconstruction**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2603.27542

首个多视图稠密匹配模型，从源图像到多个共视目标图同时联合估计稠密对应关系。多视图编码器以成对匹配结果为几何先验，通过高效的多视图特征交互建立全局一致的特征表示；像素对齐多视图精炼器利用像素级注意力精细化对应关系。在 ETH3D、IMC Photo Tourism 等标准三维重建基准上，三维重建的轨迹稠密度和精度均大幅超越现有最优方法。

---

### 2026-05-06 · Stochastic Ray Tracing for 3DGS

**Stochastic Ray Tracing for the Reconstruction of 3D Gaussian Splatting**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2603.23637

首个面向标准与可重光照 3DGS 的无排序可微随机光线追踪框架。基于无偏蒙特卡洛估计器的像素颜色梯度计算——每条光线仅对随机采样的少量高斯子集求值，完全规避排序需求。对于可重光照场景，同一随机估计器同时驱动逐高斯 PBR 着色与全光线追踪阴影光线，天然支持非针孔相机模型及反射、折射等复杂光学传输效应。

---

### 2026-05-07 · MoRE

**MoRE: 3D Visual Geometry Reconstruction Meets Mixture-of-Experts**

- **来源**：CVPR 2026
- **链接**：https://arxiv.org/abs/2510.27234

基于混合专家（MoE）架构的稠密三维视觉基础模型。将特征动态路由至任务专属专家，使各专家专注于互补的数据特征，同时提升模型的可扩展性与适应性。引入基于置信度的深度精炼模块，稳定并优化几何估计结果。将稠密语义特征与全局对齐的三维骨干表示相融合，实现高保真表面法线预测，在多个基准测试上达到最先进水平。

---

### 2026-05-08 · L4DRotorGS

**Layered 4D-Rotor Gaussian Splatting: A Compressed Representation for Long Dynamic Scenes**

- **来源**：CVPR 2026
- **链接**：https://cvpr.thecvf.com/virtual/2026/poster/36256

专为长时动态场景设计的统一压缩表示框架。将 4D 高斯按时间跨度组织成分层结构，再划分为离散的时间桶，实现按需访问与渲染。结合因式协方差量化、分层压缩和残差码本量化三种技术，实现高达 22.3 倍的压缩比。高度优化的 C++/CUDA 框架在 RTX 3090 上实现超过 500 FPS 的实时渲染速度。

---

### 2026-05-11 · PBR-NeRF

**PBR-NeRF: Inverse Rendering with Physics-Based Neural Fields**

- **来源**：CVPR 2025
- **链接**：https://arxiv.org/abs/2412.09680

将物理渲染（PBR）理论与神经辐射场相结合，构建能够联合估计场景几何、材质（基色、粗糙度、金属度）和环境光照的逆向渲染模型。引入两个新颖的物理先验损失项：基于物理一致性的材质正则化，以及基于渲染方程的光照一致性先验。在不牺牲新视角合成质量的前提下，显著提升了材质估计的精度，达到当时最先进水平。

---

### 2026-05-12 · MUSt3R

**MUSt3R: Multi-view Network for Stereo 3D Reconstruction**

- **来源**：CVPR 2025
- **链接**：https://arxiv.org/abs/2503.01661

将 DUSt3R 从图像对扩展至多视图，通过对称化架构和多层工作记忆机制将复杂度从 O(N^2) 降至 O(N)，支持千帧级实时重建与在线 SLAM。在未校准视觉里程计、相对相机位姿估计、尺度与焦距估计、三维重建以及多视图深度估计等多项下游任务上均达到最先进性能。

---

### 2026-05-13 · Fast3R

**Fast3R: Towards 3D Reconstruction of 1000+ Images in One Forward Pass**

- **来源**：CVPR 2025
- **链接**：https://arxiv.org/abs/2501.13928

单次前向传播并行处理 1000+ 张无序无位姿图像，推理速度较 DUSt3R 提升 320 倍（251 FPS vs 0.78 FPS），在相机位姿估计和三维重建基准上达到最先进性能。

---

### 2026-05-14 · SLAM3R

**SLAM3R: Real-Time Dense Scene Reconstruction from Monocular RGB Videos**

- **来源**：CVPR 2025 Highlight
- **链接**：https://arxiv.org/abs/2412.09401

端到端实时稠密重建，无需显式位姿估计，滑动窗口 + 全局配准网络，20+ FPS 达 SOTA，可在消费级显卡（RTX 4090D）上运行。

---

### 2026-05-15 · FastGS

**FastGS: Training 3D Gaussian Splatting in 100 Seconds**

- **来源**：CVPR 2026 Highlight
- **链接**：https://arxiv.org/abs/2511.04283

基于多视角一致性的稠密化与剪枝策略，100 秒完成单场景训练，相比原始 3DGS 加速 15.45 倍。通用即插即用加速框架，覆盖动态场景、表面重建、稀疏视角、大尺度重建和 SLAM 等多种任务，均可实现 2-7 倍训练加速。

---

### 2026-05-18 · DiffusionRenderer

**DiffusionRenderer: Neural Inverse and Forward Rendering with Video Diffusion Models**

- **来源**：CVPR 2025 Oral（NVIDIA Research × 多伦多大学 × 矢量研究所 × 伊利诺伊大学香槟分校）
- **链接**：https://arxiv.org/abs/2501.18590

首次将神经逆向渲染与正向渲染统一在单一框架中。逆向渲染模块利用视频扩散模型先验，从真实世界视频中准确估计 G-buffer（法线、深度、漫反射反照率、粗糙度、金属度等材质属性）；正向渲染模块则无需显式光线传输模拟，直接基于 G-buffer 和指定光照条件生成逼真图像。两个模块相互促进，形成自洽闭环。实验表明在逆向渲染和正向渲染两个任务上均超越当前最先进方法，并从单段视频输入实现重新打光（relighting）、材质编辑和真实感物体插入等实用应用。

---

### 2026-05-20 · MASt3R-SLAM

**MASt3R-SLAM: Real-Time Dense SLAM with 3D Reconstruction Priors**

- **来源**：CVPR 2025（Imperial College London）
- **链接**：https://arxiv.org/abs/2412.12392

首个以双视图三维重建先验（MASt3R）为基础自底向上构建的实时单目稠密 SLAM 系统。将 MASt3R 强大的三维重建先验深度集成到 SLAM 的跟踪、建图、回环检测和全局优化各个核心模块中，通过点图匹配实现大规模并行相机跟踪，利用光线角度误差最小化进行局部融合，并通过二阶全局优化获得全局一致的位姿和稠密几何。系统除唯一相机中心外不对相机模型做任何假设，在标准 GPU 上可达 15 FPS 实时性能，在 EuRoC、TUM-RGBD、ScanNet 等主流 SLAM 基准上达到最先进性能。

---

### 2026-05-22 · CraftsMan3D

**CraftsMan3D: High-fidelity Mesh Generation with 3D Native Generation and Interactive Geometry Refiner**

- **来源**：CVPR 2025（香港科技大学 × Adobe Research × 光影焕像）
- **链接**：https://arxiv.org/abs/2405.14979

借鉴传统艺术家建模工作流，将三维生成分为两个阶段：第一阶段由原生三维扩散模型直接在三维空间中生成具有平滑几何形状的粗糙网格（约 5 秒），无需依赖多视图图像的中间表示；第二阶段通过法线增强的几何细化器对粗糙网格进行高频细节补全（约 20 秒），利用 2D 法线扩散模型生成多视图法线图并将其转化为精细几何细节。整个流程仅需约 30 秒，生成的网格具有规则拓扑结构，可直接用于游戏、影视等工业级三维内容创作场景。在 CVPR 2025 获得三位评审一致满分评价，已被 Roblox、腾讯混元 Hunyuan3D-2 等头部平台采用。

---

*最后更新：2026-05-22 | 维护：CatDesk 自动化任务*
