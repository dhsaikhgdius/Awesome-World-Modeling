# Proposed README Additions — Driving / 3D-4D / Scientific-Physical / Occupancy-BEV

**Search date:** 2026-08-25
**Curated for sections:** 1.2 (Autonomous Driving — Generative), 1.4 (3D / 4D Scene Generation), 1.5 (Scientific & Physical World Modeling), 2.3 (Occupancy & BEV Representations)

**arXiv queries used (arXiv API, sorted by submission date):**
`"driving world model"`, `"occupancy world model"`, `"LiDAR world model"`, `"4D world model"`, `"Gaussian world model"`, `"neural simulator" AND driving`, `"climate world model"`, `"earth system" AND "world model"`, `"intuitive physics" AND "world model"`, `"molecular world model"`, `"video-to-4D"`, `"occupancy forecasting"`, `"3D world generation"`, `"4D scene generation"`, `"world exploration"`, `weather AND "world model"`, `protein AND "world model"`, `"molecular dynamics" AND "world model"`, `"Climate in a Bottle"`, `"virtual cell" AND "artificial intelligence"`, plus a broad `abs:"world model"` sweep covering 2026-07-14 → 2026-08-25 (all 2608.\* and 2607.\* after 2607.27201), plus targeted id-list checks for classics named in the curation brief.

**Counts:**
- Proposed new entries: **143** — 142 arXiv papers (all IDs verified absent from README.md as of commit `3f49ca0`) + 1 non-arXiv entry (Tesla occupancy-network technical material). Per section: 1.2.1 ×28, 1.2.2 ×15, 1.2.3 ×4, 1.2.4 ×14, 1.4.1 ×10, 1.4.2 ×21, 1.5.1 ×20, 1.5.2 ×15, 1.5.3 ×5, 2.3 ×11.
- Candidates found but already in README (skipped as duplicates): **~60** distinct IDs across queries (e.g., 2607.14005 M⁴World, 2607.20988 HyWorldVLA, 2506.24113 Epona, 2311.16038 OccWorld, 2508.03692 LiDARCrafter, 2508.08086 Matrix-3D, 2504.21650 HoloTime, 2606.27277 EO-WM, 2606.05925 Biomedical WMs, 2607.26037 Wonder, 2607.23602, 2607.19190, 2607.20653)
- Deliberately excluded after scope review: pure perception/detection/segmentation occupancy papers (e.g., SuperQuadricOcc 2511.17361, VEOcc 2605.25059, O3N 2603.12144), static object-level 4D content generation without a scene/world-modeling role (e.g., SC4D, Efficient4D, DreamMesh4D), Neural ODE (1806.07366) and Hamiltonian Neural Networks (1906.01563) — genuine dynamics-learning papers but not framed as world models (per curation brief), and MatterGen (2312.03687) — generative materials design without dynamics prediction.

**Insertion notes:**
1. **ID fix in existing README entry:** the "GaussianWorld" entry in §1.2.2 links arXiv **2412.04380**, which is actually *"EmbodiedOcc: Embodied 3D Occupancy Prediction for Vision-based Online Scene Understanding."* The correct GaussianWorld ID is **2412.10373** (title and GitHub `zuosc19/GaussianWorld` match). Recommend fixing the badge/link in place.
2. **Name clashes to watch when inserting:** three unrelated papers named **GEM** (2412.11198 ego-vision, already listed; 2605.17682 occupancy; 2605.07326 LiDAR), two named **SparseWorld** (2510.17482 already listed; 2605.24354 new), two named **PhysGen** (2603.00110 already listed in §1.3; 2409.18964 new ECCV 2024 paper), and **UniSim** (2310.06114 interactive simulators, already listed in §1.3.2; 2308.01898 driving sensor simulator, new).
3. PHYRE, CLEVRER, IntPhys, CoPhy, Physion, and Physics-IQ are benchmark-style classics proposed for §1.5.1; alternatively they can be routed to the "Benchmarks & Evaluation" table. Physics-IQ (2501.09038) is the original paper behind the already-listed "Physics-IQ Verified" (2606.18943).
4. DrivingDojo, Sekai2, and WorldRover are dataset/data-engine papers; if datasets are kept out of §1.2/§1.4, route them to "Datasets & Data Collections".
5. UniOcc and Cam4DOcc are benchmark/toolkit papers for occupancy forecasting; proposed for §2.3 but can be routed to "Benchmarks & Evaluation".
6. GraphCast and Pangu-Weather are already listed in §1.5.2 via journal links — not re-proposed here despite their arXiv IDs (2212.12794, 2211.02556) being absent from the file.

---

## 1.2.1 Multi-View Video Generation (Camera-Based)

- **GenAD (OpenDriveLab)** — "GenAD: Generalized Predictive Model for Autonomous Driving." *CVPR* 2024 Highlight. [![arXiv](https://img.shields.io/badge/arXiv-2403.09630-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2403.09630) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/OpenDriveLab/DriveAGI)
  > Large-scale video prediction model trained on ~2000 hours of web driving videos (OpenDV-2K); zero-shot generalization to unseen scenes and action-conditioned prediction.

- **DriveGAN** — "DriveGAN: Towards a Controllable High-Quality Neural Simulation." *CVPR* 2021. [![arXiv](https://img.shields.io/badge/arXiv-2104.15060-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2104.15060) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://research.nvidia.com/labs/toronto-ai/DriveGAN/)
  > Early action-conditioned neural driving simulator learned directly in pixel space from unannotated videos; a pre-diffusion classic of controllable driving simulation.

- **UniSim (Waabi)** — "UniSim: A Neural Closed-Loop Sensor Simulator." *CVPR* 2023 Highlight. [![arXiv](https://img.shields.io/badge/arXiv-2308.01898-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2308.01898) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://waabi.ai/unisim/)
  > Reconstructs logged drives into an editable neural closed-loop simulator that re-renders camera and LiDAR under new ego actions and actor behaviors. Distinct from the identically named UniSim (2310.06114) in §1.3.2.

- **Panacea** — "Panacea: Panoramic and Controllable Video Generation for Autonomous Driving." *CVPR* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2311.16813-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2311.16813) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://panacea-ad.github.io/)
  > Generates BEV-layout-controlled panoramic multi-view driving videos for annotation-aligned data augmentation.

- **WoVoGen** — "WoVoGen: World Volume-aware Diffusion for Controllable Multi-camera Driving Scene Generation." *ECCV* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2312.02934-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2312.02934) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/fudan-zvg/WoVoGen)
  > Uses an explicit predicted 4D world volume as a prior to keep multi-camera video generation cross-view and temporally consistent.

- **DriveArena** — "DriveArena: A Closed-loop Generative Simulation Platform for Autonomous Driving." *arXiv* 2408.00415 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2408.00415-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2408.00415) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://pjlab-adg.github.io/DriveArena/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/PJLab-ADG/DriveArena)
  > Closed-loop generative simulation platform coupling a traffic manager with a conditional world model so driving agents can be evaluated interactively on realistic imagery.

- **DrivingDojo** — "DrivingDojo Dataset: Advancing Interactive and Knowledge-Enriched Driving World Model." *NeurIPS* 2024 D&B. [![arXiv](https://img.shields.io/badge/arXiv-2410.10738-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.10738) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/Robertwyq/Drivingdojo)
  > Dataset built specifically for training interactive driving world models, with dense ego actions, multi-agent interplay, and rare-event clips; also defines an action-instruction-following benchmark.

- **MagicDrive-V2** — "MagicDrive-V2: High-Resolution Long Video Generation for Autonomous Driving with Adaptive Control." *arXiv* 2411.13807 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2411.13807-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2411.13807) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://gaoruiyuan.com/magicdrive-v2/)
  > Scales the MagicDrive line to high-resolution, minute-scale multi-view driving video with geometric control via a DiT backbone.

- **Cosmos-Transfer1** — "Cosmos-Transfer1: Conditional World Generation with Adaptive Multimodal Control." *arXiv* 2503.14492 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2503.14492-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.14492) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/nvidia-cosmos/cosmos-transfer1) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://research.nvidia.com/labs/dir/cosmos-transfer1/)
  > NVIDIA Cosmos family: conditional world generation with spatially adaptive control (segmentation, depth, edge, HD map, LiDAR), widely used for Sim2Real driving data generation.

- **ProphetDWM** — "ProphetDWM: A Driving World Model for Rolling Out Future Actions and Videos." *arXiv* 2505.18650 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2505.18650-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.18650)
  > Jointly rolls out future actions and future video, linking action prediction and video generation in one driving world model.

- **World Engine** — "World Engine: Towards the Era of Post-Training for Autonomous Driving." *arXiv* 2606.19836 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.19836-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.19836)
  > Uses generative world simulation to synthesize safety-critical long-tail interactions at scale for post-training end-to-end driving policies.

- **CausalDrive** — "CausalDrive: Real-time Causal World Models for Autonomous Driving." *arXiv* 2606.15341 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.15341-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.15341)
  > Real-time interactive driving simulator with reactive background agents, addressing the non-reactivity of layout-conditioned renderers and the weak semantic control of pure action-conditioned predictors.

- **CVD-STORM** — "CVD-STORM: Cross-View Video Diffusion with Spatial-Temporal Reconstruction Model for Autonomous Driving." *arXiv* 2510.07944 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.07944-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.07944)
  > Cross-view video diffusion with a spatial-temporal reconstruction VAE that additionally outputs depth alongside future multi-view video.

- **WorldSplat** — "WorldSplat: Gaussian-Centric Feed-Forward 4D Scene Generation for Autonomous Driving." *arXiv* 2509.23402 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2509.23402-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2509.23402)
  > Feed-forward 4D Gaussian generation for driving scenes, bridging generative video world models and explicit 4D scene representations.

- **PhiGenesis (Stereo Forcing)** — "4D Driving Scene Generation With Stereo Forcing." *arXiv* 2509.20251 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2509.20251-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2509.20251)
  > Extends video-generation world models to 4D driving scene generation with geometric stereo constraints across time.

- **InstaDrive** — "InstaDrive: Instance-Aware Driving World Models for Realistic and Consistent Video Generation." *arXiv* 2602.03242 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2602.03242-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2602.03242)
  > Adds instance-level temporal and geometric constraints to driving video world models for identity-consistent agents.

- **ConsisDrive** — "ConsisDrive: Identity-Preserving Driving World Models for Video Generation by Instance Mask." *arXiv* 2602.03213 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2602.03213-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2602.03213)
  > Uses instance masks to suppress identity drift (objects changing appearance or category across frames) in generated driving videos.

- **UniDWM** — "UniDWM: Towards a Unified Driving World Model via Multifaceted Representation Learning." *arXiv* 2602.01536 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2602.01536-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2602.01536)
  > Builds a structure- and dynamics-aware latent world representation that jointly grounds geometry, appearance, and planning.

- **X-Cache** — "X-Cache: Cross-Chunk Block Caching for Few-Step Autoregressive World Models Inference." *arXiv* 2604.20289 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2604.20289-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2604.20289)
  > Inference acceleration tailored to few-step autoregressive driving world models, targeting real-time closed-loop simulation.

- **Infrastructure-Centric World Models** — "Infrastructure-Centric World Models: Bridging Temporal Depth and Spatial Breadth for Roadside Perception." *arXiv* 2604.17651 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2604.17651-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2604.17651)
  > Argues for roadside (infrastructure-viewpoint) driving world models with persistent bird's-eye multi-sensor coverage, complementing ego-centric approaches.

- **HorizonDrive** — "HorizonDrive: Self-Corrective Autoregressive World Model for Long-horizon Driving Simulation." *arXiv* 2605.11596 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.11596-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.11596)
  > Self-corrective autoregressive rollout for closed-loop driving simulation, addressing drift under fast ego-motion where frame-sink distillation transfers poorly.

- **EponaV2** — "EponaV2: Driving World Model with Comprehensive Future Reasoning." *arXiv* 2605.14696 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.14696-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.14696)
  > Successor to Epona (already listed); adds future reasoning to a perception-free driving world model to improve annotation-free trajectory planning.

- **Instant NuRec** — "Instant NuRec: Feed-Forward 3D Gaussian Reconstruction for Driving Scene Simulation." *arXiv* 2607.14203 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.14203-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.14203)
  > Feed-forward, tuning-free 3D Gaussian reconstruction for neural driving simulation, removing per-scene optimization from reconstruction-based simulators.

- **Training-Free Norm Injection** — "Is Energy Guidance All You Need? Training-Free Norm Injection for Driving World Models." *arXiv* 2607.10781 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.10781-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.10781)
  > Enforces traffic norms in rectified-flow driving world models at inference time, without retraining or hand-built layout conditioning.

- **RealWeather** — "RealWeather: Realistic and Scene-Faithful Weather Translation with Driving World Models." *arXiv* 2608.02953 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.02953-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.02953)
  > Uses a driving world model to translate logged drives across weather conditions while preserving scene identity, for robustness evaluation without paired data.

- **muSync-GS** — "muSync-GS: Physics-Synchronized Driving Video Synthesis for Weather and Geometric Road Hazards." *arXiv* 2608.04412 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04412-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04412)
  > Couples weather and road-geometry edits with tire-road friction and vehicle dynamics so synthesized hazard videos stay physically consistent with the edited conditions.

- **Counterfactual Prediction in DWMs** — "How Can Driving World Models Do Counterfactual Prediction?" *arXiv* 2608.11601 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.11601-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.11601)
  > Identifies a mismatch between direct action-conditioned prediction and true counterfactual simulation of logged episodes, and proposes a fix; core to using DWMs as what-if simulators.

- **DriveCache** — "DriveCache: Action-Aware Caching for Driving World Model Inference." *arXiv* 2608.16354 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.16354-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.16354)
  > Action-aware diffusion caching designed for driving world model backbones, improving generation throughput for simulation and data generation.

## 1.2.2 Occupancy & BEV-Based Generative Models

- **MUVO** — "MUVO: A Multimodal Generative World Model for Autonomous Driving with Geometric Representations." *arXiv* 2311.11762 (2023). [![arXiv](https://img.shields.io/badge/arXiv-2311.11762-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2311.11762) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/fzi-forschungszentrum-informatik/muvo)
  > Early multimodal driving world model predicting future camera, LiDAR, and 3D occupancy jointly from raw sensor data.

- **RenderWorld** — "RenderWorld: World Model with Self-Supervised 3D Label." *arXiv* 2409.11356 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2409.11356-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.11356)
  > Vision-only driving framework that self-supervises Gaussian-based 3D occupancy labels and forecasts occupancy with an autoregressive world model for planning.

- **DFIT-OccWorld** — "An Efficient Occupancy World Model via Decoupled Dynamic Flow and Image-assisted Training." *arXiv* 2412.13772 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2412.13772-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.13772)
  > Non-autoregressive occupancy forecasting via decoupled voxel flow warping plus image-assisted training; an efficient 4D scene forecasting baseline.

- **OccProphet** — "OccProphet: Pushing Efficiency Frontier of Camera-Only 4D Occupancy Forecasting with Observer-Forecaster-Refiner Framework." *arXiv* 2502.15180 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2502.15180-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.15180) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/JLChen-C/OccProphet)
  > Lightweight observer-forecaster-refiner pipeline making camera-only 4D occupancy forecasting tractable on edge compute.

- **I²-World** — "I²-World: Intra-Inter Tokenization for Efficient Dynamic 4D Scene Forecasting." *arXiv* 2507.09144 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2507.09144-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2507.09144)
  > Decouples intra-scene and inter-scene tokenization to make occupancy-based 4D scene forecasting efficient and scalable.

- **OccTENS** — "OccTENS: 3D Occupancy World Model via Temporal Next-Scale Prediction." *arXiv* 2509.03887 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2509.03887-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2509.03887)
  > Reformulates occupancy generation as temporal next-scale prediction for controllable long-horizon occupancy rollout at lower cost than token-by-token autoregression.

- **IR-WM** — "Vision-Centric 4D Occupancy Forecasting and Planning via Implicit Residual World Models." *arXiv* 2510.16729 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.16729-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.16729)
  > Forecasts only the residual change of the scene instead of fully reconstructing future frames, saving capacity spent on static backgrounds.

- **SparseWorld-TC** — "SparseWorld-TC: Trajectory-Conditioned Sparse Occupancy World Model." *arXiv* 2511.22039 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2511.22039-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2511.22039)
  > End-to-end trajectory-conditioned multi-frame occupancy forecasting directly from image features, avoiding discrete VAE occupancy tokens.

- **GenieDrive** — "GenieDrive: Towards Physics-Aware Driving World Model with 4D Occupancy Guided Video Generation." *arXiv* 2512.12751 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.12751-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.12751)
  > Factorizes action-to-video generation through 4D occupancy prediction, improving physical consistency of generated driving futures.

- **ForecastOcc** — "ForecastOcc: Vision-based Semantic Occupancy Forecasting." *arXiv* 2602.08006 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2602.08006-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2602.08006)
  > Forecasts full semantic occupancy (not just motion classes) directly from camera input without requiring past occupancy estimates.

- **GEM (Gaussian Evolution Model)** — "GEM: Gaussian Evolution Model for Occupancy Forecasting and Motion Planning." *arXiv* 2605.17682 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.17682-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.17682)
  > Evolves a 3D Gaussian scene state continuously over time for occupancy forecasting and planning, avoiding fixed-step token autoregression. Unrelated to the ego-vision GEM (2412.11198) already listed.

- **OWMDrive** — "OWMDrive: Causality-Aware End-to-End Autonomous Driving via 4D Occupancy World Model." *arXiv* 2606.30421 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.30421-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.30421)
  > End-to-end driving that plans over explicit future occupancy rollouts with temporal causal modeling of traffic interactions.

- **CascadeOcc** — "CascadeOcc: Rethinking 3D Occupancy World Models with Cascaded VQ Representations." *arXiv* 2606.27644 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.27644-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.27644)
  > Cascaded vector-quantized occupancy representation exploiting structural hierarchy instead of auxiliary modalities or large language models.

- **InterOCF** — "InterOCF: Spatio-Temporal 2D-3D Interaction for Camera-Only 4D Occupancy Forecasting." *arXiv* 2607.24431 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.24431-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.24431)
  > Strengthens spatio-temporal 2D-3D interaction across input multi-view frames for camera-only forecasting of future semantic occupancy.

- **Geometry-Aware 4D Occupancy Forecasting** — "Geometry-Aware Spatio-Temporal Context Modeling for 4D Occupancy Forecasting." *arXiv* 2608.15279 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.15279-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.15279)
  > Targets geometric distortion of static structures and temporal drift in tokenize-then-autoregress occupancy forecasting pipelines.

## 1.2.3 LiDAR & 4D Point Cloud Generative Models

- **ViDAR** — "Visual Point Cloud Forecasting enables Scalable Autonomous Driving." *CVPR* 2024 Highlight. [![arXiv](https://img.shields.io/badge/arXiv-2312.17655-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2312.17655) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/OpenDriveLab/ViDAR)
  > Visual point cloud forecasting as a scalable pre-training task: predicts future LiDAR from historical camera input, jointly learning semantics, geometry, and dynamics.

- **LidarDM** — "LidarDM: Generative LiDAR Simulation in a Generated World." *arXiv* 2404.02903 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2404.02903-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.02903) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/vzyrianov/lidardm) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://www.zyrianov.org/lidardm/)
  > Layout-conditioned generation of realistic, temporally coherent 4D LiDAR sequences by first generating an underlying 4D world.

- **GEM (Deformable Mamba)** — "GEM: Generating LiDAR World Model via Deformable Mamba." *arXiv* 2605.07326 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.07326-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.07326)
  > Deformable Mamba architecture for LiDAR world modeling, tackling point cloud disorder and dynamic-static separation. Unrelated to the other GEM entries.

- **U4D** — "U4D: Uncertainty-Aware 4D World Modeling from LiDAR Sequences." *arXiv* 2512.02982 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.02982-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.02982)
  > Allocates generative capacity by spatial uncertainty when modeling dynamic 3D environments from LiDAR sequences, reducing artifacts in ambiguous regions.

## 1.2.4 Language-Guided & Multimodal Driving World Models

- **Occ-LLM** — "Occ-LLM: Enhancing Autonomous Driving with Occupancy-Based Large Language Models." *arXiv* 2502.06419 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2502.06419-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.06419)
  > Encodes 3D occupancy as LLM input for occupancy forecasting, self-ego planning, and scene question answering in one model.

- **GaussianDWM** — "GaussianDWM: 3D Gaussian Driving World Model for Unified Scene Understanding and Multi-Modal Generation." *arXiv* 2512.23180 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.23180-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.23180)
  > Uses a 3D Gaussian scene representation as the shared substrate for driving scene understanding, reasoning, and multi-modal future generation.

- **SparseOccVLA** — "SparseOccVLA: Bridging Occupancy and Vision-Language Models via Sparse Queries for Unified 4D Scene Understanding and Planning." *arXiv* 2601.06474 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2601.06474-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2601.06474)
  > Sparse occupancy queries feed a VLM to combine fine-grained 4D geometry with high-level language reasoning and planning without token explosion.

- **Driver-WM** — "Driver-WM: A Driver-Centric Traffic-Conditioned Latent World Model for In-Cabin Dynamics Rollout." *arXiv* 2605.05092 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.05092-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.05092)
  > Rolls out in-cabin driver dynamics conditioned on external traffic; extends driving world models from the environment to the human in the loop for L2/L3 shared control.

- **DeepSight** — "DeepSight: Long-Horizon World Modeling via Latent States Prediction for End-to-End Autonomous Driving." *arXiv* 2605.10564 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.10564-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.10564)
  > Adds driving-tailored long-horizon latent-state prediction to VLM-based end-to-end driving instead of general-domain reasoning adaptations.

- **SparseWorld (E2E driving)** — "SparseWorld: Enhancing End-to-End Autonomous Driving via World Models with Sparse Scene Representation." *arXiv* 2605.24354 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.24354-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.24354)
  > Lightweight world model over sparse scene representations for end-to-end driving; distinct from the 4D occupancy SparseWorld (2510.17482) already listed.

- **GeoWorldAD** — "GeoWorldAD: Geometry World Action Model for Autonomous Driving." *arXiv* 2607.17521 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.17521-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.17521)
  > Grounds trajectory planning in ego-aligned 3D space and anticipates short-horizon scene evolution, adding geometric grounding to vision/video-action driving policies.

- **Orbis 2** — "Orbis 2: A Hierarchical World Model for Driving." *arXiv* 2607.15898 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.15898-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.15898)
  > Companion to the listed Orbis: factorizes future prediction into a high-level semantic predictor and a low-level perceptual generator operating at different temporal scales.

- **Auto-JEPA** — "Auto-JEPA: A Latent World Model of Continuous Intent for End-to-End Autonomous Driving." *arXiv* 2607.29031 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.29031-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.29031)
  > Action-oriented latent world model that predicts only planning-relevant future features instead of dense video, occupancy, or BEV reconstruction.

- **4D-WAM** — "4D-WAM: 4D Consistent World Modeling for Autonomous Driving." *arXiv* 2608.10107 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.10107-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.10107)
  > Uses geometric foundation models at training time to make world-action-model predictions 4D-consistent rather than merely visually plausible.

- **BrainWAM** — "BrainWAM: Action-Space Coordination of Semantic Priors and Predictive Dynamics for Autonomous Driving." *arXiv* 2608.12854 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.12854-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.12854)
  > Coordinates VLA semantic priors and world-action-model predictive dynamics in action space, avoiding the attention-allocation mismatch of naive token-level fusion.

- **GaussianDWM++** — "GaussianDWM++: Language-Grounded 3D Gaussian Driving World Model for Unified Scene Understanding, Editing, and Multi-Modal Generation." *arXiv* 2608.16234 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.16234-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.16234)
  > Extends GaussianDWM with language-grounded reasoning and controllable 4D editing on the 3D Gaussian scene state.

- **DA-WAM** — "DA-WAM: Decision-Aligned Future Latents for Driving World Models." *arXiv* 2608.19085 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.19085-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.19085)
  > Makes predicted futures decision-informative: future latents are aligned so they directly shape trajectory selection rather than being merely predictive.

- **GeoWAM** — "GeoWAM: Visual Geometry World Action Models for Autonomous Driving." *arXiv* 2608.23486 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.23486-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.23486)
  > Moves world-action modeling from pixel space to visual geometry, disentangling 3D scene dynamics from appearance, texture, and illumination.

## 1.4.1 Explorable 3D Scene Generation & Persistent Representations

- **HOLODECK 2.0** — "HOLODECK 2.0: Vision-Language-Guided 3D World Generation with Editing." *arXiv* 2508.05899 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2508.05899-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.05899)
  > Follow-up to the listed Holodeck: open-domain 3D scene generation with vision-language-guided flexible editing.

- **LatticeWorld** — "LatticeWorld: A Multimodal Large Language Model-Empowered Framework for Interactive Complex World Generation." *arXiv* 2509.05263 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2509.05263-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2509.05263)
  > LLM-driven pipeline that emits large-scale interactive 3D environments with dynamic agents and physics via an industry-grade rendering engine.

- **UrbanWorld2.0** — "UrbanWorld2.0: A Multimodal Agentic Framework for Reality-Aligned 3D World Generation at City-Scale." *arXiv* 2511.18005 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2511.18005-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2511.18005)
  > Agentic multimodal engine for generating reality-aligned, city-scale 3D urban worlds.

- **WonderZoom** — "WonderZoom: Multi-Scale 3D World Generation." *arXiv* 2512.09164 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.09164-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.09164)
  > From the WonderWorld/WonderJourney line: scale-aware 3D representation that generates coherent scene content across multiple spatial scales from one image.

- **WorldFlow3D** — "WorldFlow3D: Flowing Through 3D Distributions for Unbounded World Generation." *arXiv* 2603.29089 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2603.29089-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2603.29089)
  > Models unbounded 3D world generation as flow-matching transport between 3D distributions.

- **GTA** — "GTA: Advancing Image-to-3D World Generation via Geometry Then Appearance Video Diffusion." *arXiv* 2605.12957 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.12957-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.12957)
  > Two-stage geometry-then-appearance video diffusion for image-to-3D world generation, prioritizing underlying geometry over appearance-first pipelines.

- **Walking in the Implicit** — "Walking in the Implicit: Interactive World Exploration via Neural Scene Representation." *arXiv* 2606.30045 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.30045-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.30045)
  > Interactive free exploration of generated worlds through an implicit neural scene representation rather than replayed video rollouts.

- **Genie Sim PanoWorld** — "Genie Sim PanoWorld: An Infinite Indoor 3D World Generation Pipeline via Panoramic Scene Modeling and Simulation." *arXiv* 2607.26646 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.26646-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.26646)
  > Two-stage feed-forward pipeline turning a single 360° panorama into a freely navigable indoor 3D scene with metric trajectory control, without per-scene optimization.

- **Sekai2** — "Sekai2: From World Exploration to Interactive World Modeling." *arXiv* 2608.09449 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09449-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09449)
  > Multi-source real-world video dataset with camera trajectories and temporally grounded semantics for training long-horizon, camera-controllable world exploration models (dataset resource).

- **WorldRover** — "WorldRover: A Scalable Synthetic Video Data Engine for World Exploration with Rich Annotations." *arXiv* 2608.15659 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.15659-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.15659)
  > Rendering-based data engine supplying video with exact camera motion, dense geometry, correspondence, and control signals for explorable world model training (dataset resource).

## 1.4.2 Video-to-3D / 4D World Models

- **4Real** — "4Real: Towards Photorealistic 4D Scene Generation via Video Diffusion Models." *NeurIPS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2406.07472-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2406.07472) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://snap-research.github.io/4Real/)
  > Text-to-4D photorealistic dynamic scene generation by distilling video diffusion priors into deformable 3D Gaussians.

- **DreamScene4D** — "DreamScene4D: Dynamic Multi-Object Scene Generation from Monocular Videos." *NeurIPS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2405.02280-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2405.02280) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://dreamscene4d.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/dreamscene4d/dreamscene4d)
  > Lifts in-the-wild monocular videos with multiple interacting objects and occlusions into dynamic 4D Gaussian scenes with recovered object motion.

- **DimensionX** — "DimensionX: Create Any 3D and 4D Scenes from a Single Image with Controllable Video Diffusion." *arXiv* 2411.04928 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2411.04928-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2411.04928) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/wenqsun/DimensionX) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://chenshuo20.github.io/DimensionX/)
  > Decouples spatial (camera) and temporal (dynamics) factors in controllable video diffusion to build 3D and 4D scenes from a single image.

- **CAT4D** — "CAT4D: Create Anything in 4D with Multi-View Video Diffusion Models." *CVPR* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2411.18613-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2411.18613) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://cat-4d.github.io/)
  > Multi-view video diffusion that converts monocular video into dynamic 4D scenes with disentangled camera and time control.

- **Free4D** — "Free4D: Tuning-free 4D Scene Generation with Spatial-Temporal Consistency." *ICCV* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2503.20785-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.20785) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://free4d.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/TQTQliu/Free4D)
  > Tuning-free lifting of a single image or video into a spatio-temporally consistent 4D scene representation using pretrained foundation models.

- **WonderPlay** — "WonderPlay: Dynamic 3D Scene Generation from a Single Image and Actions." *arXiv* 2505.18151 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2505.18151-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.18151) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://kyleleey.github.io/WonderPlay/)
  > Action-conditioned dynamic 3D scenes from one image: a physics simulator drives coarse dynamics and a video generator refines them, closing the loop between simulation and generation.

- **DSG-World** — "DSG-World: Learning a 3D Gaussian World Model from Dual State Videos." *arXiv* 2506.05217 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.05217-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.05217)
  > Builds an explicit, physically consistent 3D Gaussian world model from two-state video observations in a single pass, supporting simulation-ready scene manipulation.

- **4DGT** — "4DGT: Learning a 4D Gaussian Transformer Using Real-World Monocular Videos." *arXiv* 2506.08015 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.08015-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.08015) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://4dgt.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/facebookresearch/4DGT)
  > Feed-forward 4D Gaussian transformer trained purely on real-world monocular videos, unifying static and dynamic scene components with varying object lifespans.

- **4Real-Video-V2** — "4Real-Video-V2: Fused View-Time Attention and Feedforward Reconstruction for 4D Scene Generation." *arXiv* 2506.18839 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.18839-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.18839) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://snap-research.github.io/4Real-Video-V2/)
  > Fused view-time attention plus feedforward reconstruction for joint multi-view video synthesis and 4D scene recovery.

- **4DNeX** — "4DNeX: Feed-Forward 4D Generative Modeling Made Easy." *arXiv* 2508.13154 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2508.13154-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.13154) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://4dnex.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/3DTopia/4DNeX)
  > First feed-forward single-image-to-4D framework, fine-tuning a video diffusion model to output dynamic 3D scene representations without per-scene optimization.

- **TiP4GEN** — "TiP4GEN: Text to Immersive Panorama 4D Scene Generation." *arXiv* 2508.12415 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2508.12415-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.12415)
  > Text-driven 360° panoramic 4D scene generation, extending panoramic world generation from static scenes to dynamics.

- **See4D** — "See4D: Pose-Free 4D Generation via Auto-Regressive Video Inpainting." *arXiv* 2510.26796 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.26796-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.26796)
  > Pose-free video-to-4D generation via warp-then-inpaint autoregression, removing the camera-annotation requirement for in-the-wild footage.

- **Diff4Splat** — "Diff4Splat: Controllable 4D Scene Generation with Latent Dynamic Reconstruction Models." *arXiv* 2511.00503 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2511.00503-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2511.00503)
  > Combines video diffusion with latent dynamic reconstruction to produce controllable 4D Gaussian scenes.

- **One4D** — "One4D: Unified 4D Generation and Reconstruction via Decoupled LoRA Control." *arXiv* 2511.18922 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2511.18922-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2511.18922)
  > One framework spanning 4D generation from a single image, 4D reconstruction from full video, and mixed regimes, emitting synchronized RGB frames and pointmaps.

- **DynamicVerse** — "DynamicVerse: A Physically-Aware Multimodal Framework for 4D World Modeling." *arXiv* 2512.03000 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.03000-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.03000)
  > Physically-aware 4D modeling framework that converts internet video into metric-scale 4D data with geometry, motion, and captions for world-model training.

- **NeoVerse** — "NeoVerse: Enhancing 4D World Model with in-the-wild Monocular Videos." *arXiv* 2601.00393 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2601.00393-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2601.00393)
  > 4D world model trained scalably from in-the-wild monocular videos, supporting 4D reconstruction and novel-trajectory video generation without specialized multi-view data.

- **Mirage2Matter** — "Mirage2Matter: A Physically Grounded Gaussian World Model from Video." *arXiv* 2602.00096 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2602.00096-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2602.00096)
  > Builds physically grounded Gaussian world models from ordinary video without depth sensors or calibration, narrowing the visual and physical sim-to-real gap.

- **PerpetualWonder** — "PerpetualWonder: Long-Horizon Action-Conditioned 4D Scene Generation." *arXiv* 2602.04876 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2602.04876-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2602.04876)
  > Long-horizon action-conditioned 4D scene rollout, extending single-shot 4D generation toward persistent interactive dynamics.

- **Genie 4D** — "Genie 4D: Semantic-Prior-Guided 4D Dynamic Scene Reconstruction." *arXiv* 2604.09877 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2604.09877-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2604.09877)
  > Turns hand-held phone capture into a semantically grounded, action-controllable 4D world model via a real-time visual-inertial Gaussian splatting front end.

- **Full-4D** — "Full-4D: Generating Full-Scope 4D Scenes from a Single-View Video." *arXiv* 2605.25500 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.25500-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.25500)
  > Generates fully explorable dynamic 4D scenes (not just small viewpoint perturbations) from a single-view video.

- **CP4D** — "CP4D: Compositional Physics-aware 4D Scene Generation." *arXiv* 2606.09187 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.09187-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.09187)
  > Compositional 4D scene generation with per-object physical plausibility constraints.

## 1.5.1 Physics Simulation & Intuitive Physics

- **Interaction Networks** — Battaglia, P. et al. "Interaction Networks for Learning about Objects, Relations and Physics." *NeurIPS* 2016. [![arXiv](https://img.shields.io/badge/arXiv-1612.00222-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1612.00222)
  > Foundational learned physics simulator: object- and relation-centric dynamics model that rolls out n-body, rigid-collision, and non-rigid systems.

- **IntPhys** — Riochet, R. et al. "IntPhys 2019: A Benchmark for Visual Intuitive Physics Understanding." *TPAMI* 2021. [![arXiv](https://img.shields.io/badge/arXiv-1803.07616-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1803.07616) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://intphys.cognitive-ml.fr/)
  > Violation-of-expectation benchmark (object permanence, shape constancy, spatio-temporal continuity) for evaluating intuitive physics in predictive models.

- **PHYRE** — Bakhtin, A. et al. "PHYRE: A New Benchmark for Physical Reasoning." *NeurIPS* 2019. [![arXiv](https://img.shields.io/badge/arXiv-1908.05656-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1908.05656) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/facebookresearch/phyre)
  > 2D physics-puzzle benchmark where agents act by intervention (placing objects) and must predict resulting dynamics; a standard testbed for physical world models.

- **CoPhy** — Baradel, F. et al. "CoPhy: Counterfactual Learning of Physical Dynamics." *ICLR* 2020. [![arXiv](https://img.shields.io/badge/arXiv-1909.12000-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1909.12000) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://projet.liris.cnrs.fr/cophy/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/fabienbaradel/cophy)
  > Counterfactual physical dynamics benchmark and model: predict outcomes after a do-intervention modifies the initial scene.

- **CLEVRER** — Yi, K. et al. "CLEVRER: Collision Events for Video Representation and Reasoning." *ICLR* 2020. [![arXiv](https://img.shields.io/badge/arXiv-1910.01442-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1910.01442) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](http://clevrer.csail.mit.edu/)
  > Diagnostic video benchmark for descriptive, explanatory, predictive, and counterfactual reasoning about collision dynamics.

- **GNS** — Sanchez-Gonzalez, A. et al. "Learning to Simulate Complex Physics with Graph Networks." *ICML* 2020. [![arXiv](https://img.shields.io/badge/arXiv-2002.09405-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2002.09405) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/google-deepmind/deepmind-research/tree/master/learning_to_simulate) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://sites.google.com/view/learning-to-simulate)
  > Graph network simulator for fluids, rigid solids, and deformables; the standard particle-based learned physics simulator that FIGNet (already listed) builds on.

- **Physion** — Bear, D. M. et al. "Physion: Evaluating Physical Prediction from Vision in Humans and Machines." *NeurIPS* 2021 D&B. [![arXiv](https://img.shields.io/badge/arXiv-2106.08261-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2106.08261) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/cogtoolslab/physics-benchmarking-neurips2021)
  > Human-calibrated benchmark of visual physical prediction across eight scenario types (support, collide, contain, drape, etc.).

- **PhysGaussian** — "PhysGaussian: Physics-Integrated 3D Gaussians for Generative Dynamics." *CVPR* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2311.12198-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2311.12198) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://xpandora.github.io/PhysGaussian/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/XPandora/PhysGaussian)
  > Embeds continuum-mechanics (MPM) dynamics directly into 3D Gaussian scene representations, unifying simulation and rendering ("what you see is what you simulate").

- **PhysDreamer** — "PhysDreamer: Physics-Based Interaction with 3D Objects via Video Generation." *ECCV* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2404.13026-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.13026) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://physdreamer.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/a1600012888/PhysDreamer)
  > Distills material properties from video-generation priors into 3D objects so static assets respond realistically to novel interaction forces.

- **PhysGen (ECCV 2024)** — "PhysGen: Rigid-Body Physics-Grounded Image-to-Video Generation." *ECCV* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2409.18964-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.18964) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://stevenlsw.github.io/physgen/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/stevenlsw/physgen)
  > Simulation-in-the-loop image-to-video: rigid-body simulation of inferred scene physics drives generative rendering under user-specified forces. Distinct from the 2026 PhysGen (2603.00110) already listed.

- **Physics-IQ** — Motamed, S. et al. "Do generative video models learn physical principles from watching videos?" *arXiv* 2501.09038 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2501.09038-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2501.09038) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://physics-iq.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/google-deepmind/physics-iq-benchmark)
  > Original Physics-IQ benchmark (real-video physical understanding across solids, fluids, optics, thermodynamics, magnetism); shows visual realism does not imply physics understanding. The already-listed "Physics-IQ Verified" (2606.18943) is its audited follow-up.

- **ThermoForce** — "ThermoForce: A Physics-Structured Interventional World Model for Building HVAC Control." *arXiv* 2607.03942 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.03942-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.03942)
  > Separates passive forecasting from causal response to control interventions with a physics-structured thermal world model; a clean case study in intervention-valid world modeling.

- **Mechanistic World Models** — "From Observation to Insight: Mechanistic World Models and the Quest for Autonomous Discovery." *arXiv* 2607.12474 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.12474-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.12474)
  > Position paper arguing that scientific discovery requires world models that expose reusable explanatory mechanisms rather than pure predictive accuracy.

- **POKEWORLD** — "What Can Latent World Models Know? Physical Parameter Identifiability in Multimodal Predictive Representations." *arXiv* 2607.27017 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.27017-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.27017)
  > Certificate-gated protocol testing which hidden physical parameters (mass, drag, stiffness) actually enter a latent world model's representation.

- **ODEWorld** — "ODEWorld: A Continuous Predictive Architecture via Physical-Time Flow." *arXiv* 2607.27924 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.27924-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.27924)
  > Learns a continuous latent velocity field in physical time (ODE-parameterized) instead of discrete-step prediction for world modeling of continuous dynamics.

- **PhiZero** — "PhiZero: A World Model Built Around Physical Language." *arXiv* 2607.28624 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.28624-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.28624)
  > Learns a compact discrete "physical language" of world-state transitions from in-the-wild video and predicts in that space rather than in pixels.

- **ClosurePairs** — "Why Does the Future Branch? Identifiable Closure Tests for Stochastic Physical World Models." *arXiv* 2608.00591 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.00591-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.00591)
  > Proves ordinary transitions cannot distinguish state-aliasing from intrinsic stochasticity in physical world models, and gives an identifiable test that can.

- **HERA** — "HERA: Historical Evidence Routing Adapter for Physical Prediction in Latent World Models." *arXiv* 2608.05523 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05523-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05523)
  > Routes preserved historical evidence back into latent predictions so physical events under occlusion remain predictable when the evidence leaves the current view.

- **PhyS** — "Distilling Physical Priors into Streaming World Models." *arXiv* 2608.07981 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.07981-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07981)
  > Injects physics priors into few-step causal streaming world models, addressing prior loss during bidirectional-to-causal distillation.

- **Learned Physical Invariants** — "Correcting a learned physical invariant improves world-model rollouts." *arXiv* 2608.23526 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.23526-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.23526)
  > Recovers an energy-like conserved quantity inside a frozen DreamerV3 latent and projects rollouts back onto its level set, reducing long-horizon rollout error.

## 1.5.2 Climate & Earth System World Models

- **FourCastNet** — Pathak, J. et al. "FourCastNet: A Global Data-driven High-resolution Weather Model using Adaptive Fourier Neural Operators." *arXiv* 2202.11214 (2022). [![arXiv](https://img.shields.io/badge/arXiv-2202.11214-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2202.11214) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/NVlabs/FourCastNet)
  > First 0.25° global data-driven weather emulator; established that neural surrogates can roll the atmospheric state forward at competitive skill and orders-of-magnitude lower cost.

- **ClimaX** — Nguyen, T. et al. "ClimaX: A foundation model for weather and climate." *ICML* 2023. [![arXiv](https://img.shields.io/badge/arXiv-2301.10343-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2301.10343) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/microsoft/ClimaX) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://microsoft.github.io/ClimaX/)
  > Foundation model pretrained on heterogeneous climate simulations, fine-tunable to forecasting, projection, and downscaling of the earth system.

- **NeuralGCM** — Kochkov, D. et al. "Neural General Circulation Models for Weather and Climate." *Nature* (2024). [![arXiv](https://img.shields.io/badge/arXiv-2311.07222-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2311.07222) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/neuralgcm/neuralgcm)
  > Differentiable hybrid of a dynamical core with learned physics; a simulator of the atmosphere spanning weather forecasts to multi-decade climate rollouts.

- **GenCast** — Price, I. et al. "GenCast: Diffusion-based ensemble forecasting for medium-range weather." *Nature* (2025). [![arXiv](https://img.shields.io/badge/arXiv-2312.15796-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2312.15796) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/google-deepmind/graphcast)
  > Probabilistic diffusion successor to GraphCast (already listed): generates skillful forecast ensembles of future global atmospheric states.

- **ACE** — Watt-Meyer, O. et al. "ACE: A fast, skillful learned global atmospheric model for climate prediction." *arXiv* 2310.02074 (2023). [![arXiv](https://img.shields.io/badge/arXiv-2310.02074-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2310.02074) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/ai2cm/ace)
  > Ai2 Climate Emulator: autoregressive neural emulation of a full atmospheric GCM with approximate conservation, stable over multi-year rollouts.

- **Aardvark Weather** — Vaughan, A. et al. "Aardvark weather: end-to-end data-driven weather forecasting." *Nature* (2025). [![arXiv](https://img.shields.io/badge/arXiv-2404.00411-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.00411) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/annavaughan/aardvark-weather-public)
  > Replaces the entire NWP pipeline — observations to state estimation to forecast — with one end-to-end learned system of the atmosphere.

- **Aurora** — Bodnar, C. et al. "A Foundation Model for the Earth System." *Nature* (2025). [![arXiv](https://img.shields.io/badge/arXiv-2405.13063-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2405.13063) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/microsoft/aurora)
  > Earth-system foundation model pretrained on >1M hours of geophysical data; one rollout backbone fine-tuned to air quality, waves, cyclones, and weather.

- **Spherical DYffusion** — Cachay, S. R. et al. "Probabilistic Emulation of a Global Climate Model with Spherical DYffusion." *NeurIPS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2406.14798-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2406.14798) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/Rose-STL-Lab/spherical-dyffusion)
  > Dynamics-informed spherical diffusion emulator producing stable, physically consistent decade-scale probabilistic climate ensembles.

- **Prithvi WxC** — Schmude, J. et al. "Prithvi WxC: Foundation Model for Weather and Climate." *arXiv* 2409.13598 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2409.13598-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.13598) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/NASA-IMPACT/Prithvi-WxC)
  > NASA/IBM open foundation model of atmospheric state, covering forecasting, downscaling, and gravity-wave parameterization from one pretrained backbone.

- **cBottle** — "Climate in a Bottle: Towards a Generative Foundation Model for the Kilometer-Scale Global Atmosphere." *arXiv* 2505.06474 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2505.06474-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.06474) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/NVlabs/cBottle)
  > NVIDIA generative foundation model that samples kilometer-scale global atmospheric states, compressing a cloud-resolving climate simulator into a diffusion model.

- **Earth-o1** — "Earth-o1: A Grid-free Observation-native Atmospheric World Model." *arXiv* 2605.06337 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.06337-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.06337)
  > Models atmospheric dynamics directly from heterogeneous raw observations without forcing them onto predefined spatial grids.

- **VegSim** — "VegSim: A Geospatial World Model for Scenario-Conditioned Vegetation Simulation." *arXiv* 2606.21961 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.21961-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.21961)
  > Answers counterfactual "how would vegetation respond under alternative weather" questions rather than only forecasting the expected trajectory.

- **Observability Forecasting for EO** — "From Surface Forecasting to Observability Forecasting: A Latent World Model for Cloud-Aware EO Monitoring." *arXiv* 2607.13651 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.13651-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.13651)
  > Latent world model that predicts when Earth-observation acquisitions will actually be usable given clouds and weather drivers.

- **Extremes on Rewind** — "Extremes on Rewind: Generating 1,000-Member Ensembles Initialized at a Final Condition." *arXiv* 2608.19008 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.19008-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.19008)
  > Runs generative climate emulation backwards from an observed extreme event to sample large precursor ensembles for attribution and risk analysis.

- **M-JEPA** — "Tracing the Unlabeled Storm: Cross-Variable Transfer in a Lagrangian Atmospheric JEPA Framework." *arXiv* 2608.22358 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22358-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22358)
  > Multiscale JEPA world model of monsoon convection pretrained on continuous atmospheric proxies and transferred to precipitation prediction.

## 1.5.3 Molecular & Biological World Models

- **AI Virtual Cell** — Bunne, C. et al. "How to Build the Virtual Cell with Artificial Intelligence: Priorities and Opportunities." *Cell* (2024). [![arXiv](https://img.shields.io/badge/arXiv-2409.11654-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.11654)
  > Perspective defining AI virtual cells as simulators that predict and steer cell behavior across scales and under perturbations — the world-model framing for cell biology.

- **MDGen** — Jing, B. et al. "Generative Modeling of Molecular Dynamics Trajectories." *NeurIPS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2409.17808-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.17808) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/bjing2016/mdgen)
  > Generates entire molecular-dynamics trajectories, enabling forward simulation, interpolation, upsampling, and inpainting of molecular motion as a flexible MD surrogate.

- **ODesign** — "ODesign: A World Model for Biomolecular Interaction Design." *arXiv* 2510.22304 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.22304-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.22304)
  > All-atom generative world model for designing biomolecular interactions across molecular types with entity- and token-level controllability.

- **HounsWorld** — "HounsWorld: A Multimodal World Model for Hidden Patient-State Readout, Reconstruction, and Simulation." *arXiv* 2608.12904 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.12904-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.12904)
  > Treats CT volumes and clinical language as observations of a shared latent patient state, making diagnosis, reconstruction, and simulation state-dependent predictions.

- **Mol-JEPA** — "Mol-JEPA: A multimodal Joint Embedding Predictive Architecture for Molecules." *arXiv* 2608.22642 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22642-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22642)
  > JEPA-based molecular world model using modality-crossing prediction (2D graph to 3D conformer) instead of chemically invalid augmentations.

## 2.3 Occupancy & BEV Representations

- **Tesla Occupancy Networks** — Elluswamy, A. "Occupancy Networks." *Tesla, CVPR 2022 Workshop on Autonomous Driving keynote* (2022). [![Video](https://img.shields.io/badge/Video-Talk-FF0000?logo=youtube&logoColor=white)](https://www.youtube.com/watch?v=jPCV4GKX9Dw) [![Project](https://img.shields.io/badge/Workshop-Page-0A66C2?logo=googlechrome&logoColor=white)](https://cvpr2022.wad.vision/)
  > Primary technical material on Tesla's production occupancy networks: multi-camera volumetric occupancy plus occupancy flow prediction for general obstacle avoidance (non-arXiv industry source; expanded at Tesla AI Day 2022).

- **Differentiable Raycasting for Self-Supervised Occupancy Forecasting** — Khurana, T. et al. *ECCV* 2022. [![arXiv](https://img.shields.io/badge/arXiv-2210.01917-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2210.01917) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/tarashakhurana/emergent-occ-forecasting)
  > Learns ego-conditioned freespace/occupancy forecasting from raw LiDAR sweeps via differentiable raycasting, letting occupancy emerge without labels.

- **MILE** — Hu, A. et al. "Model-Based Imitation Learning for Urban Driving." *NeurIPS* 2022. [![arXiv](https://img.shields.io/badge/arXiv-2210.10577-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2210.10577) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/wayveai/mile)
  > Wayve's BEV latent world model that jointly learns driving dynamics and policy from offline urban data and can drive from imagined states; a key precursor to GAIA-1.

- **Point Cloud Forecasting as a Proxy for 4D Occupancy Forecasting** — Khurana, T. et al. *CVPR* 2023. [![arXiv](https://img.shields.io/badge/arXiv-2302.13130-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2302.13130) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/tarashakhurana/4d-occ-forecasting)
  > Forecasts a 4D spacetime occupancy field and renders point clouds from it, factoring sensor extrinsics out of self-supervised world modeling; basis of the CVPR Argoverse occupancy forecasting challenge (already listed under Workshops).

- **StreamingFlow** — "StreamingFlow: Streaming Occupancy Forecasting with Asynchronous Multi-modal Data Streams via Neural Ordinary Differential Equation." *arXiv* 2302.09585 (2023). [![arXiv](https://img.shields.io/badge/arXiv-2302.09585-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2302.09585)
  > Neural-ODE BEV state evolution that forecasts occupancy continuously in time from asynchronous camera and LiDAR streams.

- **Cam4DOcc** — "Cam4DOcc: Benchmark for Camera-Only 4D Occupancy Forecasting in Autonomous Driving Applications." *CVPR* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2311.17663-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2311.17663) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/haomo-ai/Cam4DOcc)
  > Standard benchmark and baselines for forecasting how 3D occupancy evolves from camera input only (could alternatively be routed to Benchmarks & Evaluation).

- **UnO** — Agro, B. et al. "UnO: Unsupervised Occupancy Fields for Perception and Forecasting." *CVPR* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2406.08691-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2406.08691) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://waabi.ai/uno/)
  > Continuous 4D occupancy field learned unsupervised from LiDAR, unifying perception and forecasting of the world state without object labels.

- **UniOcc** — "UniOcc: A Unified Benchmark for Occupancy Forecasting and Prediction in Autonomous Driving." *arXiv* 2503.24381 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2503.24381-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.24381) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/tasl-lab/UniOcc)
  > Unifies nuScenes, Waymo, CARLA, and OpenCOOD occupancy data with flow annotations for cross-dataset occupancy forecasting (could alternatively be routed to Benchmarks & Evaluation).

- **GASP** — "GASP: Unifying Geometric and Semantic Self-Supervised Pre-training for Autonomous Driving." *arXiv* 2503.15672 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2503.15672-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.15672)
  > Self-supervised 4D pretraining that predicts continuous spacetime occupancy, ego paths, and distilled foundation-model features as a unified geometric-semantic world representation.

- **RoboOccWorld** — "Occupancy World Model for Robots." *arXiv* 2505.05512 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2505.05512-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.05512)
  > Extends occupancy world modeling from outdoor driving grids to indoor embodied scenes with local-observation-conditioned forecasting.

- **DynaDreamer** — "Ego-Dynamics-Augmented World Model for Autonomous Driving with Zero-Shot Cross-Chassis Adaptation." *arXiv* 2607.13410 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.13410-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.13410)
  > Disentangles ego-motion from scene dynamics in BEV latent world models, freeing capacity for scene modeling and enabling zero-shot transfer across vehicle chassis.
