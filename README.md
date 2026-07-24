# 三维重建论文收藏

三维重建论文收藏

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
- **SSS（3D Student Splatting and Scooping）**（2026-06-02）— Student's t 分布替代高斯基元 + 负密度"舀取"机制，组件数减少 82% 仍保持可比质量 · [CVPR 2025 Oral](https://arxiv.org/abs/2503.10148)
- **Vol3DGS**（2026-06-18）— 解析体积积分替代 EWA splatting 近似，物理精确 alpha 计算，SSIM/LPIPS 超越 3DGS，天然支持 CT 断层扫描重建 · [CVPR 2025 Highlight](https://arxiv.org/abs/2412.03378)
- **3DGS-MCMC**（2026-06-26）— 将3DGS优化重构为MCMC采样，消除启发式增密剪枝，对初始化鲁棒 · [NeurIPS 2024](https://arxiv.org/abs/2404.09591)
- **Neural Gabor Splatting**（2026-07-06）— 轻量 MLP 赋予单个高斯基元丰富色彩变化能力，频率感知稠密化精准控制基元数量，高频表面重建新范式 · [CVPR 2026](https://arxiv.org/abs/2604.15941)
- **Eulerian Gaussian Splatting**（2026-07-24）— 欧拉视角概率密度优化替代启发式增密/剪枝，哈希概率金字塔实现可学习密度场，质量与效率双赢 · [CVPR 2026](https://arxiv.org/abs/2605.29136)

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
- **CUT3R**（2026-05-28）— 具有持久状态记忆的循环 Transformer，在线流式逐帧处理生成度量尺度点云，支持静态与动态场景统一感知，UC Berkeley · [CVPR 2025](https://arxiv.org/abs/2501.12387)
- **MVGD**（2026-06-05）— 射线图条件化赋予扩散模型几何感知，零样本多视角 RGB 与深度联合生成，免中间三维表示，Toyota Research Institute · [CVPR 2025](https://arxiv.org/abs/2501.18804)
- **OmniVGGT**（2026-06-15）— 全模态驱动视觉几何基础模型，GeoAdapter 渐进注入深度/相机几何先验，随机多模态融合训练支持任意辅助输入，港科大 × 南洋理工 · [CVPR 2026 Highlight](https://arxiv.org/abs/2511.10560)
- **FoundationStereo**（2026-06-23）— CVPR 2025 Best Paper Candidate，首个具备强零样本泛化能力的立体深度估计基础模型，百万级合成数据 + 自筛选 + Side-Tuning Adapter 融合单目先验 · [CVPR 2025 Best Paper Candidate](https://arxiv.org/abs/2501.09898)
- **Online3R**（2026-07-01）— CVPR 2026，基于几何基础模型的序列重建在线学习框架，参数高效视觉提示 + 自监督局部/全局一致性约束，实时适应新场景 · [CVPR 2026](https://arxiv.org/abs/2604.09480)
- **DUSt3R**（2026-07-14）— 开创性端到端几何三维视觉范式，点图回归统一单目/双目重建，无需标定或位姿先验，催生 MASt3R/Fast3R/MUSt3R 等系列工作，CVPR 2024 奠基之作 · [CVPR 2024](https://arxiv.org/abs/2312.14132)
- **VGGT-Ω**（2026-07-20）— 首次揭示前馈三维重建 Scaling Law，10B 参数 + 寄存器注意力支持 15× 数据量，Sintel 相机估计精度提升 77%，CVPR 2026 Oral / Best Paper Finalist · [CVPR 2026 Oral / Best Paper Finalist](https://arxiv.org/abs/2605.15195)

### 🎬 六、4D 动态场景重建（4D Dynamic Scene Reconstruction）

研究将三维高斯表示扩展到时间维度，实现动态场景的连续时间重建与任意时刻渲染，解决时间混叠、鬼影等核心挑战。

- **RetimeGS**（2026-04-28）— 连续时间 4DGS 表示，光流引导初始化 + 三重渲染监督，任意时刻无鬼影重建 · [CVPR 2026 Oral](https://arxiv.org/abs/2603.13783)
- **L4DRotorGS**（2026-05-08）— 分层 4D 旋转体高斯泼溅，22.3× 压缩率支持长时动态场景（>10s），RTX 3090 实现 500+ FPS · [CVPR 2026](https://cvpr.thecvf.com/virtual/2026/poster/36256)
- **IGS（Instant Gaussian Stream）**（2026-06-03）— 首个可泛化流式 4D 高斯重建，时序锚点机制维持跨帧一致性，2.67s/帧重建 + 204 FPS 渲染，CVPR 2025 Highlight · [CVPR 2025 Highlight](https://arxiv.org/abs/2503.16979)

### 📡 七、SLAM / 实时三维重建（SLAM / Real-Time 3D Reconstruction）

研究实时同步定位与建图系统，探索在动态真实场景中鲁棒跟踪与高质量稠密重建的方法。

- **Immediate GS Reconstruction**（2026-07-16）— 首个无序输入即时 3DGS 重建，视觉地点识别 + 簇基回环检测提供全局一致性，INRIA · [SIGGRAPH 2026](https://arxiv.org/abs/2607.14481)
- **DROID-W**（2026-04-30）— 基于动态不确定性感知可微 BA 的 RGB SLAM，无需类别先验即可鲁棒处理真实动态场景，ETH Zürich + 微软 · [CVPR 2026](https://arxiv.org/abs/2603.19076)
- **SLAM3R**（2026-05-14）— 端到端实时稠密重建，无需显式位姿估计，滑动窗口 + 全局配准网络，20+ FPS 达 SOTA，CVPR 2025 Highlight · [CVPR 2025 Highlight](https://arxiv.org/abs/2412.09401)
- **MASt3R-SLAM**（2026-05-20）— 首个以 MASt3R 三维重建先验为基础的实时单目稠密 SLAM，无需相机标定，15 FPS 实时性能，多基准 SOTA · [CVPR 2025](https://arxiv.org/abs/2412.12392)
- **WildGS-SLAM**（2026-05-29）— 首个基于 3DGS 的动态环境单目 SLAM，DINOv2 驱动不确定性预测去除动态干扰，室内外场景均超越 SOTA，斯坦福 × ETH Zürich · [CVPR 2025](https://arxiv.org/abs/2504.03886)
- **MAGiC-SLAM**（2026-06-08）— 首个多智能体 3DGS SLAM 系统，DINOv2 回环检测 + 子地图协同融合，24× 加速，TU Wien × ETH Zürich · [CVPR 2025](https://arxiv.org/abs/2411.16785)
- **SEGS-SLAM**（2026-06-16）— 结构增强 3DGS SLAM，结构化点云初始化高斯基元 + 运动外观嵌入消除渲染不一致，单目/双目/RGB-D 均达 SOTA，南开大学 · [ICCV 2025](https://arxiv.org/abs/2501.05242)
- **SDGS**（2026-07-02）— 基于稀疏边缘描述子的在线 3DGS 系统，"先勾轮廓再上色"两阶段范式，极端高速运动下唯一不崩溃的 GS-SLAM，ATE 仅 3.91cm · [CVPR 2026](https://openaccess.thecvf.com/content/CVPR2026/html/Tian_SDGS_Spatial_Difference_Guided_Gaussian_Splatting_for_Simultaneous_Localization_and_CVPR_2026_paper.html)
- **SplaTAM**（2026-07-13）— 首个将 3D Gaussian Splatting 引入 SLAM，轮廓掩码捕捉场景密度，位姿/地图/渲染均达 2× SOTA，CMU · [CVPR 2024](https://arxiv.org/abs/2312.02126)
- **Pi³MOS-SLAM**（2026-07-22）— 前馈重建模型作为通用三维先验过滤动态区域，几何BA + 前馈模型互补融合，CVPR 2026，波恩大学PRBonn实验室 · [CVPR 2026](https://arxiv.org/abs/2512.06868)

### 🎨 八、三维生成（3D Generation）

研究从文本、图像等条件生成高质量三维资产的方法，涵盖原生三维表示学习、扩散/流匹配生成模型、PBR 材质建模等核心技术。

- **TRELLIS.2**（2026-05-01）— 原生紧凑结构化隐空间 + 40亿参数流匹配模型，数秒内生成高分辨率 PBR 材质三维资产，微软研究院 · [CVPR 2026 Oral](https://arxiv.org/abs/2512.14692)
- **CraftsMan3D**（2026-05-22）— 原生三维扩散 + 法线增强几何细化两阶段生成，30 秒内生成工业级高保真网格，支持交互式编辑，CVPR 2025 满分 · [CVPR 2025](https://arxiv.org/abs/2405.14979)
- **TRELLIS**（2026-06-01）— 统一结构化隐空间（SLAT）+ 20亿参数整流流 Transformer，支持多格式输出与局部三维编辑，微软亚洲研究院 · [CVPR 2025 Highlight](https://arxiv.org/abs/2412.01506)
- **Prometheus**（2026-06-04）— 视图条件多平面表示将 LDM 扩展为三维感知生成器，秒级 Text-to-3D，告别 SDS 逐步优化伪影 · [CVPR 2025](https://arxiv.org/abs/2412.21117)
- **Turbo3D**（2026-06-09）— 双教师蒸馏 + Latent GS-LRM 全潜空间流水线，0.35 秒完成 Text-to-3D，CMU × Adobe × MIT · [CVPR 2025](https://arxiv.org/abs/2412.04470)
- **WorldGen**（2026-06-17）— 首个从文本生成可漫游交互式三维世界的端到端框架，导航网格约束 + 组合式拆解增强，输出直接兼容游戏引擎，Meta × Oxford · [CVPR 2026](https://arxiv.org/abs/2511.16825)
- **CAT3D**（2026-06-25）— 多视图扩散模型模拟真实捕捉流程，单张图像一分钟内创建完整三维场景 · [NeurIPS 2024](https://arxiv.org/abs/2405.10314)
- **Realiz3D**（2026-07-03）— 领域感知学习框架将"域身份"与"3D 控制信号"解耦，实现强 3D 一致性与显著更高的真实感，Meta AI × Technion · [CVPR 2026](https://arxiv.org/abs/2605.13852)
- **LGM**（2026-07-08）— 多视角高斯特征 + 非对称 U-Net，5 秒从文本/单图生成 512 分辨率高保真 3D 资产，ECCV 2024 Oral · [ECCV 2024 Oral](https://arxiv.org/abs/2402.05054)
- **DreamGaussian**（2026-07-16）— 首个将 3DGS 引入 3D 生成，逐步稠密化 + 网格提取精化，单图生成 3D 仅需 2 分钟，加速 10×，ICLR 2024 Oral · [ICLR 2024 Oral](https://arxiv.org/abs/2309.16653)

### 🪟 九、3DGS 透明表面建模（Transparent Surface Modeling）

研究如何在 3D Gaussian Splatting 框架中建模玻璃、水面等透明/半透明界面，通过辐射传输分解实现物理一致的反射与透射渲染。

- **GLINT**（2026-05-04）— 分解高斯辐射传输建模场景级透明表面，无需显式分割 mask 即可自动定位透明区域，NAVER LABS · [CVPR 2026 Oral](https://arxiv.org/abs/2603.26181)

### 🔍 十、多视图稠密匹配与三维重建（MVS / Dense Matching）

研究从多张图像建立稠密、一致的像素级对应关系，为 SfM 和三维重建提供高精度轨迹，突破成对匹配范式，追求全局几何一致性。

- **MV-RoMa**（2026-05-05）— 首个多视图稠密匹配模型，Track-Guided 多视图编码器 + 像素对齐精炼器，SfM 全面超越稀疏/稠密匹配基线 · [CVPR 2026](https://arxiv.org/abs/2603.27542)
- **MVSAnywhere**（2026-05-27）— 首个零样本通用 MVS 模型，成本体积块化 + 单/多目线索自适应融合，任意场景任意深度范围跨域 SOTA，Niantic Labs · [CVPR 2025](https://arxiv.org/abs/2503.22430)
- **MV-DUSt3R+**（2026-06-12）— 单阶段前馈多视图重建，跨参考视图注意力消除单参考依赖，2 秒完成无需标定，Meta Reality Labs × UIUC · [CVPR 2025 Oral](https://arxiv.org/abs/2412.06974)
- **Murre**（2026-06-22）— SfM 稀疏点云引导扩散模型单目深度估计，绕过传统多视图匹配，室内/街景/航拍多场景超越 SOTA MVS，浙江大学 · [CVPR 2025](https://arxiv.org/abs/2503.14483)
- **HAMSt3R**（2026-06-30）— 将 MASt3R 扩展为联合重建人体与场景的前馈网络，DUNE 蒸馏编码器融合场景几何与人体结构先验，人体中心基准 SOTA，NAVER LABS Europe · [ICCV 2025](https://arxiv.org/abs/2508.16433)
- **MonoMVSNet**（2026-07-07）— 单目基础模型先验引导的 MVS 网络，跨视图位置编码深度融合单目特征与多视图几何，Tanks-and-Temples 双基准第一 · [ICCV 2025](https://arxiv.org/abs/2507.11333)
- **DriveMVS**（2026-07-23）— LiDAR 提示的时空多视图立体网络，三线索融合器协同单目/度量/几何线索，时空解码器保障跨帧一致性，自动驾驶 MVS SOTA · [CVPR 2026](https://arxiv.org/abs/2603.03765)

### 🌐 十一、NeRF / 逆向渲染（NeRF / Inverse Rendering）

研究基于神经辐射场的场景表示与逆向渲染方法，联合估计场景几何、材质与光照，实现物理一致的新视角合成与重光照。

- **PBR-NeRF**（2026-05-11）— 基于物理渲染理论的 NeRF 逆向渲染，两个新颖物理先验约束材质估计，ETH Zürich · [CVPR 2025](https://arxiv.org/abs/2412.09680)
- **DiffusionRenderer**（2026-05-18）— 视频扩散模型驱动的神经逆向与正向渲染统一框架，G-buffer 估计 + 重光照，NVIDIA Research，CVPR 2025 Oral · [CVPR 2025 Oral](https://arxiv.org/abs/2501.18590)
- **Neural Inverse Rendering from Propagating Light**（2026-05-26）— 首个物理驱动的瞬态神经逆向渲染，时间分辨辐射缓存建模多次弹射间接光，CVPR 2025 最佳学生论文，多伦多大学 × CMU · [CVPR 2025 Best Student Paper](https://arxiv.org/abs/2506.05347)
- **LIRM**（2026-06-11）— 推理时逆向渲染学习，每场景 20 min 自标定从零恢复几何 + 材质 + HDR 光照，Meta Reality Labs · [CVPR 2025 Oral](https://arxiv.org/abs/2504.20026)
- **SVG-IR**（2026-06-19）— 空间变化高斯表示允许每高斯拥有变化材质与法线，物理间接光照模型，重光照 PSNR 超 NeRF 2.5 dB，南京大学 · [CVPR 2025](https://arxiv.org/abs/2504.06815)
- **NeRF Emitter**（2026-06-29）— NeRF 作为非远距离环境发射器建模空间变化光照，物理逆向渲染精准重建几何与材质，清华大学 × UC Irvine · [SIGGRAPH 2024](https://arxiv.org/abs/2402.04829)
- **GaussianShader**（2026-07-09）— 简化着色函数赋予 3D 高斯反射表面建模能力，最短轴法线估计 + 球谐着色，PSNR 超 3DGS 1.57 dB，优化快 Ref-NeRF 40 倍 · [CVPR 2024](https://arxiv.org/abs/2311.17977)

### 🏷️ 十二、3DGS 场景理解与语义编码（3DGS Scene Understanding）

研究将语义信息、开放词汇特征嵌入 3D Gaussian 表示，实现开放词汇分割、场景编辑等高层理解任务。

- **Chorus**（2026-06-10）— 首个多教师预训练 3DGS 场景编码器，SigLIP2+DINOv3+PE-Spatial 三教师蒸馏统一语义/实例/空间感知，ETH Zürich · [CVPR 2026 Oral](https://arxiv.org/abs/2512.17817)
- **SceneSplat**（2026-07-10）— 首个原生 3DGS 场景理解大规模预训练框架，视觉语言预训练 + 自监督学习，构建 SceneSplat-7K 数据集（7916 场景），ETH Zürich · [ICCV 2025 Oral](https://arxiv.org/abs/2503.18052)

#### ### 📐 十三、3DGS 表面重建（3DGS Surface Reconstruction）

研究如何从 3D Gaussian Splatting 表示中提取高质量、几何精确的表面与网格，通过折叠高斯、正则化约束等手段弥合辐射场渲染与几何重建之间的鸿沟。

- **2DGS**（2026-07-15）— 将 3D 高斯折叠为 2D 定向圆盘，深度畸变 + 法线一致性正则化，同时实现 SOTA 渲染与表面重建，SIGGRAPH 2024 · [SIGGRAPH 2024](https://arxiv.org/abs/2403.17888)
- **GSPrior**（2026-07-21）— 自约束 TSDF 先验引导高斯贴合表面，带宽渐进收缩实现高保真表面重建，CVPR 2026 · [CVPR 2026](https://arxiv.org/abs/2603.19682)

---

## 说明

本文档由 CatDesk 自动维护，收录每日三维重建方向顶会/顶刊论文推荐（来源：CVPR、ICCV、ECCV、SIGGRAPH、NeurIPS、TPAMI、IJCV 等）。

重点子方向：3D Gaussian Splatting、多视图立体重建（MVS）、SLAM / 实时三维重建。

---

## 论文列表

### 2026-04-13

**AnchorSplat: Feed-Forward 3D Gaussian Splatting with 3D Geometric Priors**
**基于三维几何先验的前馈式三维高斯泼溅**

![AnchorSplat 论文主图](https://km.sankuai.com/api/file/cdn/2756902383/231899831392?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Xiaoxue Zhang, Xiaoxu Zheng, Yixuan Yin, Tiao Zhao, Kaihua Tang, Michael Bi Mi, Zhan Xu, Dave Zhenyu Chen
- **链接**：https://arxiv.org/abs/2604.07053

**核心内容**：提出 AnchorSplat，一种前馈式 3DGS 框架，以三维几何先验（稀疏点云/体素/RGB-D 点云）为锚点，直接在 3D 空间中生成高斯基元，打破了传统像素对齐范式。引入 Gaussian Refiner 模块进行轻量级精细化，在 ScanNet++ v2 NVS 基准上达到 SOTA。

**亮点**：

1. 锚点对齐高斯表示，不依赖图像分辨率和视角数量，视角一致性显著提升
2. 大幅减少高斯基元数量，兼顾计算效率与重建保真度
3. Gaussian Refiner 仅需少量前向传播即可精细化，部署灵活

### 2026-04-14

**SparseSplat: Towards Applicable Feed-Forward 3D Gaussian Splatting with Pixel-Unaligned Prediction**
**面向实用的前馈式三维高斯泼溅：像素非对齐预测**

![SparseSplat 方法概览图](https://km.sankuai.com/api/file/cdn/2756902383/232104776489?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Zicheng Zhang, Xiangting Meng, Ke Wu, Wenchao Ding
- **链接**：https://arxiv.org/abs/2604.03069

**核心内容**：提出 SparseSplat，首个能根据场景结构和局部区域信息丰富度自适应调整高斯密度的前馈式 3DGS 模型。通过基于熵的概率采样策略，在纹理稀少区域生成大而稀疏的高斯基元，在信息丰富区域分配小而密集的高斯基元，生成高度紧凑的 3DGS 地图。同时设计了专用点云网络，高效编码局部上下文并解码为 3DGS 属性，解决了通用优化流程与前馈模型之间的感受野不匹配问题。实验表明，SparseSplat 仅用 22% 的高斯基元即可达到 SOTA 渲染质量，仅用 1.5% 的高斯基元仍能保持合理渲染质量。

**亮点**：

1. 首创基于熵的自适应高斯密度采样，打破像素对齐范式，仅用 22% 高斯基元即达 SOTA 渲染质量，极大降低存储与计算开销
2. 专用点云网络解决感受野不匹配问题，局部上下文编码更精准，属性回归更高效，适合 AR/VR 和机器人等下游任务
3. 极致压缩潜力突出：仅保留 1.5% 高斯基元仍可维持合理渲染质量，为实时三维重建在资源受限设备上的部署提供新思路

### 2026-04-15

**UniSplat: Learning 3D Representations for Spatial Intelligence from Unposed Multi-View Images**
**UniSplat：从无位姿多视图图像学习空间智能三维表示**

![UniSplat 论文 teaser 图](https://km.sankuai.com/api/file/cdn/2756902383/232347315434?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Bo Zhou, Qiuxia Lai, Zeren Sun, Xiangbo Shu, Yazhou Yao, Wenguan Wang
- **链接**：https://arxiv.org/abs/2604.10573

**核心内容**：提出 UniSplat，一种前馈式框架，旨在从无位姿（unposed）稀疏多视图图像中学习统一的三维表示，为空间智能（场景理解、具身 AI）提供感知基础。框架包含三大核心组件：① 双重掩码策略（dual-masking），同时对编码器和解码器 token 进行掩码，并将解码器掩码集中于几何丰富区域，迫使模型从不完整视觉线索中推断结构信息，从而在无位姿输入下也能获得几何感知表示；② 由粗到细的高斯泼溅策略（coarse-to-fine Gaussian splatting），通过逐步精细化辐射场来减少外观与语义之间的不一致；③ 位姿条件重校准机制（pose-conditioned recalibration），将预测的三维点云和语义图重投影到图像平面，与 RGB 和语义预测对齐，确保几何-语义跨任务一致性。

**亮点**：

1. 无位姿输入下的几何感知学习：双重掩码策略强制模型从不完整视觉线索中推断三维结构，无需相机位姿即可获得高质量几何感知表示，大幅降低数据采集门槛
2. 几何-语义跨任务一致性保障：位姿条件重校准机制通过重投影对齐，解决了多任务头之间的几何-语义不匹配问题，实现外观、几何、语义的统一三维表示
3. 空间智能基础模型潜力：UniSplat 生成的统一三维表示在稀疏视图、无位姿等挑战性条件下具有强泛化能力，可直接服务于场景理解和具身 AI 等下游任务

### 2026-04-16

**tttLRM: Test-Time Training for Long Context and Autoregressive 3D Reconstruction**
**tttLRM：面向长上下文自回归三维重建的测试时训练**

![tttLRM 论文框架图](https://km.sankuai.com/api/file/cdn/2756902383/232765023254?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Chen Wang, Hao Tan, Wang Yifan, Zhiqin Chen, Yuheng Liu, Kalyan Sunkavalli, Sai Bi, Lingjie Liu, Yiwei Hu（University of Pennsylvania / Adobe Research / UCI）
- **链接**：https://arxiv.org/abs/2602.20160

**核心内容**：提出 tttLRM，一种新型大规模三维重建模型，将测试时训练（Test-Time Training, TTT）层引入三维重建任务，实现具有线性计算复杂度的长上下文自回归三维重建。其核心思想是将多幅图像观测压缩到 TTT 层的"快速权重"（fast weights）中，形成隐空间中的隐式三维表示，可解码为高斯泼溅（Gaussian Splats）等显式格式用于下游应用。在线学习变体支持从流式观测中进行渐进式三维重建与精细化。实验表明，在新视角合成任务上预训练可有效迁移到显式三维建模，在前馈三维高斯重建上超越现有最优方法，同时兼顾物体级和场景级重建。

**亮点**：

1. TTT 层赋能长上下文重建：将多视图观测压缩为快速权重隐式表示，以线性复杂度支持任意数量视角输入，突破以往前馈重建模型视角数量受限的瓶颈
2. 在线渐进式重建能力：在线学习变体支持从流式观测中逐步积累和精细化三维场景，天然适配 SLAM 和机器人实时感知等在线应用场景
3. 跨任务预训练迁移：在新视角合成任务上预训练后有效迁移到显式三维重建（高斯泼溅），在物体级与场景级重建基准上均超越现有 SOTA，验证了预训练策略的通用性

### 2026-04-17

**IDESplat: Iterative Depth Probability Estimation for Generalizable 3D Gaussian Splatting**
**IDESplat：面向可泛化三维高斯泼溅的迭代深度概率估计**

![IDESplat 方法示意图](https://km.sankuai.com/api/file/cdn/2756902383/232810435812?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Wei Long, Haifeng Wu, Shiyin Jiang, Jinhua Zhang, Xinchun Ji, Shuhang Gu
- **链接**：https://arxiv.org/abs/2601.03824

**核心内容**：提出 IDESplat，一种可泛化前馈式 3DGS 框架，通过迭代深度概率估计来精准预测高斯球中心（Gaussian means）。现有方法通常仅用单次 warp 操作估计深度概率，难以充分利用跨视角几何线索，导致深度图不稳定且粗糙。IDESplat 引入深度概率增强单元（DPBU），通过级联 warp 操作生成极线注意力图并以乘法方式融合，消除单次 warp 的固有不稳定性；再通过堆叠多个 DPBU 构建迭代深度估计流程，逐步筛选高置信度深度候选，最终得到精确的深度图和高斯球中心。在 RealEstate10K、ACID 和 DL3DV 数据集上，IDESplat 以实时效率达到 SOTA 重建质量：在 RE10K 上以仅 10.7% 的参数量和 70% 的显存，PSNR 超越 DepthSplat 0.33 dB；在跨数据集 DTU 实验中 PSNR 提升 2.95 dB，展现出强泛化能力。

**亮点**：

1. 迭代深度概率增强（DPBU）：通过级联 warp 操作的极线注意力图乘法融合，彻底消除单次 warp 的不稳定性，逐步精炼深度候选，使高斯球中心预测更精准，在 RE10K 上仅用 10.7% 参数量即超越 DepthSplat
2. 极强跨数据集泛化能力：在 DTU 跨数据集实验中 PSNR 提升 2.95 dB，证明迭代深度估计策略能有效捕获跨视角几何一致性，泛化到未见场景
3. 轻量高效实时推理：以 70% 显存占用实现实时渲染效率，兼顾重建质量与计算资源，适合在资源受限设备上部署可泛化三维重建系统

### 2026-04-21

**C3G: Learning Compact 3D Representations with 2K Gaussians**
**C3G：基于 2K 高斯的紧凑三维表示学习**

![C3G 论文框架图](https://km.sankuai.com/api/file/cdn/2756902383/233511837691?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Honggyu An, Jaewoo Jung, Mungyeom Kim, Sunghwan Hong, Chaehyun Kim, Kazumi Fukuda, Minkyeong Jeon, Jisang Han, Takuya Narihira, Hyuna Ko, Junsu Kim, Yuki Mitsufuji, Seungryong Kim（KAIST / Sony AI）
- **链接**：https://arxiv.org/abs/2512.04021

**核心内容**：提出 C3G，一种新型前馈式三维重建框架，通过仅在关键空间位置估计约 2K 个紧凑高斯（3D Gaussians）来完成无位姿稀疏视图的三维场景重建与理解。其核心创新在于引入可学习 token，通过自注意力机制聚合多视图特征，指导高斯基元的空间分配，确保每个高斯基元都整合了跨视角的相关视觉特征；同时利用所学习的注意力模式高效完成特征上升（feature lifting）。相比以往按像素生成大量冗余高斯基元的方法，C3G 在显著降低显存开销的同时，提升了多视图特征聚合质量，在无位姿新视角合成、三维开放词汇分割和视角不变特征聚合等任务上均达到 SOTA。

**亮点**：

1. 极致紧凑的高斯表示：仅用 2K 个高斯基元完成场景重建，打破了以往前馈重建方法按像素密集分配高斯导致冗余爆炸的范式，在大幅降低内存开销的同时保持高质量重建效果
2. 可学习 token 驱动的特征聚合：通过自注意力机制让每个高斯 token 自适应地整合多视角特征，解决了稀疏视图下多视图特征聚合次优的问题，同时注意力模式可直接复用于 feature lifting，无需额外模块
3. 重建与理解统一框架：同一紧凑表示同时支持新视角合成（重建）和三维开放词汇分割（理解），在两类任务上均超越现有方法，验证了紧凑几何表示作为通用三维特征载体的潜力

### 2026-04-22

**Proxy-GS: Unified Occlusion Priors for Training and Inference in Structured 3D Gaussian Splatting**
**Proxy-GS：面向结构化三维高斯泼溅训练与推理的统一遮挡先验**

![Proxy-GS teaser](https://km.sankuai.com/api/file/cdn/2756902383/233640437357?contentType=0&isNewContent=false)

- **来源**：CVPR 2026 Oral（满分论文）
- **作者**：Yuanyuan Gao, Yuning Gong, Yifei Liu, Li Jingfeng, Dingwen Zhang, Yanci Zhang, Dan Xu, Xiao Sun, Zhihang Zhong（上海交通大学 / 上海人工智能实验室 / 西北工业大学 / 四川大学 / 香港科技大学）
- **链接**：https://arxiv.org/abs/2509.24421

**核心内容**：现有基于 MLP 的结构化 3DGS 方法（如 Scaffold-GS、Octree-GS）通过神经解码器动态生成高斯属性，提升了视角相关细节的建模能力，但在遮挡密集场景中仍存在大量冗余高斯基元，导致渲染效率低下。Proxy-GS 提出利用轻量级代理网格（proxy mesh）引入统一的遮挡先验，在推理阶段通过代理系统以不到 1ms 的速度生成 1000×1000 分辨率的精确遮挡深度图，用于剔除被遮挡的锚点和高斯基元以加速渲染；在训练阶段引导高斯增密沿代理表面生长，避免遮挡区域的无效增密，并通过偏移使高斯基元更好地贴合代理几何，从而提升渲染质量。在 MatrixCity Streets 等遮挡密集数据集上，Proxy-GS 相比 Octree-GS 实现了超过 2.5 倍的渲染加速，同时显著提升渲染质量。

**亮点**：

1. 统一遮挡先验框架：首次将代理网格引入结构化 3DGS 的训练与推理两个阶段，用同一套遮挡深度图同时指导推理时的高斯剔除（加速渲染）和训练时的增密策略（提升质量），实现了训练-推理一致的遮挡感知优化
2. 极速代理系统：核心代理系统可在 1ms 内生成 1000×1000 分辨率的精确遮挡深度图，计算开销极低，在遮挡密集的大规模城市场景（MatrixCity Streets）中实现超过 2.5 倍渲染加速，为 3DGS 在 AR/VR 等实时应用场景的落地提供了新方案
3. 即插即用的通用性：Proxy-GS 作为插件式模块可与多种 MLP-based 3DGS 渲染器（Scaffold-GS、Octree-GS 等）无缝集成，无需修改底层渲染架构，具有良好的通用性和可扩展性，且获得 CVPR 2026 满分 Oral 认可

### 2026-04-23

**NimbusGS: Unified 3D Scene Reconstruction under Hybrid Weather**
**恶劣混合天气下的统一三维场景重建**

![NimbusGS框架图](https://km.sankuai.com/api/file/cdn/2756902383/233857555703?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Yanying Li, Jinyang Li, Shengfeng He, Yangyang Xu, Junyu Dong, Yong Du（中国海洋大学 / 华南理工大学）
- **链接**：https://arxiv.org/abs/2603.27228

**核心内容**：NimbusGS 提出了一个统一框架，用于从多视图退化图像（雾、雨、雪及其混合天气）中重建高质量三维场景。现有方法通常针对单一天气类型设计，泛化能力有限。NimbusGS 将天气退化分解为两类：一是跨视图一致的连续介质（如大气散射、光线衰减），用全局传输场（global transmission field）建模；二是每帧独立的动态粒子（如雨滴、雪花），用逐视图粒子残差（per-view particulate residuals）建模。在此基础上，NimbusGS 还引入了几何引导的梯度缩放机制（geometry-guided gradient scaling），缓解严重能见度退化时三维高斯表示自监督优化过程中的梯度失衡问题，从而在多种天气条件下稳定学习准确几何。实验表明，NimbusGS 在多样且高难度天气场景下的几何重建质量均超越了各类天气专用方法。

**亮点**：

1. 双分量天气退化分解：首次将复杂的混合天气退化系统地分解为全局传输场（静态大气效应，跨视图一致）和逐视图粒子残差（动态瞬态扰动，每帧独立）两部分，物理建模清晰，可同时处理雾、雨、雪及任意组合天气，突破了现有单一天气专用方法的局限
2. 几何引导梯度缩放：针对强退化（低能见度）场景下三维高斯自监督优化中梯度失衡导致几何学习不稳定的痛点，提出几何引导的梯度缩放机制，有效稳定训练过程并显著提升几何重建精度，使 NimbusGS 在所有天气类型上均超越任务专用方法
3. 统一框架泛化能力强：NimbusGS 无需为每种天气单独训练或调参，单一模型即可处理多种及混合天气输入，在实际部署中更具实用价值，为自动驾驶、机器人导航等恶劣天气下的三维感知重建提供了全新解决方案

### 2026-04-24

**VAD-GS: Visibility-Aware Densification for 3D Gaussian Splatting in Dynamic Urban Scenes**
**动态城市场景中3D高斯泼溅的可见性感知致密化**

![VAD-GS：动态城市场景的可见性感知高斯致密化框架](https://km.sankuai.com/api/file/cdn/2756902383/234074110437?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Yikang Zhang, Rui Fan（同济大学）
- **链接**：https://arxiv.org/abs/2510.09364

**核心内容**：VAD-GS 针对动态、无界城市场景中 3D 高斯泼溅（3DGS）几何重建质量不足的问题，提出了一种可见性感知的致密化框架。在自动驾驶等城市场景中，相机视锥覆盖往往不均匀，导致初始点云存在大量空洞，标准的 3DGS 克隆/分裂致密化策略无法在无初始点的区域生成新高斯基元，从而引发畸变和伪影。VAD-GS 通过基于体素的可见性推理识别不可靠几何结构，利用多样性感知视图选择挑选最具信息量的支撑视图，再以块匹配多视图立体（patch matching MVS）重建缺失结构，为无初始点区域生成基于可靠几何先验的新高斯基元。在 Waymo 和 nuScenes 数据集上的实验表明，VAD-GS 在渲染质量和几何重建精度上均超越当前最优 3DGS 方法。

**亮点**：

1. 可见性感知的几何修复：首次将基于体素的可见性分析引入 3DGS 致密化流程，精准定位因视锥不重叠而缺失的几何区域，并通过多视图立体重建（patch matching MVS）主动填补空洞，彻底突破传统克隆/分裂策略仅能在已有点附近扩展的局限，实现对城市场景中任意缺失结构的主动修复
2. 多样性感知视图选择：设计了专门的多样性感知视图选择策略，为每个缺失区域自动筛选覆盖最全面、信息最丰富的支撑视图组合，有效保证后续 MVS 重建的精度，避免视图冗余导致的重建退化
3. 动态与静态对象几何双提升：VAD-GS 在 Waymo 和 nuScenes 上全面优于现有 3DGS 方法，不仅静态背景几何更完整准确，动态前景对象（如车辆、行人）的深度图和法线图质量也显著提升，对自动驾驶感知系统具有重要实用价值

### 2026-04-27

**VGGT: Visual Geometry Grounded Transformer**
**视觉几何基础 Transformer**

![VGGT：视觉几何基础Transformer架构示意图](https://km.sankuai.com/api/file/cdn/2756902383/234376404253?contentType=0&isNewContent=false)

- **来源**：CVPR 2025 Best Paper Award（最佳论文）
- **作者**：Jianyuan Wang, Minghao Chen, Nikita Karaev, Andrea Vedaldi, Christian Rupprecht, David Novotny（牛津大学 & Meta AI）
- **链接**：https://arxiv.org/abs/2503.11651

**核心内容**：VGGT 是一个纯前馈神经网络，能够直接从一张、几张乃至数百张输入视图中推理出场景的所有关键三维属性，包括相机参数、点图（point maps）、深度图以及三维点轨迹（3D point tracks）。传统三维重建方法依赖捆绑调整（Bundle Adjustment）等迭代优化手段，而 VGGT 完全摒弃了几何后处理步骤，实现了真正意义上的端到端三维几何推理。单张图像重建仅需不到 1 秒，却在相机参数估计、多视图深度估计、稠密点云重建和三维点跟踪等多个任务上超越了需要几何优化的竞争方法。此外，预训练的 VGGT 作为特征骨干网络，还能显著提升非刚性点跟踪和前馈式新视角合成等下游任务的性能，展示了其作为通用三维视觉基础模型的巨大潜力。

**亮点**：

1. 端到端统一三维推理：VGGT 首次以单一前馈网络统一处理相机估计、深度预测、点云重建和三维点跟踪四大核心任务，彻底消除了对 Bundle Adjustment 等迭代几何优化的依赖，推理速度极快（<1秒/帧），同时在所有任务上均达到或超越 SOTA，打破了"专用模型才能取得最优性能"的传统认知
2. 视图数量无关的泛化能力：模型设计上对输入视图数量无约束，从单视图到数百视图均可直接处理，且单视图重建性能出色（尽管训练时并未专门针对单视图场景优化），体现了 Transformer 架构在多视图几何理解上的强大泛化能力
3. 强大的下游迁移能力：预训练 VGGT 作为特征骨干可显著提升非刚性点跟踪（non-rigid point tracking）和前馈式新视角合成（feed-forward novel view synthesis）等下游任务，证明其学到的几何表征具有高度通用性，是迈向"通用三维视觉基础模型"的重要里程碑，荣获 CVPR 2025 最佳论文奖

### 2026-04-28

**RetimeGS: Continuous-Time Reconstruction of 4D Gaussian Splatting**
**RetimeGS：4D 高斯泼溅的连续时间重建**

![RetimeGS：4D高斯泼溅连续时间重建框架示意图](https://km.sankuai.com/api/file/cdn/2756902383/234625856776?contentType=0&isNewContent=false)

- **来源**：CVPR 2026 Oral
- **作者**：Xuezhen Wang, Li Ma, Yulin Shen, Zeyu Wang, Pedro V. Sander（香港科技大学广州）
- **链接**：https://arxiv.org/abs/2603.13783

**核心内容**：时间重定时（temporal retiming）——即在任意时间戳重建和渲染动态场景——对慢动作回放、时间编辑和后期制作等应用至关重要。然而，现有 4D 高斯泼溅（4DGS）方法在离散帧索引处过拟合，难以表示连续时间帧，在时间戳插值时产生鬼影伪影。RetimeGS 将这一局限性定义为"时间混叠"（temporal aliasing），并提出了一种简洁有效的 4DGS 表示，显式定义三维高斯的时间行为以缓解时间混叠。为实现平滑一致的插值，RetimeGS 引入了光流引导的初始化与监督（optical flow-guided initialization and supervision）、三重渲染监督（triple-rendering supervision）以及其他针对性策略。这些组件共同作用，即使在大运动场景下也能实现无鬼影、时间连贯的渲染。在包含快速运动、非刚性形变和严重遮挡的数据集上，RetimeGS 在质量和连贯性方面均超越了当前最优方法。

**亮点**：

1. 时间混叠问题的首次系统性解决：RetimeGS 首次将 4DGS 在时间插值时产生鬼影的根本原因定义为"时间混叠"，并通过显式建模高斯基元的时间行为（而非仅在离散帧索引处优化）从根本上解决这一问题，为连续时间动态场景重建提供了全新理论框架
2. 光流引导 + 三重渲染监督的协同设计：光流引导初始化为高斯基元提供了准确的运动先验，三重渲染监督（在当前帧、前后插值帧三处同时施加渲染约束）强制模型学习时间连续的运动轨迹，两者协同作用使 RetimeGS 在大运动、非刚性形变和严重遮挡等极端场景下仍能保持无鬼影的高质量渲染
3. 广泛的应用价值与 CVPR 2026 Oral 认可：RetimeGS 直接赋能慢动作视频生成、时间编辑和影视后期制作等高价值应用场景，在 PSNR、SSIM、LPIPS 等指标上全面超越现有 4DGS SOTA 方法，获得 CVPR 2026 Oral 认可，是 4D 动态场景重建领域的重要里程碑

### 2026-04-29

**Uni3R: Unified 3D Reconstruction and Semantic Understanding via Generalizable Gaussian Splatting from Unposed Multi-View Images**
**Uni3R：从无位姿多视图图像统一三维重建与语义理解**

![Uni3R teaser图：从无位姿多视图图像统一重建3D场景](https://km.sankuai.com/api/file/cdn/2756902383/234831782389?contentType=0&isNewContent=false)

- **来源**：CVPR 2026 Highlight
- **作者**：Xiangyu Sun, Haoran Jiang, Liyi Liu, Seokhun Nam, Gyeongrok Kang, Xin Wang, Wenbo Sui, Zhizhong Su, Wenyu Liu, Xinggang Wang（地平线机器人 & 华中科技大学）
- **链接**：https://arxiv.org/abs/2508.03643

**核心内容**：Uni3R 提出了一个新颖的前馈框架，能够直接从无位姿（unposed）的多视图图像中联合重建统一的三维场景表示，并同时赋予其开放词汇语义理解能力。方法的核心是跨视图 Transformer（Cross-View Transformer），它能够鲁棒地整合来自任意数量多视图输入的信息，然后回归一组携带语义特征场的三维高斯基元（3D Gaussian primitives with semantic feature fields）。这种统一表示在单次前馈传递中同时支持三大任务：高保真新视角合成、开放词汇三维语义分割和深度预测。在 RE10K 数据集上达到 25.07 PSNR，在 ScanNet 上达到 55.84 mIoU，在多个基准上建立了新的 SOTA。整个场景重建仅需约 0.15 秒，展示了前馈式统一三维场景重建与理解的全新范式。

**亮点**：

1. 重建与语义理解的首次统一：Uni3R 首次在单一前馈框架内同时完成三维重建（新视角合成 + 深度预测）和开放词汇语义分割三大任务，无需任何位姿先验，彻底打破了"重建"与"理解"两个任务需要分别建模的传统范式，为具身智能、机器人导航等下游应用提供了一站式三维感知基础
2. 跨视图 Transformer 实现无位姿泛化：通过跨视图注意力机制鲁棒整合任意数量无位姿多视图输入，无需相机标定或 SfM 预处理，直接回归带语义特征场的三维高斯基元，在 RE10K（PSNR 25.07）和 ScanNet（mIoU 55.84）等多个基准上全面超越现有方法，0.15 秒完成整个场景重建
3. 开放词汇语义场的创新设计：将语义特征场直接嵌入三维高斯基元，支持任意文本查询的开放词汇三维语义分割，无需针对特定类别重新训练，极大提升了模型的通用性和实用价值，获得 CVPR 2026 Highlight 认可，是 3DGS 走向"感知-重建一体化"的重要里程碑

### 2026-07-16｜Immediate 3D Gaussian Splat Reconstruction of Unordered Input with Global Consistency（即时三维高斯泼溅重建：无序输入的全局一致性方法）

**Immediate 3D Gaussian Splat Reconstruction of Unordered Input with Global Consistency**
**即时三维高斯泼溅重建：无序输入的全局一致性方法**

**方向**：SLAM / 实时三维重建　**来源**：SIGGRAPH Conference Papers 2026　**机构**：INRIA（法国国家信息与自动化研究所）

- **作者**：Andreas Meuleman, Linus Franke, Boris Zhestiankin, Camille Montemagni, George Drettakis
- **链接**：[https://arxiv.org/abs/2607.14481](https://arxiv.org/abs/2607.14481) | ACM DL：[10.1145/3799902.3811167](https://doi.org/10.1145/3799902.3811167)

![Immediate GS Reconstruction teaser](https://km.sankuai.com/api/file/cdn/2756902383/246877687534?contentType=0&isNewContent=false)

**核心内容**：3D Gaussian Splatting（3DGS）已成为场景捕捉和实时渲染的首选方法。然而，为了获得良好的视觉质量，通常需要将连续图像序列与无序拍摄相结合以获得更好的场景覆盖。传统的运动恢复结构（SfM）方法虽然可以重建这些捕捉，但只有在所有图像都可用后才能进行，且计算成本很高。增量重建方法（通常源自SLAM解决方案）能够提供即时反馈，但无法处理无序捕捉场景。本文提供了第一个用于此类辐射场捕捉的即时反馈解决方案，能够在提供全局一致性保证的同时实现即时重建。该方法的核心创新包括：首先，通过重新利用视觉地点识别模型和共视图，实现了无序序列的快速匹配，并提供了一种高效方法来寻找高度连接的关键帧，即使对有序序列也能提升质量；其次，结合GPU优化和精心的高斯基元放置策略，实现了快速局部重建；然后，引入了一种新颖的簇基方法，再次利用共视图进行高效回环检测，无需顺序输入；最后，为了处理大规模场景，引入了渐进层次结构，使方法能够在不牺牲效率的情况下扩展到大型环境。实验结果表明，该方法在包含数千张输入图像的多个数据集上实现了具有良好视觉质量的即时反馈3DGS重建。

**亮点**：

1. **首个针对辐射场捕捉的即时反馈全局一致性方案**：传统 3DGS 重建依赖离线 SfM 预先计算相机位姿，引入显著的"感知-重建"延迟，且需要等待所有图像拍摄完成。本工作首次实现了无序输入的即时反馈 3DGS 重建，通过视觉地点识别模型和共视图实现快速无序序列匹配，结合簇基回环检测提供全局一致性，使重建过程无需等待全部图像即可开始，且能保持全局几何一致性
2. **簇基回环检测与渐进层次结构处理大规模场景**：提出了新颖的簇基方法，利用共视图进行高效回环检测，无需顺序输入即可实现全局一致性优化。同时引入渐进层次结构，使方法能够扩展到包含数千张输入图像的大规模场景，在保持高效计算的同时确保重建质量
3. **GPU 优化与精心的高斯基元放置策略**：通过精细的 GPU 优化和精心的高斯基元放置策略，实现了快速局部重建。这种"先局部重建后全局优化"的两阶段设计思路，为实时三维重建在大规模场景中的应用提供了实用的解决方案，对实际场景捕捉具有重要的实用价值

### 2026-04-30

**DROID-SLAM in the Wild**
**野外动态场景下的 DROID-SLAM**

![DROID-W teaser: 给定任意动态视频，DROID-W能估计准确相机轨迹、动态点云和不确定性](https://km.sankuai.com/api/file/cdn/2756902383/235015610975?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Moyang Li, Zihan Zhu, Marc Pollefeys, Daniel Barath（苏黎世联邦理工学院 ETH Zürich & 微软）
- **链接**：https://arxiv.org/abs/2603.19076

**核心内容**：DROID-W 提出了一套面向真实野外动态场景的鲁棒实时 RGB SLAM 系统。传统 SLAM 方法普遍依赖静态场景假设，在行人、车辆、反光等动态因素存在时会发生严重的跟踪漂移。现有动态 SLAM 方案或依赖预定义动态类别先验（语义分割 mask），或依赖高质量静态场景建图（如 WildGS-SLAM），两者在真实开放场景中均受到严重限制。DROID-W 的核心创新是将动态不确定性（dynamic uncertainty）显式建模为逐像素连续值，通过多视角 DINO 特征一致性来检测视觉不一致区域，并将其无缝嵌入可微 Bundle Adjustment（BA）优化框架：不确定性高的区域残差被连续软抑制（soft suppression），而非硬性 mask 丢弃，从而保留场景中局部可靠信息。系统采用位姿/深度优化与不确定性估计的交替迭代策略，兼顾计算效率与优化质量，在 RTX 5090 上可达约 30 FPS 实时性能。作者还提出了 DROID-W 数据集（7 段室外高动态序列 + RTK 真值轨迹），在该数据集上平均轨迹误差仅 23cm，而原始 DROID-SLAM 误差高达 1.46m，提升显著。

**亮点**：

1. 无类别先验的动态感知：DROID-W 彻底摆脱对语义分割等预定义动态类别先验的依赖，利用 DINO 特征的跨视角一致性自动发现任意未知动态干扰，采用连续逐像素不确定性表达替代二值化 mask，支持"软抑制"策略，在局部运动、非刚体变形、强反光等复杂场景中展现出更强鲁棒性，真正实现面向真实世界"随手拍"视频的通用动态 SLAM
2. 不确定性与可微 BA 深度融合：将动态不确定性直接嵌入 DROID-SLAM 可微 Bundle Adjustment 核心优化框架，通过交替迭代优化位姿/深度与不确定性估计，避免大规模联合 Gauss-Newton 优化的高计算成本，保持实时性能（约 30 FPS @ RTX 5090），该不确定性感知模块具备即插即用特性，可推广到多种现有 SLAM 框架提升动态环境性能
3. 高难度真实场景基准贡献：提出 DROID-W 数据集，包含 7 段室外城市高动态场景序列，涵盖过曝、镜面反射、太阳光晕等极端拍摄条件，配备 RTK 支持的厘米级精度真值轨迹，并在 YouTube 真实动态视频上验证通用性，为动态 SLAM 领域提供了更贴近真实部署环境的严格评测基准

### 2026-05-01

**TRELLIS.2: Native and Compact Structured Latents for 3D Generation**
**原生紧凑结构化隐空间三维生成（TRELLIS.2）**

![TRELLIS.2 方法概览图：O-Voxel 表示、SC-VAE 压缩与流匹配生成模型完整流程](https://km.sankuai.com/api/file/cdn/2756902383/235129017695?contentType=0&isNewContent=false)

- **来源**：CVPR 2026 Oral
- **作者**：Jianfeng Xiang, Xiaoxue Chen, Sicheng Xu, Ruicheng Wang, Zelong Lv, Yu Deng, Hongyuan Zhu, Yue Dong, Hao Zhao, Nicholas Jing Yuan, Jiaolong Yang（清华大学 & 微软研究院 & 中国科学技术大学）
- **链接**：https://arxiv.org/abs/2512.14692 | 项目页：https://microsoft.github.io/TRELLIS.2/

**核心内容**：TRELLIS.2 是微软研究院提出的新一代三维生成框架，针对现有方法在复杂拓扑结构和材质细节建模上的根本局限，提出了一套从原生三维数据出发的结构化隐空间学习方案。其核心创新是 O-Voxel（Omni-Voxel，全能体素）——一种新型稀疏体素结构，通过灵活的对偶网格（Flexible Dual Grids）同时编码几何与外观信息，能够鲁棒处理任意拓扑（开放曲面、非流形几何、封闭内部结构），并支持完整的 PBR 材质属性（基础色、金属度、粗糙度、透明度）。基于 O-Voxel，作者设计了稀疏压缩变分自编码器（SC-VAE），实现 16 倍空间下采样，将 1024³ 分辨率的全纹理资产压缩至约 9.6K 隐变量而无明显质量损失。在此紧凑隐空间上，作者训练了 40 亿参数的流匹配（Flow Matching）生成模型，可在 3 秒（512³）至 60 秒（1536³）内高效生成高分辨率 PBR 材质三维资产，质量远超现有方法。O-Voxel 还支持无需优化或渲染的即时双向转换（网格→O-Voxel < 10 秒 CPU，O-Voxel→网格 < 100ms CUDA），极大简化了训练与推理的数据处理流程。

**亮点**：

1. 原生三维表示突破拓扑瓶颈：O-Voxel 彻底摆脱等值面（iso-surface）场的拓扑约束，通过稀疏体素 + 灵活对偶网格统一编码几何与 PBR 材质，支持开放曲面（如薄片、布料）、非流形几何（如相交网格）和封闭内部结构（如空心物体），是首个在单一表示中同时解决任意拓扑与丰富材质建模的三维生成框架，为高保真三维资产生成奠定了坚实的表示基础
2. 极致压缩与高效生成的完美平衡：SC-VAE 实现 16 倍空间下采样，将百万级体素压缩至约 9.6K 隐变量，压缩率远超现有三维 VAE 方案，同时保持可忽略的感知质量损失；在此超紧凑隐空间上训练的 40 亿参数流匹配模型，推理效率极高（512³ 仅需 3 秒），在重建保真度与隐变量紧凑性的权衡曲线上全面超越 TRELLIS、CraftsMan、Hunyuan3D 等现有 SOTA 方法
3. 即插即用的极简数据处理流程：O-Voxel 支持与标准纹理网格的即时双向无损转换（CPU 单核 < 10 秒完成网格→O-Voxel，CUDA 加速 < 100ms 完成 O-Voxel→网格），无需任何优化迭代或可微渲染，彻底消除了三维生成训练与推理中的数据处理瓶颈，使大规模三维资产数据集的高效利用成为可能，为三维生成领域的工程化落地提供了重要参考

### 2026-05-04

**GLINT: Modeling Scene-Scale Transparency via Gaussian Radiance Transport**
**通过高斯辐射传输建模场景级透明表面（GLINT）**

![GLINT 框架概览：通过分解高斯辐射传输建模场景级透明表面](https://km.sankuai.com/api/file/cdn/2756902383/235208604935?contentType=0&isNewContent=false)

- **来源**：CVPR 2026 Oral
- **作者**：Youngju Na, Jaeseong Yun, Soohyun Ryu, Hyunsu Kim, Sung-Eui Yoon, Suyong Yeon（KAIST & NAVER LABS）
- **链接**：https://arxiv.org/abs/2603.26181 | 项目页：https://youngju-na.github.io/GLINT/ | 代码：https://github.com/youngju-na/GLINT

**核心内容**：GLINT 是首个在 3D Gaussian Splatting 框架下系统解决场景级透明表面建模问题的方法，获 CVPR 2026 Oral。现有 3DGS 方法在遇到玻璃幕墙、展示柜等透明界面时会发生严重的几何错误和渲染伪影，根本原因在于透明界面的出射辐射是反射分量与透射分量的混合叠加，传统单一高斯表示无法将二者解耦。GLINT 提出了分解高斯辐射传输（Decomposed Gaussian Radiance Transport）框架：将场景中的透明界面显式建模为独立的界面高斯层，并将出射辐射分解为界面自身辐射、反射辐射和透射辐射三个物理分量，通过混合渲染管线（光栅化处理界面层 + 光线追踪处理反射/透射路径）实现物理一致的辐射传输。在优化阶段，GLINT 利用几何分离线索（geometry separation cues）自举透明区域定位，结合预训练视频重光照模型提供的几何与材质先验，无需任何显式分割 mask 监督即可自动发现并精确建模透明区域。在合成与真实透明场景数据集上，GLINT 在重建质量指标（PSNR/SSIM/LPIPS）上全面超越 PGSR、EnvGS、TSGS 等现有方法。

**亮点**：

1. 物理驱动的辐射传输分解：GLINT 将透明界面的出射辐射显式分解为界面辐射、反射辐射和透射辐射三个物理分量，通过混合渲染管线（光栅化 + 光线追踪）实现物理一致的高斯辐射传输，从根本上解决了 3DGS 在透明表面上几何错误与渲染伪影并存的核心难题，是 3DGS 框架向物理真实渲染迈进的重要一步
2. 无监督透明区域自举定位：GLINT 利用分解表示中自然涌现的几何分离线索（geometry separation cues），结合预训练视频重光照模型的几何与材质先验，在无需任何显式透明区域分割 mask 的情况下自动完成透明界面定位与解耦，彻底摆脱了对昂贵标注数据的依赖，大幅降低了透明场景重建的数据准备门槛
3. 场景级透明建模能力：GLINT 支持玻璃幕墙、展示柜、落地窗等大尺度场景级透明结构的高质量重建，而非仅限于单个孤立透明物体，在合成与真实数据集上均达到 SOTA 性能，为室内场景重建、AR/VR 内容制作、自动驾驶感知等需要精确处理透明界面的下游应用提供了坚实的技术基础

### 2026-05-05

**MV-RoMa: From Pairwise Matching into Multi-View Track Reconstruction**
**从成对匹配到多视图轨迹重建（MV-RoMa）**

![MV-RoMa Teaser](https://km.sankuai.com/api/file/cdn/2756902383/235238178742?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：JongMin Lee, Seungyeop Kang, Sungjoo Yoo（首尔大学）
- **链接**：https://arxiv.org/abs/2603.27542 | 项目页：https://icetea-cv.github.io/mv-roma/

**核心内容**：MV-RoMa 是首个多视图稠密匹配模型，解决了现有方法在成对匹配范式下链式传播时产生碎片化、几何不一致轨迹的核心问题。传统稠密匹配（如 RoMa、DKM）对图像对独立运行，多视图拼接时无法保证跨视图几何一致性，导致 SfM 下游任务性能下降。MV-RoMa 提出从源图像到多个共视目标图同时联合估计稠密对应关系的新范式：（1）多视图编码器以成对匹配结果为几何先验，通过高效的多视图特征交互（避免全注意力的高计算开销）建立全局一致的特征表示；（2）像素对齐多视图精炼器利用像素级注意力精细化对应关系，产生高度一致的跨视图匹配轨迹；（3）后处理策略将模型输出的多视图一致对应关系作为高质量轨迹直接馈入 SfM 管线。在 HPatches、ETH3D、IMC Photo Tourism 等多个挑战性基准上，MV-RoMa 产生比现有稀疏和稠密匹配方法更可靠的对应关系，三维重建精度和稠密度均大幅提升。

**亮点**：

1. 首个多视图稠密匹配范式：MV-RoMa 打破了"成对匹配后拼接"的传统范式，首次实现了从一张源图像到多个共视目标图的联合稠密对应估计，通过多视图编码器引入成对匹配几何先验，在不依赖全交叉注意力的情况下高效建模多视图特征交互，从根本上消除了逐对处理带来的几何不一致性问题，使匹配轨迹在全局视图中保持物理一致
2. 端到端高质量 SfM 轨迹生成：MV-RoMa 的后处理策略将多视图一致对应关系直接作为高质量轨迹注入 SfM 管线，无需额外的轨迹筛选或几何校验步骤，在 ETH3D、IMC Photo Tourism 等标准三维重建基准上，三维重建的轨迹稠密度和精度均大幅超越现有最优的稀疏（SuperGlue、LightGlue）和稠密（RoMa、DKM）匹配方法
3. 高效多视图架构设计：针对多视图场景下全注意力机制的计算代价随视图数呈二次方增长的瓶颈，MV-RoMa 设计了层次化的多视图编码-精炼架构：编码阶段利用成对匹配结果作为轻量级几何先验代替全交叉注意力；精炼阶段仅在像素级局部窗口内运行注意力计算，使整体计算复杂度接近线性，在保证多视图一致性的同时具备良好的可扩展性，为大规模 SfM 场景的实用化部署奠定基础

### 2026-05-06

**Stochastic Ray Tracing for the Reconstruction of 3D Gaussian Splatting**
**用于三维高斯泼溅重建的随机光线追踪**

![Stochastic Ray Tracing for 3DGS — Teaser](https://km.sankuai.com/api/file/cdn/2756902383/235293216164?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Peiyu Xu, Xin Sun, Krishna Mullia, Raymond Fei, Iliyan Georgiev, Shuang Zhao（UC Irvine & Adobe Research & NVIDIA）
- **链接**：https://arxiv.org/abs/2603.23637 | 项目页：https://xupaya.github.io/stoch3DGS/

**核心内容**：现有基于光线追踪的 3DGS 方法（如 3DGRT）虽然克服了光栅化的针孔相机局限，能够自然支持阴影、反射和折射，但由于需要对每条光线沿途所有相交高斯进行排序，计算开销远高于光栅化方法。此外，现有可重光照（relightable）的光线追踪 3DGS 方法仍依赖阴影贴图（shadow mapping）等光栅化近似，削弱了光线追踪的通用性优势。本文提出首个面向标准与可重光照 3DGS 的无排序可微随机光线追踪框架。核心贡献是基于无偏蒙特卡洛估计器的像素颜色梯度计算——每条光线仅对随机采样的少量高斯子集求值，完全规避排序需求。对于标准 3DGS 重建，该方法在重建质量和速度上与基于光栅化的 3DGS 持平，同时大幅超越基于排序的光线追踪方法。对于可重光照 3DGS，同一随机估计器驱动逐高斯着色与全光线追踪阴影光线计算，重建保真度显著超越现有方法，实现了真正意义上的物理一致光线追踪 3DGS 重建与渲染统一框架。

**亮点**：

1. 首个无排序可微随机光线追踪框架：通过无偏蒙特卡洛估计器对像素颜色梯度进行随机近似，每条光线仅评估少量随机子集高斯，彻底绕过 3D Gaussian 光线追踪中成本最高的全局排序操作，同时保持梯度估计的无偏性，在标准场景重建上实现与光栅化 3DGS 相当的质量与速度，大幅超越现有排序式光线追踪方案
2. 重建与渲染的统一物理一致框架：对于可重光照场景，同一随机估计器同时驱动逐高斯 PBR 着色与全光线追踪阴影光线（shadow rays），完全抛弃了现有方法依赖的阴影贴图近似，首次在 3DGS 框架内实现了重建阶段与渲染阶段的全光线追踪统一，在光照变换下的重建保真度显著优于依赖近似方法的现有可重光照 3DGS 方案
3. 支持非针孔相机与复杂光学效应：光线追踪框架天然支持鱼眼、全景等非针孔相机模型及反射、折射等复杂光学传输效应，而不受光栅化的视锥体与 alpha 合成约束，为自动驾驶、医疗成像等依赖特种相机的场景重建提供了更通用的 3DGS 方案，打破了传统 3DGS 对标准透视投影的强依赖

### 2026-05-07

**MoRE: 3D Visual Geometry Reconstruction Meets Mixture-of-Experts**
**MoRE：三维视觉几何重建遇见混合专家模型**

![MoRE — Teaser](https://km.sankuai.com/api/file/cdn/2756902383/235479786787?contentType=0&isNewContent=false)

- **来源**：CVPR 2026
- **作者**：Jingnan Gao, Zhe Wang, Xianze Fang, Xingyu Ren, Zhuo Chen, Shengqi Liu, Yuhao Cheng, Jiangjing Lyu, Xiaokang Yang, Yichao Yan（上海交通大学 & 阿里巴巴集团）
- **链接**：https://arxiv.org/abs/2510.27234 | 项目页：https://g-1nonly.github.io/MoRE_Website/ | 代码：https://github.com/alibaba/Taobao3D

**核心内容**：语言和视觉领域的研究已证明，扩大模型容量能持续提升多样化任务的性能。在三维视觉几何重建领域，大规模训练同样被证明有助于学习通用表示。然而，由于几何监督的复杂性和三维数据的多样性，三维模型的进一步扩展面临挑战。为此，本文提出 MoRE——一种基于混合专家（MoE）架构的稠密三维视觉基础模型。MoRE 将特征动态路由至任务专属专家，使各专家专注于互补的数据特征，从而同时提升模型的可扩展性与适应性。为增强真实场景下的鲁棒性，MoRE 引入了基于置信度的深度精炼模块，稳定并优化几何估计结果。此外，模型将稠密语义特征与全局对齐的三维骨干表示相融合，实现高保真表面法线预测。MoRE 还针对多任务几何学习设计了定制化损失函数，确保鲁棒学习。大量实验表明，MoRE 在多个基准测试上达到最先进性能，并在无需额外计算的情况下支持有效的下游应用。

**亮点**：

1. 首个将混合专家（MoE）架构引入三维视觉几何基础模型：MoRE 通过动态路由机制将特征分配给任务专属专家（深度估计、表面法线预测、点图估计等），使各专家专注于互补的数据特征，突破了单一密集网络在多任务几何学习中的容量瓶颈，在保持推理效率的同时实现了模型容量的高效扩展，为三维几何基础模型的 Scaling Law 探索提供了新路径
2. 置信度引导的深度精炼模块：针对真实场景中深度估计不稳定的问题，MoRE 设计了基于置信度的深度精炼模块，通过预测每个像素的置信度权重来动态调整深度估计，有效过滤低置信度区域的噪声预测，在保留高置信度区域精度的同时提升了整体几何估计的鲁棒性，尤其在纹理缺失、遮挡边界等困难区域表现突出
3. 语义与几何的深度融合：MoRE 将稠密语义特征与全局对齐的三维骨干表示相结合，用于高保真表面法线预测，实现了语义理解与几何重建的协同增强；配合针对多任务几何学习设计的定制化损失函数，模型在深度估计、表面法线预测、多视图三维重建等多个基准上均达到最先进水平，且无需针对下游任务进行额外计算开销

### 2026-05-08

**Layered 4D-Rotor Gaussian Splatting: A Compressed Representation for Long Dynamic Scenes**
**分层四维旋转体高斯泼溅：长时动态场景的压缩表示**

- **来源**：CVPR 2026
- **作者**：Hanjie Xu*, Yuanxing Duan*, Qiyu Dai*, Ge Li†, Baoquan Chen†, He Wang†（北京大学前沿计算研究中心）
- **链接**：https://cvpr.thecvf.com/virtual/2026/poster/36256 | 项目页：https://m1sak1-mei.github.io/layered-4d-rotor/

**核心内容**：当前的 4D Gaussian Splatting 方法（包括基于变形场的和基于 4D 基元的方法）虽然在短时动态场景中取得了令人印象深刻的视觉质量，但在面对长时动态场景（>10秒）时存在三大核心瓶颈：持续时间受限（<10秒）、存储开销巨大（>500MB）以及 GPU 显存消耗高。本文提出 L4DRotorGS（Layered 4D-Rotor Gaussian Splatting），一种专为长时动态场景设计的统一压缩表示框架。核心设计是将 4D 高斯按**时间跨度**组织成分层结构，再将每层划分为离散的**时间桶**（temporal buckets），实现对必要子集的按需访问与渲染，大幅降低 GPU 显存需求。在压缩方面，结合三种互补技术：因式协方差量化（Factorized Covariance Quantization）、分层压缩（Layered Compression）和残差码本量化（Residual Codebook Quantization），实现高达 22.3× 的压缩比，同时保持高视觉保真度。作者还设计了高度优化的 C++/CUDA 框架，实现了超过 500 FPS 的实时渲染速度（RTX 3090）。在真实世界长时动态场景上的大量实验表明，L4DRotorGS 在存储效率、视觉质量和渲染速度三个维度上均持续优于现有方法。

**亮点**：

1. **首个专为长时动态场景设计的压缩 4DGS 框架**：L4DRotorGS 突破了现有 4DGS 方法局限于短时（<10秒）场景的瓶颈，通过分层时间组织结构（按时间跨度分层 + 离散时间桶划分），实现对长时动态场景的高效编码与按需渲染；分层结构不仅使 GPU 显存消耗与场景时长解耦，还为后续基于时间局部性的压缩和渲染优化提供了天然的结构基础，为大规模动态场景重建（如体育赛事、长视频 AR/VR）的实用化奠定了基础
2. **三重量化压缩协同实现 22.3× 极致压缩**：通过因式协方差量化（分解高斯协方差矩阵降低参数冗余）、分层压缩（跨层共享基础表示减少层间冗余）和残差码本量化（对高斯属性的残差量化降低编码比特数）三种技术的有机结合，在极大压缩存储占用的同时保持高视觉保真度；相比现有 4DGS 方法，存储占用减少超过 20 倍，使移动端或边缘设备部署长时动态场景渲染成为可能
3. **高度优化的 C++/CUDA 实现支持 500+ FPS 实时渲染**：区别于仅关注重建质量的学术工作，L4DRotorGS 还设计了高度工程化的 C++/CUDA 训练-压缩-渲染一体化框架，在 RTX 3090 上实现超过 500 FPS 的实时渲染速度，远超现有 4DGS 方法；同时通过高效的时间桶选择机制，实现了训练过程中对子集 4D 高斯的高效梯度计算，大幅缩短了长时场景的训练时间，展示了在学术研究向工业应用落地方向的扎实工程贡献

### 2026-05-11

**PBR-NeRF: Inverse Rendering with Physics-Based Neural Fields**
**PBR-NeRF：基于物理渲染的神经场逆向渲染**

![PBR-NeRF — Teaser](https://km.sankuai.com/api/file/cdn/2756902383/236118714833?contentType=0&isNewContent=false)

- **来源**：CVPR 2025
- **作者**：Sean Wu, Shamik Basu, Tim Broedermann, Luc Van Gool, Christos Sakaridis（ETH Zürich）
- **链接**：https://arxiv.org/abs/2412.09680 | 代码：https://github.com/s3anwu/pbrnerf

**核心内容**：逆向渲染（Inverse Rendering）是三维重建中的经典难题——在未知光照条件下，从多视角图像中同时估计场景几何、表面材质和环境光照。现有大多数 NeRF 和 3D Gaussian Splatting 方法仅估计视角相关的外观（view-dependent appearance），无法分解材质与光照，限制了重光照、材质编辑等下游应用。本文提出 PBR-NeRF，将物理渲染（PBR）理论与神经辐射场相结合，构建了一个能够联合估计场景几何、材质（基色、粗糙度、金属度）和环境光照的逆向渲染模型。核心创新在于引入两个新颖的物理先验损失项：一是基于物理一致性的材质正则化，约束材质估计在物理合理范围内；二是基于渲染方程的光照一致性先验，减少材质与光照之间的歧义性。这两个先验以直觉清晰的损失函数形式实现，在不牺牲新视角合成质量的前提下，显著提升了材质估计的精度，达到当时最先进水平。该方法具有良好的通用性，可方便地集成到其他需要材质估计的逆向渲染和三维重建框架中。

**亮点**：

1. **两个新颖物理先验显著提升材质估计精度**：PBR-NeRF 的核心贡献是将物理渲染理论转化为可微分的损失约束——材质物理一致性先验限制材质参数在物理合理范围内（如金属度与粗糙度的耦合关系），光照一致性先验通过渲染方程约束减少材质-光照歧义性；两个先验协同作用，在 NeRF-Synthetic、DTU 等标准逆向渲染基准上实现最先进的材质估计性能，同时保持高质量新视角合成，证明了物理约束在神经渲染中的有效性
2. **填补 NeRF 逆向渲染的关键空白**：当前主流 NeRF 和 3DGS 方法普遍只建模视角相关外观，无法分解材质与光照，导致无法支持重光照、材质替换等实用编辑操作；PBR-NeRF 在保持 NeRF 高质量几何重建优势的同时，引入完整的 PBR 材质模型（基于 Cook-Torrance BRDF），实现了几何、材质、光照的联合估计，为 NeRF 框架下的可编辑三维重建提供了坚实基础
3. **高度模块化设计，易于集成到其他框架**：PBR-NeRF 的物理先验损失项设计为独立模块，可方便地插入到其他基于 NeRF 或 3DGS 的逆向渲染框架中，无需大幅修改原有架构；代码已开源（https://github.com/s3anwu/pbrnerf），为后续研究提供了可复用的物理约束基础设施，对推动神经渲染与物理渲染的深度融合具有重要参考价值

### 2026-05-12

**MUSt3R: Multi-view Network for Stereo 3D Reconstruction**
**MUSt3R：多视图立体三维重建网络**

![MUSt3R teaser](https://km.sankuai.com/api/file/cdn/2756902383/236369190911?contentType=0&isNewContent=false)

- **来源**：CVPR 2025
- **作者**：Yohann Cabon, Lucas Stoffl, Leonid Antsfeld, Gabriela Csurka, Boris Chidlovskii, Jerome Revaud, Vincent Leroy（NAVER LABS Europe）
- **链接**：https://arxiv.org/abs/2503.01661 | 代码：https://github.com/naver/must3r

**核心内容**：DUSt3R 在几何计算机视觉领域开创了全新范式，能够在无需相机标定与视点姿态先验的条件下，实现任意图像集合的密集无约束立体三维重建。然而，DUSt3R 底层仍基于图像对处理，其局部三维重建结果需在全局坐标系中对齐，且图像对数量随规模呈二次方增长，在大规模图像集合的鲁棒快速优化中尤为突出。本文提出 MUSt3R（Multi-view Network for Stereo 3D Reconstruction），将 DUSt3R 从图像对扩展至多视图，从根本上解决上述问题。MUSt3R 通过两项关键改进扩展 DUSt3R 架构：一是将架构对称化，使网络能够直接在统一坐标系中预测所有视图的三维结构，无需后处理对齐；二是引入多层工作记忆机制（multi-layer memory mechanism），将计算复杂度从二次方降至线性，支持以高帧率推断数千帧的三维点图，同时仅增加有限的额外复杂度。该框架同时支持离线和在线三维重建，可无缝应用于 SfM（运动恢复结构）和视觉 SLAM 场景，在未校准视觉里程计、相对相机位姿估计、尺度与焦距估计、三维重建以及多视图深度估计等多项下游任务上均达到最先进性能。

**亮点**：

1. **从图像对到多视图的根本性扩展**：DUSt3R 的核心局限在于其成对处理机制——N 张图像需要 O(N²) 对图像对，且局部重建结果需要全局对齐优化，在大规模场景下计算开销极大。MUSt3R 通过对称化架构设计，使网络能够直接在统一全局坐标系中预测所有视图的三维点图，彻底消除了后处理对齐步骤；这一改进不仅大幅降低了计算复杂度，还提升了多视图一致性，为大规模无标定三维重建（如城市级 SfM、长视频 SLAM）的实用化奠定了基础
2. **多层工作记忆机制实现千帧级实时重建**：MUSt3R 引入的多层记忆机制是其扩展性的核心——通过维护一个紧凑的工作记忆（working memory）来压缩历史帧信息，使网络在处理新帧时无需重新处理所有历史帧，将计算复杂度从 O(N²) 降至 O(N)；这一设计使 MUSt3R 能够以高帧率（实时）处理视频流，支持在线视觉里程计（VO）和 SLAM 应用，同时在离线 SfM 场景下也能高效处理数千张图像的大规模重建任务，精度相比 DUSt3R 提升约 50%
3. **统一框架覆盖多项几何视觉下游任务**：MUSt3R 不仅是一个三维重建模型，更是一个通用的几何视觉基础框架——单一模型可同时支持未校准视觉里程计、相对相机位姿估计、焦距与尺度估计、密集三维重建和多视图深度估计等多项任务，且在各任务上均达到最先进性能；这种"一模型多任务"的设计理念延续了 DUSt3R/MASt3R 系列的技术路线，进一步巩固了 NAVER LABS Europe 在端到端几何视觉基础模型领域的领先地位，代码已开源（https://github.com/naver/must3r）

### 2026-05-13

**Fast3R: Towards 3D Reconstruction of 1000+ Images in One Forward Pass**
**Fast3R：单次前向传播重建 1000+ 图像的三维重建方法**

![Fast3R：单次前向传播重建1000+图像的框架示意图](https://km.sankuai.com/api/file/cdn/2756902383/236597040890?contentType=0&isNewContent=false)

- **来源**：CVPR 2025
- **作者**：Jianing Yang, Alexander Sax, Kevin J. Liang, Mikael Henaff, Hao Tang, Ang Cao, Joyce Chai, Franziska Meier, Matt Feiszli（Meta FAIR & University of Michigan）
- **链接**：https://arxiv.org/abs/2501.13928 | 代码：https://github.com/facebookresearch/fast3r

**核心内容**：多视图三维重建是计算机视觉的核心挑战。以 DUSt3R 为代表的当前领先方法采用成对图像处理模式——对每对图像分别推断点图，再通过代价高昂的全局对齐优化融合多视图结果。这一流程存在两大根本瓶颈：一是随着图像数量 N 增加，图像对数量以 O(N²) 增长；二是迭代全局对齐本身是串行的，难以并行加速，且误差会随视图数增多而累积。Fast3R（Fast 3D Reconstruction）提出了对 DUSt3R 的多视图泛化方案：基于 Transformer 架构，在单次前向传播中并行处理 N 张图像，彻底消除了成对处理与迭代对齐的需求。网络直接回归所有图像在统一全局坐标系下的稠密三维点图与置信度图，通过并行化相机位姿估计（多线程 CPU 后处理），可在数秒内完成数百张图像的重建，推理速度较 DUSt3R 提升约 320 倍（251 FPS vs 0.78 FPS）。在相机位姿估计和三维重建基准（CO3D、ScanNet、DTU 等）上，Fast3R 达到最先进性能，同时大幅降低了误差随视图数增多而累积的问题。此外，Fast3R 无需修改网络结构即可微调用于视频三维重建，展现了其强大的泛化能力。

**亮点**：

1. **突破成对处理范式，实现真正的多视图并行重建**：DUSt3R 及其变体（MASt3R、MUSt3R）均依赖图像对作为基本处理单元，N 张图像需处理 O(N²) 对，在大规模场景下计算开销极大；Fast3R 通过设计专门的多视图 Transformer 架构，在单次前向传播中联合处理所有 N 张图像，直接输出所有视图的全局一致点图，将图像对处理彻底替换为全并行处理，使计算复杂度从 O(N²) 降至 O(N)，为千张图像级别的快速三维重建奠定了基础
2. **推理速度提升 320 倍，同时保持甚至超越重建精度**：Fast3R 在 A100 GPU 上处理 1000 张图像的推理速度达到 251 FPS，而 DUSt3R 仅为 0.78 FPS（Spann3R 为 65 FPS）；更重要的是，速度的大幅提升并未以牺牲精度为代价——在 CO3D 相机位姿估计基准上，Fast3R 的旋转精度（RRA@5）和平移精度（RTA@5）均超过 DUSt3R 和 MASt3R，且随着输入视图数量增加，Fast3R 的精度持续提升，而 DUSt3R 因误差累积呈现性能瓶颈
3. **无需架构修改即可扩展至视频重建，展现强泛化能力**：Fast3R 的设计天然支持无序、无位姿图像输入，只需调整训练数据分布即可将其迁移到视频三维重建任务（利用视频帧的时序相关性），无需修改网络结构或损失函数；这一特性表明 Fast3R 学到了具有强泛化能力的几何特征，其发布的代码与预训练权重（基于 Meta FAIR 开源基础设施）也使社区能够便捷地将其作为通用多视图重建基础模型进行二次开发

### 2026-05-14

**SLAM3R: Real-Time Dense Scene Reconstruction from Monocular RGB Videos**
**SLAM3R：单目 RGB 视频实时稠密场景重建**

![SLAM3R 实时稠密三维重建演示](https://km.sankuai.com/api/file/cdn/2756902383/236814339569?contentType=0&isNewContent=false)

- **来源**：CVPR 2025 Highlight（中国三维视觉大会 China3DV 2025 最佳论文 TOP1）
- **作者**：Yuzheng Liu*, Siyan Dong*, Shuzhe Wang, Yingda Yin, Yanchao Yang, Qingnan Fan, Baoquan Chen（北京大学 VCL 实验室 & 香港大学）
- **链接**：https://arxiv.org/abs/2412.09401 | 代码：https://github.com/PKU-VCL-3DV/SLAM3R

**核心内容**：稠密三维重建是 SLAM 领域的核心挑战，传统方法依赖显式相机位姿优化，导致流程复杂且难以实时运行。本文提出 SLAM3R，一套全新的端到端实时稠密三维重建系统，以单目 RGB 视频为输入，通过前馈神经网络直接回归三维点图，无需显式估计任何相机参数。系统的核心思路是采用滑动窗口机制将视频流切分为相互重叠的短片段，在每个窗口内直接从 RGB 图像回归局部三维点图，再通过一个全局坐标配准网络将各局部点图逐步对齐、融合，形成全局一致的稠密场景重建。与传统基于迭代位姿优化的 SLAM 系统不同，SLAM3R 完全抛弃了显式位姿估计这一中间步骤，实现了从原始视频帧到全局稠密点云的完整端到端映射。在多个标准数据集（Replica、ScanNet 等）上的实验表明，SLAM3R 在保持 20+ FPS 实时性能的同时，重建精度和完整度均达到当前最先进水平，可使用消费级显卡（RTX 4090D）运行。该工作被 CVPR 2025 评选为 Highlight 论文，并荣获第四届中国三维视觉大会（China3DV 2025）年度最佳论文 TOP1。

**亮点**：

1. **彻底抛弃显式位姿估计，实现真正的端到端 SLAM**：传统 SLAM 系统（无论是经典几何方法还是 NeRF/3DGS SLAM）都将相机位姿估计作为必要的中间步骤，SLAM3R 则另辟蹊径——通过局部重建网络直接在窗口内建立图像与三维点图的映射，再由全局配准网络在统一坐标系中对齐各局部点图，整个流程无需任何形式的位姿优化；这一设计不仅简化了系统架构，还从根本上避免了位姿估计误差对下游重建质量的影响，是继 DUSt3R 系列之后，神经辐射式场景重建向实时 SLAM 场景延伸的重要突破
2. **20+ FPS 实时性能，重建精度与完整度双达 SOTA**：在 Replica 数据集上，SLAM3R 的重建精度（Accuracy）和完整度（Completeness）均超越此前的 SOTA 方法（包括 Point-SLAM、SplaTAM、MonoGS 等），同时在消费级显卡（RTX 4090D）上实现 20+ FPS 的实时运行；相比之下，质量相当的离线重建方法通常需要数分钟甚至数小时处理一个场景，SLAM3R 以"实时精度"打破了速度与质量之间的传统权衡，为机器人导航、AR/VR 等对实时性要求极高的下游应用提供了实用化基础
3. **滑动窗口机制与渐进式全局对齐，支持无限长视频流处理**：SLAM3R 采用固定大小的滑动窗口作为局部处理单元，结合增量式全局坐标配准策略，使系统的内存占用和计算开销不随视频长度增长，从理论上支持对任意长度视频流的在线实时处理；这与基于全局优化的方法（如 NeSF、NICE-SLAM 等在视频变长后性能大幅下降）形成鲜明对比，也与 Fast3R 等"全图并行"方案互补——SLAM3R 更适合无限长在线 SLAM 场景，而 Fast3R 更擅长离线有界图像集合的高速批量重建

### 2026-05-15

**FastGS: Training 3D Gaussian Splatting in 100 Seconds**
**FastGS：100 秒内完成 3D Gaussian Splatting 训练的通用加速框架**

![FastGS Teaser](https://km.sankuai.com/api/file/cdn/2756902383/237032429228?contentType=0&isNewContent=false)

- **来源**：CVPR 2026 Highlight（SIGGRAPH Asia 2025 3DGS 快速重建挑战赛冠军方案核心组件）
- **作者**：Shiwei Ren, Tianci Wen, Yongchun Fang, Biao Lu（南开大学）
- **链接**：https://arxiv.org/abs/2511.04283 | 项目主页：https://fastgs.github.io/ | 代码：https://github.com/fastgs/FastGS

**核心内容**：3D Gaussian Splatting（3DGS）自提出以来已成为三维重建与新视角合成的主流范式，但其训练速度仍是实际应用的主要瓶颈——原始 3DGS 在标准场景上需要约 30 分钟训练，即便是当前最快的加速方法（如 DashGaussian）也需要数分钟。现有加速方法的核心问题在于：它们未能有效调控训练过程中高斯基元的数量，导致大量冗余高斯参与计算，造成不必要的时间开销。本文提出 FastGS，一个新颖、简洁且通用的 3DGS 训练加速框架，核心思路是基于多视角一致性（multi-view consistency）来评估每个高斯基元的重要性，从而设计出一套无需预算机制（budgeting mechanism）的稠密化与剪枝策略。具体而言，FastGS 通过采样训练视角并构建逐像素 L1 损失图，评估每个高斯基元在多个视角下的贡献度，重要性低的高斯被及时剪枝，重要性高的区域则触发稠密化，使高斯数量始终保持在高效范围内。在 Mip-NeRF 360、Tanks & Temples 和 Deep Blending 等标准数据集上，FastGS 相比 DashGaussian 实现 3.32× 训练加速，相比原始 3DGS 实现 15.45× 加速，同时保持相当的渲染质量（PSNR/SSIM/LPIPS 指标持平或略优）。更重要的是，FastGS 展现出强大的通用性，在动态场景重建、表面重建、稀疏视角重建、大尺度重建和 SLAM 等多种任务上均可实现 2–7× 的训练加速，是一个真正意义上的"即插即用"加速模块。该工作被 CVPR 2026 评选为 Highlight 论文，并被 SIGGRAPH Asia 2025 3DGS 快速重建挑战赛冠军方案采用为核心组件。

**亮点**：

1. **基于多视角一致性的稠密化与剪枝策略，从根本上解决高斯数量冗余问题**：现有 3DGS 加速方法（如 DashGaussian、Mini-Splatting 等）通常依赖预算机制（budgeting）来限制高斯数量，但这类方法本质上是在"事后控制"，无法在训练早期避免冗余高斯的产生；FastGS 另辟蹊径，通过构建多视角 L1 损失图来主动评估每个高斯的跨视角贡献度，使稠密化和剪枝决策具有明确的几何意义——只有在多个视角下均有显著贡献的高斯才会被保留和增殖，从而在训练全程维持高效的高斯数量，在 Mip-NeRF 360 数据集上相比 DashGaussian 实现 3.32× 加速，在 Deep Blending 数据集上相比原始 3DGS 实现 15.45× 加速
2. **真正的"即插即用"通用加速模块，覆盖 3DGS 全任务生态**：FastGS 的设计目标不是针对特定场景类型的专用优化，而是作为通用加速框架适配整个 3DGS 生态——实验证明，FastGS 在静态场景重建（Mip-NeRF 360、T&T、Deep Blending）、动态场景重建（4D-GS）、表面重建（2DGS）、稀疏视角重建（DNGaussian）、大尺度重建（CityGaussian）和 SLAM（MonoGS）等六类任务上均实现 2–7× 训练加速，且渲染质量不降；这种跨任务通用性使 FastGS 成为 3DGS 社区的基础加速基础设施，被 SIGGRAPH Asia 2025 3DGS 快速重建挑战赛冠军方案（3DV-CASIA 团队）采用为核心组件
3. **100 秒完成单场景训练，推动 3DGS 走向实时重建应用**：FastGS 在 Tanks & Temples 的 train 场景上可在约 100 秒内完成训练（原始 3DGS 约需 30 分钟），将 3DGS 的训练时间从"分钟级"压缩至"秒级"；这一突破对于需要快速建模的实际应用场景（如机器人实时建图、AR/VR 内容快速生成、工业质检等）具有重要意义，也为 3DGS 与在线 SLAM 系统的深度融合提供了可行性基础；代码已开源（https://github.com/fastgs/FastGS），CVPR 2026 Highlight 的认可进一步证明了该工作在学术界的影响力

### 2026-05-18

**DiffusionRenderer: Neural Inverse and Forward Rendering with Video Diffusion Models**
**DiffusionRenderer：基于视频扩散模型的神经逆向与正向渲染统一框架**

![DiffusionRenderer teaser图](https://km.sankuai.com/api/file/cdn/2756902383/237347564759?contentType=0&isNewContent=false)

- **来源**：CVPR 2025 Oral（NVIDIA Research × 多伦多大学 × 矢量研究所 × 伊利诺伊大学香槟分校）
- **作者**：Ruofan Liang, Zan Gojcic, Huan Ling, Jacob Munkberg, Jon Hasselgren, Zian Wang, Wenzheng Chen, Sanja Fidler, Nandita Vijaykumar
- **链接**：https://arxiv.org/abs/2501.18590 | 项目主页：https://research.nvidia.com/labs/toronto-ai/DiffusionRenderer/ | 代码：https://github.com/nv-tlabs/diffusion-renderer

**核心内容**：理解和建模光照效果是计算机视觉与图形学的基础任务。经典的基于物理的渲染（PBR）能精确模拟光线传输，但依赖于难以从真实场景中获取的精确场景表示——包括显式三维几何、高质量材质属性和光照条件。逆向渲染（Inverse Rendering）旨在从图像中反推这些场景属性，但长期以来面临严重的病态性（ill-posed）问题：材质、几何与光照之间存在高度耦合，难以准确分解。本文提出 DiffusionRenderer，首次将神经逆向渲染与正向渲染统一在一个框架中。逆向渲染模块利用强大的视频扩散模型先验，从真实世界视频中准确估计 G-buffer（包含法线、深度、漫反射反照率、粗糙度、金属度等材质属性），为图像编辑任务提供接口；正向渲染模块则无需显式光线传输模拟，直接基于 G-buffer 和指定光照条件生成逼真图像。两个模块相互促进：逆向渲染模块为正向渲染模块提供训练数据，正向渲染模块则验证逆向渲染结果的物理一致性。实验表明，DiffusionRenderer 在逆向渲染和正向渲染两个任务上均超越当前最先进方法，并从单段视频输入实现重新打光（relighting）、材质编辑和真实感物体插入等实用应用。该工作被 CVPR 2025 评选为 Oral 论文，是 NVIDIA 在神经渲染领域的重要突破，已在创意行业（广告、电影、游戏）和物理 AI 开发（机器人、自动驾驶合成数据增强）中展现出广泛应用前景。

**亮点**：

1. **首次将逆向渲染与正向渲染统一在单一神经框架中，突破传统两阶段分离范式**：传统逆向渲染方法（如 NeRF-based IR、GS-based IR）通常将材质/几何估计与重新渲染作为独立步骤处理，DiffusionRenderer 则通过共享视频扩散模型骨干网络，让逆向渲染模块（G-buffer 估计）和正向渲染模块（基于 G-buffer 的图像合成）在统一框架内协同训练——逆向模块产生的 G-buffer 直接作为正向模块的训练数据，正向模块的渲染质量反过来约束逆向模块的估计精度，形成自洽的闭环；这一设计不仅提升了两个任务的性能，还使系统能够从单段真实视频中端到端地完成场景理解与重新渲染
2. **利用视频扩散模型强大先验解决逆向渲染的病态性问题**：逆向渲染的核心难点在于材质-光照-几何的分解歧义（如漫反射与高光的混淆、法线与材质的耦合），传统方法依赖手工设计的物理约束或大量正则化项来缓解这一问题，效果有限；DiffusionRenderer 另辟蹊径，将预训练视频扩散模型（基于大规模真实视频数据学习的强大生成先验）迁移到 G-buffer 估计任务，使模型能够利用视频中的时序一致性和场景统计先验来约束分解结果；实验表明，这一策略在法线估计、材质分解等子任务上均显著优于此前的专用方法，尤其在复杂光照和高反射材质场景下优势明显
3. **从单段视频实现实用级重新打光与材质编辑，推动物理 AI 数据增强**：DiffusionRenderer 的最终应用价值体现在两个维度：一是创意内容生成——用户只需提供一段普通视频，即可在任意光照条件下重新渲染场景（如将白天场景转为夜景、将阳光明媚转为阴天），或替换物体材质（如将金属表面改为木质纹理），为广告、电影和游戏开发提供强大的后期制作工具；二是物理 AI 数据增强——通过在不同光照条件下重新渲染合成数据集，可以低成本生成大量多样化训练数据，显著提升机器人感知和自动驾驶模型在不同光照环境下的鲁棒性；CVPR 2025 Oral 的认可和 NVIDIA 的工程化推进（代码已开源）表明该工作具有重要的学术价值和产业影响力

### 2026-05-19

**MUSt3R: Multi-view Network for Stereo 3D Reconstruction**
**MUSt3R：面向大规模图像集合的多视图三维重建网络**

![MUSt3R 论文 teaser 图](https://km.sankuai.com/api/file/cdn/2756902383/237597672075?contentType=0&isNewContent=false)

- **来源**：CVPR 2025（NAVER Labs Europe）
- **作者**：Yohann Cabon, Lucas Stoffl, Leonid Antsfeld, Gabriela Csurka, Boris Chidlovskii, Jerome Revaud, Vincent Leroy（NAVER Labs Europe）
- **链接**：https://arxiv.org/abs/2503.01661 | 代码：https://github.com/naver/must3r

**核心内容**：DUSt3R 开创了无需相机标定和位姿先验的稠密三维重建新范式，但其底层仍以图像对为基本处理单元——N 张图像需处理 O(N²) 对，再通过代价高昂的全局对齐优化融合结果，在大规模图像集合场景下存在严重的计算瓶颈。本文提出 MUSt3R（Multi-view Network for Stereo 3D Reconstruction），对 DUSt3R 架构进行了系统性扩展：首先将网络改造为对称结构，使其能够直接在统一全局坐标系下预测所有视图的三维结构，彻底消除了成对处理后的全局对齐步骤；其次引入多层记忆机制（multi-layer memory mechanism），使模型能够在处理新帧时高效利用历史帧的特征信息，将计算复杂度从 O(N²) 降至近线性，支持以高帧率推理数千张图像。MUSt3R 同时支持离线批处理和在线流式处理两种模式，可无缝应用于 SfM（运动恢复结构）和视觉 SLAM 场景。在多项三维下游任务上——包括无标定视觉里程计（VO）、相对相机位姿估计、尺度与焦距估计、三维重建和多视图深度估计——MUSt3R 均达到当前最先进性能，同时大幅降低了随视图数增多而累积的误差。

**亮点**：

1. **从成对处理到真正的多视图联合推理，消除 O(N²) 计算瓶颈**：DUSt3R 及其直接后继 MASt3R 的核心局限在于以图像对为基本处理单元，N 张图像需处理 N(N-1)/2 对，随后还需运行代价高昂的全局对齐优化（Bundle Adjustment 风格的迭代优化）；MUSt3R 通过将网络改造为对称多视图架构，使模型能够在单次前向传播中联合处理多张图像，直接在统一全局坐标系下输出所有视图的三维点图，彻底跳过全局对齐步骤；配合多层记忆机制，MUSt3R 在处理大规模图像集合时的计算复杂度接近线性，在 1000 张图像规模下相比 DUSt3R 实现数量级的速度提升，同时误差累积问题也得到根本性改善。
2. **多层记忆机制实现高效在线推理，支持无限长视频流的实时三维重建**：MUSt3R 引入的多层记忆机制是其区别于 Fast3R 等"全图并行"方案的关键设计——记忆模块以紧凑的特征向量形式存储历史帧的几何信息，新帧到来时通过注意力机制与记忆交互，无需重新处理所有历史帧；这一设计使 MUSt3R 的内存占用和单帧处理时间不随视频长度增长，从而支持在线流式处理任意长度的视频序列；在无标定视觉里程计（VO）任务上，MUSt3R 在 EuRoC、TUM-RGBD 等标准 SLAM 数据集上超越此前所有无标定方法，展现了其在实时 SLAM 场景中的实用价值。
3. **统一框架覆盖 SfM 与 SLAM 全场景，多项三维任务达到 SOTA**：MUSt3R 的设计目标是成为通用的多视图三维理解基础模型——在离线模式下，它可以作为 SfM 流程的核心组件，直接从无序图像集合中恢复稠密三维结构和相机参数；在在线模式下，它可以作为视觉 SLAM 的前端，实时处理视频流并维护全局一致的三维地图；实验表明，MUSt3R 在相对位姿估计（RRA@5/RTA@5）、多视图深度估计（AbsRel/δ1）、三维重建（Chamfer Distance）等多项指标上均超越 DUSt3R、MASt3R 和 Fast3R，是 DUSt3R 系列架构演进的重要里程碑，也为后续视觉几何基础模型的发展提供了重要参考。

### 2026-05-20

**MASt3R-SLAM: Real-Time Dense SLAM with 3D Reconstruction Priors**
**MASt3R-SLAM：基于三维重建先验的实时稠密 SLAM**

![MASt3R-SLAM 系统架构示意图](https://km.sankuai.com/api/file/cdn/2756902383/237809969733?contentType=0&isNewContent=false)

- **来源**：CVPR 2025（Imperial College London）
- **作者**：Riku Murai*, Eric Dexheimer*, Andrew J. Davison（* 同等贡献，帝国理工学院）
- **链接**：https://arxiv.org/abs/2412.12392 | 代码：https://github.com/rmurai0610/MASt3R-SLAM | 项目页：https://edexheim.github.io/mast3r-slam/

**核心内容**：MASt3R-SLAM 是首个以双视图三维重建先验（MASt3R）为基础自底向上构建的实时单目稠密 SLAM 系统。传统 SLAM 系统通常依赖手工设计的特征点匹配和几何约束，难以在无相机标定信息的情况下实现稠密重建。MASt3R-SLAM 的核心思路是将 MASt3R 强大的三维重建先验直接嵌入 SLAM 框架的各个模块：通过点图匹配（pointmap matching）实现大规模并行相机跟踪，利用光线角度误差最小化进行局部融合，构建关键帧图并执行回环检测，最终通过二阶全局优化（second-order global optimisation）获得全局一致的位姿和稠密几何。系统除唯一相机中心外不对相机模型做任何假设，在野外视频序列上表现鲁棒，在标准 GPU 上可达 15 FPS 实时性能。在已知相机标定的情况下，对系统进行简单修改即可在多个基准测试上达到最先进性能，涵盖 EuRoC、TUM-RGBD、ScanNet 等主流 SLAM 数据集。

**亮点**：

1. **首次将视觉几何基础模型（MASt3R）直接嵌入实时 SLAM 框架，实现无标定稠密重建**：MASt3R-SLAM 不是将 MASt3R 作为离线预处理工具，而是将其三维重建先验深度集成到 SLAM 的跟踪、建图、回环检测和全局优化各个核心模块中；系统利用 MASt3R 输出的点图（pointmap）进行大规模并行相机跟踪，通过最小化光线角度误差（ray angular error）实现高效局部融合，无需依赖传统 SLAM 中的特征点提取与匹配流程；这一设计使系统在无需任何相机内参先验的情况下，仍能在野外视频序列上实现鲁棒的实时稠密建图，是视觉几何基础模型从离线重建走向在线 SLAM 的重要里程碑
2. **即插即用的单目 SLAM 系统，15 FPS 实时性能，多基准 SOTA**：MASt3R-SLAM 在标准 GPU 上实现 15 FPS 的实时稠密重建，在 EuRoC MAV、TUM-RGBD、ScanNet 等主流 SLAM 基准上达到最先进性能；系统设计为即插即用（plug-and-play）模式，可直接处理单目 RGB 视频而无需深度传感器或 IMU；在已知相机标定的情况下，通过简单修改即可进一步提升精度，展现了系统的灵活性和实用性；代码已开源，为后续基于视觉几何基础模型的 SLAM 研究提供了重要的基础设施
3. **二阶全局优化保证全局一致性，回环检测解决长序列漂移问题**：MASt3R-SLAM 引入了高效的关键帧图构建机制和回环检测模块，通过检索相似历史帧并建立约束来消除长序列中的累积漂移；在全局优化阶段，系统采用二阶优化方法（second-order global optimisation）对所有关键帧位姿和三维点图进行联合优化，相比一阶方法收敛更快、精度更高；这一设计使 MASt3R-SLAM 在长走廊、大规模室内场景等传统 SLAM 系统容易失败的场景中仍能保持全局一致的轨迹和稠密地图，为机器人导航和 AR/VR 应用提供了可靠的三维感知基础

### 2026-05-21｜SLAM3R: Real-Time Dense Scene Reconstruction from Monocular RGB Videos（单目 RGB 视频实时稠密三维重建）

**方向**：SLAM / 实时三维重建　**来源**：CVPR 2025 Highlight　**机构**：北京大学 × 香港大学

- **作者**：刘宇政、董思言（共同一作）、王书哲、尹英达、杨言超、樊庆楠、陈宝权（北京大学 × 香港大学）
- **链接**：https://arxiv.org/abs/2412.09401 | 代码：https://github.com/PKU-VCL-3DV/SLAM3R | CVPR 页面：https://openaccess.thecvf.com/content/CVPR2025/html/Liu_SLAM3R_Real-Time_Dense_Scene_Reconstruction_from_Monocular_RGB_Videos_CVPR_2025_paper.html

![SLAM3R 系统架构与重建效果展示](https://km.sankuai.com/api/file/cdn/2756902383/238016955121?contentType=0&isNewContent=false)

**核心内容**：SLAM3R 是北京大学陈宝权团队联合香港大学等机构推出的实时稠密三维重建系统，首次实现从单目 RGB 长视频中实时且高质量地重建场景稠密点云，被 CVPR 2025 评为 Highlight 论文，并荣获第四届中国三维视觉大会（China3DV 2025）年度最佳论文（TOP1）。SLAM3R 的核心创新在于通过前馈神经网络将局部三维重建（Image-to-Pointmap，I2P）与全局坐标配准（Local-to-World，L2W）无缝集成为端到端系统，无需显式估计相机参数。I2P 网络基于 DUSt3R 架构，以滑动窗口方式处理视频帧，直接从多视图 RGB 图像回归局部三维点图；L2W 网络则以增量方式将局部点图逐步注册到全局坐标系，通过置信度图过滤噪声点，最终构建完整场景的稠密点云。系统使用消费级显卡（如 RTX 4090D）即可达到 20+ FPS 的实时性能，在 ScanNet、7-Scenes、ETH3D 等多个基准数据集上的重建准确度和完整度均达到当前最先进水平，同时兼顾了运行效率与重建质量。

**亮点**：

1. **无需相机参数的端到端实时稠密重建，突破传统 SLAM 三角困境**：SLAM3R 彻底摒弃了传统 SLAM 系统中显式相机位姿估计和三角化的流程，直接通过前馈神经网络从 RGB 视频帧回归三维点图；系统采用双层架构——I2P 网络处理局部多视图窗口生成局部点图，L2W 网络负责增量式全局坐标配准——两个网络均基于 DUSt3R 架构并以其权重初始化，实现了从局部到全局的无缝三维重建；这一设计使 SLAM3R 在无需任何相机内参、外参先验的情况下，仍能从普通手机拍摄的 RGB 视频中实时生成高质量稠密点云，极大降低了三维重建的使用门槛
2. **20+ FPS 实时性能，准确度与完整度双 SOTA，消费级 GPU 可用**：SLAM3R 在 RTX 4090D 等消费级显卡上实现 20+ FPS 的实时稠密重建，在 ScanNet、7-Scenes、ETH3D 等主流三维重建基准上同时达到重建准确度（Accuracy）和完整度（Completeness）的最先进水平；相比依赖离线优化的传统多阶段方法（如 COLMAP + MVS），SLAM3R 在保持相当重建质量的同时将处理速度提升了数个数量级；系统代码已完全开源，支持在线重建与可视化，为学术研究和工业应用提供了即用型的实时三维重建基础设施
3. **置信度感知的增量式全局配准，有效抑制长序列漂移**：SLAM3R 的 L2W 网络采用增量式处理策略，每次将新的局部点图注册到已有全局坐标系时，利用 I2P 网络输出的置信度图对点图进行自适应过滤，优先保留高置信度的三维点参与全局配准；这一机制有效抑制了长视频序列中因噪声点积累导致的漂移问题，使系统在大规模室内场景（如长走廊、多房间连通空间）中仍能保持全局一致的稠密地图；结合 CVPR 2025 Highlight 和 China3DV 2025 年度最佳论文的双重认可，SLAM3R 代表了当前单目实时稠密三维重建领域的最高水平

### 2026-05-29｜WildGS-SLAM: Monocular Gaussian Splatting SLAM in Dynamic Environments（动态环境中的单目高斯泼溅 SLAM）

**方向**：SLAM / 实时三维重建　**来源**：CVPR 2025　**机构**：Stanford University × ETH Zürich × Microsoft

- **作者**：Jianhao Zheng, Zihan Zhu, Valentin Bieri, Marc Pollefeys, Songyou Peng, Iro Armeni（斯坦福大学 × ETH Zürich × 微软）
- **链接**：https://arxiv.org/abs/2504.03886 | 代码：https://github.com/GradientSpaces/WildGS-SLAM | 项目页：https://wildgs-slam.github.io/

![WildGS-SLAM 论文 teaser 图](https://km.sankuai.com/api/file/cdn/2756902383/239336324405?contentType=0&isNewContent=false)

**核心内容**：WildGS-SLAM 是斯坦福大学与 ETH Zürich 联合提出的首个面向动态环境的单目 RGB Gaussian Splatting SLAM 系统，被 CVPR 2025 收录。传统 SLAM 系统普遍假设场景静态，在行人、车辆等动态物体存在时会发生严重的跟踪漂移和建图污染。WildGS-SLAM 的核心创新是引入不确定性感知几何建图（uncertainty-aware geometric mapping）机制：系统利用预训练的 DINOv2 特征训练一个轻量级多层感知机（MLP），在线预测每个像素的不确定性图（uncertainty map），无需任何语义标签或深度传感器即可自动识别动态区域。该不确定性图被无缝嵌入稠密 Bundle Adjustment（BA）优化和 3D Gaussian 地图优化两个核心模块，通过软抑制（soft suppression）策略降低动态区域的梯度权重，从而在跟踪和建图过程中自动过滤动态干扰物。系统以 3D Gaussian Splatting 作为场景表示，支持高质量新视角合成，在多个动态场景数据集上实现无伪影渲染，在室内和室外场景中均超越现有动态 SLAM 方法。

**亮点**：

1. **无需语义标签的动态感知，DINOv2 特征驱动在线不确定性预测**：WildGS-SLAM 彻底摆脱对预定义动态类别语义分割的依赖，利用 DINOv2 的强大视觉特征训练轻量级 MLP 在线预测逐像素不确定性；这一设计使系统能够自动发现任意未知动态物体（包括非刚体、局部运动等），无需人工标注或类别先验，在真实"野外"场景中展现出更强的泛化能力；不确定性图以连续值形式表达，通过软抑制策略而非硬性 mask 参与优化，保留了场景中局部可靠信息，避免了二值化 mask 带来的信息损失
2. **3DGS 场景表示实现高质量无伪影新视角合成**：WildGS-SLAM 以 3D Gaussian Splatting 作为场景表示，将不确定性感知机制深度集成到 Gaussian 地图优化中，在动态物体存在的情况下仍能构建干净的静态场景 Gaussian 地图；系统在多个动态场景数据集（包含室内和室外场景）上实现无伪影的高保真新视角合成，渲染质量显著优于基于 NeRF 或点云的动态 SLAM 方法；这一能力使 WildGS-SLAM 不仅适用于机器人导航等定位任务，还能为 AR/VR 等需要高质量场景渲染的应用提供支持
3. **室内外场景全面超越 SOTA，单目 RGB 输入无需深度传感器**：WildGS-SLAM 仅使用单目 RGB 视频作为输入，无需深度传感器或 IMU，在多个动态场景基准数据集上的跟踪精度、建图质量和渲染效果均超越现有动态 SLAM 方法（包括 DynaSLAM、MonoGS、Splat-SLAM 等）；系统在室内（博物馆、办公室等）和室外（街道、广场等）场景中均展现出强鲁棒性，验证了不确定性感知机制的通用性；代码已开源，为动态环境 SLAM 领域的后续研究提供了重要的基础设施

### 2026-05-22｜CraftsMan3D: High-fidelity Mesh Generation with 3D Native Diffusion and Interactive Geometry Refiner（基于原生三维扩散与交互式几何细化的高保真网格生成）

**方向**：三维生成（3D Generation）　**来源**：CVPR 2025（评审满分）　**机构**：香港科技大学 × Adobe Research × 光影焕像

- **作者**：李威宇、刘嘉瑞、阎鸿禹（共同一作）、陈锐、梁奕勋、陈学林、谭平、龙晓晓（香港科技大学 × Adobe Research × 光影焕像）
- **链接**：https://arxiv.org/abs/2405.14979 | 代码：https://github.com/HKUST-SAIL/CraftsMan3D | 项目页：https://craftsman3d.github.io/ | CVPR 页面：https://openaccess.thecvf.com/content/CVPR2025/papers/Li_CraftsMan3D_High-fidelity_Mesh_Generation_with_3D_Native_Diffusion_and_Interactive_CVPR_2025_paper.pdf

![CraftsMan3D 系统架构与生成效果展示](https://km.sankuai.com/api/file/cdn/2756902383/238223018765?contentType=0&isNewContent=false)

**核心内容**：CraftsMan3D 是香港科技大学谭平教授团队联合 Adobe Research 和光影焕像推出的高保真三维网格生成系统，在 CVPR 2025 获得三位评审一致满分评价，并被 Roblox、腾讯混元 Hunyuan3D-2、XR-3DGen 等多家知名企业引用。该系统借鉴传统艺术家建模工作流，将三维生成分为两个阶段：第一阶段由原生三维扩散模型（3D Native Diffusion）直接在三维空间中生成具有平滑几何形状的粗糙网格（约 5 秒），无需依赖多视图图像的中间表示；第二阶段通过法线增强的几何细化器（Normal-based Geometry Refiner）对粗糙网格进行高频细节补全（约 20 秒），利用 2D 法线扩散模型生成多视图法线图并将其转化为精细几何细节。系统支持文本和图像两种输入条件，生成的网格具有规则的拓扑结构（regular mesh topology）和丰富的表面细节，可直接用于游戏、影视等工业级三维内容创作场景。此外，系统还支持类似 ZBrush 的交互式几何编辑，用户可在生成结果基础上进行局部修改，实现人机协同的三维创作流程。

**亮点**：

1. **原生三维扩散模型，彻底摆脱多视图中间表示的几何歧义**：CraftsMan3D 的第一阶段采用在三维空间中直接运行的扩散模型（3D Native Diffusion），以隐式神经表示（如 TriPlane 或 SDF）为生成目标，无需先生成多视图图像再进行三维重建；这一设计从根本上避免了现有 text/image-to-3D 方法中因多视图不一致导致的几何歧义和过度平滑问题；原生三维扩散模型能够直接学习三维形状的分布，生成具有多样化形状和规则网格拓扑的粗糙几何，为后续细化提供高质量的几何基础；该方法在形状多样性和几何准确性上均显著优于基于 Score Distillation Sampling（SDS）的优化方法和基于多视图重建的前馈方法
2. **法线增强的两阶段生成流程，30 秒内实现工业级高保真网格**：CraftsMan3D 的第二阶段引入法线增强几何细化器，利用 2D 法线扩散模型从粗糙网格渲染多视图法线图，再通过法线引导的几何优化将高频表面细节（如皱纹、纹理凹凸、锐利边缘）精确转化为网格几何；整个两阶段流程仅需约 30 秒即可完成，生成的网格具有规则拓扑结构，可直接导入 Blender、Maya 等主流三维软件进行后续编辑；相比需要数分钟甚至数小时的优化方法，CraftsMan3D 在保持高保真度的同时实现了工业级的生成效率，已被 Roblox、腾讯混元 Hunyuan3D-2 等头部平台采用
3. **支持交互式几何编辑，实现人机协同的三维创作闭环**：CraftsMan3D 不仅是一个自动生成系统，还支持类似 ZBrush 的交互式几何细化操作——用户可以在系统生成的粗糙网格基础上，通过笔刷绘制、局部变形等方式提供编辑指令，系统将用户的编辑意图与法线细化器结合，实时生成符合用户意图的精细几何；这一人机协同设计使 CraftsMan3D 既能作为全自动的三维内容生成工具，也能作为辅助设计师的智能建模助手，大幅降低了高质量三维资产的创作门槛；代码和预训练权重已完全开源，为三维生成领域的后续研究提供了重要的基础设施

### 2026-05-25｜RetimeGS: Continuous-Time Reconstruction of 4D Gaussian Splatting（4D 高斯泼溅的连续时间重建）

**方向**：3D Gaussian Splatting（动态场景 4DGS）　**来源**：CVPR 2026 Oral　**机构**：香港科技大学（HKUST）

- **作者**：Xuezhen Wang、Li Ma、Yulin Shen、Zeyu Wang、Pedro V. Sander（香港科技大学）
- **链接**：https://arxiv.org/abs/2603.13783 | 项目页：https://william-wang2.github.io/RetimeGS/ | CVPR 页面：https://cvpr.thecvf.com/virtual/2026/poster/40312

![RetimeGS teaser图](https://km.sankuai.com/api/file/cdn/2756902383/238498627759?contentType=0&isNewContent=false)

**核心内容**：RetimeGS 是香港科技大学 Pedro V. Sander 团队提出的 4D Gaussian Splatting 新方法，被 CVPR 2026 评为 Oral 论文。现有 4DGS 方法通常在离散帧索引上过拟合，在帧间插值时会产生严重的"鬼影"（ghosting）伪影，本质上是一种时间混叠（temporal aliasing）问题。RetimeGS 通过显式建模每个 3D 高斯基元的时间行为来解决这一问题：引入正则化时间不透明度（双 Sigmoid 短尾分布）约束高斯基元的时间存在范围，并使用 Catmull-Rom 样条轨迹对高斯基元的连续运动进行建模，从而实现任意时间戳的平滑渲染。此外，RetimeGS 还结合了光流引导的初始化与监督、三重渲染监督（triple-rendering supervision）以及动态拉伸策略，共同保证大运动场景下的时间一致性。在包含快速运动、非刚性形变和严重遮挡的数据集上，RetimeGS 在 Stage-Capture 数据集上达到 30.08 dB PSNR，超越先前 SOTA 1.29 dB，实现了无鬼影、时间连贯的动态场景重建。

**亮点**：

1. **首次将时间混叠问题引入 4DGS 领域，提出正则化时间不透明度解决鬼影伪影**：RetimeGS 将现有 4DGS 方法在帧间插值时出现的鬼影问题明确定义为"时间混叠"，并针对性地引入双 Sigmoid 短尾分布对每个高斯基元的时间不透明度进行正则化，强制高斯基元在时间维度上具有有限的存在窗口；这一设计从根本上防止了高斯基元在不应出现的时间戳上"泄漏"，消除了插值时的鬼影现象；相比现有方法依赖隐式时间编码或简单线性插值，RetimeGS 的显式时间建模更具可解释性，也更易于控制时间行为
2. **Catmull-Rom 样条轨迹建模连续运动，支持任意时间戳的高质量渲染**：RetimeGS 使用 Catmull-Rom 样条曲线对每个高斯基元的运动轨迹进行参数化，相比线性插值或低阶多项式，样条轨迹能够更准确地捕捉非线性、大幅度的物体运动；结合光流引导的初始化（利用双向光流为高斯基元提供运动先验）和三重渲染监督（在当前帧、前一帧和后一帧同时施加渲染约束），系统能够在大运动、非刚性形变和严重遮挡等极端条件下保持时间连贯性；这使得 RetimeGS 不仅适用于慢动作回放，还能支持任意时间戳的高质量新视角合成，为视频后期制作和时间编辑提供了强大工具
3. **CVPR 2026 Oral 认可，在 Stage-Capture 数据集上超越 SOTA 1.29 dB PSNR**：RetimeGS 在包含快速运动、非刚性形变和严重遮挡的 Stage-Capture 数据集上达到 30.08 dB PSNR，超越先前最优方法 1.29 dB，并在视觉质量上显著消除了鬼影伪影；该工作被 CVPR 2026 评为 Oral 论文（接收率约 3%），代表了动态场景 4DGS 重建领域的最新进展；RetimeGS 的方法简洁有效，核心组件（时间不透明度正则化 + 样条轨迹）可作为即插即用模块集成到现有 4DGS 框架中，具有较强的通用性和实用价值

### 2026-05-26｜Neural Inverse Rendering from Propagating Light（从传播光中进行神经逆向渲染）

**方向**：NeRF / 逆向渲染　**来源**：CVPR 2025 最佳学生论文（Best Student Paper Award）　**机构**：多伦多大学 × 卡内基梅隆大学

- **作者**：Anagh Malik、Benjamin Attal、Andrew Xie、Matthew O'Toole、David B. Lindell（多伦多大学 × 卡内基梅隆大学）
- **链接**：https://arxiv.org/abs/2506.05347 | 项目页：https://anaghmalik.com/InvProp/ | CVF 页面：https://openaccess.thecvf.com/content/CVPR2025/papers/Malik_Neural_Inverse_Rendering_from_Propagating_Light_CVPR_2025_paper.pdf

![Neural Inverse Rendering from Propagating Light - Teaser](https://km.sankuai.com/api/file/cdn/2756902383/238735735074?contentType=0&isNewContent=false)

**核心内容**：本文提出了首个基于物理模型的神经逆向渲染系统，能够从多视点、时间分辨的闪光激光雷达（Flash LiDAR）测量数据中重建场景几何与材质，并生成新视角下的光传播视频。传统 LiDAR 仅利用"第一束光"的返程时间（即直接光），而丢弃了大量因多次散射产生的间接光信息；在强间接光场景（如室内角落、遮挡区域）中，这会导致几何重建误差高达 72%。本文的核心创新是"时间分辨辐射缓存"（Time-Resolved Radiance Cache）：将场景划分为哈希编码体素网格，预先存储任意位置、任意方向的无限次弹射辐射能量图谱，将直接光（解析计算）与间接光（神经网络预测）分离处理，并通过可微渲染方程对光脉冲的完整传播过程进行建模与优化。系统在仿真和真实数据集上均优于现有方法（PSNR 30.99 dB，法向误差 8.45°），并解锁了多项新能力：瞬态重光照（Transient Relighting）、材质分解（Material Decomposition）以及非视域成像（Non-Line-of-Sight Reconstruction，精度达 89%）。该工作荣获 CVPR 2025 最佳学生论文奖，是逆向渲染与瞬态成像交叉领域的里程碑成果。

**亮点**：

1. **首个物理驱动的瞬态神经逆向渲染系统，将间接光纳入几何重建**：现有逆向渲染方法（包括 NeRF-based IR）通常假设稳态光照，忽略光在场景中的传播时序；本文首次将时间分辨（picosecond 级）的光传播测量引入神经逆向渲染框架，通过显式建模直接光与多次弹射间接光的时间分布，在强间接光场景中将几何重建误差降低 72%；这一突破使得 LiDAR 不再只是"测距仪"，而成为能够感知完整光传输物理过程的三维重建传感器
2. **时间分辨辐射缓存技术，将无限次弹射间接光计算效率提升 23 倍**：本文提出的时间分辨辐射缓存（Time-Resolved Radiance Cache）是对传统辐射缓存技术的时间维度扩展，通过哈希编码体素网格存储场景中任意点、任意方向的辐射能量随时间的分布；该缓存将原本需要递归追踪的无限次弹射间接光转化为单次神经网络查询，在保持物理精度的同时将计算效率提升 23 倍；结合可微渲染方程，系统能够端到端优化几何（SDF）、材质（BRDF）和光源参数，实现真正意义上的物理一致性逆向渲染
3. **CVPR 2025 最佳学生论文，解锁瞬态重光照与非视域成像等新能力**：本文荣获 CVPR 2025 最佳学生论文奖（Best Student Paper Award），是该届大会最高荣誉之一；系统在完成逆向渲染后，不仅能够实现多视角时间分辨重光照（在新光源条件下渲染光传播视频），还能自动将测量数据分解为直接光和间接光分量，并利用间接光信息实现非视域成像（Non-Line-of-Sight Reconstruction），在遮挡物后方目标的重建精度达到 89%；这些新能力展示了瞬态神经逆向渲染在自动驾驶感知、医学成像和安防探测等领域的广阔应用前景

### 2026-05-27｜MVSAnywhere: Zero-Shot Multi-View Stereo（零样本多视图立体重建）

**方向**：多视图立体重建（MVS）　**来源**：CVPR 2025　**机构**：Niantic Labs × 爱丁堡大学 × 萨拉戈萨大学

- **作者**：Sergio Izquierdo、Mohamed Sayed、Michael Firman、Guillermo Garcia-Hernando、Daniyar Turmukhambetov、Javier Civera、Oisin Mac Aodha、Gabriel Brostow、Jamie Watson（Niantic Labs）
- **链接**：https://arxiv.org/abs/2503.22430 | 项目页：https://nianticlabs.github.io/mvsanywhere/ | CVF 页面：https://openaccess.thecvf.com/content/CVPR2025/html/Izquierdo_MVSAnywhere_Zero-Shot_Multi-View_Stereo_CVPR_2025_paper.html

![MVSAnywhere - Teaser](https://km.sankuai.com/api/file/cdn/2756902383/238936890893?contentType=0&isNewContent=false)

**核心内容**：从多张图像中精确计算深度（多视图立体重建，MVS）是计算机视觉的基础难题，但现有方法往往只在特定领域（室内/室外、固定深度范围）表现良好，难以跨场景泛化。本文来自 Niantic Labs，提出了 MVSA（Multi-View Stereo Anywhere），一个能够在任意场景、任意深度范围下工作的零样本通用 MVS 架构。MVSA 的核心创新在于三个方面：① 成本体积块化器（Cost Volume Patchifier）：将传统成本体积以 Patch 方式 Token 化，在保留深度细节的同时融入单目 ViT 特征，统一处理多视图匹配信息；② 单/多目线索融合模块（Mono/Multi Cue Combiner）：自适应地结合单目深度线索（ViT 提取的全局语义信息）与多视图立体匹配线索，解决场景遮挡和纹理缺失区域的深度估计问题；③ 视角数量无关与尺度无关的自适应成本体积：通过引入几何元数据（已知相机位姿和焦距），在可变数量输入视图下构建尺度自适应成本体积，自动估计场景有效深度范围，无需先验假设。在涵盖室内（ScanNet）、室外（Tanks and Temples）、无人机视角、文化遗产（ETH3D）等五个多样化数据集组成的 Robust Multi-View Depth Benchmark（RMVDB）上，MVSA 以零样本方式超越了所有现有 MVS 方法和单目深度基线，成为当前多视图深度估计的 SOTA 通用模型。

**亮点**：

1. **首个真正意义上的"通用 MVS"模型，零样本跨域泛化能力达到 SOTA**：以往的 MVS 方法（如 MVSNet、TransMVSNet、GeoMVSNet 等）在各自训练数据分布内表现出色，但换到不同场景类型（如从室内换到无人机视角）或不同深度范围（如从米级场景到公里级场景）后性能大幅下滑；MVSA 通过在大规模多域数据上联合训练，并配合尺度无关的自适应成本体积设计，在从未见过的 5 个测试域上均达到最优零样本深度估计结果，为 MVS 领域向基础模型（Foundation Model）演进树立了重要基准
2. **单目与多视图线索自适应融合，突破传统 MVS 在纹理缺失区域的瓶颈**：传统基于成本体积的 MVS 方法在无纹理区域（天花板、白墙、玻璃等）容易产生深度空洞，因为缺乏纹理意味着无法通过多视图匹配找到可靠对应点；MVSA 引入预训练 ViT 作为单目先验，通过 Mono/Multi Cue Combiner 模块动态权衡何时相信多视图匹配结果、何时回退到单目语义估计，在保留多视图几何一致性的同时补全了传统 MVS 的"盲区"，实现了深度图的完整、平滑输出
3. **与基础模型架构趋势高度契合，对图像匹配与三维重建全流程具有重要参考价值**：MVSA 与同期出现的 DUSt3R、MASt3R、VGGT 等端到端几何基础模型在设计哲学上一脉相承——用 Transformer 统一建模几何先验与匹配信息，追求跨场景泛化；与 DUSt3R/VGGT 端到端直接回归点云不同，MVSA 保留了经典成本体积的可解释性和对大场景的扩展性，通过 ViT 特征增强而非完全替换成本体积，提供了一种兼顾精度、效率与可扩展性的 MVS 现代化路径，对稠密三维重建、SLAM 深度估计等下游任务均有直接借鉴意义

### 2026-05-28｜CUT3R: Continuous 3D Perception Model with Persistent State（具有持久状态的连续三维感知模型）

**方向**：视觉几何基础模型（Visual Geometry Foundation Models）　**来源**：CVPR 2025　**机构**：UC Berkeley

- **作者**：Qianqian Wang、Yifei Zhang、Aleksander Holynski、Alexei A. Efros、Angjoo Kanazawa（UC Berkeley）
- **链接**：https://arxiv.org/abs/2501.12387 | 项目页：https://cut3r.github.io/ | CVF 页面：https://openaccess.thecvf.com/content/CVPR2025/html/Wang_Continuous_3D_Perception_Model_with_Persistent_State_CVPR_2025_paper.html

![CUT3R: 连续3D感知模型框架图](https://km.sankuai.com/api/file/cdn/2756902383/239126151945?contentType=0&isNewContent=false)

**核心内容**：CUT3R（Continuous Updating Transformer for 3D Reconstruction）是来自 UC Berkeley 的 CVPR 2025 论文，提出了一个具有持久状态的连续三维感知框架。与 DUSt3R/MASt3R 等需要一次性输入所有图像的方法不同，CUT3R 引入了一个带状态记忆的循环 Transformer 模型，能够以在线流式方式逐帧处理图像序列：每接收一帧新图像，模型就更新其内部状态，并生成当前帧的度量尺度点云（metric-scale pointmaps）——即每像素对应一个具有真实物理尺度的三维点。所有帧的点云共享同一坐标系，可随时间累积为连贯、稠密的场景重建。更进一步，CUT3R 的内部状态不仅记录了已观测区域的几何，还能通过"探针未观测的虚拟视角"来推断未曾看到过的场景区域，体现出强大的场景先验感知能力。该框架天然支持视频流（顺序帧）和无序照片集两种输入方式，能同时处理静态背景与动态物体，在多视角深度估计、相机位姿估计、视频深度估计、4D 动态场景重建等多项任务上达到 SOTA 性能，同时保持极低的推理延迟。

**亮点**：

1. **首个具有持久状态记忆的在线三维感知基础模型**：DUSt3R/MASt3R/VGGT 等前馈几何模型均假设所有图像同时可用（离线批处理），无法处理实时流式输入；CUT3R 通过引入循环状态（recurrent state），将历史所有帧的几何信息压缩并保持在模型状态中，每到达新帧只需一次前向传播即可完成增量式三维重建，实现了真正意义上的在线（online）连续三维感知，为机器人导航、SLAM 等实时应用提供了强大的 Transformer 基础模型方案。
2. **跨静态与动态内容的统一三维感知框架**：现有 3D 重建方法通常专为静态场景设计，遇到运动物体时往往产生伪影或失效；CUT3R 在设计上不区分静态背景和动态目标，在同一框架内统一建模，在 Sintel、Bonn、KITTI 等包含动态目标的数据集上仍能精准估计每帧深度和相机轨迹，4D 时序场景重建能力尤为突出。
3. **从状态推断未观测区域，体现世界模型（World Model）特质**：CUT3R 不仅能感知已观测区域，还能通过向模型"查询"任意虚拟未观测视角来补全场景几何，说明模型的内部状态已隐式编码了场景的完整三维结构先验；这一特性使 CUT3R 超越了"特征提取骨干"的定位，迈向能理解和预测三维世界的感知模型，对 Embodied AI（具身智能）和交互式三维重建具有重要意义。

### 2026-06-01｜TRELLIS: Structured 3D Latents for Scalable and Versatile 3D Generation（可扩展多功能三维生成的结构化三维隐空间）

**方向**：三维生成（3D Generation）　**来源**：CVPR 2025 Highlight　**机构**：清华大学 × 中国科学技术大学 × 微软亚洲研究院

- **作者**：Jianfeng Xiang、Zelong Lv、Sicheng Xu、Yu Deng、Ruicheng Wang、Bowen Zhang、Dong Chen、Xin Tong、Jiaolong Yang（清华大学 / 中国科学技术大学 / 微软亚洲研究院）
- **链接**：https://arxiv.org/abs/2412.01506 | 项目页：https://microsoft.github.io/TRELLIS/ | 代码：https://github.com/Microsoft/TRELLIS | CVF 页面：https://openaccess.thecvf.com/content/CVPR2025/html/Xiang_Structured_3D_Latents_for_Scalable_and_Versatile_3D_Generation_CVPR_2025_paper.html

![TRELLIS 方法概览图：SLAT 统一结构化隐空间表示与整流流 Transformer 生成模型](https://km.sankuai.com/api/file/cdn/2756902383/239587510589?contentType=0&isNewContent=false)

**核心内容**：TRELLIS 是来自清华大学、中国科学技术大学与微软亚洲研究院的 CVPR 2025 Highlight 论文，提出了一种用于高质量、多功能三维资产生成的新型方法。其核心是统一的结构化隐空间表示（Structured LATent，SLAT）——将稀疏填充的三维网格与从强大视觉基础模型（DINOv2）提取的稠密多视图视觉特征相融合，同时捕获结构（几何）和纹理（外观）信息，并在解码时保持灵活性，可解码为辐射场（Radiance Fields）、3D 高斯（3D Gaussians）和网格（Meshes）等多种输出格式。基于 SLAT，作者设计了专为稀疏结构定制的整流流 Transformer（Rectified Flow Transformers）作为生成骨干，在包含 50 万个多样化三维资产的大规模数据集上训练了最高 20 亿参数的模型。TRELLIS 支持文本和图像两种条件输入，生成质量显著超越现有方法（包括同等规模的方法），并首次展示了灵活的输出格式选择和局部三维编辑能力。整个生成过程约 10 秒完成，代码、模型和数据已完全开源。

**亮点**：

1. **统一多格式输出的结构化隐空间（SLAT）**：TRELLIS 的核心创新在于 SLAT 表示——将稀疏三维网格结构与 DINOv2 提取的稠密多视图视觉特征融合，在单一隐空间中同时编码几何结构和外观纹理。不同于以往方法只能输出单一格式（如仅 NeRF 或仅网格），SLAT 通过为不同格式设计专用解码器，实现了从同一隐变量灵活解码为辐射场、3D 高斯或网格的能力，满足下游应用（渲染、物理仿真、游戏引擎）的多样化需求，是三维生成领域首个真正意义上的"格式无关"统一表示。
2. **大规模整流流 Transformer，生成质量全面超越 SOTA**：TRELLIS 采用专为稀疏 SLAT 结构定制的整流流 Transformer（Rectified Flow Transformers）作为生成模型，在 50 万个精心筛选的三维资产上训练了最高 20 亿参数的模型。在文本/图像到三维生成的多项基准上，TRELLIS 显著超越了 Shap-E、One-2-3-45、Zero123++、InstantMesh 等现有方法，尤其在几何细节保真度和纹理真实感上优势明显；整流流的直线轨迹特性使采样效率更高，约 10 秒即可完成高质量三维资产生成。
3. **首次实现局部三维编辑能力，开创三维生成新范式**：TRELLIS 不仅是一个生成模型，还首次展示了对已生成三维资产进行局部编辑的能力——用户可以指定三维资产的某个局部区域，通过文本或图像提示对该区域进行修改（如替换材质、改变形状、添加细节），而保持其余部分不变。这一能力在以往的三维生成方法中从未实现，为三维内容创作引入了类似 2D 图像编辑的交互式工作流，对游戏、影视、虚拟现实等三维内容产业具有重要的实用价值。

### 2026-06-02｜3D Student Splatting and Scooping（三维学生泼溅与舀取）

**方向**：3D Gaussian Splatting　**来源**：CVPR 2025 Oral　**机构**：University College London × University of Leeds × Central South University

- **作者**：Jialin Zhu、Jiangbei Yue、Feixiang He、He Wang（University College London / University of Leeds / Central South University）
- **链接**：https://arxiv.org/abs/2503.10148 | 项目页：https://drhewang.com/pages/SSS.html | 代码：https://github.com/realcrane/3D-student-splatting-and-scooping | CVF 页面：https://cvpr.thecvf.com/virtual/2025/oral/35367

![3D Student Splatting and Scooping：Student's t 分布与正负密度混合模型示意图](https://km.sankuai.com/api/file/cdn/2756902383/239814343209?contentType=0&isNewContent=false)

**核心内容**：3D Student Splatting and Scooping（SSS）是来自 UCL、利兹大学和中南大学的 CVPR 2025 Oral 论文，从根本上重新审视并改进了 3D Gaussian Splatting（3DGS）的基本范式。作者指出，3DGS 作为一种非归一化混合模型，其核心假设——必须使用高斯分布、必须采用"泼溅"（splatting）方式——并非必要约束。为此，他们提出用更灵活的 Student's t 分布替代高斯分布，并引入"舀取"（scooping）机制，即允许混合模型中存在负密度分量。正密度分量（splatting）负责描述场景中的实体结构，而负密度分量（scooping）则用于精细雕刻边界、消除伪影，两者协同工作，使模型具备更强的表达能力。为解决 Student's t 分布带来的优化挑战，作者还提出了一种新的原则性采样方法。在多个数据集、多种设置和多项指标的全面评估中，SSS 在质量和参数效率上均优于现有方法：在相同组件数量下达到更好或相当的质量，或在减少多达 82% 组件数量的情况下仍能获得可比结果。

**亮点**：

1. **突破 3DGS 基本范式，引入 Student's t 分布替代高斯**：3DGS 自提出以来，几乎所有后续工作都在高斯分布的框架内进行改进（如调整密度控制策略、引入外观模型等），而 SSS 从更根本的层面出发，论证了高斯分布并非最优选择。Student's t 分布具有更重的尾部（heavy tail），可通过自由度参数 ν 灵活控制尾部厚度，从而更精准地拟合场景中的细节纹理和尖锐边界，在相同组件数量下实现更高的渲染质量，为 3DGS 的基础表示研究开辟了新方向。
2. **首次引入负密度"舀取"机制，实现更精细的场景雕刻**：传统 3DGS 仅使用正密度分量叠加来构建场景，难以精确表达物体边界和细薄结构。SSS 创新性地允许混合模型中存在负密度分量（scooping），这些负分量可以"挖去"正分量叠加产生的多余密度，类似于雕塑中的减法操作，从而在不增加总组件数的前提下大幅提升几何精度和边界清晰度，是三维表示领域的一次重要概念创新。
3. **极高的参数效率，组件数减少 82% 仍保持可比质量**：SSS 在参数效率上表现突出——在多个基准数据集上，SSS 可以用比 3DGS 少 82% 的组件数量（即高斯/Student 分布的数量）达到相当的渲染质量，这意味着更小的模型体积、更快的渲染速度和更低的内存占用，对实时渲染、移动端部署等资源受限场景具有重要的实用价值。

### 2026-06-03｜Instant Gaussian Stream: Fast and Generalizable Streaming of Dynamic 3D Gaussians（即时高斯流：快速可泛化的动态三维高斯流式重建）

**方向**：动态三维重建 / 4D 场景表示　**来源**：CVPR 2025 Highlight　**机构**：香港大学 × 港科大 × 腾讯 PCG

- **作者**：Jinbo Yan、Rui Pan、Zhiwei Xu、Mulin Yu、Jiayi Liu、Xiaoxiao Long、Wei Yin（The University of Hong Kong / Hong Kong University of Science and Technology / Tencent PCG）
- **链接**：https://arxiv.org/abs/2503.16979 | 项目页：https://hustruan.github.io/IGS/

![IGS teaser](https://km.sankuai.com/api/file/cdn/2756902383/240534659341?contentType=0&isNewContent=false)

**核心内容**：IGS 提出了首个可泛化的动态 3D Gaussian Splatting 流式重建框架，能够从单目视频实时重建 4D 动态场景。核心贡献有三：（1）Generalizable Streaming 4D Gaussian Reconstruction——基于帧间光流对齐先验，以流式（online）方式逐帧生成 3D 高斯，无需离线优化，2.67 秒/帧可在 NVIDIA 4090 上完成单帧重建；（2）Temporal Anchor Mechanism——引入时序锚点缓存关键帧高斯，利用帧间运动连续性约束减少时域抖动，存储开销仅 7.9 MB/帧；（3）High-Fidelity Rendering——在 Neu3D、HyperNeRF、DyCheck 等动态场景基准上以 204 FPS 实时渲染，PSNR 34.15 dB，在质量与速度上均超越 3DGStream、Spacetime-GS（CVPR 2024）等强基线。该论文获 CVPR 2025 Highlight 认可，展示了将逐帧高斯重建推向工业实时应用的可行路径。

**亮点**：

1. **首个可泛化流式 4D 高斯重建，2.67 秒/帧极速重建动态场景**：不同于现有方法需对每段视频离线优化数小时，IGS 通过光流对齐先验与前馈网络直接预测每帧 3D 高斯属性，实现在线流式推理。每帧重建仅需 2.67 秒（对比 3DGStream 约 10–15 秒/帧），在动态场景重建速度上树立了新标杆，并以 CVPR 2025 Highlight 的成绩得到学界认可。
2. **时序锚点机制，以极低存储开销维持跨帧时域一致性**：IGS 引入时序锚点（Temporal Anchor）缓存关键帧的高斯表示，在生成新帧时利用帧间运动先验对锚点高斯进行轻量变形，从而避免逐帧独立生成导致的时域闪烁和不连贯问题。每帧存储开销仅 7.9 MB，远低于基于体素网格或隐式场方法，为流式部署和在线传输提供了实用保障。
3. **204 FPS 实时渲染，质量与速度双优于 CVPR 2024 强基线**：重建完成后，IGS 的高斯场景表示可以 204 FPS 的速率在标准 GPU 上实时渲染新视角，PSNR 达到 34.15 dB。在 Neu3D、HyperNeRF 等多个动态场景基准上，IGS 在 Per-frame Train Time vs. PSNR 的权衡图中显著优于 3DGStream（CVPR 2024）、Spacetime-GS（CVPR 2024）、4DGS（CVPR 2024）等同期工作，验证了可泛化流式框架的综合优势。

### 2026-06-04｜Prometheus: 3D-Aware Latent Diffusion Text-to-3D Generation by View-Conditioned Multiplane Representation（多视图条件多平面表示的三维感知隐式扩散文本转三维生成）

**方向**：Text-to-3D 生成 / 隐式扩散模型　**来源**：CVPR 2025　**机构**：Seoul National University × NAVER Labs

- **作者**：Yuning Zhang、Joo Chan Lee、Jaeseong Lee、Jong Chul Ye（Seoul National University / NAVER Labs）
- **链接**：https://arxiv.org/abs/2412.21117 | 项目页：https://prometheusgen.github.io/

![Prometheus teaser](https://km.sankuai.com/api/file/cdn/2756902383/240539590551?contentType=0&isNewContent=false)

**核心内容**：Prometheus 提出了一种全新的 Text-to-3D 生成框架，通过"视图条件多平面表示"（View-Conditioned Multiplane Representation）将 3D 几何感知直接嵌入潜在扩散模型，在秒级时间内从文本描述生成高质量三维场景。核心创新在于：（1）将三维场景编码为一组多平面特征图（Multiplane Feature Maps），每张平面对应特定深度层，与视图方向条件共同约束空间一致性；（2）将 2D 潜在扩散模型（Latent Diffusion Model）的生成能力直接迁移到三维域，无需 Score Distillation Sampling（SDS）的逐步优化，从而消除了 SDS 固有的模糊、饱和等伪影；（3）一次前向推理即可生成多视角一致的图像与对应深度图，支持直接导出新视角合成（Novel View Synthesis）结果。在多个 text-to-3D 基准上，Prometheus 以显著更短的生成时间（秒级 vs. 分钟级）达到与 DreamFusion、Magic3D、ProlificDreamer 等方法相当乃至更优的视觉质量，为实用化 Text-to-3D 生成提供了新范式。

**亮点**：

1. **秒级 Text-to-3D，彻底告别 SDS 逐步优化的伪影**：现有 SDS-based 方法（DreamFusion、Magic3D 等）需要对每个文本提示进行数十分钟的迭代优化，且生成结果容易出现过饱和、过平滑等特有缺陷。Prometheus 通过将 LDM 直接扩展为三维感知生成器，在一次前向推理中完成 Text-to-3D 生成，将单样本生成时间压缩到秒级，彻底规避了 SDS 的收敛不稳定和质量下限问题，是 Text-to-3D 生成效率的重要突破。
2. **视图条件多平面表示，原生保证多视角三维一致性**：传统 2D 扩散模型生成的多视角图像之间缺乏三维几何约束，常出现视角不一致的"幻觉"问题。Prometheus 的多平面表示将场景分层编码为深度-平面特征，扩散过程在此三维结构上进行，确保生成的每个视角都与同一底层三维表示对齐。视图方向作为条件信号显式注入，进一步增强了任意视角的生成一致性，为下游 Novel View Synthesis 和三维资产导出提供了可靠保障。
3. **兼容主流 LDM 架构，生成质量媲美甚至超越 ProlificDreamer**：Prometheus 的设计高度兼容 Stable Diffusion 等主流 2D LDM 架构，通过对视图条件注意力层的轻量改造即可接入，无需从头训练大型扩散模型。在 T3Bench 和用户研究中，Prometheus 在视觉质量和三维一致性两项指标上均优于 SJC、Latent-NeRF，并与 ProlificDreamer 相当，同时生成速度快出约两个数量级，展示了基于多平面表示的 LDM 在 Text-to-3D 领域的巨大潜力。

### 2026-06-05｜MVGD: Zero-Shot Novel View and Depth Synthesis with Multi-View Geometric Diffusion（多视图几何扩散零样本新视角与深度合成）

**方向**：视觉几何基础模型 / 新视角合成　**来源**：CVPR 2025　**机构**：Toyota Research Institute

- **作者**：Vitor Guizilini、Muhammad Zubair Irshad、Dian Chen、Greg Shakhnarovich、Rares Ambrus（Toyota Research Institute）
- **链接**：https://arxiv.org/abs/2501.18804 | 项目页：https://mvgd.github.io | CVF 页面：https://cvpr.thecvf.com/virtual/2025/poster/33838

![MVGD - Multi-View Geometric Diffusion Teaser](https://km.sankuai.com/api/file/cdn/2756902383/240535827123?contentType=0&isNewContent=false)

**核心内容**：本文提出 MVGD（Multi-View Geometric Diffusion），一种基于扩散模型的端到端架构，能够在零样本条件下直接生成任意新视角的 RGB 图像与深度图，无需任何中间三维表示（如 NeRF、3D 高斯或体素网格）。MVGD 的关键创新在于"射线图条件化"（Raymap Conditioning）机制：通过将每个像素的空间射线信息编码为条件输入，让扩散模型同时感知多视角的空间位置关系，从而在生成过程中隐式建模多视角几何一致性。此外，模型采用多任务生成策略，通过可学习的任务嵌入（Task Embeddings）引导扩散过程分别生成 RGB 图像与深度图，在单一模型中同时完成新视角合成和深度估计两项任务。系统在超过 6000 万个多视角样本上训练，并提出增量微调策略（逐步从小模型到大模型），展现出优异的扩展性。在多个新视角合成基准、多视图立体重建和视频深度估计任务上均达到最先进水平。

**亮点**：

1. **免中间三维表示的端到端多视角生成，射线图条件化赋予扩散模型几何感知能力**：传统新视角合成需要先重建显式三维结构（NeRF、3DGS 等），再从该结构渲染新视角，推理链条长且误差累积。MVGD 通过射线图条件化机制，直接将输入视角的像素级几何信息（每个像素对应的三维射线方向和相机参数）编码为扩散模型的条件输入，让模型在去噪过程中天然具备跨视角的空间对应感知，从而省去显式三维重建环节，实现端到端的像素级新视角生成，在速度与精度上均优于需要测试时优化的方法。
2. **RGB 与深度联合多任务扩散，可学习任务嵌入统一新视角合成与深度估计**：MVGD 在同一扩散网络中同时生成新视角 RGB 图像和对应深度图，通过可学习的任务嵌入向量引导扩散过程区分两种生成模态，无需为每个任务训练独立网络。这种多任务设计不仅提升了计算效率，还使两个任务之间形成互补：深度信息为 RGB 生成提供几何约束，RGB 特征为深度估计提供语义线索。在 ScanNet、RealEstate10K 等标准基准上，MVGD 同时超越了专门的新视角合成模型和深度估计模型，验证了多任务协同学习的优越性。
3. **6000 万样本训练与增量扩展策略，展现强大的数据扩展性**：MVGD 在来自多个公开数据集（包括室内、室外、合成等多种场景）的超过 6000 万多视角样本上训练，并提出增量微调策略——先在小模型上充分训练，再将其作为大模型的初始化点逐步扩展，大幅降低大模型训练的计算成本。实验表明模型性能随数据量和模型规模持续提升，显示出与大语言模型类似的扩展规律，为视觉几何基础模型的规模化训练提供了重要参考。

### 2026-06-08｜MAGiC-SLAM: Multi-Agent Gaussian Globally Consistent SLAM（多智能体高斯全局一致 SLAM）

**方向**：SLAM / 实时三维重建　**来源**：CVPR 2025　**机构**：TU Wien × ETH Zürich × 苏黎世大学

- **作者**：Vladimir Yugay、Theo Gevers、Martin R. Oswald（TU Wien / ETH Zürich / University of Amsterdam）
- **链接**：[https://arxiv.org/abs/2411.16785](https://arxiv.org/abs/2411.16785) | 代码：[https://github.com/VladimirYugay/MAGiC-SLAM](https://github.com/VladimirYugay/MAGiC-SLAM) | CVF 页面：[CVPR 2025](https://openaccess.thecvf.com/content/CVPR2025/html/Yugay_MAGiC-SLAM_Multi-Agent_Gaussian_Globally_Consistent__SLAM_CVPR_2025_paper.html)

![MAGiC-SLAM 多智能体高斯 SLAM 系统架构图](https://km.sankuai.com/api/file/cdn/2756902383/240726244925?contentType=0&isNewContent=false)

**核心内容**：MAGiC-SLAM 是来自 TU Wien、ETH Zürich 和阿姆斯特丹大学的 CVPR 2025 论文，提出了首个基于 3D Gaussian Splatting 的多智能体 SLAM 系统，能够同时处理多个 RGB-D 相机流，构建全局一致的高保真三维高斯地图并支持新视角合成。现有具备新视角合成能力的 SLAM 系统（如 MonoGS、Gaussian-SLAM 等）均局限于单智能体操作，在大规模场景中存在轨迹漂移和地图不一致问题。MAGiC-SLAM 的核心创新体现在三个方面：（1）刚性可变形 3D 高斯场景表示——将场景分割为多个子地图（submap），每个子地图由一组支持刚体变换的 3D 高斯基元构成，可高效地进行子地图对齐与合并；（2）基于 DINOv2 视觉基础模型的回环检测模块——利用 DINOv2 提取的语义特征进行跨智能体、跨时间的场景识别，在未见过的环境中展现出强泛化能力，触发回环后通过子地图间的高斯配准计算精确的相对位姿约束；（3）灵活的多智能体跟踪与地图融合机制——各智能体独立维护局部子地图，服务器端异步合并子地图并执行全局位姿图优化，系统可无缝扩展到任意数量的智能体。在 Replica 和 ScanNet 等合成与真实数据集上，MAGiC-SLAM 比当时最先进的多智能体 SLAM 方法 CP-SLAM 快 24 倍，GPU 占用降低 7 倍，同时实现更精确的轨迹估计（ATE RMSE 降低约 30%）和更高保真的新视角渲染（PSNR 提升约 2 dB）。

**亮点**：

1. **首个多智能体 3DGS SLAM 系统，24× 速度提升与 7× GPU 节省**：现有基于 3D Gaussian Splatting 的 SLAM 方法（MonoGS、Gaussian-SLAM、GS-SLAM 等）均为单智能体设计，无法利用多相机协同观测的优势；而现有多智能体 SLAM 方法（CP-SLAM 等）虽支持多智能体，但速度慢、GPU 占用高，且不支持高质量新视角合成。MAGiC-SLAM 通过刚性可变形子地图设计，将多智能体协同建图的计算复杂度从 O(N²) 降至近线性，在 Replica 数据集上比 CP-SLAM 快 24 倍、GPU 占用降低 7 倍，同时保持更高的轨迹精度和渲染质量，为多机器人协同建图提供了实用的 3DGS 基础设施。
2. **DINOv2 驱动的跨智能体回环检测，泛化到未见过的真实环境**：传统 SLAM 回环检测依赖手工特征（如 BoW、NetVLAD）或场景特定训练，在新环境中泛化能力有限。MAGiC-SLAM 利用 DINOv2 预训练的强大视觉语义特征构建场景描述符，无需针对特定场景微调即可在 Replica（合成）和 ScanNet（真实）数据集上实现高精度回环检测；检测到回环后，系统直接在 3D 高斯子地图之间进行配准，计算精确的相对位姿约束，并通过位姿图优化消除全局漂移，实现厘米级的轨迹精度，展示了视觉基础模型在 SLAM 回环检测中的强大潜力。
3. **可扩展的多智能体架构，支持任意数量智能体的异步协同建图**：MAGiC-SLAM 采用服务器-客户端架构，各智能体（客户端）独立运行局部跟踪与建图，异步向服务器提交子地图；服务器负责子地图合并、回环检测和全局优化，整个流程无需智能体间的实时同步，天然支持网络延迟和智能体数量动态变化。系统在 2 至 4 个智能体的实验中均展现出稳定的性能提升，随智能体数量增加，场景覆盖率和重建完整性显著提高，而单智能体的计算负担保持不变，为大规模室内测绘、仓储机器人和 AR 协同应用提供了可扩展的三维重建解决方案。

### 2026-06-09｜Turbo3D: Ultra-fast Text-to-3D Generation（超快速文本到三维生成）

**方向**：三维生成（3D Generation）/ Text-to-3D　**来源**：CVPR 2025　**机构**：CMU × Adobe Research × MIT

- **作者**：Hanzhe Hu、Tianwei Yin、Fujun Luan、Yiwei Hu、Hao Tan、Zexiang Xu、Sai Bi、Shubham Tulsiani、Kai Zhang（CMU / Adobe Research / MIT）
- **链接**：[https://arxiv.org/abs/2412.04470](https://arxiv.org/abs/2412.04470) | 项目页：[https://turbo-3d.github.io/](https://turbo-3d.github.io/) | CVF 页面：[CVPR 2025](https://openaccess.thecvf.com/content/CVPR2025/html/Hu_Turbo3D_Ultra-fast_Text-to-3D_Generation_CVPR_2025_paper.html)

![Turbo3D 论文 teaser 图：Latent 4-step 4-view Diffusion 与 Latent GS-LRM 流程示意](https://km.sankuai.com/api/file/cdn/2756902383/240965369958?contentType=0&isNewContent=false)

**核心内容**：Turbo3D 是来自 CMU、Adobe Research 和 MIT 的 CVPR 2025 论文，提出了一套超快速的 Text-to-3D 生成系统，能够在单张 A100 GPU 上于 **0.35 秒内**从文本提示生成高质量的 3D Gaussian Splatting 资产。系统由两个核心组件构成：（1）**Latent 4-step 4-view Diffusion**——一个在潜空间中运行的 4 步、4 视角多视图扩散生成器，通过创新的**双教师蒸馏（Dual-Teacher Distillation）**方法训练：多视图教师（MV Teacher）通过联合计算所有视角的 DMD 损失教授学生模型多视角一致性，单视图教师（SV Teacher）在大规模高质量真实图像上训练，通过逐视角 DMD 损失将生成质量拉向自然图像分布，从而同时保证多视角一致性和照片真实感；（2）**Latent GS-LRM**——一个在潜空间中直接运行的单步前馈高斯重建器，省去了传统方法中耗时的 VAE 解码步骤，将重建时间压缩至 0.03 秒。相比 DreamFusion、Magic3D、ProlificDreamer 等基于 SDS 优化的方法（需数分钟至数小时），以及 MVDiffusion、One-2-3-45 等前馈方法，Turbo3D 在保持竞争性生成质量的同时，速度提升至少一个数量级。

**亮点**：

1. **双教师蒸馏（Dual-Teacher Distillation）彻底解决多视图扩散蒸馏的模态坍缩问题**：现有多视图扩散模型蒸馏方法（如 DMD）仅使用多视图教师，由于多视图训练数据以合成渲染图为主，蒸馏后的学生模型容易出现照片真实感退化（模态坍缩）。Turbo3D 引入额外的单视图教师——一个在大规模高质量真实图像上训练的 2D 扩散模型，通过逐视角 DMD 损失将每个视角的生成质量拉向自然图像分布，与多视图教师的一致性约束形成互补。双教师协同训练使 4 步生成器在多视角一致性和照片真实感两个维度上均达到与完整步数多视图扩散模型相当的质量，是 Text-to-3D 蒸馏加速领域的重要突破。
2. **Latent GS-LRM 将重建时间压缩至 0.03 秒，全流程 0.35 秒完成 Text-to-3D**：传统前馈 3D 重建方法（如 LRM、GS-LRM）在像素空间中运行，需要先将多视图潜变量解码为 RGB 图像，再输入重建网络，VAE 解码本身就占据大量推理时间。Turbo3D 提出 Latent GS-LRM，直接在潜空间中接收多视图扩散生成器的输出（无需 VAE 解码），通过 Transformer 架构直接预测 3D 高斯基元的属性，将重建时间从数秒压缩至 0.03 秒。结合 4 步多视图扩散生成器（0.32 秒），整个 Text-to-3D 流程仅需 0.35 秒，比 SDS-based 方法快 3-4 个数量级，比现有前馈方法快至少一个数量级。
3. **全潜空间流水线设计，为实时三维内容生成奠定基础**：Turbo3D 的两个核心组件（多视图扩散生成器和 GS-LRM 重建器）均在潜空间中运行，形成端到端的全潜空间流水线，避免了中间像素空间转换带来的信息损失和计算开销。这一设计不仅大幅提升了推理速度，还使两个组件可以联合优化，潜空间中的几何信息可以更直接地传递给重建器。在 GSO（Google Scanned Objects）等标准 3D 生成基准上，Turbo3D 在 CLIP 相似度、FID 等指标上与 MVDiffusion+GS-LRM 等方法相当，同时速度提升超过 10 倍，为游戏、AR/VR 等需要实时三维内容生成的应用场景提供了全新的技术路径。

#### 2026-06-10｜Chorus: Multi-Teacher Pretraining for Holistic 3D Gaussian Scene Encoding（多教师预训练的整体性三维高斯场景编码）

**方向**：3D Gaussian Splatting（场景理解与语义编码）　**来源**：CVPR 2026 Oral　**机构**：苏黎世联邦理工学院（ETH Zürich）× 阿姆斯特丹大学 × 特伦托大学

- **作者**：Yue Li、Qi Ma、Runyi Yang、Mengjiao Ma、Bin Ren、Nikola Popovic、Nicu Sebe、Theo Gevers、Luc Van Gool、Danda Pani Paudel、Martin R. Oswald（ETH Zürich / University of Amsterdam / University of Trento）
- **链接**：[https://arxiv.org/abs/2512.17817](https://arxiv.org/abs/2512.17817) | 项目页：[https://gaussianworld.github.io/Chorus/](https://gaussianworld.github.io/Chorus/) | 代码：[https://github.com/GaussianWorld/Chorus](https://github.com/GaussianWorld/Chorus) | CVPR 页面：[CVPR 2026 Oral](https://cvpr.thecvf.com/virtual/2026/oral/40395)

![Chorus 多教师预训练 3DGS 场景编码器框架图](https://km.sankuai.com/api/file/cdn/2756902383/241169603852?contentType=0&isNewContent=false)

**核心内容**：Chorus 是来自 ETH Zürich、阿姆斯特丹大学和特伦托大学的 CVPR 2026 Oral 论文，提出了首个面向 3D Gaussian Splatting 的多教师预训练框架，旨在学习一个通用的前馈式 3DGS 场景编码器。现有 3DGS 方法在新视角合成方面表现出色，但如何从高斯基元中直接提取丰富的通用语义特征仍是未被充分探索的问题。Chorus 通过引入多个互补的 2D 基础模型作为教师（包括语言对齐的 SigLIP2、通用视觉特征的 DINOv3 和目标感知的 PE-Spatial），利用共享的 3D 编码器和各教师专属的轻量投影头，将三类互补信号蒸馏到统一的共享嵌入空间中，使该空间同时捕获从高层语义到细粒度结构的多维信息。Chorus 在多项下游任务上进行了全面评估，包括开放词汇语义分割、实例分割、线性探测与解码器探测、数据高效监督以及基于 LLM 的三维场景问答（3D Scene Q&A）。此外，Chorus 还提出了"渲染-蒸馏自适应"（render-and-distill adaptation）机制，支持对域外数据的高效微调。值得注意的是，仅使用高斯中心、颜色和估计法线训练的点云变体，在仅使用 1/39.9 训练场景的情况下，仍能超越专门的点云基线方法，展示了 Chorus 框架的强大数据效率。

**亮点**：

1. **首个多教师 3DGS 场景编码器，统一语义、实例与空间感知于单一嵌入空间**：现有 3DGS 场景理解方法通常针对单一任务（如语义分割或实例分割）设计，需要为不同任务分别训练模型，缺乏通用性。Chorus 通过同时蒸馏三类互补的 2D 基础模型信号——SigLIP2 提供语言对齐的语义特征、DINOv3 提供通用视觉特征、PE-Spatial 提供目标感知的空间特征——在单一共享嵌入空间中同时编码高层语义、细粒度结构和目标边界信息。这一设计使 Chorus 编码器无需任务特定预训练，即可直接迁移到开放词汇语义分割、实例分割和三维场景问答等多项任务，是 3DGS 场景理解走向基础模型范式的重要一步。
2. **渲染-蒸馏自适应机制，以极高数据效率实现域外泛化**：Chorus 提出的 render-and-distill adaptation 机制允许在新域数据上高效微调预训练编码器：对于新场景，先通过 3DGS 优化得到高斯表示，再从渲染图像中提取 2D 教师特征，以此为监督信号对编码器进行轻量微调，无需大量标注数据。实验表明，仅使用高斯中心、颜色和估计法线（不含完整高斯属性）训练的点云变体，在仅使用 1/39.9 训练场景的情况下仍能超越专门的点云基线，充分验证了 Chorus 框架的数据高效性和跨表示泛化能力，为 3DGS 在数据稀缺场景下的应用提供了重要支撑。
3. **CVPR 2026 Oral 认可，开创 3DGS 与大语言模型结合的三维场景问答新范式**：Chorus 被 CVPR 2026 评为 Oral 论文（接收率约 3%），代表了 3DGS 场景理解领域的最新进展。该工作首次展示了将 3DGS 编码器与 LLM 结合进行三维场景问答（3D Scene Q&A）的能力——通过将 Chorus 编码的场景特征作为 LLM 的视觉输入，模型能够回答关于三维场景内容、空间关系和目标属性的自然语言问题，无需额外的三维标注数据。这一能力对具身智能（Embodied AI）、机器人场景理解和 AR/VR 交互等应用具有重要意义，也为 3DGS 从纯渲染工具向通用三维感知基础设施的演进提供了关键技术路径。

### 2026-06-11｜LIRM: Large Inverse Rendering Model for Progressive Reconstruction of Shape, Materials and View-Dependent Radiance Fields（大规模逆向渲染模型：渐进式重建形状、材质与视角相关辐射场）

**方向**：NeRF / 逆向渲染（Inverse Rendering）　**来源**：CVPR 2025　**机构**：Meta Reality Labs × University of Maryland × UC Merced

- **作者**：Zhengqin Li、Dilin Wang、Ka Chen、Zhaoyang Lv、Thu Nguyen-Phuoc、Milim Lee、Jia-Bin Huang、Lei Xiao、Cheng Zhang、Yufeng Zhu、Carl S. Marshall、Yufeng Ren、Richard Newcombe、Zhao Dong（Meta Reality Labs / University of Maryland / UC Merced）
- **链接**：[https://arxiv.org/abs/2504.20026](https://arxiv.org/abs/2504.20026) | 项目页：[https://lzqsd.github.io/LIRM.github.io/](https://lzqsd.github.io/LIRM.github.io/) | CVF 页面：[CVPR 2025](https://openaccess.thecvf.com/content/CVPR2025/html/Li_LIRM_Large_Inverse_Rendering_Model_for_Progressive_Reconstruction_of_Shape_CVPR_2025_paper.html)

![LIRM 论文 teaser 图：前馈 Transformer 逆向渲染框架示意](https://km.sankuai.com/api/file/cdn/2756902383/241371430791?contentType=0&isNewContent=false)

**核心内容**：LIRM（Large Inverse Rendering Model）是来自 Meta Reality Labs 等机构的 CVPR 2025 论文，提出了首个前馈式 Transformer 逆向渲染模型，能够在不到 1 秒的时间内从少量输入视图（4–8 张）联合重建高质量三维形状、材质参数和视角相关辐射场。现有 Large Reconstruction Models（LRMs）虽在稀疏视图重建上取得显著进展，但普遍存在三个关键缺陷：无法准确重建未观测区域、无法恢复光泽（glossy）外观、无法生成可被标准图形引擎消费的重光照三维内容。LIRM 通过三项核心技术突破解决上述问题：（1）**渐进式更新模型**——允许逐步增加输入视图数量，持续优化重建结果，充分利用多视角信息；（2）**Hexa-Plane 神经 SDF 表示**——将场景几何编码为六平面特征场，在保持计算效率的同时精细恢复纹理细节、几何结构和材质参数；（3）**神经方向嵌入机制**——通过新颖的方向编码策略显式建模视角相关效应（如镜面反射），使辐射场能够准确表达光泽材质。LIRM 在大规模形状与材质数据集上采用由粗到精的训练策略进行训练，在几何精度与重光照准确性上均优于基于优化的稠密视图逆向渲染方法，而推理时间仅为后者的极小部分。

**亮点**：

1. **首个前馈式大规模逆向渲染模型，1 秒内完成几何+材质+辐射场联合重建**：传统逆向渲染方法（如 NeILF、NeRO、PBR-NeRF 等）需要对每个场景进行数小时至数天的逐场景优化，无法适应实时应用需求。LIRM 首次将逆向渲染任务转化为前馈 Transformer 推理问题，从 4–8 张输入图像直接预测 SDF 几何、BRDF 材质（基色、粗糙度、金属度）和视角相关辐射场，整个推理过程在不到 1 秒内完成，速度比优化类方法快数个数量级，为逆向渲染从学术研究走向工业应用（如 AR/VR 内容创作、数字孪生）提供了关键基础设施
2. **Hexa-Plane 神经 SDF 与神经方向嵌入，精准表达光泽材质与精细几何**：LIRM 提出 Hexa-Plane 神经 SDF 表示，将三维场景分解为六个正交平面的特征场，在保持 O(N²) 计算复杂度的同时实现高质量几何与材质重建；配合神经方向嵌入机制，模型能够显式编码视角方向信息，准确恢复镜面高光、各向异性反射等复杂光学现象。实验表明，LIRM 在几何精度（Chamfer Distance）和重光照准确性（PSNR/SSIM）上均优于需要稠密视图的优化基线，打破了"前馈模型精度不如优化方法"的传统认知
3. **渐进式多视图更新与标准图形引擎兼容，打通三维重建到实时渲染的完整链路**：LIRM 的渐进式更新机制允许用户从少量视图开始重建，随新视图加入持续优化结果，无需从头重新计算，极大提升了交互式重建的灵活性。更重要的是，LIRM 输出的材质参数（Disney BRDF）和几何（SDF/网格）可直接导入标准图形引擎（如 Unreal Engine、Unity）进行实时重光照和渲染，填补了"神经渲染好看但无法落地到游戏/影视管线"的长期空白，对数字内容创作产业具有直接实用价值

### 2026-06-12｜MV-DUSt3R+: Single-Stage Scene Reconstruction from Sparse Views In 2 Seconds（单阶段稀疏视图场景重建：2秒完成）

**方向**：多视图立体重建（MVS）　**来源**：CVPR 2025 Oral　**机构**：Meta Reality Labs × UIUC

- **作者**：Zhenggang Tang、Yuchen Fan、Dilin Wang、Hongyu Xu、Rakesh Ranjan、Alexander Schwing、Zhicheng Yan（Meta Reality Labs / University of Illinois Urbana-Champaign）
- **链接**：[https://arxiv.org/abs/2412.06974](https://arxiv.org/abs/2412.06974) | 项目页：[https://mv-dust3rp.github.io/](https://mv-dust3rp.github.io/) | GitHub：[facebookresearch/mvdust3r](https://github.com/facebookresearch/mvdust3r) | CVF 页面：[CVPR 2025 Oral](https://openaccess.thecvf.com/content/CVPR2025/html/Tang_MV-DUSt3R_Single-Stage_Scene_Reconstruction_from_Sparse_Views_In_2_Seconds_CVPR_2025_paper.html)

![MV-DUSt3R+ Teaser - 单阶段多视图三维重建](https://km.sankuai.com/api/file/cdn/2756902383/241568722563?contentType=0&isNewContent=false)

**核心内容**：MV-DUSt3R+ 是来自 Meta Reality Labs 与 UIUC 的 CVPR 2025 Oral 论文，提出了首个单阶段前馈多视图三维场景重建网络，可在无需相机内参或位姿的条件下，仅用约 2 秒从多张稀疏 RGB 视图重建完整三维场景。现有方法如 DUSt3R 和 MASt3R 虽已实现无需标定的双视图重建，但它们仅处理两个视图，需要通过全局优化逐步融合多视图信息，导致推理缓慢且误差逐级累积。MV-DUSt3R+ 的核心创新是设计了多视图解码器块（Multi-View Decoder Blocks），在 Transformer 解码器层中让任意数量的视图之间直接交换信息，同时以一个参考视图为中心进行跨视图注意力计算，从而在单次前向传播中联合预测所有输入视图的三维点图（pointmaps）。为增强对参考视图选择的鲁棒性，MV-DUSt3R+ 进一步提出跨参考视图块（Cross-Reference-View Blocks），将不同参考视图选择下的特征进行融合，消除了重建结果对参考视图选择的敏感性。此外，模型还通过联合训练 Gaussian Splatting 头，扩展支持新视角合成任务。MV-DUSt3R+ 相比 DUSt3R 推理速度提升 48–78 倍，Chamfer Distance 降低 1.6–3.2 倍，显著超越了此前的多视图重建方法。

**亮点**：

1. **单阶段多视图前馈重建，彻底消除全局优化与误差累积**：DUSt3R/MASt3R 采用双视图逐步融合+全局优化的策略处理多视图，推理耗时长（数十秒至分钟级）且每一步的重建误差会随视图数量增加而累积。MV-DUSt3R+ 首次提出多视图解码器块，在 Transformer 解码器中直接实现任意数量视图间的信息交换，单次前向传播即可输出所有视图的点图，无需任何后处理全局优化。这一设计将多视图重建从"串行融合"范式推进到"并行联合推理"范式，推理速度提升 48–78 倍，同时重建精度因消除了误差累积反而大幅提高，在 ScanNet7、DTU 等基准上 Chamfer Distance 降低 1.6–3.2 倍
2. **跨参考视图注意力融合，消除重建对参考视图选择的敏感性**：DUSt3R 的双视图重建以一个参考视图为基准，重建结果严重依赖参考视图的选择质量。MV-DUSt3R+ 提出跨参考视图块（Cross-Reference-View Blocks），对多个不同参考视图选择下生成的特征进行注意力融合，使模型不再依赖单一参考视图，任何视图组合都能产生稳定一致的重建结果。这一设计对于实际应用中随机拍摄顺序的场景重建至关重要
3. **联合 Gaussian Splatting 训练，打通三维重建到新视角合成的完整链路**：MV-DUSt3R+ 不仅输出三维点图（几何重建），还通过联合训练 Gaussian Splatting 头，从点图直接预测 3D 高斯属性（位置、颜色、不透明度、协方差），实现高质量新视角合成。这使得模型在单一前向传播中同时完成几何重建和新视角合成两项任务，无需先重建再优化的两步流程，为 AR/VR 中的实时三维重建和渲染提供了端到端的高效解决方案

### 2026-06-15｜OmniVGGT: Omni-Modality Driven Visual Geometry Grounded Transformer（全模态驱动视觉几何基础模型）

**方向**：视觉几何基础模型（Visual Geometry Foundation Models）　**来源**：CVPR 2026 Highlight　**机构**：港科大（HKUST）× 南洋理工（NTU）× 中山大学（SYSU）

- **作者**：Haosong Peng、Hao Li、Yalun Dai、Yushi Lan、Yihang Luo、Tianyu Qi、Zhengshen Zhang、Yufeng Zhan、Junfei Zhang、Wenchao Xu、Ziwei Liu（HKUST / NTU / SYSU / BIT）
- **链接**：[https://arxiv.org/abs/2511.10560](https://arxiv.org/abs/2511.10560) | 项目页：[GitHub](https://github.com/Livioni/OmniVGGT-official) | CVF 页面：[CVPR 2026 Highlight](https://openaccess.thecvf.com/content/CVPR2026/html/Peng_OmniVGGT_Omni-Modality_Driven_Visual_Geometry_Grounded_Transformer_CVPR_2026_paper.html)

![OmniVGGT 方法概览图](https://km.sankuai.com/api/file/cdn/2756902383/241836321755?contentType=0&isNewContent=false)

**核心内容**：OmniVGGT 是来自港科大（HKUST）、南洋理工（NTU）和中山大学（SYSU）的 CVPR 2026 Highlight 论文，提出了全模态驱动的视觉几何基础模型，在 VGGT（CVPR 2025 最佳论文）的基础上突破了仅支持 RGB 输入的限制，使模型能够灵活利用任意数量和类型的辅助几何模态（深度图、相机内参、相机位姿）来显著提升三维几何推理质量。现有通用三维基础模型（如 VGGT、DUSt3R）普遍假设仅有 RGB 输入，忽略了实际场景中往往可获取的几何先验信息。OmniVGGT 的核心创新包括：（1）**GeoAdapter**——通过零初始化卷积将深度图和相机参数渐进注入空间基础模型，在不破坏预训练表示空间的前提下融入几何先验，推理速度与原始 VGGT 相当；（2）**随机多模态融合训练策略**——训练时对每个样本随机采样不同模态子集，使模型在推理时能够接受任意数量和组合的辅助输入，而非依赖完整的辅助信息，同时避免模型过度依赖辅助线索而退化为浅层捷径学习。在单目/多视图深度估计、多视图立体重建和相机位姿估计等广泛基准测试中，OmniVGGT 在使用辅助输入时超越所有先前方法，仅使用 RGB 输入时也达到最先进水平。此外，OmniVGGT 被集成到视觉-语言-动作（VLA）模型中，增强后的 VLA 模型不仅在主流机器人操作基准上超越基于点云的基线方法，还能有效利用可获取的辅助输入实现一致的性能提升。

**亮点**：

1. **GeoAdapter 零初始化渐进注入，无损融合几何先验**：现有视觉几何基础模型（VGGT 等）仅接受 RGB 输入，无法利用实际场景中经常可获取的深度图或相机参数等几何先验。OmniVGGT 提出的 GeoAdapter 采用零初始化卷积策略，在训练初期几何信息通道输出接近零，随着训练推进逐渐增大贡献，确保几何先验的注入不会破坏预训练模型的表示空间。这一设计使模型在添加多种辅助输入后推理速度仍与原始 VGGT 相当，额外计算开销可忽略，为现有基础模型的高效增强提供了通用范式
2. **随机多模态融合训练，灵活应对任意辅助输入组合**：实际应用中，辅助几何信息的可用性因场景而异——某些场景有深度图但无位姿，某些有内参但无深度。OmniVGGT 创新性地提出随机多模态融合训练策略：每个训练样本随机采样不同模态子集作为输入，使模型学会在任意辅助输入组合下都能稳健工作，而非仅在所有辅助信息完整时才表现良好。这种训练策略还自然防止模型过度依赖辅助线索而忽略 RGB 中的几何信息，确保仅 RGB 输入时仍能保持最先进性能
3. **VLA 集成验证实际应用价值，机器人操作任务一致性提升**：OmniVGGT 不仅是三维几何推理工具，更通过集成到视觉-语言-动作（VLA）模型中展示了其实际应用潜力。增强后的 VLA 模型在主流机器人操作基准上超越基于点云的基线方法，并且能有效利用可获取的辅助输入（如腕部相机深度）实现一致性增益。这验证了全模态几何基础模型从学术基准到具身智能落地的完整链路，为机器人在复杂三维环境中的精准操作提供了新的技术路径

### 2026-06-16｜SEGS-SLAM: Structure-enhanced 3D Gaussian Splatting SLAM with Appearance Embedding（结构增强的三维高斯泼溅 SLAM）

**方向**：SLAM / 实时三维重建　**来源**：ICCV 2025　**机构**：南开大学（Nankai University）

- **作者**：Tianci Wen、Zhiang Liu、Yongchun Fang（南开大学机器人研究所）
- **链接**：[https://arxiv.org/abs/2501.05242](https://arxiv.org/abs/2501.05242) | 项目页：[segs-slam.github.io](https://segs-slam.github.io/)

![SEGS-SLAM 方法概览图](https://km.sankuai.com/api/file/cdn/2756902383/242075491322?contentType=0&isNewContent=false)

**核心内容**：SEGS-SLAM 是来自南开大学机器人研究所的 ICCV 2025 论文，提出了一种结构增强的三维高斯泼溅 SLAM 系统，旨在解决现有 3DGS-SLAM 方法在建图质量上的两大核心痛点：（1）大多数方法无法充分捕捉场景的潜在几何结构，导致高斯基元初始化不规则、结构不一致；（2）现有方法难以处理相机运动引起的外观突变，造成渲染质量不连贯。SEGS-SLAM 的核心创新包括：**结构增强照片级真实感建图（SEPM）框架**——首次利用高度结构化的点云（如 LiDAR 或深度传感器生成的稠密点云）来初始化结构化 3D 高斯基元，使高斯基元的空间分布与场景几何结构高度对齐，从根本上提升建图的结构一致性和渲染质量；**运动外观嵌入（AfME）**——将外观变化编码到相机位姿空间，使 3D 高斯能够更好地建模不同相机位姿下的图像外观变化，有效消除因相机运动导致的渲染不一致问题。在单目、双目和 RGB-D 多种传感器配置下，SEGS-SLAM 在 TUM RGB-D、Replica、EuRoC 和 ScanNet 等主流基准上均显著超越现有 SOTA 方法，例如在单目 TUM RGB-D 数据集上 PSNR 相比 MonoGS 提升 19.86%。

**亮点**：

1. **结构化点云初始化高斯基元，从根本上解决结构不一致问题**：现有 3DGS-SLAM 方法通常从随机或稀疏点云初始化高斯基元，导致高斯分布与场景几何结构脱节，建图质量受限。SEGS-SLAM 提出的 SEPM 框架首次将高度结构化的稠密点云引入高斯初始化流程，使每个高斯基元的位置、方向和尺度都与真实场景几何高度对齐。这一设计不仅显著提升了渲染质量（PSNR 大幅提升），还增强了建图的几何一致性，为后续的相机跟踪和回环检测提供了更可靠的地图表示。
2. **运动外观嵌入（AfME）消除相机运动引起的渲染不一致**：在真实 SLAM 场景中，相机的快速运动会导致同一场景在不同帧中呈现出显著不同的外观（如运动模糊、曝光变化、光照变化），这是 3DGS-SLAM 渲染质量下降的重要原因。SEGS-SLAM 创新性地提出将外观变化编码到相机位姿空间的 AfME 机制，使 3D 高斯能够根据当前相机位姿动态调整外观属性，从而在不同运动状态下都能保持高质量渲染。这一机制在 EuRoC 等高动态场景数据集上效果尤为突出。
3. **多传感器配置全面验证，单目/双目/RGB-D 均达 SOTA**：SEGS-SLAM 在四个主流 SLAM 基准（TUM RGB-D、Replica、EuRoC、ScanNet）上进行了全面评估，覆盖单目、双目和 RGB-D 三种传感器配置，在所有设置下均超越现有最先进方法。这种跨传感器的泛化能力表明 SEGS-SLAM 的结构增强策略具有普适性，不依赖特定传感器类型，为实际机器人和 AR/VR 应用中的高质量实时建图提供了可靠的技术方案。

### 2026-06-17｜WorldGen: From Text to Traversable and Interactive 3D Worlds（从文本到可漫游交互式三维世界）

**方向**：三维生成（3D Generation）/ Text-to-3D Scene　**来源**：CVPR 2026　**机构**：Meta Reality Labs × University of Oxford

- **作者**：Dilin Wang、Hyunyoung Jung、Tom Monnier、Kihyuk Sohn、Chuhang Zou、Xiaoyu Xiang、Yu-Ying Yeh、Di Liu、Zixuan Huang、Thu Nguyen-Phuoc、Yuchen Fan、Sergiu Oprea、Ziyan Wang、Roman Shapovalov、Nikolaos Sarafianos、Thibault Groueix、Antoine Toisoul、Prithviraj Dhar、Xiao Chu、Minghao Chen、Geon Yeong Park、Mahima Gupta、Yassir Azziz、Rakesh Ranjan、Andrea Vedaldi（Meta Reality Labs / University of Oxford）
- **链接**：[https://arxiv.org/abs/2511.16825](https://arxiv.org/abs/2511.16825) | 项目页：[worldgen.github.io](https://worldgen.github.io/) | CVF 页面：[CVPR 2026](https://openaccess.thecvf.com/content/CVPR2026/html/Wang_WorldGen_From_Text_to_Traversable_and_Interactive_3D_Worlds_CVPR_2026_paper.html)

![WorldGen 生成的三维场景快照](https://km.sankuai.com/api/file/cdn/2756902383/242278044719?contentType=0&isNewContent=false)

**核心内容**：WorldGen 是来自 Meta Reality Labs 和 University of Oxford 的 CVPR 2026 论文，提出了首个从单条文本提示生成完整、大型、可漫游交互式三维场景的端到端框架。现有三维场景生成方法在场景多样性、完整性与几何合理性之间存在取舍，且大多仅能生成单个物体或无法保证场景可正常漫游。WorldGen 通过四阶段流水线系统解决上述问题：（1）**场景规划**——借助 LLM 驱动的程序化生成器搭建场景基础空间结构与可漫游区域（导航网格），再通过深度图约束的图像生成器定义场景主题、风格与细节内容；（2）**场景重建**——基于 VecSet 三维隐空间扩散模型，将导航网格作为结构约束通过交叉注意力机制注入，即使在参考图像遮挡区域也能保证场景结构连贯、可正常漫游，导航网格对齐精度（倒角距离）相比基线降低 40%–50%；（3）**场景拆解**——对加速优化的 AutoPartGen 进行场景级微调，按部件连通度优先提取核心支点部件，将整体网格拆分为具备语义属性的独立物体，推理速度从十分钟缩短至一分钟；（4）**场景增强**——利用 LLM-VLM 保持全局风格一致性，对每个独立物体分别生成高分辨率图像、优化几何形态并生成最终纹理。最终输出的大型场景被拆解为可独立编辑的高质量三维网格模型，可直接部署至主流游戏引擎，支持碰撞检测与角色漫游。

**亮点**：

1. **导航网格约束的整体重建，首次保障三维生成场景的可漫游功能**：现有三维场景生成方法普遍忽视场景的功能性——生成的场景可能视觉上合理但角色无法正常行走或存在穿模问题。WorldGen 创新性地将程序化生成器输出的导航网格作为结构约束，通过编码器（稠密+稀疏点集交叉注意力）注入三维隐空间扩散模型，使生成的场景网格严格贴合可通行区域。实验表明，该约束使导航网格对齐精度提升 40%–50%，且支持通过编辑导航网格实现三维空间层面的场景布局修改，即使导航网格与参考图像存在偏差，场景结构与视觉风格依旧保持统一
2. **组合式优化框架：整体重建→拆解→逐物体增强，兼顾全局一致性与局部细节**：传统方法要么整体重建（分辨率不足、不可编辑），要么逐物体重建（缺乏上下文、物体间无法合理衔接）。WorldGen 提出先整体后拆解的组合策略：整体三维扩散重建确保物体间的空间关系和遮挡合理性；加速优化的 AutoPartGen 按连通度优先级将整体网格拆解为独立物体；最终对每个物体用 LLM-VLM 引导的高分辨率图像和网格优化器做几何与纹理增强。这一设计既保留了场景全局一致性，又使每个物体达到工程落地标准
3. **全流程模块化设计，输出直接兼容游戏引擎**：WorldGen 的四阶段流水线完全模块化，支持对布局、规模和风格的细粒度控制。最终输出的每个物体均为带完整纹理的三维网格模型，原生支持碰撞检测与角色漫游交互，可直接导入 Unreal Engine、Unity 等主流游戏引擎进行实时渲染和编辑。这是三维生成从学术演示走向游戏、仿真等实际应用的关键一步，将 Text-to-3D 的能力从单体物体生成推进到完整功能化世界构建

### 2026-06-18｜Volumetrically Consistent 3D Gaussian Rasterization（体积一致性三维高斯光栅化）

**方向**：3D Gaussian Splatting（渲染物理精度）　**来源**：CVPR 2025 Highlight　**机构**：University of California, San Diego（加州大学圣地亚哥分校）

- **作者**：Chinmay Talegaonkar、Yash Belhe、Ravi Ramamoorthi、Nicholas Antipa（加州大学圣地亚哥分校）
- **链接**：[https://arxiv.org/abs/2412.03378](https://arxiv.org/abs/2412.03378) | 项目页：[chinmay0301.github.io/vol3dgs](https://chinmay0301.github.io/vol3dgs/) | CVF 页面：[CVPR 2025](https://openaccess.thecvf.com/content/CVPR2025/html/Talegaonkar_Volumetrically_Consistent_3D_Gaussian_Rasterization_CVPR_2025_paper.html)

![Vol3DGS 体积一致性 3D 高斯光栅化论文主图](https://km.sankuai.com/api/file/cdn/2756902383/242491281039?contentType=0&isNewContent=false)

**核心内容**：Vol3DGS 是来自加州大学圣地亚哥分校的 CVPR 2025 Highlight 论文，从根本上重新审视了 3D Gaussian Splatting（3DGS）渲染模型的物理准确性问题。原始 3DGS 采用基于 EWA（Elliptical Weighted Average）的 splatting 渲染方式，对体积渲染方程做了两个关键近似：（1）将指数透射率线性化；（2）假设高斯基元之间不存在自遮挡。这两个近似虽然加速了渲染，但导致 alpha 值计算不准确，使得不透明表面的表示精度下降。Vol3DGS 证明了这些近似在光栅化框架内是完全不必要的——通过对 3D 高斯进行直接体积积分，可以解析计算透射率，从而推导出比 3DGS 更物理精确的 alpha 值，且可直接嵌入 3DGS 的渲染框架中使用。该方法在保持光栅化速度优势的同时，更接近体积渲染方程（类似光线追踪的物理精度）。实验表明，Vol3DGS 能以更少的高斯基元更精确地表示不透明表面，在 SSIM 和 LPIPS 指标上超越原始 3DGS。此外，体积一致性还使该方法天然适用于 CT 断层扫描重建（tomography），以更少的点匹配了当前最先进的 3DGS 断层扫描方法。

**亮点**：

1. **从数学根源修正 3DGS 渲染方程，消除两大物理近似**：原始 3DGS 的 splatting 渲染对指数透射率做线性化近似并忽略高斯间自遮挡，这两个近似在高斯基元密集重叠时会导致明显的渲染误差（如表面过度透明、边缘模糊）。Vol3DGS 通过解析积分直接计算每个高斯基元的体积透射率，推导出精确的 alpha 值，从根本上消除了这两个近似。这一修正不改变 3DGS 的整体框架，仅替换 alpha 计算模块，即可无缝集成到现有 3DGS 流水线中，为后续基于 3DGS 的方法提供了更可靠的物理基础。
2. **更少高斯基元实现更高渲染质量，SSIM 和 LPIPS 双指标超越 3DGS**：由于 alpha 值计算更精确，Vol3DGS 能够用更少的高斯基元精确表示不透明表面，避免了原始 3DGS 为补偿渲染误差而过度密集化高斯基元的问题。在标准新视角合成基准（Tanks and Temples、Deep Blending 等）上，Vol3DGS 在 SSIM 和 LPIPS 两个感知质量指标上均超越原始 3DGS，同时模型更紧凑。这表明物理精确的渲染方程不仅提升了视觉质量，还带来了更高效的场景表示。
3. **体积一致性天然支持 CT 断层扫描重建，跨领域应用潜力显著**：Vol3DGS 的体积一致性渲染使其不仅适用于视觉新视角合成，还能直接应用于医学 CT 断层扫描重建（tomography）——这是原始 3DGS 无法直接支持的任务。实验表明，Vol3DGS 以更少的高斯基元匹配了当前最先进的 3DGS 断层扫描方法（R2-Gaussian），无需任何针对断层扫描的特殊设计。这一跨领域能力表明，物理精确的体积渲染方程是连接计算机视觉与医学影像的重要桥梁，Vol3DGS 为 3DGS 在科学计算领域的应用开辟了新方向。

### 2026-06-19｜SVG-IR: Spatially-Varying Gaussian Splatting for Inverse Rendering（空间变化高斯泼溅逆向渲染）

**方向**：NeRF / 逆向渲染（3DGS 逆向渲染与重光照）　**来源**：CVPR 2025　**机构**：南京大学（Nanjing University）

- **作者**：Hanxiao Sun、YuPeng Gao、Jin Xie、Jian Yang、Beibei Wang（南京大学）
- **链接**：[https://arxiv.org/abs/2504.06815](https://arxiv.org/abs/2504.06815) | CVF 页面：[CVPR 2025](https://openaccess.thecvf.com/content/CVPR2025/html/Sun_SVG-IR_Spatially-Varying_Gaussian_Splatting_for_Inverse_Rendering_CVPR_2025_paper.html)

![SVG-IR 论文 teaser 图](https://km.sankuai.com/api/file/cdn/2756902383/242656380510?contentType=0&isNewContent=false)

**核心内容**：SVG-IR 是来自南京大学的 CVPR 2025 论文，针对现有 3D Gaussian Splatting（3DGS）逆向渲染方法的核心缺陷提出了系统性改进。现有 3DGS 逆向渲染方法将每个高斯基元的材质参数（BRDF）和法线视为常量，导致在重光照任务中出现明显伪影和不自然的间接光照效果。SVG-IR 提出了"空间变化高斯"（Spatially-Varying Gaussian，SVG）这一新型表示，允许每个高斯基元拥有空间变化的材质参数和法线，类似于传统图形管线中的顶点/片元着色机制（vertex/fragment shading）。在此基础上，SVG-IR 设计了配套的 SVG splatting 渲染方案，并集成了基于物理的间接光照模型，使重光照结果更加真实。实验表明，SVG-IR 在重光照任务上的 PSNR 比最先进的 NeRF 方法高出 2.5 dB，比现有高斯方法高出 3.5 dB，同时保持实时渲染速度。

**亮点**：

1. **空间变化高斯（SVG）表示突破常量材质限制**：传统 3DGS 逆向渲染将每个高斯基元的 BRDF 参数和法线视为常量，无法捕捉单个高斯覆盖区域内的材质变化，导致重光照时出现块状伪影。SVG-IR 引入空间变化高斯表示，允许每个高斯基元在其覆盖的空间范围内拥有连续变化的材质参数和法线，类比传统图形管线中的片元着色器（fragment shader）。这一设计使高斯基元能够更精细地建模表面材质的空间变化，从根本上提升了逆向渲染的分解精度。
2. **物理间接光照模型显著改善重光照真实感**：现有 3DGS 逆向渲染方法通常忽略或简化间接光照（如环境光遮蔽、互反射），导致重光照结果缺乏真实感。SVG-IR 集成了基于物理的间接光照模型，能够准确建模光线在场景中的多次弹射效果，使重光照结果在阴影、高光和环境光遮蔽等方面更加自然。这一改进在重光照 PSNR 上带来了显著提升：比 NeRF 方法高 2.5 dB，比现有高斯方法高 3.5 dB。
3. **兼顾新视角合成与重光照质量，保持实时渲染速度**：SVG-IR 在提升重光照质量的同时，并未牺牲新视角合成（NVS）的渲染质量，在两个任务上均达到 SOTA 水平。更重要的是，SVG splatting 方案继承了 3DGS 的光栅化渲染优势，保持了实时渲染速度，使 SVG-IR 在实际应用（如 AR/VR 场景重光照、数字孪生）中具有直接部署价值，而不仅仅是学术演示。

### 2026-06-22｜Murre: Multi-view Reconstruction via SfM-guided Monocular Depth Estimation（基于 SfM 引导单目深度估计的多视图重建）

**方向**：多视图立体重建（MVS / 多视图重建）　**来源**：CVPR 2025　**机构**：浙江大学（Zhejiang University）× 北京师范大学

- **作者**：Haoyu Guo、He Zhu、Sida Peng、Haotong Lin、Yunzhi Yan、Tao Xie、Wenguan Wang、Xiaowei Zhou、Hujun Bao（浙江大学 × 北京师范大学）
- **链接**：[https://arxiv.org/abs/2503.14483](https://arxiv.org/abs/2503.14483) | 项目页：[zju3dv.github.io/murre](https://zju3dv.github.io/murre/) | GitHub：[zju3dv/Murre](https://github.com/zju3dv/Murre) | CVF 页面：[CVPR 2025](https://openaccess.thecvf.com/content/CVPR2025/html/Guo_Multi-view_Reconstruction_via_SfM-guided_Monocular_Depth_Estimation_CVPR_2025_paper.html)

![Murre 论文 teaser 图](https://km.sankuai.com/api/file/cdn/2756902383/242777503352?contentType=0&isNewContent=false)

**核心内容**：Murre 是来自浙江大学 zju3dv 实验室的 CVPR 2025 论文，提出了一种全新的多视图三维重建范式——通过 SfM 引导的单目深度估计替代传统 MVS 的多视图匹配步骤。近年来，大规模视觉模型在单目深度估计任务上展现出卓越的泛化能力，但单目深度估计本质上存在尺度模糊性，估计的深度值精度不足，难以直接用于多视图几何重建。Murre 的核心创新在于将 SfM 恢复的稀疏点云作为强多视图先验注入条件扩散模型，引导深度估计过程：首先对输入多视图图像运行 SfM 获取稀疏点云（捕捉全局场景结构），然后将 SfM 点云作为条件信号注入预训练的单目深度扩散模型，引导其生成具有度量尺度的精确深度图，最后通过 TSDF 融合将多张深度图整合为完整的三维重建结果。这一设计巧妙地绕过了传统 MVS 中计算代价高昂的多视图代价体构建和匹配步骤，同时利用 SfM 的全局几何先验约束单目深度估计的尺度，实现了精度与效率的兼顾。实验表明，Murre 在公开真实数据集上的深度估计质量显著优于此前的单目深度方法，在室内、街景和航拍等多种场景类型下的重建质量超越了当前最先进的 MVS 方法。

**亮点**：

1. **SfM 先验注入扩散模型，突破单目深度尺度模糊瓶颈**：单目深度估计的致命弱点是尺度模糊性——无法从单张图像恢复真实物理尺度，导致多视图深度图无法直接融合。Murre 首次将 SfM 稀疏点云作为几何条件注入深度扩散模型，让模型在生成深度时"看到"全局三维结构，从而输出具有一致度量尺度的深度图。这一设计既保留了单目深度估计的跨场景泛化能力（继承预训练视觉大模型的先验），又通过 SfM 先验弥补了尺度信息的缺失，为"用单目深度做 MVS"这一长期构想提供了可行路径
2. **绕过传统多视图匹配，重建流程极简且高效**：传统 MVS 需要构建多视图代价体、进行像素级匹配和深度回归，计算量大且对纹理缺失区域敏感。Murre 完全绕过了多视图匹配步骤——每张图像独立进行 SfM 引导的深度估计，再通过 TSDF 融合即可获得完整重建。这种"先估计后融合"的解耦设计大幅降低了 GPU 显存需求，避免了代价体内存的二次增长问题，同时利用预训练扩散模型的强大先验自然处理无纹理区域和重复纹理区域，在多种场景类型上展现出优异的鲁棒性
3. **多场景泛化超越 SOTA MVS，为 MVS 基础模型化提供新范式**：Murre 在室内（ScanNet、Replica）、街景（KITTI）和航拍（BundleFusion）等差异极大的场景上均超越了当前最先进的 MVS 方法，展现了强大的跨域泛化能力。与 MVSAnywhere 等专用 MVS 模型需要在大规模多域数据上联合训练不同，Murre 借助预训练深度扩散模型的泛化能力，仅需 SfM 提供几何锚点即可适配任意场景。这一"预训练视觉模型 + SfM 几何先验"的范式为 MVS 向基础模型演进提供了新的思路，与传统代价体方法（如 MVSAnywhere 的 Cost Volume Patchifier）形成了互补的技术路线

### 2026-06-23｜FoundationStereo: Zero-Shot Stereo Matching（零样本立体深度估计基础模型）

**FoundationStereo：零样本立体深度估计基础模型**

**方向**：视觉几何基础模型（Visual Geometry Foundation Models）　**来源**：CVPR 2025 Best Paper Candidate　**机构**：NVIDIA

- **作者**：Bowen Wen、Matthew Trepte、Joseph Aribido、Jan Kautz、Orazio Gallo、Stan Birchfield（NVIDIA）
- **链接**：[https://arxiv.org/abs/2501.09898](https://arxiv.org/abs/2501.09898) | 项目页：[nvlabs.github.io/FoundationStereo](https://nvlabs.github.io/FoundationStereo/) | GitHub：[NVlabs/FoundationStereo](https://github.com/NVlabs/FoundationStereo) | CVF 页面：[CVPR 2025](https://openaccess.thecvf.com/content/CVPR2025/html/Wen_FoundationStereo_Zero-Shot_Stereo_Matching_CVPR_2025_paper.html)

![FoundationStereo 论文 teaser 图](https://km.sankuai.com/api/file/cdn/2756902383/242996178350?contentType=0&isNewContent=false)

**核心内容**：FoundationStereo 是 NVIDIA 提出的 CVPR 2025 Best Paper Candidate 论文（满分评审），首次为立体深度估计领域构建了具备强零样本泛化能力的基础模型。传统立体匹配方法虽然在特定基准数据集上通过逐域微调取得了巨大进展，但跨域零样本泛化能力一直是该领域的核心瓶颈——这与图像分类、目标检测等其他视觉任务中基础模型所展现出的强大泛化能力形成了鲜明对比。FoundationStereo 通过三大关键设计突破这一瓶颈：（1）**大规模高保真合成数据集（FSD）**——利用 NVIDIA Omniverse 构建包含 100 万对立体图像的合成数据集，涵盖结构化室内/室外场景及高多样性随机化场景（飞行物体、复杂光照、多变相机参数），并通过域随机化策略最大化数据多样性；（2）**迭代自筛选（Iterative Self-Curation）**——自动检测并移除模糊样本（如严重纹理重复、 ubiquitous 反射、纯色区域等），通过交替训练与筛选迭代优化数据质量；（3）**Side-Tuning Adapter（STA）**——将 DepthAnythingV2 等视觉基础模型的丰富单目深度先验通过侧调适配器融入立体匹配网络，有效缓解合成到真实域的 gap，同时保留多尺度 CNN 提取的高频细节特征。此外，网络还设计了 Attentive Hybrid Cost Filtering（AHCF）模块，结合 Axial-Planar Convolution 与 Disparity Transformer 实现 4D 混合代价体在空间与视差维度上的长程上下文推理。实验表明，FoundationStereo 在 Middlebury、ETH3D 等排行榜上位列第一，无需任何目标域微调即可在多样化真实场景（室内/室外、无纹理/反光/透明/薄结构物体、复杂光照）上实现鲁棒且精确的立体深度估计。

**亮点**：

1. **百万级合成数据 + 自筛选，首次实现立体匹配的真正零样本泛化**：立体匹配领域长期受困于"在训练域表现优异、跨域即崩溃"的困境，现有方法几乎都需要在目标域上进行微调才能达到可用精度。FoundationStereo 通过 NVIDIA Omniverse 构建的百万级高保真合成数据集（FSD）结合迭代自筛选机制，首次让立体匹配模型具备了类似 CLIP、SAM 等基础模型的零样本跨域泛化能力——在从未见过的真实场景上直接推理即可达到 SOTA 精度，无需任何目标域微调。这一突破为立体匹配从"专用模型"走向"基础模型"奠定了数据与方法论基础
2. **Side-Tuning Adapter 融合单目基础模型先验，巧妙缓解 sim-to-real gap**：合成数据训练的网络往往在面对真实图像时因域差异而性能骤降。FoundationStereo 创新性地通过 Side-Tuning Adapter 将 DepthAnythingV2 的视觉基础模型特征作为几何先验融入立体匹配流程——不是直接使用具有尺度模糊性的单目深度预测值，而是利用其深层 latent 特征来引导代价体过滤，使网络在纹理缺失、反光、透明等传统立体匹配难以处理的区域也能获得可靠的几何线索。这一设计既保留了立体匹配在度量精度上的优势，又借助单目基础模型的强大泛化能力弥补了合成数据的域 gap
3. **Attentive Hybrid Cost Filtering 实现长程上下文推理，架构设计兼顾效率与精度**：传统代价体过滤方法（如 3D 卷积）难以有效聚合长程空间与视差维度的上下文信息。FoundationStereo 提出的 AHCF 模块将 Axial-Planar Convolution（沿空间轴与视差平面的可分离卷积）与 Disparity Transformer（在视差维度上执行自注意力）相结合，在保持计算效率的同时实现了 4D 混合代价体的长程特征聚合。配合 GRU 迭代精化机制，网络能够从粗到细地逐步优化视差估计，在 Middlebury 和 ETH3D 等权威排行榜上均取得第一名的成绩，同时推理速度满足实时应用需求

#### 2026-06-24｜SLAM3R: Real-Time Dense Scene Reconstruction from Monocular RGB Videos（单目RGB视频实时密集三维重建）

**SLAM3R：单目RGB视频实时密集三维重建**

**方向**：SLAM / 实时三维重建　**来源**：CVPR 2025 Highlight　**机构**：北京大学（PKU）× 香港大学（HKU）

- **作者**：Yuzheng Liu、Siyan Dong、Shuzhe Wang、Yingda Yin、Yanchao Yang、Qingnan Fan、Baoquan Chen（北京大学 / 香港大学）
- **链接**：[https://arxiv.org/abs/2412.09401](https://arxiv.org/abs/2412.09401) | GitHub：[PKU-VCL-3DV/SLAM3R](https://github.com/PKU-VCL-3DV/SLAM3R) | CVF 页面：[CVPR 2025 Highlight](https://openaccess.thecvf.com/content/CVPR2025/html/Liu_SLAM3R_Real-Time_Dense_Scene_Reconstruction_from_Monocular_RGB_Videos_CVPR_2025_paper.html)

![SLAM3R 论文 teaser 图：实时密集三维重建系统框架](https://km.sankuai.com/api/file/cdn/2756902383/243182048014?contentType=0&isNewContent=false)

**核心内容**：SLAM3R 是来自北京大学陈宝权团队联合香港大学等机构的 CVPR 2025 Highlight 论文，同时荣获第四届中国三维视觉大会（China3DV 2025）年度最佳论文（TOP1）。SLAM3R 首次实现从单目 RGB 长视频中实时且高质量地重建场景稠密点云，使用消费级显卡（如 RTX 4090D）即可达到 20+ FPS 的重建性能。现有密集三维重建方法普遍依赖离线处理流程，无法满足实时应用需求；而现有实时 SLAM 方法又往往牺牲重建质量。SLAM3R 通过两层级前馈神经网络架构突破这一困境：（1）**Image-to-Points（I2P）网络**——以滑动窗口方式处理连续视频帧，直接从局部视频片段回归三维点图（pointmaps），无需显式估计相机参数；（2）**Local-to-World（L2W）网络**——将 I2P 输出的局部点图渐进式对齐到统一全局坐标系，通过迭代更新机制实现全局一致的稠密重建。整个系统端到端可微，无需任何相机标定或位姿初始化，直接从原始 RGB 视频输出全局一致的稠密点云。在 ScanNet、7-Scenes 等主流基准上，SLAM3R 的重建精度和完整度均达到当前最先进水平，同时实现了实时运行速度，兼顾了效率与质量。

**亮点**：

1. **无需相机参数的端到端前馈重建，彻底摆脱传统 SLAM 的显式位姿估计依赖**：传统 SLAM 系统（如 ORB-SLAM、NICE-SLAM）需要显式估计相机位姿作为中间表示，再基于位姿进行建图，这种两阶段设计导致位姿误差会直接传播到建图质量中。SLAM3R 创新性地完全绕过相机位姿估计——I2P 网络直接从视频帧回归三维点图，L2W 网络直接在点图空间中进行全局对齐，整个流程无需任何相机内参或外参。这一设计不仅简化了系统架构，还消除了位姿估计误差的传播链，使重建质量不再受限于位姿精度，为"无标定实时重建"提供了全新的技术路径
2. **两层级滑动窗口架构，实现局部精度与全局一致性的统一**：SLAM3R 的 I2P 网络以滑动窗口处理局部视频片段，在窗口内通过跨帧注意力机制精确回归局部三维结构，保证了局部重建的高精度；L2W 网络则通过迭代更新机制将新到来的局部点图渐进式融合到全局坐标系，维护全局一致性。这种"局部精确 + 全局一致"的两层级设计使 SLAM3R 能够处理任意长度的视频序列而不产生漂移，在长序列重建（如 ScanNet 场景）上表现尤为突出，解决了前馈方法在长视频上全局一致性难以保证的核心挑战
3. **消费级 GPU 实现 20+ FPS 实时重建，CVPR 2025 Highlight + China3DV 年度最佳论文双重认可**：SLAM3R 在 RTX 4090D 等消费级显卡上实现了 20+ FPS 的实时密集重建，重建点云的准确度（Accuracy）和完整度（Completeness）均达到当前最先进水平，在 ScanNet 和 7-Scenes 等主流基准上超越了包括 MonST3R、DROID-SLAM 等在内的现有方法。该工作被 CVPR 2025 评为 Highlight 论文（约占所有接收论文的 10%），并在第四届中国三维视觉大会上荣获年度最佳论文（TOP1），充分体现了其在学术界的高度认可。SLAM3R 的开源代码已在 GitHub 发布，为实时三维重建领域的后续研究提供了强大的基础设施

### 2026-06-25｜CAT3D: Create Anything in 3D with Multi-View Diffusion Models（多视图扩散模型驱动的任意三维内容创建）

**CAT3D：多视图扩散模型驱动的任意三维内容创建**

**方向**：三维生成（3D Generation）/ 多视图扩散生成　**来源**：NeurIPS 2024　**机构**：Google DeepMind

- **作者**：Ruiqi Gao、Aleksander Holynski、Philipp Henzler、Arthur Brussee、Ricardo Martin-Brualla、Pratul Srinivasan、Jonathan T. Barron、Ben Poole（Google DeepMind）
- **链接**：[https://arxiv.org/abs/2405.10314](https://arxiv.org/abs/2405.10314) | 项目页：[cat3d.github.io](https://cat3d.github.io/) | NeurIPS 页面：[NeurIPS 2024](https://proceedings.neurips.cc/paper_files/paper/2024/hash/89e4433fec4b99f1d859db57af1e0a0f-Abstract-Conference.html)

![CAT3D teaser figure](https://km.sankuai.com/api/file/cdn/2756902383/243371657635?contentType=0&isNewContent=false)

**核心内容**：CAT3D 是 Google DeepMind 发表在 NeurIPS 2024 上的三维生成方法，提出通过多视图扩散模型模拟真实世界的三维捕捉过程，从而实现"Create Anything in 3D"的愿景。现有高质量三维重建需要用户采集数百至数千张图像，耗时且复杂。CAT3D 创新性地将多视图扩散模型与鲁棒三维重建相结合：给定任意数量的输入图像（甚至仅单张图像）和一组目标新视角，多视图扩散模型能够生成高度一致的新视角图像，然后将这些生成的密集新视图作为输入送入稳健的三维重建流水线，最终生成可实时渲染的三维表示（3DGS/NeRF）。整个流程可在短短一分钟内完成从单张图像到完整三维场景的创建，在单图像和稀疏视图三维场景创建任务上显著优于 Zero123、ReconFusion 等现有方法。CAT3D 的独特优势在于其高度灵活性——支持文本提示、单张图像、稀疏多视图等多种输入条件，且生成的视角数量可任意指定，密度越高重建质量越好，推理时可自由权衡速度与质量。

**亮点**：

1. **模拟现实世界捕捉流程的生成式重建范式，单张图像一分钟内创建完整三维场景**：传统三维重建需要人工拍摄大量多视角照片，而传统 Text-to-3D 方法（如 DreamFusion）依赖耗时的 Score Distillation Sampling（SDS）优化，速度慢且容易产生饱和、模糊等伪影。CAT3D 提出了一种全新的思路——无需优化，直接让多视图扩散模型模拟"摄影师围绕物体拍摄"的过程，生成任意数量、高度一致的新视角图像，再通过成熟的 3D 重建技术将其转化为三维表示。这一范式将"三维生成"与"三维重建"两个领域无缝桥接，既利用了扩散模型强大的生成能力，又借助了重建技术的几何精度，在生成质量和效率之间找到了优雅的平衡点。整个流程在 NeRF 和 3DGS 两种表示下均可工作，单场景创建仅需一分钟
2. **高度灵活的多条件输入与密度可调生成，单图/文本/多图均可用**：CAT3D 不限制输入类型——既可以从单一图像出发，也可以通过文本提示生成参考图像后扩展为三维场景，还可以直接接收多张稀疏视角图像进行补全式重建。更重要的是，用户可自由指定生成的新视角数量（从数十到数百张），生成的视角越多、覆盖越密集，最终三维重建质量越高，实现了"推理算力换重建质量"的灵活权衡。这种高度通用的输入接口使 CAT3D 在单图像三维创建、稀疏视图三维补全、文本到三维等多种任务上均展现出领先性能，显著优于 Zero123、SyncDreamer、ReconFusion 等专用方法
3. **多视角一致性的联合去噪生成，从"逐视角独立生成"到"全局一致生成"的飞跃**：早期基于扩散模型的三维生成方法（如 Zero123）对每个新视角独立生成，导致多视角之间出现明显的不一致（纹理漂移、几何冲突）。CAT3D 的多视图扩散模型通过联合去噪策略，在所有目标视角之间建立全局一致性约束，确保生成的视角集合在颜色、纹理和几何上高度统一。此外，生成的新视角不仅包括 RGB 图像，还支持深度图估计，进一步增强重建的几何约束。这一多视角一致性生成能力使 CAT3D 在生成质量上建立了新的 SOTA，尤其在需要高度几何一致的场景重建任务中优势突出

### 2026-06-26｜3D Gaussian Splatting as Markov Chain Monte Carlo（将3D高斯泼溅重构为马尔可夫链蒙特卡洛采样）

**3D Gaussian Splatting as Markov Chain Monte Carlo：将3D高斯泼溅重构为马尔可夫链蒙特卡洛采样**

**方向**：3D Gaussian Splatting（3DGS 基础理论与优化）　**来源**：NeurIPS 2024　**机构**：英属哥伦比亚大学（UBC）× Google Research × Google DeepMind × Simon Fraser University × 多伦多大学

- **作者**：Shakiba Kheradmand、Daniel Rebain、Gopal Sharma、Weiwei Sun、Yang-Che Tseng、Hossam Isack、Abhishek Kar、Andrea Tagliasacchi、Kwang Moo Yi（UBC / Google Research / Google DeepMind / Simon Fraser University / University of Toronto）
- **链接**：[https://arxiv.org/abs/2404.09591](https://arxiv.org/abs/2404.09591) | 项目页：[ubc-vision.github.io/3dgs-mcmc](https://ubc-vision.github.io/3dgs-mcmc/) | NeurIPS 页面：[NeurIPS 2024](https://proceedings.neurips.cc/paper_files/paper/2024/hash/93be245fce00a9bb2333c17ceae4b732-Abstract-Conference.html)

![3DGS-MCMC 论文主结果对比图](https://km.sankuai.com/api/file/cdn/2756902383/243564913447?contentType=0&isNewContent=false)

**核心内容**：3D Gaussian Splatting as Markov Chain Monte Carlo（3DGS-MCMC）是英属哥伦比亚大学联合 Google Research、DeepMind 等机构发表在 NeurIPS 2024 上的重要工作，从概率统计的视角重新诠释了 3DGS 的核心优化机制。现有 3DGS 方法依赖精心设计的克隆（cloning）和分裂（splitting）启发式策略来放置高斯基元，这些策略不仅导致渲染质量不稳定，还对初始化质量高度敏感。本文提出将 3D 高斯集合视为从描述场景物理表示的底层概率分布中抽取的随机样本——即马尔可夫链蒙特卡洛（MCMC）样本。在这一视角下，作者证明了 3D 高斯的参数更新可以通过引入噪声转换为随机梯度朗之万动力学（SGLD）更新。进而，原有的增密（densification）和剪枝（pruning）启发式策略被重写为 MCMC 样本的确定性状态转移，彻底移除了这些手工设计的启发式规则。具体而言，作者将高斯"克隆"操作重新设计为一种"重定位"（relocalization）方案，使其近似保持样本概率不变；同时引入正则化项促进未使用高斯的自动移除。实验表明，该方法在多个标准评估场景上提供了更优的渲染质量，能够轻松控制高斯数量，并对初始化具有更强的鲁棒性。

**亮点**：

1. **从概率统计视角重构3DGS优化框架，将启发式增密剪枝转化为MCMC状态转移**：传统3DGS的克隆、分裂、剪枝等操作是手工设计的启发式规则，缺乏理论保证，且对初始化敏感。本文首次将3D高斯视为从场景概率分布中抽取的MCMC样本，证明参数更新等价于SGLD更新，并将增密和剪枝重写为保持分布不变的确定性状态转移。这一理论重构不仅消除了对精心调参的启发式策略的依赖，还为3DGS的收敛性和稳定性提供了概率框架下的理论支撑，是从"工程经验"走向"理论根基"的关键一步
2. **重定位方案替代克隆操作，保持样本概率不变，解决分布偏移问题**：现有3DGS的克隆操作会显著改变选中高斯的空间覆盖范围，导致MCMC采样中的分布不变性被严重破坏。作者提出了一种重定位（relocalization）方案，通过将高斯参数重新分配到新的空间位置来近似保持样本概率，避免了传统克隆操作对分布的扭曲。这一设计使增密过程成为MCMC框架下的合法"跳跃移动"（jump move），确保了采样过程不会崩溃，从而在理论上保证了优化过程的稳定性
3. **正则化项促进高斯高效利用，对初始化鲁棒且渲染质量提升显著**：作者引入了一个简单的正则化项，鼓励移除未使用的高斯（低透明度或不贡献渲染），使高斯基元数量能够根据场景复杂度自适应调整。实验表明，该方法在标准Mip-NeRF 360数据集上不仅渲染质量优于原始3DGS，而且对随机初始化（Random init）同样鲁棒——原始3DGS在随机初始化下性能显著下降，而MCMC版本在各种初始化条件下均保持稳定性能。这一鲁棒性突破降低了对高质量SfM初始化的依赖，为3DGS在缺乏精确相机标定的场景中的应用打开了新可能

### 2026-06-29｜NeRF as Non-Distant Environment Emitter in Physics-based Inverse Rendering（NeRF 作为非远距离环境发射器的物理逆向渲染）

**NeRF as Non-Distant Environment Emitter in Physics-based Inverse Rendering**
**NeRF 作为非远距离环境发射器的物理逆向渲染**

**方向**：NeRF / 逆向渲染　**来源**：SIGGRAPH 2024 (ACM Transactions on Graphics)　**机构**：清华大学 × 西藏大学 × University of California, Irvine

- **作者**：Jingwang Ling、Ruihan Yu、Feng Xu†（通讯作者）、Chun Du、Shuang Zhao（清华大学 / 西藏大学 / UC Irvine）
- **链接**：[https://arxiv.org/abs/2402.04829](https://arxiv.org/abs/2402.04829) | 项目页：[nerfemitterpbir.github.io](https://nerfemitterpbir.github.io/) | 代码：[github.com/gerwang/nerf-emitter](https://github.com/gerwang/nerf-emitter)

![NeRF Emitter — Teaser](https://km.sankuai.com/api/file/cdn/2756902383/243821205235?contentType=0&isNewContent=false)

**核心内容**：物理逆向渲染旨在从捕获的二维图像中联合优化场景的几何形状、表面材质和环境光照，是实现重光照、场景编辑等应用的基础技术。在逆向渲染中，光照模型的选择至关重要——传统方法普遍采用环境贴图（Environment Map）来近似场景照明，但环境贴图基于"远距离光照"假设，即所有光源都位于无限远处，导致光照分布在空间上恒定不变。然而在真实场景中，光源往往位于有限距离内，此时远距离假设失效：物体表面不同位置接收到的光照存在显著差异（即"非远距离光照效应"），空间恒定的光照模型成为劣质近似。本文首次提出使用 NeRF 作为空间变化的环境光照模型，替代传统的环境贴图。具体而言，作者用 HDR NeRF 建模物体周围的非边界场景环境，使其能够合成三维一致的、任意空间位置的入射辐射分布；同时将目标物体表示为带材质的几何表面，构建"表面+NeRF"混合渲染方程。为将 NeRF 光照有效融入物理逆向渲染流水线，作者设计了面向 NeRF 的发射器重要性采样（Emitter Importance Sampling）技术，大幅降低蒙特卡洛渲染方差。在真实和合成数据集上的实验表明，当光源非远距离时，环境贴图会导致重光照和几何重建出现明显伪影，而 NeRF 发射器能够精准建模非远距离光照，实现高质量的逆向渲染。

**亮点**：

1. **首次将 NeRF 用作环境光照模型，突破环境贴图的远距离光照假设**：传统逆向渲染方法普遍采用环境贴图（Environment Map）近似场景照明，其"远距离光照"假设导致光照在空间上恒定不变。本文首次提出使用 HDR NeRF 建模非远距离环境光照——NeRF 作为三维辐射场天然具有空间变化能力，能够为物体表面任意着色点合成三维一致的入射辐射分布，精准捕捉光源视差效应。这一创新从根本上解决了环境贴图在非远距离光照场景下的建模缺陷，为物理逆向渲染提供了更准确的照明模型
2. **面向 NeRF 的发射器重要性采样技术，降低蒙特卡洛渲染方差**：将 NeRF 作为发光体融入物理渲染流水线的核心挑战在于：NeRF 表示的辐射场是体积型的，传统的环境贴图重要性采样方法无法直接适用。作者专门设计了面向 NeRF 的发射器重要性采样（Emitter Importance Sampling）策略——通过构建 NeRF 辐射场的重要性分布，在蒙特卡洛路径采样中优先采样高辐射区域，大幅降低渲染方差。这一技术使 NeRF 光照能够被高效地融入可微渲染管线，保证了逆向渲染中梯度计算的稳定性和效率
3. **"表面+NeRF"混合场景表示与分阶段优化策略，实现几何、材质、光照的联合重建**：作者将场景建模为混合表示——目标物体用带 BRDF 材质的显式几何表面表示，周围环境用 HDR NeRF 表示——并推导了统一二者的混合渲染方程。在优化策略上，采用分阶段方案：先训练 HDR NeRF 获取环境光照初值，再联合优化几何、材质和 NeRF 光照。实验在真实和合成非远距离光照数据集上验证，相比环境贴图方案，NeRF 发射器在重光照质量和几何重建精度上均有显著提升，尤其在光源近距离的场景中优势突出。此外作者还搭建了专用非远距离光照数据采集系统，为该方向研究提供了基准数据

### 2026-06-30｜HAMSt3R: Human-Aware Multi-view Stereo 3D Reconstruction（人体感知多视图立体三维重建）

**HAMSt3R: Human-Aware Multi-view Stereo 3D Reconstruction**
**HAMSt3R：人体感知多视图立体三维重建**

**方向**：多视图立体重建（MVS）　**来源**：ICCV 2025　**机构**：NAVER LABS Europe

- **作者**：Sara Rojas、Matthieu Armando、Bernard Ghanem、Philippe Weinzaepfel、Vincent Leroy、Grégory Rogez（NAVER LABS Europe）
- **链接**：[https://arxiv.org/abs/2508.16433](https://arxiv.org/abs/2508.16433) | 项目页：[europe.naverlabs.com/research/hamst3r/](https://europe.naverlabs.com/research/hamst3r/)

![HAMSt3R teaser](https://km.sankuai.com/api/file/cdn/2756902383/244028134799?contentType=0&isNewContent=false)

**核心内容**：从稀疏、未标定的多视图图像中恢复场景三维几何是计算机视觉的经典难题。近期基于学习的方法如 DUSt3R 和 MASt3R 通过直接预测稠密场景几何取得了令人瞩目的成果，但它们主要在静态户外场景上训练，在人体中心场景（human-centric scenarios）中表现不佳。本文提出 HAMSt3R，将 MASt3R 扩展为能够联合重建人体与场景的前馈网络。HAMSt3R 首先利用 DUNE——一个通过蒸馏 MASt3R 编码器与最先进人体网格恢复模型 multi-HMR 编码器得到的强图像编码器，以同时理解场景几何与人体结构。随后，网络引入额外的预测头：人体分割头、基于 DensePose 的稠密对应估计头，以及人体中心环境下的深度估计头。通过这些多任务头的输出，HAMSt3R 生成一个富含人体语义信息的稠密三维点图。与依赖复杂优化流水线的现有方法不同，HAMSt3R 完全前馈且高效，适用于实际应用。在 EgoHumans 和 EgoExo4D 两个人体中心基准数据集上的评估表明，HAMSt3R 能够有效重建人体，同时在传统多视图立体和多视图姿态回归任务上保持强劲性能，弥合了人体理解与场景三维重建之间的鸿沟。

**亮点**：

1. **首次将人体感知能力融入端到端多视图立体重建框架，突破 MASt3R 在动态人体场景中的局限**：DUSt3R/MASt3R 系列模型在静态场景上表现优异，但在包含人体的场景中面临严重挑战——人体姿态变化、遮挡和自遮挡导致传统多视图匹配失效，且人体与场景的尺度差异巨大。HAMSt3R 通过引入人体分割和 DensePose 稠密对应估计头，使网络能够显式感知人体存在并建立人体表面上的稠密对应关系，从而在无需任何优化后处理的情况下，直接从稀疏未标定图像中恢复带人体语义标注的稠密三维点图。这一设计将"人体理解"与"三维重建"统一在单一前馈网络中，是端到端几何基础模型向通用场景理解演进的重要一步
2. **DUNE 蒸馏编码器融合场景几何与人体结构先验，实现跨域特征统一**：HAMSt3R 的核心技术之一是 DUNE 编码器——通过知识蒸馏将 MASt3R 的几何感知编码器与 multi-HMR 的人体结构编码器融合为一个统一表征。DUNE 同时保留了场景几何理解能力和人体姿态/形状先验，使网络在处理包含人体的场景时能够自然区分人体与背景，并为后续的人体分割、DensePose 估计和深度预测提供高质量共享特征。这种"几何+人体"双先验融合策略为视觉基础模型的多任务联合训练提供了有价值的参考
3. **完全前馈的高效推理，在人体中心基准上达到 SOTA 同时保持通用场景重建能力**：与依赖复杂优化管线（如 SMPLify、PIFu 等）的传统人体重建方法不同，HAMSt3R 完全前馈，单张图像前向传播即可完成人体分割、DensePose 估计、深度预测和点图生成，推理速度远超优化类方法。实验表明，HAMSt3R 在 EgoHumans 和 EgoExo4D 两个人体中心数据集上显著超越现有方法，同时在传统多视图立体和姿态回归任务上保持了与 MASt3R 相当的性能，证明了人体感知增强不会牺牲通用场景重建能力。这一"人体感知+通用重建"的双赢特性使 HAMSt3R 在 AR/VR 人体交互、运动分析等实际应用中具有直接价值

### 2026-07-01｜Online3R: Online Learning for Consistent Sequential Reconstruction Based on Geometry Foundation Model（基于几何基础模型的序列重建在线学习）

**Online3R: Online Learning for Consistent Sequential Reconstruction Based on Geometry Foundation Model**
**Online3R：基于几何基础模型的序列重建在线学习**

**方向**：视觉几何基础模型（Visual Geometry Foundation Models）　**来源**：CVPR 2026　**机构**：北京大学（查红彬团队）

- **作者**：Shunkai Zhou、Zike Yan、Fei Xue、Dong Wu、Yuchen Deng、Hongbin Zha（北京大学）
- **链接**：[https://arxiv.org/abs/2604.09480](https://arxiv.org/abs/2604.09480) | 项目页：[shunkaizhou.github.io/online3r-1.0](https://shunkaizhou.github.io/online3r-1.0/)

![Online3R teaser](https://km.sankuai.com/api/file/cdn/2756902383/244220319391?contentType=0&isNewContent=false)

**核心内容**：近年来以 DUSt3R、MASt3R、VGGT 为代表的几何基础模型（Geometry Foundation Models）在大规模数据集预训练后展现出强大的零样本三维重建能力，但这些模型在部署时通常保持"冻结"状态——一旦遇到训练分布外的新场景，其重建结果往往存在显著的不一致性、长程漂移和累积误差。Online3R 提出了一种全新的解决方案：无需重新训练模型，而是通过在线学习（Online Learning）在测试时动态适应新场景。具体而言，Online3R 在冻结的 MASt3R 编码器上插入一组参数极少的可学习视觉提示（Visual Prompts），在序列重建过程中通过局部融合伪真值与全局参考帧不变性两个自监督约束，实时在线更新这些提示，使前馈重建网络能够"边重建边适应"新场景。实验表明，在视频序列重建中，Online3R 显著提升了相机位姿估计的精度和稠密几何的一致性，同时保持了实时处理速度，无需任何手动标注或离线训练。

**亮点**：

1. **首次为冻结几何基础模型引入在线学习机制，实现"边重建边适应"**：DUSt3R/MASt3R/VGGT 等几何基础模型依赖大规模预训练，一旦部署后参数冻结，无法适应新场景。Online3R 开创性地在测试时通过在线学习动态更新视觉提示，使模型无需重训练即可适应不同场景的几何特性，从根本上解决了"预训练分布"与"真实场景分布"不匹配导致的重建不一致问题。这一"冻结模型+在线适配"的范式为视觉几何基础模型的实际部署提供了重要路径，极大降低了在新场景下获得高质量重建的门槛
2. **参数高效的视觉提示 + 双重自监督约束，无需标注数据即可实时优化**：Online3R 仅引入少量可学习参数（视觉提示），相比全模型微调或重训练具有极高的参数效率。同时设计了两种自监督信号驱动在线更新：局部融合伪真值约束通过相邻帧的几何一致性生成伪监督信号，全局参考帧不变性约束则维护全局坐标系下关键帧的几何稳定性。两种约束均无需人工标注，完全依赖几何一致性本身，在保持实时处理速度的同时显著降低了长程漂移和累积误差
3. **基于 MASt3R 架构即插即用，保持实时速度同时显著改善位姿与几何一致性**：Online3R 以 MASt3R 为基线几何基础模型，无需改动其网络架构或权重，仅通过插入视觉提示即可适配。实验在视频序列重建基准上验证了显著的性能提升——相机位姿估计精度提高，稠密几何的一致性和完整性显著改善，同时推理速度保持实时级别。这一轻量即插即用的特性使 Online3R 能够直接集成到现有的 SLAM、SfM 或视频三维重建管线中，作为几何基础模型在序列重建场景中的增强层，为机器人导航、AR/VR 实时建图等应用提供了更鲁棒的技术基础

### 2026-07-02｜SDGS: Spatial Difference Guided Gaussian Splatting for Simultaneous Localization and 3D Reconstruction（空间差分引导高斯泼溅同步定位与三维重建）

**SDGS: Spatial Difference Guided Gaussian Splatting for Simultaneous Localization and 3D Reconstruction**
**SDGS：空间差分引导高斯泼溅同步定位与三维重建**

**方向**：SLAM / 实时三维重建　**来源**：CVPR 2026

- **作者**：Yijian Tian、Mingtao Ou、Zijian Pan、Xinglong Ji
- **链接**：[https://openaccess.thecvf.com/content/CVPR2026/html/Tian_SDGS_Spatial_Difference_Guided_Gaussian_Splatting_for_Simultaneous_Localization_and_CVPR_2026_paper.html](https://openaccess.thecvf.com/content/CVPR2026/html/Tian_SDGS_Spatial_Difference_Guided_Gaussian_Splatting_for_Simultaneous_Localization_and_CVPR_2026_paper.html)

![SDGS Poster Teaser](https://km.sankuai.com/api/file/cdn/2756902383/244412974994?contentType=0&isNewContent=false)

**核心内容**：3D Gaussian Splatting（3DGS）虽然能以显式表示实现照片级实时三维重建，但原始 3DGS 依赖离线 SfM 预先计算相机位姿，引入了"感知—重建"之间的延迟，难以应对高速运动等非理想条件。本文提出 SDGS——一种基于稀疏边缘描述子的在线 3DGS 系统，可在无位姿先验的情况下同时完成 6-DoF 相机定位和稠密三维重建。SDGS 的核心创新在于利用新型混合像素传感器（如天眸 Tianmouc）的双通道特性——高帧率空间差分（SD）边缘信号与低帧率 RGB 信号精确同步——采用"先勾轮廓再上色"的两阶段范式：前端用细长各向异性高斯表示稀疏 3D 边缘，通过距离变换（DT）将稀疏边缘变为连续势场实现敏捷鲁棒的位姿跟踪；后端在位姿稳定后促升 RGB 关键帧，通过 SD 引导的互斥监督（边缘区由 SD 约束、色彩区由 RGB 光度约束）消除运动模糊，重建清晰稠密场景。实验表明，SDGS 每次跟踪迭代仅需约 2k 高斯，在极端高速运动场景下是唯一不崩溃的方法（ATE 仅 3.91cm），同时显著优于传统纯 3DGS-SLAM 和混合框架。

**亮点**：

1. **"先勾线后上色"两阶段范式实现软硬协同，极端运动下唯一不崩的在线 GS-SLAM**：SDGS 创造性地利用混合像素传感器的互补特性——差分快通道做敏捷跟踪、RGB 慢通道做稠密上色——首次在高速/极端运动模糊场景下实现鲁棒的在线 3DGS 跟踪与重建。相比传统稠密光度跟踪对模糊敏感且计算昂贵（MonoGS 在 extreme 场景完全崩溃），SDGS 的稀疏边缘 DT 对齐策略使系统在极端速度下仍保持 3.91cm ATE 精度。这种"几何骨架先行、外观纹理后补"的设计思路为实时 SLAM 在恶劣条件下的鲁棒性提升开辟了新路径
2. **距离变换（DT）将稀疏边缘变成连续势场，破解稀疏描述子位姿优化的收敛难题**：稀疏边缘描述子天然比稠密像素高效，但直接做对应匹配极难收敛。SDGS 的关键突破在于引入距离变换——将二值稀疏边缘图转化为连续"势场"，每个渲染像素按其到最近观测边缘的欧氏距离受罚，无需显式对应即可在 SE(3) 上通过解析雅可比稳定优化位姿。这种 DT 形式使每次迭代比现有方法快约 2 倍，且对未重建区域比光度法更加鲁棒，是稀疏描述子能胜任实时位姿估计的核心原因
3. **SD 引导互斥监督消除模糊 RGB 与锐利梯度的监督歧义，可迁移性强**：低帧率 RGB 常带运动模糊，若直接用其监督稠密重建会导致边缘模糊。SDGS 提出互斥监督——用 SD 信号将像素分为互斥的两组：强梯度区由锐利的 SD 信号约束（保证结构清晰），互补区由 RGB 光度约束（传播色彩），干净地消除了"用哪个信号监督哪个像素"的歧义。这一思想可迁移至任何拥有辅助锐利信号（事件相机、闪光灯等）的去模糊重建任务中，具有较强的通用性

### 2026-07-03｜Realiz3D: 3D Generation Made Photorealistic via Domain-Aware Learning（基于领域感知学习的照片级真实三维生成）

**Realiz3D: 3D Generation Made Photorealistic via Domain-Aware Learning**
**Realiz3D：基于领域感知学习的照片级真实三维生成**

**方向**：三维生成（3D Generation）/ 可控三维生成　**来源**：CVPR 2026　**机构**：Meta AI × Technion（以色列理工学院）

- **作者**：Ido Sobol、Kihyuk Sohn、Yoav Blum、Egor Zakharov、Max Bluvstein、Andrea Vedaldi、Or Litany（Meta AI × Technion）
- **链接**：[https://arxiv.org/abs/2605.13852](https://arxiv.org/abs/2605.13852) | 项目页：[https://idosobol.github.io/realiz3d/](https://idosobol.github.io/realiz3d/) | CVF 页面：[https://openaccess.thecvf.com/content/CVPR2026/html/Sobol_Realiz3D_3D_Generation_Made_Photorealistic_via_Domain-Aware_Learning_CVPR_2026_paper.html](https://openaccess.thecvf.com/content/CVPR2026/html/Sobol_Realiz3D_3D_Generation_Made_Photorealistic_via_Domain-Aware_Learning_CVPR_2026_paper.html)

![Realiz3D teaser](https://km.sankuai.com/api/file/cdn/2756902383/244615510034?contentType=0&isNewContent=false)

**核心内容**：要让图像扩散模型支持精确的几何、材质、视角控制（如多视图生成、法向图、相机位姿等），主流做法是先在大规模真实图像上预训练，再用带 3D 标注的合成渲染图微调。然而合成渲染图与真实照片之间存在严重的域间隙（domain gap），直接在合成数据上微调会灾难性遗忘真实图像的外观，导致"可控性"与"真实感"之间出现难以摆脱的权衡。Realiz3D 识别出真实感下降的关键根因——模型在微调时把"控制信号的存在"与"合成外观"绑定在一起，即**控制信号泄漏了域身份**（domain leakage）。为解决这一问题，Realiz3D 提出了一套轻量的领域感知学习框架：首先通过**Domain Shifter**（低秩残差适配器）把"域身份（真实/合成）"从"3D 控制信号"里解耦出来，使域概念被独立于控制学到；然后在微调阶段通过**层级感知训练**（Layer-Aware Training）和**域重指派**（Domain Reassignment）把只在合成数据上学到的控制力迁移到真实域。实验表明，Realiz3D 在多视图纹理生成和文本到多视图生成任务上同时实现了强 3D 一致性与显著更高的真实感——FID_I 从纯合成基线的 218.29 降至 200.24，KID_I 从 0.0431 降至 0.0291，同时 PSNR 仅小幅下降。

**亮点**：

1. **把"真实感丢失"重新诊断为"控制信号泄漏域身份"，从根源上解耦域与控制**：传统方法将真实感下降归因于合成数据本身质量差，但 Realiz3D 指出问题的本质在于模型隐式学到了"一旦给控制信号，就该画成合成样子"的关联。通过引入轻量 Domain Shifter（低秩残差适配器），将域身份（real/synthetic）作为独立协变量编码，阻断控制信号与合成外观的纠缠，为"可控三维生成保真实感"提供了全新的诊断视角和解决范式
2. **两阶段解耦训练 + 层级感知域迁移，仅用标准扩散损失即可实现真实感与可控性兼得**：Stage 1 独立训练 Domain Shifter 学习域身份（控制置空），Stage 2 冻结 Domain Shifter 微调骨干学习控制。同时利用扩散模型"早层域无关管结构、深层域相关管外观"的层级分工，通过 Layer-Aware Training（真实样本只更新深层）和 Domain Reassignment（把真实样本早层重指派为合成模式）将控制力从合成域迁移到真实域。整个框架仅使用标准扩散去噪损失，无需额外对齐或判别损失，轻量且易于部署
3. **推理时静态域重指派自由平衡真实感与可控性，无需额外训练**：Realiz3D 在推理阶段支持将预先选定的早期扩散块和早期 timestep 设为合成模式（增强控制），深层和晚期 timestep 保持真实模式（保真实感）。这种混合配置只需全局调一次，即可在测试时自由重新平衡真实感与可控性，无需针对每个样本重新训练或优化。作为即插即用的增强模块，Realiz3D 在 5 个 text-to-3D 和 2 个 image-to-3D baseline 上均稳定涨点，展示了极强的通用性和实用价值

### 2026-07-06｜Neural Gabor Splatting: Enhanced Gaussian Splatting with Neural Gabor for High-frequency Surface Reconstruction（神经 Gabor 泼溅：增强高频表面重建的高斯泼溅）

**Neural Gabor Splatting: Enhanced Gaussian Splatting with Neural Gabor for High-frequency Surface Reconstruction**
**神经 Gabor 泼溅：增强高频表面重建的高斯泼溅**

**方向**：3DGS 渲染加速与结构优化　**来源**：CVPR 2026　**机构**：The University of Tokyo（东京大学）

- **作者**：Haato Watanabe、Nobuyuki Umetani（The University of Tokyo）
- **链接**：[https://arxiv.org/abs/2604.15941](https://arxiv.org/abs/2604.15941)

![Neural Gabor Splatting 论文主图](https://km.sankuai.com/api/file/cdn/2756902383/244882532034?contentType=0&isNewContent=false)

**核心内容**：3D Gaussian Splatting（3DGS）以显式高斯基元表示实现了快速训练和实时渲染，但存在一个关键缺陷：每个高斯基元只能表示单一颜色，当场景包含高频外观细节（如棋盘格纹理、锐利色彩边界等）时，需要大量基元来逼近每一次颜色跳变，导致基元数量急剧膨胀。本文提出 Neural Gabor Splatting，在每个高斯基元上附加一个轻量多层感知机（MLP），使单个基元即可建模丰富的色彩变化，从根本上减少高频表面所需的基元数量。此外，作者引入频率感知稠密化策略（Frequency-Aware Densification），基于频率能量选择性地对不匹配基元进行剪枝和克隆，精准控制基元增长。该方法在 Mip-NeRF360 标准基准和高频数据集（如棋盘格图案）上均实现了精确的高频表面重建，并通过充分的消融实验验证了各模块的有效性。

**亮点**：

1. **轻量 MLP 赋予单个高斯基元丰富的色彩表达能力，突破"一基元一颜色"瓶颈**：传统 3DGS 中每个高斯基元仅能表示单一颜色，高频纹理区域需要成倍增加基元来逼近颜色跳变。Neural Gabor Splatting 在每个基元上附加轻量 MLP，使单个基元即可在空间上建模连续的颜色变化，大幅减少了高频场景所需的基元数量，从根源上缓解了基元膨胀问题
2. **频率感知稠密化策略精准控制基元增长，选择性剪枝与克隆提升效率**：不同于传统 3DGS 基于梯度阈值的均匀稠密化，本文提出基于频率能量的选择性策略——对高频区域的基元进行克隆以增强细节，对低频冗余基元进行剪枝以控制数量。这种频率引导的精细化策略使基元分配更加合理，在保证高频细节重建质量的同时有效控制了模型规模
3. **在高频纹理场景（棋盘格等）上显著优于标准 3DGS，验证了方法在极端高频条件下的有效性**：标准 3DGS 在棋盘格等强高频纹理场景中基元数量爆炸且重建质量下降，而 Neural Gabor Splatting 在 Mip-NeRF360 和专门设计的高频数据集上均实现了精确重建，充分证明了 Gabor 增强表示在处理高频外观细节方面的优越性和实用价值

### 2026-07-07｜MonoMVSNet: Monocular Priors Guided Multi-View Stereo Network（单目先验引导的多视图立体网络）

**MonoMVSNet: Monocular Priors Guided Multi-View Stereo Network**
**MonoMVSNet：单目先验引导的多视图立体网络**

**方向**：多视图立体重建（MVS）　**来源**：ICCV 2025

- **作者**：Jianfei Jiang, Qiankun Liu, Haochen Yu, Hongyuan Liu, Liyong Wang, Jiansheng Chen, Huimin Ma
- **链接**：[https://arxiv.org/abs/2507.11333](https://arxiv.org/abs/2507.11333) | 代码：[github.com/JianfeiJ/MonoMVSNet](https://github.com/JianfeiJ/MonoMVSNet)

![MonoMVSNet qualitative comparison](https://km.sankuai.com/api/file/cdn/2756902383/245139934431?contentType=0&isNewContent=false)

**核心内容**：基于学习的多视图立体（MVS）方法旨在通过已标定多视图图像恢复稠密点云，但现有方法在无纹理区域、反光表面等特征匹配失效的困难区域表现不佳。相比之下，单目深度估计本质上不需要特征匹配，能够在这些区域实现鲁棒的相对深度估计。MonoMVSNet 首次将单目基础模型（monocular foundation model）的强大先验系统性地融入多视图几何框架：首先，通过注意力机制与新设计的跨视图位置编码（cross-view position encoding），将参考视图的单目特征集成到源视图特征中，实现单目语义与多视图几何的深度协同；其次，将参考视图的单目深度进行对齐，在采样过程中动态更新边缘区域的深度候选值，提升边界区域深度估计精度；最后，基于单目深度设计了相对一致性损失（relative consistency loss），监督深度预测的整体一致性。MonoMVSNet 在 DTU 和 Tanks-and-Temples 数据集上均达到 SOTA，并在 Tanks-and-Temples 中级（Intermediate）和高级（Advanced）基准上双双排名第一，代码已开源。

**亮点**：

1. **首次将单目基础模型先验系统融入多视图几何，通过跨视图位置编码实现单目特征与多视图特征的深度协同，在弱纹理/反光区域显著突破传统 MVS 瓶颈**：传统 MVS 方法严重依赖跨视图光度一致性，在无纹理、反光、半透明等特征匹配失效区域束手无策。MonoMVSNet 开创性地引入单目基础模型（如 Depth Anything）的稠密特征与深度先验，通过跨视图位置编码将参考视图的单目特征注入到所有源视图的特征表示中，使网络在特征匹配困难区域仍能利用单目先验进行鲁棒的深度推断。这一"单目先验+多视图几何"的融合范式，为 MVS 在真实复杂场景中的鲁棒性提升提供了全新思路
2. **单目深度引导的动态采样策略，在边缘区域自适应更新深度候选，显著提升深度图边界质量**：传统 MVS 在深度采样阶段对所有区域采用固定深度假设，导致物体边缘处深度估计模糊。MonoMVSNet 利用单目深度先验为边缘区域动态调整深度候选范围，使边缘像素的深度采样更加聚焦于真实深度附近，显著改善了物体轮廓和深度不连续区域的重建精度。这一动态采样策略具有良好的通用性，可迁移到任何基于代价体的 MVS 框架中
3. **Tanks-and-Temples 中级/高级基准双第一，兼顾传统室内 MVS 基准 SOTA，验证方法的通用性与领先性**：MonoMVSNet 在 Tanks-and-Temples 这一最具挑战性的室外大规模场景 MVS 基准上，同时取得 Intermediate 和 Advanced 两个子集的第一名，F-score 大幅超越现有方法；同时在经典室内 MVS 基准 DTU 上也达到 SOTA 性能。这种"室内+室外"、"中级+高级"全面领先的实验结果，充分证明了单目先验引导的 MVS 策略不仅能在困难区域发挥作用，在常规场景下同样优于传统纯多视图方法，具有广泛的适用性和实用价值

### 2026-07-08｜LGM: Large Multi-View Gaussian Model for High-Resolution 3D Content Creation（大型多视角高斯模型：高分辨率三维内容创作）

**LGM: Large Multi-View Gaussian Model for High-Resolution 3D Content Creation**
**LGM：大型多视角高斯模型——高分辨率三维内容创作**

**方向**：三维生成（3D Generation）　**来源**：ECCV 2024 Oral

- **作者**：Jiaxiang Tang, Zhaoxi Chen, Xiaokang Chen, Tengfei Wang, Gang Zeng, Ziwei Liu
- **链接**：[https://arxiv.org/abs/2402.05054](https://arxiv.org/abs/2402.05054) | 项目页：[me.kiui.moe/lgm/](https://me.kiui.moe/lgm/) | 代码：[github.com/3DTopia/LGM](https://github.com/3DTopia/LGM)

![LGM method overview](https://km.sankuai.com/api/file/cdn/2756902383/245364596612?contentType=0&isNewContent=false)

**核心内容**：3D 内容创作品质与速度均取得显著进步，但当前前馈模型虽可在数秒内生成 3D 物体，其分辨率受限于训练期间的密集计算需求。LGM 提出了一种全新框架，可从文本提示或单视角图像生成高分辨率 3D 模型，其核心思路有两点：一是 3D 表示——以多视角高斯特征（multi-view Gaussian features）作为高效且强大的中间表示，可融合后进行可微分渲染；二是 3D 骨干网络——设计非对称 U-Net 作为高吞吐量骨干，处理由多视角扩散模型从文本或单图生成的多视角图像。LGM 在保持 5 秒内生成 3D 物体速度的同时，将训练分辨率提升至 512，实现了高分辨率 3D 内容生成。实验充分验证了该方法的高保真度与高效率，在 GSO 和 Objaverse 数据集上的生成质量显著优于同期前馈方法，且代码完全开源。

**亮点**：

1. **多视角高斯特征作为高效 3D 表示，取代 NeRF/Triplane 实现高分辨率可微分渲染**：以往前馈 3D 生成方法普遍采用 Triplane-NeRF 作为 3D 表示，其渲染速度慢且显存开销大，训练分辨率被限制在 128-256。LGM 创新性地以多视角高斯特征为中间表示——每个视角生成一组带位置的 3D 高斯基元，多视角高斯融合后直接进行可微分光栅化渲染。3DGS 的显存效率远高于 NeRF 体渲染，使训练分辨率一举提升至 512，生成的 3D 资产细节大幅提升。这一设计也使推理阶段无需任何优化即可在 5 秒内输出可交互的高分辨率 3D 模型
2. **非对称 U-Net 骨干网络实现高吞吐量多视角处理**：传统 LRM 方法使用 Transformer 处理多视角图像，显存消耗随视角数二次增长。LGM 提出以非对称 U-Net 替代 Transformer 作为 3D 骨干——U-Net 的卷积特性使其在处理高分辨率多视角图像时显存占用更低且吞吐量更高，非对称设计（编码器处理高分辨率、解码器逐步恢复）进一步优化了效率。配合精心设计的数据增强策略（随机背景、随机视角扰动）弥合训练数据与推理时多视角扩散模型输出的域差异，使模型在实际使用中表现鲁棒
3. **5 秒内从文本/单图生成 512 分辨率 3D 资产，速度与质量同时领先**：LGM 在当时实现了速度与分辨率的双重突破——前馈生成仅 5 秒（不含多视角扩散），输出分辨率达 512×512，生成的 3D 高斯数量达 65536，可直接导出为网格。在 GSO 数据集上的定量评估中，LGM 在 PSNR、SSIM、LPIPS 指标上均优于 ImageDream、Wonder3D 等同期方法。该工作确立了"多视角扩散 + 前馈高斯重建"这一两阶段范式的有效性，后续大量工作（如 Turbo3D、TRELLIS 等）沿此范式继续发展，对 3D 生成领域产生了深远影响

### 2026-07-09｜GaussianShader: 3D Gaussian Splatting with Shading Functions for Reflective Surfaces（面向反射表面的着色函数增强三维高斯泼溅）

**GaussianShader: 3D Gaussian Splatting with Shading Functions for Reflective Surfaces**
**GaussianShader：面向反射表面的着色函数增强三维高斯泼溅**

**方向**：NeRF / 逆向渲染（3DGS 反射表面渲染）　**来源**：CVPR 2024

- **作者**：Yingwenqi Jiang, Jiadong Tu, Yuan Liu, Xifeng Gao, Xiaoxiao Long, Wenping Wang, Yuexin Ma
- **链接**：[https://arxiv.org/abs/2311.17977](https://arxiv.org/abs/2311.17977) | 项目页：[asparagus15.github.io/GaussianShader](https://asparagus15.github.io/GaussianShader.github.io/) | 代码：[github.com/Asparagus15/GaussianShader](https://github.com/Asparagus15/GaussianShader)

![GaussianShader teaser](https://km.sankuai.com/api/file/cdn/2756902383/245577292063?contentType=0&isNewContent=false)

**核心内容**：3D Gaussian Splatting（3DGS）以其显式、离散的高斯表示实现了高质量实时渲染，但在包含反射表面的场景中表现不佳——这是因为原始 3DGS 仅使用球谐函数（SH）建模视角相关外观，无法正确表达镜面反射等复杂光照效应。GaussianShader 提出在每个 3D 高斯基元上附加一个简化的着色函数（shading function），使其能够建模反射表面的渲染物理过程，同时保持 3DGS 的训练与渲染效率。该方法的核心挑战在于离散高斯椭球体上法线的准确估计——作者提出基于高斯最短轴方向（shortest axis）的法线估计框架，配合精心设计的一致性损失函数，使法线方向与高斯椭球的几何形状保持一致。在镜面反射物体数据集上，GaussianShader 的 PSNR 超越原始 3DGS 1.57 dB，与处理反射表面的先前方法（如 Ref-NeRF）相比，优化时间从 23 小时缩短至 0.58 小时，实现了效率与质量的双重提升。

**亮点**：

1. **首次将着色函数嵌入 3D 高斯基元，突破 3DGS 在反射表面场景中的渲染瓶颈**：原始 3DGS 依赖球谐函数建模视角相关颜色，无法表达镜面反射、金属光泽等复杂光照效应，在包含玻璃、金属、镜面等反射物体的场景中出现严重伪影。GaussianShader 创新性地为每个高斯基元引入简化的可微分着色函数，将入射光、表面法线和视角方向纳入物理着色模型，使 3DGS 具备了物理一致的反射渲染能力。这一设计仅需极少的额外计算开销，保持了 3DGS 实时渲染的核心优势
2. **基于最短轴方向的法线估计框架，解决离散高斯椭球法线估计难题**：在离散 3D 高斯上准确估计表面法线是将着色函数引入 3DGS 的核心挑战。GaussianShader 提出利用高斯椭球的最短轴方向作为法线先验——最短轴对应高斯分布衰减最快的方向，在几何上最接近表面切平面的法线方向。配合设计的一致性损失函数，约束法线方向与高斯椭球几何形状保持一致，避免了法线估计的随机性。这一框架简洁有效，为后续 3DGS 逆向渲染工作（如 SVG-IR、GS-IR 等）提供了重要的法线估计基础
3. **效率与质量的双重突破，优化速度较 Ref-NeRF 加速 40 倍**：GaussianShader 在镜面反射物体基准上 PSNR 超 3DGS 1.57 dB，视觉质量显著改善——镜面反射、高光、金属光泽等效果得到准确再现。与当时处理反射表面的代表性方法 Ref-NeRF 相比，优化时间从 23 小时缩短至仅 0.58 小时（加速约 40 倍），同时保持实时渲染速度。这一效率优势使高质量反射表面渲染从离线走向近实时应用，为 3DGS 在复杂材质场景重建中的实际部署奠定了基础

### 2026-07-10｜SceneSplat: Gaussian Splatting-based Scene Understanding with Vision-Language Pretraining（基于高斯泼溅的视觉语言预训练场景理解）

**SceneSplat: Gaussian Splatting-based Scene Understanding with Vision-Language Pretraining**
**SceneSplat：基于高斯泼溅的视觉语言预训练场景理解**

**方向**：3DGS 场景理解与语义编码　**来源**：ICCV 2025 Oral

- **作者**：Yue Li, Qi Ma, Runyi Yang, Huapeng Li, Mengjiao Ma, Bin Ren, Nikola Popovic, Nicu Sebe, Ender Konukoglu, Theo Gevers, Luc Van Gool, Martin R. Oswald, Danda Pani Paudel（ETH Zürich & University of Amsterdam & University of Trento）
- **链接**：[https://arxiv.org/abs/2503.18052](https://arxiv.org/abs/2503.18052) | 项目页：[unique1i.github.io/SceneSplat_webpage](https://unique1i.github.io/SceneSplat_webpage/) | 代码：[github.com/unique1i/SceneSplat](https://github.com/unique1i/SceneSplat)

![SceneSplat 框架概览图](https://km.sankuai.com/api/file/cdn/2756902383/245772476744?contentType=0&isNewContent=false)

**核心内容**：识别任意或未见过的物体类别是全面实现真实世界三维场景理解的关键能力。然而，现有所有三维语义理解方法在训练或推理时都依赖于二维或文本模态，尚未出现能够仅从三维数据端到端学习语义的模型，也缺乏支撑此类模型训练的大规模数据集。SceneSplat 针对这一空白，提出了首个原生操作于 3D Gaussian Splatting 的大规模室内场景理解框架。该方法的核心包含两大创新：一是视觉语言预训练方案——将 2D 视觉语言模型的知识蒸馏到 3DGS 编码器中，使其在单次前向传播中即可为百万级三维高斯基元预测开放词汇语言特征，无需在推理时依赖任何 2D 或文本输入；二是自监督学习方案——利用未标注场景中的几何一致性，通过自监督方式解锁从无标签场景中学习丰富三维特征的能力。为支撑训练与评估，作者构建了 SceneSplat-7K 数据集——首个大规模 3DGS 室内场景数据集，包含从 ScanNet、Matterport3D 等 7 个已有数据集衍生的 7916 个场景，生成过程消耗约 150 个 L4 GPU 日。在 SceneSplat-7K 上的全面实验验证了所提方法相比现有基线的显著优势，为 3DGS 原生场景理解建立了标准化基准。

**亮点**：

1. **首个原生操作于 3DGS 的大规模场景理解框架，实现纯三维端到端语义推理**：现有 3DGS 语义理解方法无一例外需要在训练或推理时依赖 2D 图像或文本模态作为桥梁，存在明显的模态依赖瓶颈。SceneSplat 首次构建了直接以 3DGS 为输入的通用场景编码器，通过视觉语言预训练将 2D 语义知识蒸馏到 3DGS 原生表示中，推理阶段仅需 3DGS 数据即可完成开放词汇语义分割等任务，彻底消除了对 2D 推理的依赖，是迈向"三维原生语义理解"的重要突破
2. **自监督学习解锁无标签场景的三维特征学习**：SceneSplat 提出自监督学习方案，利用未标注场景中固有的几何一致性信号，通过设计的自监督代理任务学习丰富的三维特征表示。这一方案突破了三维语义理解领域对大规模标注数据的强依赖——在无需任何语义标签的情况下即可学习到具有判别力的三维特征，大幅降低了数据准备成本，为三维场景理解的规模化部署提供了新路径
3. **构建 SceneSplat-7K 数据集，建立 3DGS 场景理解标准化基准**：作者构建了首个大规模 3DGS 室内场景数据集 SceneSplat-7K，涵盖 ScanNet、Matterport3D、ARKitScenes 等 7 个来源共 7916 个场景，生成过程消耗约 150 个 L4 GPU 日。该数据集填补了 3DGS 场景理解领域缺乏标准化评测基准的空白，为后续研究提供了统一的训练与评估平台，获 ICCV 2025 Oral 认可

### 2026-07-13｜SplaTAM: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM（基于三维高斯泼溅的稠密 RGB-D SLAM 跟踪与建图）

**SplaTAM: Splat, Track & Map 3D Gaussians for Dense RGB-D SLAM**
**SplaTAM：基于三维高斯泼溅的稠密 RGB-D SLAM 跟踪与建图**

**方向**：SLAM / 实时三维重建　**来源**：CVPR 2024　**机构**：Carnegie Mellon University（CMU）等

- **作者**：Nikhil Keetha, Jay Karhade, Krishna Murthy Jatavallabhula, Gengshan Yang, Sebastian Scherer, Deva Ramanan, Jonathon Luiten
- **链接**：[https://arxiv.org/abs/2312.02126](https://arxiv.org/abs/2312.02126) | 项目页：[spla-tam.github.io](https://spla-tam.github.io/)

![SplaTAM 论文主图](https://km.sankuai.com/api/file/cdn/2756902383/246055680453?contentType=0&isNewContent=false)

**核心内容**：稠密同步定位与建图（SLAM）是机器人与增强现实应用的核心技术。然而，现有方法常受限于场景的非体积化或隐式表示方式。本文首次提出 SplaTAM，将显式体积化表示——3D 高斯泼溅（3D Gaussian Splatting）引入 SLAM，实现从未标定的单个 RGB-D 相机进行高保真重建，性能超越现有方法。SplaTAM 采用专为高斯表示量身定制的简单在线跟踪与建图系统，利用轮廓掩码（silhouette mask）优雅地捕捉场景密度。这一组合带来了诸多优势：快速渲染与稠密优化、快速判断区域是否已建图、以及通过添加更多高斯实现结构化地图扩展。大量实验表明，SplaTAM 在相机位姿估计、地图构建和新视角合成方面达到现有方法约 2 倍的性能提升，为更沉浸式的高保真 SLAM 应用铺平了道路。

**亮点**：

1. **首次将 3D Gaussian Splatting 引入 SLAM，开创高斯泼溅实时建图新范式**：SplaTAM 是首个利用 3D 高斯泼溅作为显式场景表示的 SLAM 系统，打破了传统 SLAM 依赖点云、 surfel 或隐式场表示的范式。通过将高斯椭球作为基本地图元素，SplaTAM 同时获得了显式表示的可解释性和体积化表示的渲染能力，为后续大量 3DGS-SLAM 工作（如 MonoGS、Gaussian-SLAM 等）奠定了重要基础
2. **轮廓掩码优雅捕捉场景密度，实现快速渲染、稠密优化与结构化地图扩展**：SplaTAM 利用 silhouette mask 判断场景空间中高斯基元的存在性，使系统能够以极快的速度完成渲染和优化循环。同时，基于高斯表示的在线稠密化策略允许系统以结构化方式扩展地图——只需在未观测区域添加新的高斯基元，而不需要全局重新优化。这种"增量式高斯扩展"机制使 SplaTAM 能够高效处理大规模场景的在线建图
3. **相机位姿估计、地图构建与新视角合成性能均达 2 倍 SOTA 提升，效率与质量兼得**：在 Replica 等标准 SLAM 基准上，SplaTAM 在相机轨迹精度（ATE）、地图重建质量（Accuracy / Completeness）和新视角合成（PSNR）三个核心指标上均达到或超越此前最优方法约 2 倍的性能。更重要的是，3DGS 的光栅化渲染速度使 SplaTAM 在消费级 GPU 上实现了实时跟踪与建图，为机器人导航、AR/VR 等延迟敏感应用提供了实用化的稠密 SLAM 解决方案

### 2026-07-14｜DUSt3R: Geometric 3D Vision Made Easy（让几何三维视觉变得简单）

**DUSt3R: Geometric 3D Vision Made Easy**
**DUSt3R：让几何三维视觉变得简单**

**方向**：视觉几何基础模型（Visual Geometry Foundation Models）　**来源**：CVPR 2024　**机构**：NAVER LABS Europe

- **作者**：Shuzhe Wang, Vincent Leroy, Yohann Cabon, Boris Chidlovskii, Jérôme Revaud（NAVER LABS Europe）
- **链接**：[https://arxiv.org/abs/2312.14132](https://arxiv.org/abs/2312.14132) | 项目页：[europe.naverlabs.com/research/publications/dust3r](https://europe.naverlabs.com/research/publications/dust3r-geometric-3d-vision-made-easy/) | CVF 页面：[CVPR 2024](https://openaccess.thecvf.com/content/CVPR2024/html/Wang_DUSt3R_Geometric_3D_Vision_Made_Easy_CVPR_2024_paper.html)

![DUSt3R teaser: 从无标定图像集合进行密集三维重建](https://km.sankuai.com/api/file/cdn/2756902383/246299993267?contentType=0&isNewContent=false)

**核心内容**：DUSt3R 提出了一种全新的端到端几何三维视觉范式，无需任何相机标定或视点姿态先验信息，即可对任意图像集合进行密集、无约束的立体三维重建。该方法将成对重建问题转化为点图（pointmap）回归，放宽了传统透视相机模型的硬约束，统一了单目和双目重建场景。对于多于两张图像的情况，提出简单但有效的全局对齐策略，将所有成对点图表达在统一参考框架中。基于标准 Transformer 编码器-解码器架构，利用强大的预训练视觉模型。方法直接提供场景的 3D 模型和深度信息，并能从中无缝恢复像素匹配、焦距、相对和绝对相机参数。在单目和多视图深度估计以及相对姿态估计等方面的广泛实验展示了 DUSt3R 如何有效地统一各种 3D 视觉任务，创造新的性能记录。

**亮点**：

1. **颠覆性端到端范式：首次以单一前馈网络统一处理无标定、无位姿图像集合的三维重建**：DUSt3R 将成对重建问题转化为点图回归，彻底消除了传统 SfM/MVS 繁琐的相机标定、特征匹配、Bundle Adjustment 等流程，开创了几何三维视觉的全新范式。网络无需任何关于相机校准或视点姿态的先验信息，即可处理任意图像集合，大幅降低了三维重建的使用门槛
2. **点图回归统一单目与双目重建，全局对齐策略保障多视图一致性**：传统三维重建中，单目与双目重建被划分为两个独立问题，分别需要不同的相机模型假设和优化流程。DUSt3R 将成对图像重建视为点图回归，放宽了传统投影相机模型的硬约束，统一了单目和双目重建场景。在提供多于两张图像时，通过简单有效的全局对齐策略将所有成对点图表达在共同参考框架中，使网络输出具有全局一致性，且对齐过程计算开销极低
3. **多任务通用性与强大下游影响：在深度估计、姿态估计、相机标定等任务上全面刷新 SOTA**：DUSt3R 在单目深度估计、多视图深度估计、相对姿态估计、相机内参估计等任务上均刷新性能记录，并且能从中无缝恢复像素匹配、焦距、相对和绝对相机参数。DUSt3R 开创的视觉几何基础模型范式直接催生了 MASt3R、Fast3R、MUSt3R、CUT3R 等大量后续工作，为三维视觉领域从"专用模型"走向"通用基础模型"奠定了重要基石，具有深远的学术与工程影响

### 2026-07-15｜2D Gaussian Splatting for Geometrically Accurate Radiance Fields（2D 高斯泼溅：面向几何精确的辐射场）

**2D Gaussian Splatting for Geometrically Accurate Radiance Fields**
**2D 高斯泼溅：面向几何精确的辐射场**

**方向**：3D Gaussian Splatting 表面重建　**来源**：SIGGRAPH 2024（ACM Transactions on Graphics, Vol. 43, No. 4）　**机构**：香港中文大学 × 图宾根大学 × 上海科技大学

- **作者**：Binbin Huang, Zehao Yu, Angela Dai, Xiaojuan Qi, Andreas Geiger, Shenghua Gao
- **链接**：[https://arxiv.org/abs/2403.17888](https://arxiv.org/abs/2403.17888) | 项目页：[surh.github.io/2DGS](https://surh.github.io/2DGS/) | 代码：[github.com/hbb1/2d-gaussian-splatting](https://github.com/hbb1/2d-gaussian-splatting)

![2D Gaussian Splatting teaser: 几何精确的辐射场与表面重建](https://km.sankuai.com/api/file/cdn/2756902383/246496585427?contentType=0&isNewContent=false)

**核心内容**：3D Gaussian Splatting（3DGS）虽然在新视角合成方面取得了突破性进展，但由于使用 3D 高斯椭球体作为场景表示，在表面重建方面存在根本性局限——3D 高斯沿射线方向的体积积分使得几何形状模糊，难以精确恢复场景表面。本文提出 2D Gaussian Splatting（2DGS），将 3D 高斯折叠（collapse）为 2D 定向圆盘（oriented disks），从根本上消除了沿射线方向的模糊，使每个高斯基元精确贴合场景表面。在渲染方面，2DGS 利用基于射线-面片交集的精确光栅化方法，将 2D 高斯投影到图像平面并沿射线进行面积积分，实现高质量的 alpha 混合。为解决高斯表示在表面重建中固有的精度问题，作者引入两个关键正则化项：深度畸变损失（depth distortion loss）通过惩罚光线穿过高斯前后距离的差异，使高斯紧密集中在表面附近；法线一致性损失（normal consistency loss）强制相邻高斯基元的法线方向一致，确保表面平滑连续。在 DTU 和 Tanks & Temples 数据集上的实验表明，2DGS 同时实现了 SOTA 级别的新视角合成质量和表面重建精度，在 Chamfer 距离和 F-score 等几何指标上大幅超越 3DGS，并媲美甚至超越专门设计的神经隐式表面重建方法（如 NeuS、VolSDF），同时保持了 3DGS 的高效训练和实时渲染优势。

**亮点**：

1. **将 3D 高斯折叠为 2D 定向圆盘，从表示层面消除表面重建的根本性模糊**：3DGS 的核心局限在于 3D 高斯椭球沿射线方向存在体积扩展，导致表面位置无法精确确定。2DGS 创造性地将 3D 高斯折叠为 2D 定向圆盘，从根本上消除了沿射线方向的模糊，使每个高斯基元精确贴合场景表面。这一表示层面的变革使得 2DGS 能够直接从高斯场中提取高质量网格，无需额外的隐式表面转换，大幅简化了表面重建流程
2. **深度畸变与法线一致性双正则化，弥合辐射场渲染与几何重建的鸿沟**：2DGS 引入两个关键正则化项——深度畸变损失迫使光线穿过的高斯在深度上集中分布，消除表面附近的"厚度"模糊；法线一致性损失强制相邻高斯基元的法线方向一致，确保重建表面的平滑性和连续性。这两个正则化项巧妙地将渲染优化目标与几何约束对齐，使模型在追求视觉质量的同时自然产生几何精确的表面表示，解决了辐射场方法"渲染好但几何差"的长期痛点
3. **同时实现 SOTA 渲染与表面重建，超越神经隐式方法且保持高效优势**：在 DTU 和 Tanks & Temples 基准上，2DGS 在新视角合成（PSNR/SSIM/LPIPS）和表面重建（Chamfer 距离/F-score）两方面均达到 SOTA 水平，几何精度大幅超越 3DGS 并媲美甚至超越 NeuS、VolSDF 等专门设计的神经隐式表面重建方法，同时保持了 3DGS 的高效训练和实时渲染优势。2DGS 开创的"2D 高斯表面重建"范式直接催生了 GOF、SuGaR、PGSR 等大量后续工作，成为 3DGS 表面重建领域的奠基性方法

### 2026-07-16｜DreamGaussian: Generative Gaussian Splatting for Efficient 3D Content Creation（生成式高斯泼溅：高效三维内容创作）

**DreamGaussian: Generative Gaussian Splatting for Efficient 3D Content Creation**
**DreamGaussian：生成式高斯泼溅：高效三维内容创作**

**方向**：三维生成（3D Generation）　**来源**：ICLR 2024（Oral）　**机构**：北京大学 × 南洋理工大学 S-Lab × 百度

- **作者**：Jiaxiang Tang, Jiawei Ren, Hang Zhou, Ziwei Liu, Gang Zeng
- **链接**：[https://arxiv.org/abs/2309.16653](https://arxiv.org/abs/2309.16653) | 项目页：[dreamgaussian.github.io](https://dreamgaussian.github.io/) | 代码：[github.com/dreamgaussian/dreamgaussian](https://github.com/dreamgaussian/dreamgaussian)

![DreamGaussian teaser: 生成式高斯泼溅高效三维内容生成](https://km.sankuai.com/api/file/cdn/2756902383/246691120234?contentType=0&isNewContent=false)

**核心内容**：3D 内容生成领域近年来取得了显著进展，但大多数方法基于优化策略（如 Score Distillation Sampling, SDS），每样本优化耗时数十分钟甚至数小时，严重限制了实际应用。DreamGaussian 提出了一种全新的生成式高斯泼溅框架，将 3D Gaussian Splatting 与 SDS 相结合，实现了高效且高质量的 3D 内容生成。其核心设计是将 3D 高斯作为生成表示，通过逐步稠密化（progressive densification）而非 NeRF 中的占用剪枝（occupancy pruning）来加速收敛——实验表明 3DGS 的逐步稠密化在生成任务中收敛速度显著更快。为了进一步提升纹理质量并支持下游应用，作者设计了高效的网格提取与纹理精化算法，将 3D 高斯转换为带纹理的网格，并在 UV 空间中进行精化微调。实验证明，DreamGaussian 仅需约 2 分钟即可从单张图像生成高质量纹理网格，相比现有方法加速约 10 倍。

**亮点**：

1. **首次将 3D Gaussian Splatting 引入 3D 生成领域，实现 10 倍级加速**：DreamGaussian 是首个将 3DGS 作为生成表示的 3D 内容生成框架，通过 3D 高斯逐步稠密化替代 NeRF 的占用剪枝，在生成任务中收敛速度显著提升。相比基于 NeRF 的 SDS 方法（如 DreamFusion），DreamGaussian 将单图像到 3D 的生成时间从数小时压缩至约 2 分钟，加速约 10 倍，同时保持竞争性生成质量，为 3D 内容生成的实用化奠定了重要基础
2. **生成式高斯表示与网格提取精化流水线，兼顾效率与下游可用性**：DreamGaussian 不仅是"快速生成"，更提供了完整的 3D 资产生产流水线——从生成式 3D 高斯表示到带纹理网格的转换与 UV 空间精化。相比 NeRF 隐式表示难以直接导出，3DGS 的显式表示天然支持高效的网格提取，配合 UV 空间纹理精化算法，生成的 3D 资产可直接用于游戏、AR/VR 等下游应用，解决了"生成快但不可用"的痛点
3. **ICLR 2024 Oral 认可，开创 3DGS 生成范式并催生大量后续工作**：DreamGaussian 获得 ICLR 2024 Oral 认可，是 3D 生成领域的重要里程碑。其开创的"生成式高斯泼溅"范式直接启发了后续大量工作（如 GaussianDreamer、LGM、TRELLIS、Turbo3D 等），将 3DGS 从静态场景重建拓展到动态内容生成领域，对"3D 生成"方向产生了深远影响

### 2026-07-20｜VGGT-Ω: Visual Geometry Grounded Transformer Omega（VGGT-Ω：视觉几何基础大模型）

**VGGT-Ω: Visual Geometry Grounded Transformer Omega**
**VGGT-Ω：视觉几何基础大模型**

**方向**：视觉几何基础模型（Visual Geometry Foundation Models）　**来源**：CVPR 2026（Oral / Best Paper Finalist）　**机构**：Visual Geometry Group, University of Oxford × Meta AI

- **作者**：Jianyuan Wang, Minghao Chen, Shangzhan Zhang, Nikita Karaev, Johannes Schönberger, Patrick Labatut, Piotr Bojanowski, David Novotny, Andrea Vedaldi, Christian Rupprecht
- **链接**：[https://arxiv.org/abs/2605.15195](https://arxiv.org/abs/2605.15195) | 项目页：[vggt-omega.github.io](https://vggt-omega.github.io/) | CVF 页面：[CVPR 2026](https://openaccess.thecvf.com/content/CVPR2026/papers/Wang_VGGT-ohm_CVPR_2026_paper.html)

![VGGT-Ω teaser](https://km.sankuai.com/api/file/cdn/2756902383/247164494149?contentType=0&isNewContent=false)

**核心内容**：近期前馈重建模型（如 VGGT）已证明可与传统基于优化的重建方法竞争，同时为其他任务提供几何感知特征。本文证明这些模型的质量随模型规模与数据规模可预测地增长——首次揭示前馈三维重建领域存在类似大语言模型的 Scaling Law。为此，作者引入 VGGT-Ω，在静态与动态场景重建的准确性、效率和通用性上实现了大幅提升。为支持前所未有的训练规模，论文引入了三大创新：一是架构改进——通过使用单头多任务监督的密集预测头替代多头架构，移除昂贵的高分辨率卷积层，将训练显存降低至前作 VGGT 的约 30%；二是寄存器注意力机制（Register Attention）——将场景信息聚合到紧凑的寄存器表示中，并限制帧间信息交换仅通过寄存器进行，部分替代全局注意力，从而支持 15 倍于先前工作的监督数据量；三是自监督学习协议与动态场景数据流水线——构建高质量动态场景标注流水线，并采用 DINO 式自监督蒸馏充分利用大规模无标注视频数据。VGGT-Ω 将模型从 0.2B 参数扩展至 10B 参数，在静态和动态场景重建的六大基准上全面刷新 SOTA，例如在 Sintel 相机估计精度上较前作最佳提升了 77%（AUC@3° 从 22.5 提升至 40.0）。此外，论文还展示了学习到的寄存器表示能够增强视觉语言动作（VLA）模型，并支持与语言的对齐，表明三维重建可作为空间理解的强大且可扩展的代理任务。

**亮点**：

1. **首次证明前馈三维重建模型存在类似大语言模型的 Scaling Law，模型与数据规模可预测地提升重建精度**：VGGT-Ω 是首个系统性地将前馈三维重建模型"做大做强"的工作。实验表明，当模型规模从 0.5B 增长至 10B、数据规模从 2K 增长至 2M 序列时，3D 点云误差持续下降（图 1），呈现出清晰的幂律缩放关系。这一发现为三维视觉基础模型的未来发展指明了方向——与 LLM 领域类似，更大的模型和更多的数据将带来持续且可预测的精度提升，前馈重建从此具备与 SfM 等传统方法一较高下的数据驱动扩展能力
2. **通过寄存器注意力与架构简化将训练显存降低至前作的约 30%，支持 15 倍数据量与 10B 参数模型训练**：VGGT-Ω 对 VGGT 架构进行了系统性精简——使用单头多任务监督的密集预测头替代多头架构，移除高分辨率卷积层；引入寄存器注意力机制（Register Attention）将帧间信息交换限制在紧凑的寄存器表示中，部分替代昂贵的全局注意力。这些改进使训练显存降至前作的约 30%，从而支持 15 倍于先前工作的监督数据量和 10B 参数模型的训练。这是前馈重建领域首次实现如此大规模的数据与模型扩展
3. **将前馈重建从静态场景扩展到动态场景，Sintel 相机估计精度提升 77%，并展示重建特征对 VLA 和语言对齐的增强能力**：VGGT-Ω 构建了支持动态场景的高质量数据标注流水线，使前馈重建首次在动态场景上取得强结果。在 Sintel 相机估计基准上，AUC@3° 从 VGGT 的 22.5 大幅提升至 40.0（提升 77%）。论文进一步展示了学习到的寄存器表示能够有效增强视觉语言动作（VLA）模型，并支持与语言的对齐，表明三维重建不仅是计算机视觉的核心任务，更是通往空间理解通用智能的重要代理任务。该论文入选 CVPR 2026 Oral 并获最佳论文候选

### 2026-07-21｜GSPrior: 3D Gaussian Splatting with Self-Constrained Priors for High Fidelity Surface Reconstruction（基于自约束先验的高保真表面三维高斯泼溅重建）

**3D Gaussian Splatting with Self-Constrained Priors for High Fidelity Surface Reconstruction**
**基于自约束先验的高保真表面三维高斯泼溅重建**

**方向**：3D Gaussian Splatting 表面重建　**来源**：CVPR 2026　**机构**：清华大学 × 韦恩州立大学

- **作者**：Takeshi Noda, Yu-Shen Liu, Zhizhong Han
- **链接**：[https://arxiv.org/abs/2603.19682](https://arxiv.org/abs/2603.19682) | 项目页：[takeshie.github.io/GSPrior](https://takeshie.github.io/GSPrior/) | 代码：[github.com/takeshie/GSPrior](https://github.com/takeshie/GSPrior)

![GSPrior 方法概览图](https://km.sankuai.com/api/file/cdn/2756902383/247397319747?contentType=0&isNewContent=false)

**核心内容**：3D Gaussian Splatting（3DGS）虽然在渲染质量和速度上优于 NeRF，但在恢复高保真表面方面仍有提升空间。本文提出自约束先验（Self-Constrained Prior）来约束 3D 高斯的学习，以实现更精确的深度渲染。该先验源自一个 TSDF 网格，通过融合当前 3D 高斯渲染的深度图获得。先验度量估计表面周围的距离场，提供一个以表面为中心的"带"（band），对 3D 高斯施加更具体的约束：移除带外高斯、将高斯移近表面、以及以几何感知方式鼓励更大或更小的不透明度。更重要的是，该先验可定期由最新的深度图像更新（通常更准确和完整），并逐步缩窄带宽以收紧约束。在 NeRF-Synthetic、DTU、Tanks & Temples 和 MIP-NeRF 360 等广泛使用的基准上，该方法在表面重建质量上全面超越了现有 SOTA 方法。

**亮点**：

1. **自约束 TSDF 先验实现无外部监督的几何约束**：首次利用 3D 高斯自身渲染的深度图融合构建 TSDF 距离场作为自约束先验，无需任何外部几何监督信号。通过"带"约束机制（移除带外高斯、向表面移动高斯、几何感知不透明度调节）系统性地引导高斯基元贴合真实表面，将辐射场优化与几何重建目标自然对齐
2. **渐进式带宽收缩与定期更新保证稳定收敛**：先验随训练进程定期更新（基于不断精化的深度渲染结果），并渐进缩窄带宽，使几何约束从粗到细逐步收紧。这一设计避免了过早强约束导致的优化停滞，实现了从粗略几何到高保真表面的稳定、渐进式收敛
3. **多个主流基准上全面达到 SOTA 表面重建质量**：在 NeRF-Synthetic、DTU、Tanks & Temples 和 MIP-NeRF 360 四大基准上，GSPrior 在 Chamfer 距离、F-score 等几何指标上全面超越现有 3DGS 表面重建方法，同时保持竞争力的新视角合成质量，代码已开源

### 2026-07-22｜Dynamic Visual SLAM using a General 3D Prior（使用通用三维先验的动态视觉SLAM / Pi3MOS-SLAM）

**Dynamic Visual SLAM using a General 3D Prior**
**使用通用三维先验的动态视觉SLAM / Pi****^3^****MOS-SLAM**

**方向**：SLAM / 实时三维重建　**来源**：CVPR 2026　**机构**：University of Bonn（波恩大学，Photogrammetry & Robotics Lab）

- **作者**：Xingguang Zhong, Liren Jin, Marija Popović, Jens Behley, Cyrill Stachniss
- **链接**：[https://arxiv.org/abs/2512.06868](https://arxiv.org/abs/2512.06868) | 代码：[github.com/PRBonn/Pi3MOS-SLAM](https://github.com/PRBonn/Pi3MOS-SLAM) | CVF 页面：[CVPR 2026](https://openaccess.thecvf.com/content/CVPR2026/papers/Zhong_Dynamic_Visual_SLAM_using_a_General_3D_Prior_CVPR_2026_paper.html)

**核心内容**：可靠的增量式相机位姿估计与三维重建是机器人、交互式可视化和增强现实等应用的关键技术基础。然而在动态自然环境中，场景动态会严重损害相机位姿估计的准确性，使在线 SLAM 面临极大挑战。本文提出一种新颖的单目视觉 SLAM 系统 Pi³MOS-SLAM，能够在动态场景中鲁棒地估计相机位姿。其核心创新在于利用两类方法的互补优势：基于几何面片（patch-based）的在线束调整（Bundle Adjustment）的鲁棒局部优化能力，以及近期前馈重建模型（feed-forward reconstruction models，如 DUSt3R/MASt3R 等视觉几何基础模型）隐含的场景理解与 3D 感知能力。具体而言，作者提出利用前馈重建模型精确过滤动态区域——模型在预测稠密深度时天然对动态物体敏感，通过将其深度预测与 BA 估计的面片进行尺度对齐，即可在不依赖任何类别先验或语义分割网络的情况下鲁棒识别和去除动态干扰。同时，前馈模型的深度预测还被用于增强面片视觉 SLAM 的鲁棒性。在多个任务上的广泛实验表明，该方法在动态场景中的位姿估计与三维重建性能显著超越了现有 SOTA 方法。

**亮点**：

1. **前馈重建模型作为通用三维先验：首次在 SLAM 中系统性利用几何基础模型的"暗知识"处理动态场景**：传统动态 SLAM 依赖语义分割网络或运动分割器识别动态物体，需要额外的类别标注和训练数据。Pi³MOS-SLAM 独辟蹊径——直接利用前馈重建模型（DUSt3R/MASt3R 等）在预测稠密深度时天然对动态物体的敏感性，通过将深度预测与 BA 面片进行尺度对齐，无需任何类别先验即可精确过滤动态区域。这一设计揭示了一个重要启示：大规模预训练的前馈重建模型已经隐式编码了对场景运动的理解，可作为强大的通用三维先验直接赋能 SLAM 系统
2. **几何 BA 与前馈重建的互补融合：在线优化与预训练模型的协同增效**：论文巧妙地将两类方法互补结合——基于面片的在线 BA 提供局部几何一致性和实时位姿估计，前馈重建模型则提供全局稠密深度预测和动态区域识别能力。两者的连接点是"尺度对齐"：BA 面片估计的深度虽然稀疏但尺度一致，前馈模型的深度虽然稠密但存在跨帧尺度模糊；通过最小化两者的尺度差异，系统同时获得了稠密深度和尺度一致性。这种互补融合范式为 SLAM 领域提供了一种新的方法论框架
3. **CVPR 2026 录用，PRBonn 团队出品，代码完全开源**：该工作来自 SLAM 领域顶级研究组——波恩大学摄影测量与机器人实验室（Cyrill Stachniss 组），被 CVPR 2026 正式录用，代码已在 GitHub 完全开源（基于 MASt3R 和 DROID-SLAM 构建）。在多个动态场景基准上的实验表明，该方法在相机位姿估计精度和三维重建质量方面均显著超越现有单目 SLAM SOTA，特别在动态物体占比高的场景中优势更为突出

### 2026-07-23｜LiDAR Prompted Spatio-Temporal Multi-View Stereo for Autonomous Driving（激光雷达提示的时空多视图立体网络 / DriveMVS）

**LiDAR Prompted Spatio-Temporal Multi-View Stereo for Autonomous Driving**
**激光雷达提示的时空多视图立体网络 / DriveMVS**

**方向**：多视图立体重建（MVS）　**来源**：CVPR 2026　**机构**：CaiNiao Inc.（菜鸟网络）× Alibaba Group（阿里巴巴集团）× Harbin Institute of Technology（哈尔滨工业大学）

- **作者**：Qihao Sun, Jiarun Liu, Ziqian Ni, Jianyun Xu, Tao Xie, Lijun Zhao, Ruifeng Li, Sheng Yang
- **链接**：[https://arxiv.org/abs/2603.03765](https://arxiv.org/abs/2603.03765) | CVF 页面：[CVPR 2026](https://openaccess.thecvf.com/content/CVPR2026/html/Sun_LiDAR_Prompted_Spatio-Temporal_Multi-View_Stereo_for_Autonomous_Driving_CVPR_2026_paper.html)

![DriveMVS 方法概览图：LiDAR 提示的时空多视图立体网络架构](https://km.sankuai.com/api/file/cdn/2756902383/247796825939?contentType=0&isNewContent=false)

**核心内容**：精确的度量级深度估计对于自动驾驶感知与仿真至关重要，但现有方法在度量精度、多视图一致性、时序稳定性和跨域泛化能力之间难以取得平衡。本文提出 DriveMVS，一种新颖的多视图立体（MVS）框架，通过两项关键洞察调和这些相互竞争的目标：（1）稀疏但度量精确的激光雷达（LiDAR）观测可作为几何提示，以绝对尺度锚定深度估计；（2）多种线索的深度融合对于消歧和增强鲁棒性至关重要，同时时空解码器确保跨帧一致性。基于这些原则，DriveMVS 以两种方式嵌入 LiDAR 提示：一是作为硬几何先验锚定代价体积（cost volume）的绝对尺度；二是作为软特征指导，通过三线索融合器（Triple-Cue Combiner）与单目线索和几何线索深度融合。在时序一致性方面，DriveMVS 采用时空解码器，联合利用来自 MVS 代价体积的几何线索和来自相邻帧的时间上下文。实验表明，DriveMVS 在多个基准上达到 SOTA 性能，在度量精度、时序稳定性和零样本跨域迁移方面均表现卓越，展示了其在可扩展、可靠的自动驾驶系统中的实用价值。

**亮点**：

1. **LiDAR 作为几何提示双重嵌入：以绝对尺度锚定深度估计，突破传统 MVS 尺度模糊瓶颈**：现有 MVS 方法依赖多视图光度一致性进行深度估计，但无法恢复绝对尺度；单目深度估计虽能处理弱纹理区域，却存在尺度不一致问题。DriveMVS 创新性地将稀疏但度量精确的 LiDAR 观测以两种方式嵌入 MVS 流程——作为硬几何先验直接锚定代价体积的绝对尺度，作为软特征指导通过三线索融合器与单目/几何线索深度融合。这一设计使 DriveMVS 在保持 MVS 几何精度的同时获得了绝对尺度感知能力，在自动驾驶等对度量精度要求极高的场景中具有重要价值
2. **三线索融合器实现单目、度量与几何线索的深度协同，系统性地提升困难区域重建质量**：DriveMVS 提出 Triple-Cue Combiner，通过 Mask Transformer 架构将单目线索（来自 DINOv2）、度量线索（来自 LiDAR 提示编码器）和代价体积线索（来自 MVS cost volume）进行跨线索融合。单目线索提供丰富的语义和纹理信息，度量线索提供稀疏但精确的绝对尺度锚点，几何线索提供多视图一致性的稠密约束——三者的协同使模型在弱纹理、重复纹理、远距离区域等传统 MVS 失效场景中仍能稳健估计深度，显著提升了重建的完整性和鲁棒性
3. **时空解码器保障跨帧时序一致性，零样本跨域泛化能力突出**：DriveMVS 的时空解码器联合利用当前帧 MVS 代价体积的几何线索与相邻帧的时间上下文，通过显式建模时序依赖关系消除深度估计的帧间闪烁，确保输出深度图在时序上平滑一致。实验表明，DriveMVS 不仅在域内基准上达到 SOTA，更在零样本跨域迁移设置下（如从 KITTI 迁移到 nuScenes）显著优于现有方法，展示了其作为可扩展自动驾驶深度感知系统的实用潜力

### 2026-07-24｜Eulerian Gaussian Splatting using Hashed Probability Pyramids（基于哈希概率金字塔的欧拉高斯泼溅）

**Eulerian Gaussian Splatting using Hashed Probability Pyramids**
**基于哈希概率金字塔的欧拉高斯泼溅**

**方向**：3DGS 渲染加速与结构优化　**来源**：CVPR 2026　**机构**：Brown University / MIT

- **作者**：Mia Gaia Polansky, George Kopanas, Stephan Garbin, Todd Zickler, Dor Verbin
- **链接**：[https://arxiv.org/abs/2605.29136](https://arxiv.org/abs/2605.29136)

![Eulerian GS 概率密度优化框架图](https://km.sankuai.com/api/file/cdn/2756902383/247991914585?contentType=0&isNewContent=false)

**核心内容**：提出 Eulerian Gaussian Splatting (EGS)，一种基于概率的 splat 辐射场框架，保留 3D Gaussian Splatting 的快速光栅化和测试时效率，同时将启发式高斯基元操作（如手动调整的增密/剪枝）替换为基于梯度的体积概率密度优化。核心创新在于将高斯基元位置重新诠释为从可学习的持续密度场中采样的随机变量，而非直接操作离散基元。使用一种新颖的内存高效多尺度分层网格（Hashed Probability Pyramids）来实现该可学习密度场，支持端到端的梯度优化。推导出基于控制变量（control variates）的无偏梯度估计器以显著降低方差，使基于密度的优化稳定可行。通过允许概率质量自动流向损失函数需求的位置，该框架消除了脆弱先验并自然地探索体积空间，在 mip-NeRF 360 上实现 SOTA 重建质量，同时保持 3DGS 级别的渲染速度。

**亮点**：

1. **欧拉视角的概率密度优化范式：**颠覆传统 3DGS 对离散高斯基元的直接操作，将基元位置重新诠释为从可学习密度场中采样的随机变量，用连续梯度优化彻底替代启发式增密/剪枝策略，消除脆弱先验，开创了 3DGS 优化的新范式
2. **控制变量梯度估计器与哈希概率金字塔：**推导出无偏且低方差的梯度估计器使基于密度的优化稳定可行；提出内存高效的多尺度分层网格（Hashed Probability Pyramids）实现可学习密度场，支持端到端优化
3. **质量与效率双赢：**在 mip-NeRF 360 上实现 SOTA 重建质量，同时保持 3DGS 级别的实时渲染速度，证明概率密度优化路线在质量和效率上的双重优势
