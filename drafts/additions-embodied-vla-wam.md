# Draft additions — 1.3 Embodied AI & Robotics (Generative), 3.2 World-Model-Guided Planning, 3.3 Closed-Loop Simulation & Evaluation

> Curation draft only — do **not** merge into `README.md` without review. All entries below were verified absent from the current README (no arXiv-ID overlap with the 730 IDs already listed).

**Search date:** 2026-08-25

**Sources searched:** arXiv API (`export.arxiv.org`), full 2025–2026 range with emphasis on the 2026-07-12 → 2026-08-25 window (2607 IDs after 2607.27201 and all 2608.\*), plus targeted title searches for missing classics.

**Queries used:** `"world action model"`, `"embodied world model"`, `"robot world model"`, `"world model" AND "vision-language-action"`, `"world model" AND robot`, `"world model" AND manipulation`, `"world model" AND navigation`, `"world model" AND humanoid`, `"world model" AND locomotion/legged`, `"video world model"`, `"world model" AND planning`, `"policy evaluation" AND "world model"`, `real2sim OR "real-to-sim"`, `Cosmos OR UniSim OR "Genie Envisioner"`, and title searches for: UniPi, UniSim, DayDreamer, RoboDreamer, IRASim, GR-1/GR-2, 1X World Model Challenge, AgiBot World, EnerVerse, DreamZero, V-JEPA, NVIDIA Isaac/Cosmos robotics, SIMPLER, Seer, PIVOT-R, ManiGaussian, DreMa, RoboTransfer, GigaBrain-0, UniVLA, LAPA, IGOR, Moto, VidMan, WMPO, SuSIE, CLOVER, VLMPC, Track2Act, ATM, FOREWARN, RialTo, ACDC, URDFormer, Real2Render2Real, PhysWorld, X-Sim, GAF, PEVA, Humanoid World Models.

**Counts:** 152 new entries proposed (13 → 1.3.1, 10 → 1.3.2, 10 → 1.3.3, 74 → 1.3.4, 15 → 1.3.5, 17 → 3.2, 13 → 3.3). 33 distinct already-listed papers (duplicates) were encountered during search and skipped, including AeroAct 2607.14997, GigaWorld-Policy-0.5 2607.13960, FlowWAM 2607.13017, Lumo-2 2607.11270, RoboInter1.5 2607.18709, Xiaomi-Robotics-U0 2607.11643, CheckVLA 2607.26789, Masked Visual Actions 2607.19343, DriftWorld 2607.15065, FeelWorld 2607.24267, ViTacWorld 2607.22530, Robot-Factored WM 2607.22535, Agentic Real2Sim 2607.19190, EnerVerse 2501.01895 / 2505.09723, Genie Envisioner 2508.05635, AgiBot World Colosseo 2503.06669, and DWL 2408.14472.

**Classics status check (per task list):** UniPi (2302.00111), UniSim (2310.06114), RoboDreamer (2404.12377), IRASim (2406.14540), GR-1 (2312.13139), GR-2 (2410.06158), AgiBot World (2503.06669), EnerVerse (2501.01895), DreamZero (2602.15922), V-JEPA 2 (2506.09985), Cosmos Policy (2601.16163), and DreamGen/GR00T-Dreams (2505.12705) are **already listed** — not duplicated here. DayDreamer, the 1X World Model Challenge report, Cosmos-Transfer1, SIMPLER, Seer, and the other classics below were **missing** and are proposed.

**Curation notes:**
- Name collisions inside the new 2608 wave: two distinct papers are titled "SG-WAM" (2608.08839 and 2608.01397) and two are titled "Faster-WAM" (2608.02365 and 2608.04404); both pairs are kept with disambiguating descriptions. The README already lists a different "Fast-WAM" (2603.16666).
- The README's existing "SuSIE" bullet (§1.3.2) links arXiv 2311.18588, which is a different paper; the canonical SuSIE paper is 2310.10639 and is proposed below for 1.3.4.
- Excluded as driving-domain (belong in §1.2 / driving parts of §3.2, not §1.3): GeoWAM 2608.23486, WA-JEPA 2608.20974, BrainWAM 2608.12854, SimWAM 2608.07468, 4D-WAM-driving 2608.10107, DA-WAM 2608.19085, Adaptive-WAM 2608.06008, RISE 2608.20430, PerceptDrive 2607.20175, GeoWorldAD 2607.17521, Auto-JEPA 2607.29031.
- Excluded as out of strict scope (no explicit world model / prediction-action coupling): GR00T N1 2503.14734 (generic VLA), HiFi-UMI 2607.25895, RoboHarness 2607.18060, Teach-and-Grow 2608.17209, ArmnetBench 2607.24481 (real-robot eval infra without prediction), RoboSynChallenge 2608.12416 (competition), Real2Sim2Real-ROCm 2607.22997 (vendor pipeline), Embodied GPT-5.1 2607.23899 (LLM probe).

---

## → 1.3.1 Robotic Manipulation

### Missing classics

- **SWIM** — "Structured World Models from Human Videos." *RSS* 2023. [![arXiv](https://img.shields.io/badge/arXiv-2308.10901-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2308.10901) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://human-world-model.github.io)
  > Trains a world model over a structured, affordance-grounded action space extracted from internet human videos, then fine-tunes with under an hour of real robot interaction for efficient real-world manipulation skill learning.

- **ManiGaussian** — "ManiGaussian: Dynamic Gaussian Splatting for Multi-task Robotic Manipulation." *ECCV* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2403.08321-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2403.08321) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://guanxinglu.github.io/ManiGaussian/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/GuanxingLu/ManiGaussian)
  > Builds a dynamic Gaussian Splatting world model that predicts future scene reconstruction to supervise scene-level spatiotemporal dynamics for language-conditioned multi-task action prediction.

- **ManiGaussian++** — "ManiGaussian++: General Robotic Bimanual Manipulation with Hierarchical Gaussian World Model." *arXiv* 2506.19842 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.19842-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.19842) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/April-Yz/ManiGaussian_Bimanual)
  > Extends ManiGaussian with a hierarchical Gaussian world model that captures multi-body spatiotemporal dynamics for dual-arm collaboration in multi-task bimanual manipulation.

- **DreMa** — "Dream to Manipulate: Compositional World Models Empowering Robot Imitation Learning with Imagination." *ICLR* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2412.14957-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.14957) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://dreamtomanipulate.github.io/)
  > Constructs learnable digital-twin world models by combining Gaussian Splatting with physics simulators, letting robots imagine novel object configurations and generate imagination-augmented demonstrations for imitation learning.

- **PIVOT-R** — "PIVOT-R: Primitive-Driven Waypoint-Aware World Model for Robotic Manipulation." *NeurIPS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2410.10394-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.10394) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/abliao/PIVOT-R)
  > Restricts world-model prediction to task-relevant waypoints via primitive action parsing, pairing a waypoint-aware world model with a lightweight action decoder for language-guided manipulation.

- **GAF** — "GAF: Gaussian Action Field as a 4D Representation for Dynamic World Modeling in Robotic Manipulation." *arXiv* 2506.14135 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.14135-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.14135) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://ChaiYing1.github.io/projects/GAF/)
  > Extends 3D Gaussian Splatting with learnable motion attributes into a Gaussian Action Field, jointly reconstructing the current scene, predicting future frames, and reasoning actions from motion-aware 4D representations.

- **RoboTransfer** — "RoboTransfer: Controllable Geometry-Consistent Video Diffusion for Manipulation Policy Transfer." *arXiv* 2505.23171 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2505.23171-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.23171) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://horizonrobotics.github.io/robot_lab/robotransfer)
  > Geometry-consistent multi-view video diffusion framework that synthesizes robot manipulation data with fine-grained control over backgrounds and object appearance, improving downstream policy transfer.

### New (window 2026-07-12 → 2026-08-25, plus missing 2026 entries)

- **DreamX-Phi 1.0** — "DreamX-Phi 1.0: Action-Conditioned Video World Model for Robotic Manipulation." *arXiv* 2608.13489 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.13489-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13489) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/AMAP-ML/DreamX-Phi)
  > Action-conditioned manipulation video world model that injects per-arm SE(3) transformations via PRoPE-style geometric attention encoding, plus a depth branch and V-JEPA-teacher mask supervision for faithful arm and object dynamics.

- **GeniWorld** — "GeniWorld: A Generalizable Interactive World Model for Robotic Manipulation via Visual Actions." *arXiv* 2608.06332 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.06332-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.06332)
  > Renders numerical robot actions into URDF-based visual action representations to condition a pretrained video generator, decoupling embodiment kinematics from environment dynamics for out-of-distribution policy interaction and evaluation.

- **ABot-PhysWorld** — "ABot-PhysWorld: Interactive World Foundation Model for Robotic Manipulation with Physics Alignment." *arXiv* 2603.23376 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2603.23376-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2603.23376) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/amap-cvlab/ABot-PhysWorld)
  > A 14B action-controllable manipulation world model trained on three million physics-annotated clips with DPO-based post-training and decoupled discriminators that suppress object penetration and anti-gravity artifacts, evaluated on the training-independent EZSbench.

- **EmbodiedVAE** — "EmbodiedVAE: Disentangled Video VAE for Efficient and Controllable Embodied Manipulation." *ECCV* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2608.02990-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.02990)
  > Dual-encoder video VAE with asymmetric spatio-temporal compression that disentangles robot-arm motion from scene content, giving manipulation world models compact and controllable latents.

- **S2-HWM** — "S2-HWM: Sparse Event-Structured Hierarchical World Model for Long-Horizon Surgical Robot Manipulation." *arXiv* 2608.13103 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.13103-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13103)
  > Learns sparse event evidence from latent trajectories to coordinate an event-level manager and a primitive-step worker, with an event transition model enabling variable-duration imagination for sparse-reward surgical manipulation.

- **EgoGenesis** — "EgoGenesis: Egocentric World-Action Modeling with Online Anchored Projective Memory and Action-3D RoPE." *arXiv* 2607.28243 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.28243-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.28243) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://egogenesis.github.io/)
  > Egocentric world-action simulator that synthesizes controllable manipulation videos using a first-frame 3D scene anchor memory and camera-aware 3D rotary action encoding for precise end-effector control during autoregressive generation.

---

## → 1.3.2 Navigation & Scene Understanding

- **WNM-3D** — "WNM-3D: A World Navigation Model with 3D Scene Conditioning for Closed-Loop VLN." *arXiv* 2608.07267 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.07267-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07267)
  > Conditions joint future-view and action generation on geometry-aware representations extracted by a frozen feed-forward geometry encoder from the observed history, targeting closed-loop continuous vision-language navigation.

- **UniNav** — "UniNav: A Unified World-Action Diffusion Model for Visual Navigation." *arXiv* 2608.03244 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.03244-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.03244)
  > Jointly denoises future visual observations and continuous waypoint trajectories in a single diffusion transformer with geometry-aware camera tokens, co-training on trajectory-labeled navigation data and video-only data.

- **SC²-WM** — "SC²-WM: A Self-Correcting World Model with Closed-Loop Feedback for Vision-and-Language Navigation in Continuous Environments." *ICML* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2608.07548-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07548) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/sunrise-ikun/SC2_WM)
  > Derives internal feedback from world-model foresight to refine navigation plans before execution and selectively updates the world model at test time when feedback reveals model capacity insufficiency.

- **UA-NWM** — "Uncertainty-Aware World Model for Aerial Image-Goal Navigation." *arXiv* 2608.05597 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05597-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05597) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://duryi.github.io/UA-NWM-Project-Page)
  > Formulates UAV trajectory scoring as conditional out-of-distribution detection, representing plausible futures with an uncertainty subspace and ranking candidates by the unexplainable residual of the prediction-goal discrepancy.

- **FlowPilot** — "FlowPilot: Real-Time World-Action Modeling for Agile UAV Navigation." *arXiv* 2608.00635 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.00635-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.00635)
  > Compact UAV world-action model that jointly denoises future depth observations and Bernstein-polynomial trajectories with flow matching, running action-centrically onboard for agile real-time navigation.

- **EndoWAM** — "EndoWAM: A Grounded World-Action Model for Generalizable Endoscopic Navigation." *arXiv* 2608.01221 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.01221-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.01221)
  > First world-action model for robotic endoscopy, adding future grounding that predicts task-relevant target regions in future observations to handle tissue deformation, occlusion, and rapid viewpoint change.

- **Monotone-Cost Latent Nav-WM** — "Latent World Models with Monotone Planning Costs for Image-Goal Navigation." *arXiv* 2608.09073 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09073-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09073)
  > Trains a DINO-based latent navigation world model with an autoregressive rollout loss and a Monotone Cost Ranking loss so that CEM planners receive planning costs that reliably order candidate action sequences.

- **DF³** — "DF³: World Modeling via Decoder-Free Feature Forecasting in Autonomous Navigation." *arXiv* 2608.02428 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.02428-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.02428)
  > Forecasts future states entirely in the latent space of a frozen vision foundation model via learnable spatial queries and derives navigation task outputs directly, eliminating pixel decoders from the world-modeling loop.

- **PEF Endovascular WM** — "Progressive Experience Fusion for Multi-Task World Model Control in Endovascular Navigation." *arXiv* 2608.18647 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.18647-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.18647)
  > Trains a multi-task TD-MPC2 controller with progressive experience fusion and adaptive-horizon MPPI planning, achieving 90% success in held-out vasculatures for autonomous endovascular navigation.

- **Depth-Regularized JEPA-WM** — "Depth-Regularized JEPA World Models Learn More Transferable Representations from Real Outdoor Robot Data." *arXiv* 2607.16314 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.16314-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.16314)
  > Combines depth supervision with an isotropy-inducing latent regularizer to learn robust latent dynamics from real agricultural-robot video, improving transferability of outdoor navigation world models.

---

## → 1.3.3 Locomotion & Full-Body Control

### Missing classics

- **DayDreamer** — "DayDreamer: World Models for Physical Robot Learning." *CoRL* 2022. [![arXiv](https://img.shields.io/badge/arXiv-2206.14176-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2206.14176) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://danijar.com/daydreamer) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/danijar/daydreamer)
  > Applies Dreamer world-model learning directly on four physical robots without simulators, most famously teaching an A1 quadruped to walk from scratch in about one hour of real-world interaction.

- **1X World Model Challenge Report** — "Generative World Modelling for Humanoids: 1X World Model Challenge Technical Report." *arXiv* 2510.07092 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.07092-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.07092)
  > First-place solution to both tracks of the 1X humanoid world model challenge, adapting Wan-2.2 TI2V-5B for robot-state-conditioned future frame sampling and training a spatio-temporal transformer for future latent-code compression.

- **HWM** — "Humanoid World Models: Open World Foundation Models for Humanoid Robotics." *arXiv* 2506.01182 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.01182-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.01182)
  > Family of lightweight open-source masked-transformer and flow-matching models that forecast future egocentric video conditioned on humanoid control tokens, trained on 100 hours of humanoid demonstrations.

- **PEVA** — "Whole-Body Conditioned Egocentric Video Prediction." *arXiv* 2506.21552 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.21552-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.21552) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://dannytran123.github.io/PEVA)
  > Trains an autoregressive conditional diffusion transformer on Nymeria to predict egocentric video from relative 3D whole-body pose actions, simulating how physical human actions reshape the first-person view.

### New (window 2026-07-12 → 2026-08-25)

- **DreamMimic** — "DreamMimic: Learning Visuomotor Whole-Body Loco-Manipulation via World Model." *IROS* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2608.22278-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22278) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/DreamMimic/DreamMimic)
  > Distills privileged teacher policies into vision-based humanoid controllers by repurposing an RSSM as an action-conditioned multi-step supervision signal and predictive feature source, with auxiliary heads for privileged state, contact, and object state.

- **GigaBrain-WBC-0.5** — "GigaBrain-WBC-0.5: A Behavior World Model for Robust Whole-Body Control with Environment Interaction." *arXiv* 2608.18234 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.18234-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.18234) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://shepherd1226.github.io/gigabrain-wbc-0.5/)
  > First Behavior World Model for humanoid whole-body control: a causal transformer jointly predicts next action, next state, and the distribution over next latent behavior commands so tracking stays robust when terrain and object contact reshape dynamics.

- **LUCID** — "LUCID: Latent-Skill Unified Control via Imagined Dynamics for Long-Horizon Humanoid Loco-Manipulation." *arXiv* 2608.07746 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.07746-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07746)
  > Hierarchical MBRL framework that freezes a latent-conditioned low-level skill policy and learns a macro-dynamics world model whose imagined rollouts of temporally extended transitions optimize the high-level humanoid policy.

- **ω-0** — "ω-0: A Latent Predictive World Action Model for Concurrent Humanoid Loco-Manipulation." *arXiv* 2608.06375 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.06375-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.06375)
  > Whole-body world-action model that predicts controller-compatible action latents for real humanoid loco-manipulation, coupling compact future-observation embeddings with diffusion-based whole-body action generation instead of reconstructing future videos.

- **DECOWAM** — "DECOWAM: Decoupled Whole-Body World-Action Model for Legged Mobile Manipulation." *arXiv* 2608.20114 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.20114-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.20114)
  > Separates camera ego-motion from base and arm actions through dedicated conditional interfaces on a frozen FastWAM backbone, and introduces the ARMDOG real-robot dataset synchronizing video, whole-body state/action, and language.

- **GraphOp-WM** — "Graph-Operator World Models for Morphology-Parameter Generalization in Continuous Control." *arXiv* 2608.20936 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.20936-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.20936)
  > Represents articulated robots as attributed graphs and factorizes transitions into a morphology-independent local dynamics basis plus a morphology-conditioned structured operator, generalizing world models to unseen link lengths, masses, and actuation.

---

## → 1.3.4 World-Model-Based Vision-Language-Action (VLA) & World Action Models (WAM)

### Missing classics

- **Seer** — "Predictive Inverse Dynamics Models are Scalable Learners for Robotic Manipulation." *ICLR* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2412.15109-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.15109) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://nimolty.github.io/Seer/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/OpenRobotLab/Seer)
  > Canonical predict-then-act formulation: an end-to-end Predictive Inverse Dynamics Model forecasts future visual states and conditions action prediction on them, pretrained on large robot datasets such as DROID.

- **SuSIE** — "Zero-Shot Robotic Manipulation with Pretrained Image-Editing Diffusion Models." *ICLR* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2310.10639-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2310.10639) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](http://rail-berkeley.github.io/susie) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/kvablack/susie)
  > Fine-tunes InstructPix2Pix on human and robot video to hallucinate future subgoal observations from language commands, which a low-level goal-conditioned policy then reaches — the canonical subgoal-image predict-then-act paper. (Note: the README's existing "SuSIE" bullet links a different paper, arXiv 2311.18588.)

- **CLOVER** — "Closed-Loop Visuomotor Control with Generative Expectation for Robotic Manipulation." *NeurIPS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2409.09016-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2409.09016) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/OpenDriveLab/CLOVER)
  > Generates text-conditioned video-diffusion visual plans as reference expectations and uses a measurable embedding space with a feedback-driven controller to close the loop on long-horizon manipulation.

- **VidMan** — "VidMan: Exploiting Implicit Dynamics from Video Diffusion Model for Effective Robot Manipulation." *NeurIPS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2411.09153-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2411.09153)
  > Two-stage dual-process framework that first pretrains a video diffusion model on Open X-Embodiment to predict future visual trajectories, then adapts its implicit dynamics knowledge for action prediction.

- **Moto** — "Moto: Latent Motion Token as the Bridging Language for Learning Robot Manipulation from Videos." *ICCV* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2412.04445-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.04445) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://chenyi99.github.io/moto/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/TencentARC/Moto)
  > Autoregressively pretrains Moto-GPT on hardware-agnostic latent motion tokens tokenized from video frame transitions, then co-fine-tunes for real robot control so motion priors from action-free video transfer to manipulation.

- **LAPA** — "Latent Action Pretraining from Videos." *ICLR* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2410.11758-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.11758) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://latentactionpretraining.github.io) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/LatentActionPretraining/LAPA)
  > Learns VQ-VAE discrete latent actions between video frames as a future-transition code, pretrains a latent VLA on internet videos without robot action labels, and fine-tunes on small robot datasets to ground latent to real actions.

- **IGOR** — "IGOR: Image-GOal Representations are the Atomic Control Units for Foundation Models in Embodied AI." *arXiv* 2411.00785 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2411.00785-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2411.00785) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://www.microsoft.com/en-us/research/project/igor-image-goal-representations/)
  > Compresses visual changes between an image and its goal state into a unified latent action space shared by humans and robots, enabling joint training of foundation policy and world models over internet-scale video.

- **UniVLA** — "UniVLA: Learning to Act Anywhere with Task-centric Latent Actions." *RSS* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2505.06111-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.06111) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/OpenDriveLab/UniVLA)
  > Derives task-centric latent actions from cross-embodiment videos with a latent action model built in DINO feature space, letting one generalist policy transfer across embodiments, perspectives, and environments.

- **LAWM** — "Latent Action Pretraining Through World Modeling." *arXiv* 2509.18428 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2509.18428-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2509.18428)
  > Model-agnostic self-supervised framework that pretrains imitation policies by learning latent action representations from unlabeled robot and human video through world modeling, targeting deployable model sizes.

- **Track2Act** — "Track2Act: Predicting Point Tracks from Internet Videos enables Generalizable Robot Manipulation." *ECCV* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2405.01527-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2405.01527) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://homangab.github.io/track2act/)
  > Predicts goal-conditioned future point tracks from web videos, infers object rigid transforms and end-effector poses from the predicted tracks, and refines execution with a residual policy for zero-shot manipulation.

- **ATM** — "Any-point Trajectory Modeling for Policy Learning." *RSS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2401.00025-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2401.00025) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://xingyu-lin.github.io/atm) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/Large-Trajectory-Model/ATM)
  > Pretrains a trajectory model to predict future tracks of arbitrary points in a video frame from action-free demonstrations, then uses the predicted tracks as dense control guidance for visuomotor policies across 130+ tasks.

- **GigaBrain-0** — "GigaBrain-0: A World Model-Powered Vision-Language-Action Model." *arXiv* 2510.19430 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.19430-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.19430) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://gigabrain0.github.io/)
  > VLA foundation model trained predominantly on world-model-generated data (video generation, real2real, human-transfer, view-transfer, and sim2real data), with RGBD input modeling and embodied chain-of-thought supervision; precursor to the already-listed GigaBrain-0.5M.

- **WMPO** — "WMPO: World Model-based Policy Optimization for Vision-Language-Action Models." *arXiv* 2511.09515 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2511.09515-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2511.09515) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://wm-po.github.io)
  > Runs on-policy GRPO for VLA policies entirely inside a pixel-based action-conditioned world model whose imagined trajectories align with web-pretrained VLA features, enabling self-improvement without physical rollouts.

### New (window 2026-07-12 → 2026-08-25)

- **Hydra-0** — "Hydra-0: Action Flow for Generalist World Modeling and Control." *arXiv* 2608.18077 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.18077-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.18077) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://nvidia-isaac.github.io/video_to_data/hydra-0/)
  > NVIDIA Isaac generalist world model conditioned on action flow (robot actions as pixel motion), reporting r=0.96 policy-evaluation correlation on RoboLab and an emergent inverse mode that maps desired object flow from human demos to executable robot motion.

- **LD4WAM** — "LD4WAM: Learning Latent Dynamics from Human Videos for World Action Models." *arXiv* 2608.22403 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22403-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22403)
  > Pairs a motion-aligned latent dynamics model trained on human videos with a mixture-of-transformers world-dynamics action model that distills embodiment-agnostic latent dynamics from generated futures into robot actions.

- **WAM-OPD** — "WAM-OPD: On-Policy Distillation for World Action Models." *arXiv* 2608.22364 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22364-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22364)
  > Deployment-consistent post-training in which a frozen WAM teacher labels student-visited histories with coherent video and action targets, repairing accelerated students without sparse-reward RL on RoboTwin 2.0.

- **WM-Policy vs. Imitated WAM Separation** — "On the Capability Separation Between World-Model Policy Learning and Imitated World-Action Models." *arXiv* 2608.22197 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22197-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22197)
  > Proves that imitation-trained world-action policies collapse to the observational behavior policy under realizability, formally separating them from policies optimized against an action-conditioned world model.

- **DELE-w0.5** — "Inferring Action from Future Latent State for Robotic Manipulation." *arXiv* 2608.22067 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22067-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22067)
  > Argues video generation is an unnecessary intermediate for world-action modeling and infers action sequences from compact predicted future end states rather than dense frame-by-frame rollouts.

- **ForeTime-VLA** — "ForeTime-VLA: Causal Future-Token Distillation from a World Action Model for Conveyor-Belt Manipulation." *arXiv* 2608.20735 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.20735-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.20735)
  > Distills a future-aware, action-equivalent representation from a frozen Fast-WAM teacher into a dense pi0.5 policy that stays causal at inference, targeting moving-object manipulation on conveyor belts.

- **Surgical Visual-Trajectory WAM** — "Towards Surgical World-Action Modeling: A Preliminary Joint Visual-Trajectory Forecasting for Surgical Motion Planning." *arXiv* 2608.20284 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.20284-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.20284)
  > Jointly forecasts future surgical scenes and instrument trajectories in one world-action model so predicted motion can be evaluated at the trajectory level while remaining consistent with visual scene evolution.

- **HiTac-WAM** — "HiTac-WAM: A Hierarchical Tactile World Action Model for Contact-Rich Robot Manipulation." *arXiv* 2608.19574 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.19574-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.19574)
  > Forecasts future tactile states factorized into a contact-state → 3D-deformation-field → slip-risk hierarchy for each candidate action chunk and ranks candidates by their tactile forecasts before execution.

- **Foresight Without Seeing (ForeWAM)** — "Foresight Without Seeing: Latent Futures for World Action Models." *arXiv* 2608.11605 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.11605-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.11605)
  > Dynamics-conditioned direct-policy WAM whose Future-KV performs a single Video-DiT prefill over the current latent and stochastic future slots, exposing predictive context to the action DiT without decoding future videos.

- **RIFT** — "Keep the Future, Drop the Rollout: RIFT for World Action Models." *arXiv* 2608.11521 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.11521-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.11521)
  > Closed-loop interventions on 40 LIBERO tasks show some WAMs can reuse a fixed final-clean KV cache with ~98% success, motivating rollout-free imagination that keeps future representations while dropping iterative video denoising.

- **StageWAM** — "StageWAM: Joint-Embedding Stage Prediction for World-Action Models in Robot Manipulation." *arXiv* 2608.10780 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.10780-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.10780)
  > Augments a Motus-based WAM with a goal-conditioned Stage-JEPA predictor over frozen V-JEPA2 features, adding a stage-level semantic future on top of the short-term physical video-action future.

- **HarnessWAM** — "HarnessWAM: Bridging Prediction and Deliberation in World Action Models." *arXiv* 2608.09516 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09516-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09516)
  > Agentic framework wrapping WAMs with a VLM task manager that maintains scene beliefs and task graphs, projecting open-ended plans into atomic-skill sequences within the WAM's capability boundary to close the prediction-deliberation gap.

- **TempoWAM** — "Rethink Before You Execute: Adaptive Execution for World Action Models." *arXiv* 2608.09492 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09492-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09492)
  > Plug-and-play execution scheme that monitors task progress online and adaptively decides when a WAM should replan, replacing the fixed action-chunk execution horizon with progress-calibrated timing.

- **SLIM-0.5B** — "SLIM-0.5B: Learning Action-Grounded Predictive Latents for Robot Manipulation." *arXiv* 2608.09771 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09771-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09771) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://kzz1031.github.io/slim-project-page/)
  > Compact 0.5B latent interaction policy that learns action-grounded predictive latents via self-supervised masked trajectory prediction, capturing both action-conditioned transitions and inverse-dynamics structure.

- **World Tokens** — "World Tokens: Enhancing Embodied Policies with Training-Time World Modeling." *arXiv* 2608.09730 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09730-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09730)
  > A World Adapter transforms VLM features into a fixed set of world tokens that condition a jointly fine-tuned future-video denoiser during training only, keeping deployment as cheap as a plain VLA.

- **JEPA-WAM** — "JEPA-WAM: Learning Vision-Language-Action Policies with Joint-Embedding World Modeling." *arXiv* 2608.09381 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09381-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09381) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://spritewithoutice.github.io/JEPA_WAM/)
  > Latent WAM built in pretrained V-JEPA space that couples latent transition prediction and continuous action generation through a shared predictor over a spatially structured joint current-future target.

- **Flex-π** — "Flex-π: A Multi-Stream World-Action Model with Compute Flexibility." *arXiv* 2608.10860 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.10860-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.10860) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://flex-pi.github.io/)
  > Shows a frozen video VAE also encodes 3D pointmaps almost losslessly, letting a 6B mixture-of-transformers WAM jointly denoise RGB, geometry, DINO semantics, and actions, with per-stream dropout enabling anything from action-only to full-generation inference.

- **SG-WAM (semantic guidance)** — "SG-WAM: Text-Grounded and Spatial-aware Semantic Guidance for World-Action Models." *arXiv* 2608.08839 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.08839-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.08839)
  > Uses a VLM-based semantic planner to produce text-grounded and spatial-aware semantic foresight, correcting instruction-video misalignment in WAM future prediction and downstream actions.

- **Vid2WAM** — "Vid2WAM: Distilling Video Diffusion Priors into World Action Models." *arXiv* 2608.08558 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.08558-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.08558) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://qch-fa.github.io/vid2wam-website/)
  > Offline distillation that supervises a compact WAM student with task-conditioned future rollouts from a large video foundation model plus inverse-dynamics pseudo-actions, reducing dependence on expert robot demonstrations.

- **4D-WAM (trajectory fields)** — "4D-WAM: Infusing Spatiotemporal Awareness into World Action Models through Trajectory Fields." *arXiv* 2608.08023 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.08023-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.08023)
  > Model-agnostic training strategy that aligns WAM representations with 3D trajectory fields through motion alignment and destination alignment objectives, closing the 2D-pixel vs. 3D-action representation gap.

- **FACT** — "FACT: Failure-Aware Causal Training for World-Action Models." *arXiv* 2608.10232 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.10232-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.10232) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://fact-wam.github.io/)
  > Causal WAM that predicts future video and task progress conditioned on the executed action, so failure rollouts become valid supervision for action consequences instead of being discarded.

- **PILOT** — "Decoupling Intention from Trajectory: A Representational Deduction Framework for World Action Models." *arXiv* 2608.06994 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.06994-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.06994)
  > Disentangles high-level physical condition evolution from low-level trajectory generation via representational deduction with motion chain-of-thought guidance inside the action model.

- **WA-SpecDec** — "WA-SpecDec: World-Aware Speculative Decoding for Vision-Language-Action Models." *arXiv* 2608.08725 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.08725-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.08725)
  > Injects world-model-derived scene awareness into speculative decoding for VLAs, adapting the token-acceptance tolerance to physical risk so free-space and near-contact deviations are treated differently.

- **GWM-VLA** — "GWM-VLA: Geometry-Aware Latent World Modeling for Vision-Language-Action Learning." *arXiv* 2608.07619 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.07619-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07619)
  > Aggregates multi-view observations into geometry-aware states with VGGT-Ω and predicts next-step target-view patch tokens under shared latent-action representations grounded by robot-action supervision.

- **LAWM-3D** — "LAWM-3D: Learning 3D-Aware Latent Actions from Human Videos for Generalizable Robot World Models." *arXiv* 2608.05706 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05706-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05706)
  > Shows naive multi-view training does not make latent action models 3D-aware due to appearance leakage and inter-camera discrepancies, and proposes fixes for learning 3D-aware latent actions from human videos.

- **JoyAI-RA 0.5** — "JoyAI-RA 0.5: Scaling Robot Manipulation Learning via Dual Action Alignment." *arXiv* 2608.05674 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05674-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05674) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://joyai-ra-05.github.io/)
  > Vision-Language-World-Action framework whose implicit alignment infers latent actions from visual transitions to teach a latent-action-conditioned world model from human, sim, and robot data, while explicit alignment grounds trajectories in a unified action space.

- **DreamWAM** — "DreamWAM: Beyond RGB Future Prediction for World Action Models." *arXiv* 2608.04996 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04996-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04996) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/hustvl/DreamWAM)
  > Reformulates WAM future prediction as structured world modeling across appearance, motion, geometry, and semantics, combining joint RGB-motion latent denoising with gated residual geometry/semantics branches.

- **MobileWAM** — "MobileWAM: Bridging World Action Models to Mobile Manipulation with Chain-of-Foresight." *arXiv* 2608.04657 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04657-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04657)
  > Extends video-backbone WAMs beyond tabletop settings with a three-expert (shared/locomotion/manipulation) action mixture routed by motion intent and chain-of-foresight supervision for whole-body mobile manipulation.

- **Faster-WAM (future conditioning)** — "Faster-WAM: Efficient Inference-Time Future Conditioning for Robust World Action Models." *arXiv* 2608.04404 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04404-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04404)
  > Shows inference-time future conditioning is critical for WAM robustness under distribution shift and preserves it cheaply by computing future representations once and sparsely reusing them.

- **LiLa-WAM** — "LiLa-WAM: Lightweight Latent Reasoning World-Action Model for Robotic Manipulation." *arXiv* 2608.03701 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.03701-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.03701)
  > End-to-end-trainable WAM that reasons about the future in a compact latent space jointly shaped by future-state prediction and action generation, fitting training on a single 24GB GPU.

- **Faster-WAM (DoT)** — "Faster-WAM: Do World Action Models Need Deep Action Modules?" *arXiv* 2608.02365 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.02365-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.02365)
  > Dock-of-Transformer design that treats a pretrained 30-layer video transformer as a representation hub and docks a single-layer action head onto it, decoupling action-module depth from video-backbone depth. (Same name as 2608.04404 but a different paper.)

- **CoWAM** — "CoWAM: Coordination Contracts for Selective Policy Intervention with WAMs." *arXiv* 2608.02578 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.02578-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.02578)
  > Selective intervention layer for bimanual policies that expresses synchronization, role compatibility, and collision convergence as typed coordination contracts checked against WAM-predicted futures before overriding nominal actions.

- **Async WAM Deployment** — "World Action Models in Real Time: An Empirical Study of Smooth Execution via Asynchronous Deployment." *arXiv* 2608.01880 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.01880-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.01880)
  > Compares six asynchronous execution strategies for latency-heavy WAM inference on a 10 Hz bimanual robot, identifying temporal alignment between observations, predictions, and executed commands as the key requirement.

- **SG-WAM (self-guided)** — "SG-WAM: Self-Guided World Modeling in Geometry-Aware Policy Space." *arXiv* 2608.01397 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.01397-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.01397)
  > Learns geometry-aware action-conditioned dynamics directly in policy-derived representation space with learnable dynamics tokens and EMA-generated prediction targets. (Same acronym as 2608.08839 but a different paper.)

- **DynamicWAM** — "DynamicWAM: Dual-Path Motion Conditioning for World-Action Models in Dynamic Manipulation." *arXiv* 2608.00793 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.00793-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.00793) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://dynamicwam.github.io/)
  > Compact WAM for moving-object manipulation that fuses history-flow conditioning through a frozen video VAE with kinematic descriptors in the action expert, deployed with real-time-chunking asynchronous execution.

- **SelfWAM** — "SelfWAM: A Self-Grounded Unified World Action Model for Fast Robot Control." *arXiv* 2608.00725 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.00725-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.00725)
  > Mixture-of-transformers WAM that jointly predicts actions, action-conditioned future frames, and robot self-masks, grounding future prediction in the robot's visible body while keeping a fast action-only inference path.

- **OVTF** — "Disentangling Visuo-Tactile Foresight: Oracle-Guided Interface Discovery for World Action Models." *arXiv* 2608.00547 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.00547-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.00547)
  > Controlled oracle framework supplying verified paired RGB and tactile futures to isolate how visuo-tactile foresight should be structured at the future-to-action interface of tactile WAMs.

- **SCVC** — "Selective Cross-View Consistency for World Action Models: Held-Out Viewpoint Robustness Without Test-Time Camera Information." *arXiv* 2608.21402 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.21402-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.21402)
  > Proves consistency losses on view-covariant WAM outputs shrink legitimate view-specific content, and constrains only the view-invariant action/proprioception/value block for held-out viewpoint robustness.

- **FBFM** — "FBFM: A Training-Free Asynchronous Feedback Mechanism for Flow-Matching in World-Action Models Execution." *arXiv* 2607.29235 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.29235-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.29235)
  > Pushes observation re-grounding inside actively generated WAM action chunks via masked pseudoinverse corrections to the flow-matching velocity field, correcting prediction error at individual time steps.

- **ST-WAM** — "ST-WAM: Semantic-Temporal World Action Model for Robust Manipulation under Visual Distribution Shifts." *arXiv* 2607.28993 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.28993-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.28993)
  > Identifies training-distribution hallucination in pixel-supervised WAMs under visual shift and switches future supervision to DINOv3 semantic features that better preserve task-state distinctions.

- **QuantWAMs** — "QuantWAMs: Calibrating at the Right Granularity for World Action Models." *arXiv* 2607.28405 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.28405-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.28405)
  > Post-training quantization framework tailored to WAMs, with shared-basis outlier calibration, joint video-action Fisher saliency for precision assignment, and fixed-intervention closed-loop calibration.

- **TacWAM** — "TacWAM: Anchor-Guided World Action Model with Mechanics-Aware Tactile Prediction." *arXiv* 2607.28391 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.28391-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.28391)
  > Maps tactile appearance, dense force fields, and deformation flow into a shared latent prediction space with force/torque reconstruction, keeping tactile futures physically meaningful without becoming privileged action cues.

- **DC-WAM** — "DC-WAM: Dynamic-Centric Visual Supervision and Reasoning for World-Action Models." *arXiv* 2607.25918 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.25918-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.25918)
  > Redirects RGB-based WAM future prediction from appearance-dominated reconstruction toward interaction-induced visual dynamics without adding modality-specific predictions or extra deployment inputs.

- **LeapBot-WA** — "LeapBot-WA: World-Anchor Action Models via Predictive Latent Alignments." *arXiv* 2607.23969 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.23969-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.23969) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/LeapWM/leapbot-wa)
  > Operationalizes JEPA as a world anchor for WAMs, replacing pixel synthesis with predictive semantic alignment and an isotropic semantic autoencoder that bridges predictive features and diffusion priors.

- **N0-TWAM** — "N0-TWAM: Scaling Tactile-Native World-Action Model for Contact-Rich Manipulation." *arXiv* 2607.23783 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.23783-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.23783)
  > First large-scale tactile-native WAM, pretrained with visuo-tactile joint training across six embodiments and 450 tasks using the unified NeoForce contact representation and tactile contact events for task staging.

- **WorldDiT** — "WorldDiT: A Unified Diffusion Architecture for World and Action Modeling." *arXiv* 2607.23909 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.23909-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.23909)
  > Sub-billion-parameter diffusion transformer that generates continuous action chunks while predicting normalized future RGB patch targets, sitting on the parameter-vs-success Pareto frontier across four LIBERO suites without a VLM backbone.

- **ContactFlow** — "ContactFlow: A Video Action Conditioning that Transfers Across Embodiments." *arXiv* 2607.26579 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.26579-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.26579)
  > Encodes manipulation as trajectories of 3D contact points between actor and object, giving human and robot interaction videos a shared embodiment-agnostic conditioning signal for a large video world model.

- **Enfold** — "Enfold: Folding World Model Imagination into Predictive Representations for Ultra-Efficient Embodied Control." *arXiv* 2607.26657 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.26657-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.26657) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://zwl666666.github.io/enfold/)
  > Internalizes the future-generative computation of a video world model into a representation predicted from the present alone, supervised by the generator's multi-level intermediate states during training.

- **WCM (World Critic Model)** — "WCM: A World Critic Model for Vision-Language-Action Reinforcement Learning." *arXiv* 2607.29613 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.29613-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.29613)
  > Adds an explicit world-modeling objective to the critic in VLA reinforcement learning so value estimation captures cross-temporal dynamics under partial observability instead of single-frame state approximations.

- **τ0-VLA** — "τ0-VLA: A Hierarchical Robot Foundation Model with World-Model-Guided Test-Time Computation." *arXiv* 2608.16885 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.16885-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.16885) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://tau0-vla.github.io/)
  > Hierarchical robot foundation model trained on 40,115 hours of real-world data whose high-level policy searches over alternative subtasks with world-model guidance before committing, scaling test-time compute on consequential decisions.

- **DreamTrajectory** — "DreamTrajectory: Trajectory-Guided Action Generation with World Model Alignment for Mobile Manipulation." *arXiv* 2608.01381 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.01381-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.01381)
  > Adds an explicit task-space motion plan for coordinated base-arm prediction and a world-model alignment check that verifies predicted action chunks will realize the intended motion before execution.

- **Robust-WAM** — "Robust-WAM: Bridging Generative Pretraining and Semantic Foresight in World-Action Models." *arXiv* 2608.05903 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05903-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05903)
  > Post-training method that keeps the VAE-based generative path of video-pretrained WAMs while adding a lightweight semantic-foresight alignment objective on the action stream for appearance-shift robustness.

- **ContactGuard** — "ContactGuard: Pre-Contact Execution Monitoring with Action-Conditioned Latent World Models." *arXiv* 2608.13438 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.13438-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13438)
  > Predicts the short-horizon latent consequence of a chunked policy's planned actions from unlabeled trajectories and aborts before contact when a lightweight probe flags likely failure in wrist-camera manipulation.

- **FoMo-FD** — "Failure Detection for Surgical Robot Imitation Policies via Flow-Matching World Modeling." *arXiv* 2607.27511 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.27511-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.27511)
  > Learns nominal short-horizon visual dynamics with an action-conditioned flow-matching world model and scores inverse-transport nonconformity of observed latents to detect surgical policy failures without failure demonstrations.

- **Surgical WAM** — "Surgical WAM: A World-Action Model for Data-Efficient Surgical Robot Learning." *arXiv* 2608.11204 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.11204-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.11204)
  > Tests whether action-free endoscopic video pretraining of a surgical world model improves closed-loop dVRK manipulation under a fixed budget of action-labeled demonstrations.

- **Geometric Test-Time Scaling for WAMs** — "Test-Time Scaling for World Action Models via Zero-Shot Geometric Evaluation." *arXiv* 2607.17454 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.17454-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.17454)
  > Training-free selective Best-of-N framework that ranks sampled WAM rollouts by cross-view depth-reprojection consistency of predicted futures, gated by an action-future consistency check on RoboCasa, LIBERO-Long, and RoboTwin 2.0.

- **WA-LQR** — "Steering Robustness into World Action Models via Mechanistic Interpretability and Optimal Control." *arXiv* 2607.14943 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.14943-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.14943)
  > Finds robustness-critical features are linearly separable in some WAM activation spaces and exploits local linearity for training-free contrastive steering plus a reduced-order LQR feedback controller.

- **WorldScape Policy 2.0** — "WorldScape Policy 2.0: Empowering Steerable World Action Modeling with Reasoning-Augmented Memory." *arXiv* 2607.18840 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.18840-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.18840)
  > Controllable WAM with causal short-term visual memory as DiT prefill and long short-term event memory over VLM outputs for progress-aware retrieval and fine-grained language-video-action grounding.

- **BadWAM** — "BadWAM: When World-Action Models Dream Right but Act Wrong." *arXiv* 2607.15207 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.15207-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.15207)
  > Introduces world-action drift attacks — small visual perturbations that break the alignment between what a WAM imagines and what it executes — undermining the assumption that imagined futures can safety-check actions.

- **ShadowDancer** — "ShadowDancer: Teaching Video World Models Any Action by Learning Unified Dynamics Representations from a Video and Its Shadow." *arXiv* 2607.28362 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.28362-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.28362) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://ShadowDancer-1.github.io)
  > Achieves any-action frame-level control of video world models by training on shadow pairs — video pairs replaying the same dynamics under independently resampled appearance — so demonstration-specified dynamics transfer to new scenes.

- **PhyAI** — "PhyAI: Real-Time Physical AI at the Edge, Scalable Rollouts in the Cloud." *arXiv* 2608.03682 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.03682-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.03682) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/mingti-org/phyai)
  > Unified inference engine that serves VLA models and WAMs from one runtime across onboard, edge, and cloud deployments, reporting 1.40-4.65x speedups over official implementations of pi0, pi0.5, and GR00T N1.7.

---

## → 1.3.5 Real2Sim & Simulation Construction

### Missing classics

- **Cosmos-Transfer1** — "Cosmos-Transfer1: Conditional World Generation with Adaptive Multimodal Control." *arXiv* 2503.14492 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2503.14492-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.14492) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/nvidia-cosmos/cosmos-transfer1)
  > NVIDIA's conditional world generator with adaptive, spatially weighted multimodal controls (segmentation, depth, edge) applied to robotics Sim2Real transfer and autonomous-vehicle data enrichment, with real-time generation on a GB200 NVL72 rack.

- **RialTo** — "Reconciling Reality through Simulation: A Real-to-Sim-to-Real Approach for Robust Manipulation." *RSS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2403.03949-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2403.03949) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://real-to-sim-to-real.github.io/RialTo/)
  > Robustifies real-world imitation policies by scanning scenes into on-the-fly digital-twin simulations, running reinforcement learning inside them, and transferring back with an inverse-distillation procedure.

- **ACDC (Digital Cousins)** — "Automated Creation of Digital Cousins for Robust Policy Learning." *CoRL* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2410.07408-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.07408) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://digital-cousins.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/cremebrule/digital-cousins)
  > Automatically converts a single real image into "digital cousin" simulation scenes that preserve geometric and semantic affordances without exact twin modeling, improving sim-to-real robustness over digital twins.

- **URDFormer** — "URDFormer: A Pipeline for Constructing Articulated Simulation Environments from Real-World Images." *RSS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2405.11656-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2405.11656) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://urdformer.github.io) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/WEIRDLabUW/urdformer)
  > Infers articulated URDF scene and object structure directly from single real-world images, providing a scalable pipeline from photos to simulation-ready interactive environments with kinematic structure.

- **Real2Render2Real** — "Real2Render2Real: Scaling Robot Data Without Dynamics Simulation or Robot Hardware." *arXiv* 2505.09601 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2505.09601-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.09601) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://real2render2real.com) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/uynitsuj/real2render2real)
  > Renders thousands of high-fidelity robot-agnostic demonstrations from one smartphone object scan and one human video by reconstructing 3DGS assets and tracking 6-DoF object motion, with no dynamics simulation or robot hardware.

- **X-Sim** — "X-Sim: Cross-Embodiment Learning via Real-to-Sim-to-Real." *arXiv* 2505.07096 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2505.07096-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.07096) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://portal-cornell.github.io/X-Sim/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/portal-cornell/X-Sim)
  > Reconstructs photorealistic simulation from RGBD human video, trains RL policies with object-centric rewards as a dense cross-embodiment signal, and distills them into image-conditioned diffusion policies with online domain adaptation.

- **PhysWorld** — "PhysWorld: From Real Videos to World Models of Deformable Objects via Physics-Aware Demonstration Synthesis." *arXiv* 2510.21447 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.21447-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.21447)
  > Builds physics-consistent MPM digital twins of deformable objects from limited real video via constitutive-model selection and global-to-local property optimization, then synthesizes diverse perturbed demonstrations to train efficient dynamics world models.

### New (window 2026-07-12 → 2026-08-25)

- **Video2DoorTraversal** — "Video2DoorTraversal: Push Door Traversal via Simulated Door Twins." *arXiv* 2608.20251 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.20251-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.20251) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://video2doortraversal.github.io/)
  > Single-video real-to-sim-to-real framework that reconstructs an instance-aligned articulated door twin, refines parameterized skill programs with a simulation-in-the-loop agent, and trains the ArticuACT base-arm-gripper policy for onboard wheel-legged door traversal.

- **Torque-Level Real2Sim2Real** — "Enhancing Sim2Real Transfer for Torque-Controlled Robots through Real2Sim Dynamics Estimation and Reinforcement Learning." *IEEE AIM* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2608.22629-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22629)
  > Identifies friction, inertia, and gravity-compensation parameters of a 7-DOF Franka Panda by trajectory matching with genetic-algorithm optimization, then trains TQC reinforcement-learning policies on the calibrated dynamics for torque-level Sim2Real transfer.

- **GCA** — "Learning Implicit Constitutive Laws for Dynamic 3D Gaussian Splatting from Monocular Videos." *arXiv* 2608.22102 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22102-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22102)
  > Learns implicit constitutive laws of deformable objects represented as dynamic 3D Gaussians from a single fixed-viewpoint video, using rank-based depth-geometric anchors and LoRA adaptation to keep physical dynamics recovery stable in the monocular setting.

- **R2S-EGO** — "R2S-EGO: Dual-Proxy Refinement for Sparse-Capture Real-to-Sim." *arXiv* 2608.06827 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.06827-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.06827)
  > Couples a simulator-derived robot proxy defining behavior-scoped executable view queries with a capture-anchored geometry proxy, assimilating camera-controlled synthesized views as pseudo-observations to refine real-to-sim visual assets from sparse human captures.

- **RORA** — "RORA: Realistic Object Reconstruction with Articulation." *arXiv* 2608.04842 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04842-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04842)
  > First end-to-end pipeline that reconstructs simulation-ready assets with accurate multi-joint articulation from a single static object video, exporting a hybrid 3DGS-plus-mesh representation via a suggestion-based human-in-the-loop process.

- **Sling2Sim2Real** — "Sling2Sim2Real: One-Shot Elastic System Identification for Non-Destructive Slingshot Policy Learning." *IROS* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2607.23268-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.23268)
  > One-shot Real2Sim2Real framework that identifies elastic object parameters from a single non-destructive interaction, enabling large-scale safe policy learning in simulation for slingshot-style elastic object manipulation.

- **TableVerse** — "TableVerse: A Large-scale Tabletop Dataset with Real-world Grounded Layouts for Generalizable Manipulation." *arXiv* 2607.21017 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.21017-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.21017)
  > Fully automated Real2Sim pipeline that deterministically reconstructs simulation-ready cluttered tabletop environments with metric scale and verified mechanical stability from unstructured internet images, plus task-conditioned trajectory generation.

- **World Translation** — "World Translation: Minimizing Sim-to-Real Gap with Backward Dynamics Extraction and Unpaired Domain Translation." *arXiv* 2607.18154 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.18154-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.18154)
  > Combines deterministic-but-imperfect simulators with learned real-world dynamics via backward dynamics extraction and unpaired domain translation, addressing partial-observability failures of learned real-to-sim dynamics such as sudden unheralded contact events.

---

## → 3.2 World-Model-Guided Planning & Decision-Making (robotics)

### Missing classics

- **FOREWARN** — "From Foresight to Forethought: VLM-In-the-Loop Policy Steering via Latent Alignment." *arXiv* 2502.01828 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2502.01828-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.01828) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://yilin-wu98.github.io/forewarn/)
  > Decouples foresight (latent world-model rollouts of candidate action plans) from forethought (VLM reasoning over decoded outcomes), unlocking VLMs as open-vocabulary verifiers for runtime steering of generative robot policies.

### New (window 2026-07-12 → 2026-08-25)

- **World Action Planner** — "World Action Planner: Generalizable Decision-Making with Action-Conditioned World Models." *arXiv* 2607.27599 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.27599-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.27599) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://worldactionplanner.github.io)
  > VLM-driven planning system that proposes action plans and iteratively refines them via optimization and search over imagined rollouts of a multi-task pose-image-conditioned world model, outperforming end-to-end VLAs and WAMs on compositional and zero-shot generalization.

- **SAGE** — "SAGE: Subgoal-Conditioned Action Generation for Latent World Model Planning." *arXiv* 2607.17973 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.17973-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.17973)
  > Replaces random proposal initialization in latent world-model planning with a goal-conditioned generator that predicts reachable latent subgoals at multiple temporal scales to condition candidate action-sequence generation.

- **Affordance Planning with Real-to-Sim Conversion** — "Affordance-Based Manipulation Planning with Text Goals and Sim-to-Real Generalisation via Real-to-Sim Image Conversion." *arXiv* 2607.11004 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.11004-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.11004)
  > Plans manipulation by predicting action effects as visual futures and scoring candidate plans by multimodal agreement with run-time text goals, adding real-to-sim image conversion so the visual world model transfers to a physical robot setup.

- **RP1 (Reinforced Planning)** — "Reinforced Planning with Latent World Models." *arXiv* 2608.18669 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.18669-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.18669)
  > Learns the plan-improvement operator itself — a critic that evaluates imagined outcomes and an optimizer that revises multi-step plans — trained fully offline from imagined world-model rollouts rather than hand-designed search.

- **Orbit-Planner** — "Orbit-Planner: Towards Latent World Models for On-Orbit Obstacle Avoidance of Satellite Agents." *AP-GARSS* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2608.16651-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.16651) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://zhijianli2003.github.io/Orbit_Planner/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/ZhijianLi2003/Orbit_Planner)
  > Two-stage latent world model that rolls out action-conditioned spacecraft dynamics in latent space with a Physics Probe decoding physical state changes, attaining 91.7% closed-loop obstacle-avoidance success in Isaac Sim.

- **ELWM** — "Energy-Structured Latent World Models with Neural Time Fields for Physically Consistent Open-World Motion Planning." *arXiv* 2608.09876 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09876-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09876)
  > Structures latent world-model states to explicitly carry energy and momentum with strictly causal dissipation and control ports, guaranteeing physically consistent predictions for open-world motion planning from RGB-D and inertial histories.

- **hint²** — "hint²: Hierarchical World Models for Inference-Time Temporal Logic Guidance." *arXiv* 2608.13678 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.13678-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13678) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://anonymous-hint2.github.io/)
  > Guides short-horizon chunked manipulation policies toward satisfying long-horizon linear temporal logic specifications at inference time by deriving complementary guidance objectives from hierarchical world models at two abstraction levels.

- **Onto-EV-WM** — "Ontology-Grounded World Models for Failure Diagnosis and Closed-Loop Repair in Physical AI Systems." *arXiv* 2608.13901 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.13901-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13901)
  > Layers an ontology-grounded diagnosis and verification-gated correction interface over event-scored world models, recording unmet task predicates and routing failures to available correction mechanisms for closed-loop repair.

- **Traj-LeWM** — "Traj-LeWM: Path-Aware World-Model Planning via Latent Trajectory Cost." *arXiv* 2608.14125 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.14125-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.14125)
  > Extends the lightweight LeWM visual world model with a goal-conditioned latent trajectory cost so planning ranks candidate action sequences by the evolution of the whole predicted trajectory rather than predicted endpoint distance alone.

- **Neurosymbolic World Models** — "Towards Zero-Shot Task Transfer with Neurosymbolic World Models." *arXiv* 2608.17959 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.17959-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.17959)
  > World-model formulation whose reward prediction depends only on structured symbolic latent components, decoupling reconstruction from reward so planners adapt zero-shot to new reward functions over the same symbolic state space.

- **ProWorld** — "ProWorld: Progress-Aware Hyperbolic World Models for Long-Horizon Visual Goal Reaching." *arXiv* 2608.01926 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.01926-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.01926)
  > Augments JEPA-style world models with a goal-conditioned progress order embedded in hyperbolic space, so long-horizon visual goal-reaching rollouts respect coarse-to-fine progress toward the goal instead of only local transition consistency.

- **SR-WM** — "Beyond Instance Slots: Semantically Rich World Models for Physical Interaction Planning." *arXiv* 2608.22294 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22294-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22294)
  > Task-conditioned world model structured around five functional roles — gripper, target, goal, relation, and phase — that checks whether candidate actions produce task-consistent futures while preserving essential relations.

- **DA-LeWM** — "Decision-Metric Alignment in Latent World Models: Diagnostics and Action-Conditioned Objectives for MPC Planning." *arXiv* 2608.18746 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.18746-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.18746)
  > Introduces Plan-Real and CEM-stage Spearman diagnostics for whether latent goal distance ranks action candidates by real task progress, and adds inverse-dynamics and demonstration-conditioned goal-action heads to close the alignment gap.

- **Objective-Bottleneck Study** — "The Objective Is the Bottleneck: Latent World Models Encode What Their Planners Cannot Use." *arXiv* 2608.12959 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.12959-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.12959) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/joyjeet-singh/tinylab)
  > Empirical study showing latent world models encode task-relevant information that their planning objectives cannot exploit, locating the planning bottleneck in the objective rather than the learned representation.

- **VERDI** — "verdi: retrieval is not transfer for continual world model optimization." *arXiv* 2608.09537 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09537-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09537)
  > Continual framework for evidence-licensed optimization of foundation world models that treats retrieved strategies as hypotheses requiring target-side experimental validation before they count as transferable knowledge.

- **WM-Grounded LLM Marine Planning** — "World-Model-Grounded LLM Planning for AUV and ASV Navigation Near Offshore Wind Farms." *IROS Workshops* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2608.19661-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.19661)
  > Grounds LLM mission planning for 6-DOF AUVs and 3-DOF ASVs in a physics-grounded neural world model with three-phase gradient trajectory optimization and MPC-style closed-loop replanning behind a trust-region guard.

---

## → 3.3 Closed-Loop Simulation & Policy Evaluation

### Missing classics

- **SIMPLER** — "Evaluating Real-World Robot Manipulation Policies in Simulation." *CoRL* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2405.05941-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2405.05941) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://simpler-env.github.io) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/simpler-env/SimplerEnv)
  > The de-facto standard simulated evaluation suite for real-robot manipulation policies, mitigating control and visual real-to-sim disparities and demonstrating strong correlation between simulated and real-world policy performance.

### New (window 2026-07-12 → 2026-08-25)

- **KineBench** — "KineBench: Benchmarking Embodied World Models via IDM-Free Kinematic Grounding." *ECCV* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2607.19876-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.19876)
  > IDM-free closed-loop benchmark that grounds world-model-generated videos kinematically with cascaded visual foundation models, removing the attribution ambiguity introduced by brittle learned inverse-dynamics action extractors.

- **XEWorld** — "XEWorld: Can Action-Conditioned World Models Generalize to Unseen Robot Embodiments?" *arXiv* 2608.05799 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05799-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05799)
  > Controlled cross-embodiment testbed that evaluates action-conditioned world models on held-out robots in physically identical scenes, finding current models behave as 2D visual pattern matchers governed by visual rather than kinematic similarity.

- **WorldSimProbe** — "WorldSimProbe: Diagnosing Simulator Faithfulness in Action-Conditioned World Models for Embodied Manipulation." *arXiv* 2608.09298 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09298-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09298) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://evophys.com/WorldSimProbe/)
  > Formalizes an Observable Simulator Contract — supplied actions must induce corresponding agent motion and environment responses grounded in that motion — and diagnoses action-conditioned world models against it beyond visual quality.

- **SurgWMBench** — "SurgWMBench: A Vision-Based Benchmark for World-Modeling Surgical Instrument Motion Planning." *arXiv* 2608.08070 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.08070-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.08070)
  > Benchmark evaluating whether surgical world models jointly capture future video state transitions and instrument motion dynamics, moving beyond FVD-style generation metrics that are poorly aligned with instrument motion.

- **H2R-Bench** — "H2R-Bench: Benchmarking Human-to-Robot Manipulation Video Generation in World Models." *arXiv* 2608.13049 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.13049-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13049)
  > Benchmark for cross-embodiment human-to-robot video generation in which world models must transform egocentric human demonstrations into robot manipulation videos under specified target embodiments.

- **CG-World** — "CG-World: A Large-Scale World-State Dataset and Protocol for World Models." *arXiv* 2607.26452 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.26452-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.26452)
  > ~850K temporally aligned segments from industrial CG production pipelines with explicit latent states, events, physics caches, and branch lineages, supporting intervention learning and counterfactual evaluation of world models.

- **BWM** — "BWM: A Low-Cost High-Fidelity World Simulator for Robot Learning." *arXiv* 2607.29302 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.29302-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.29302)
  > Open-source action-conditioned world simulator combining initial-environment guidance, dynamic visual history, and temporally aligned robot-action conditioning for stateful autoregressive prediction of action consequences before physical execution.

- **CaliBench** — "CaliBench: Are the Stochastic Dynamics of Video World Models Physically Calibrated?" *arXiv* 2608.16829 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.16829-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.16829)
  > Tests aleatoric calibration of video world models by scoring generations in discrete outcome spaces with closed-form reference distributions (Galton boards, dice, roulette), decomposing performance into scorability and calibration.

- **GAUGE** — "GAUGE: A Measurement-Grounded Benchmark for Physical Fidelity in Simulation Engines and Video World Models." *arXiv* 2608.05948 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05948-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05948)
  > Diagnostic benchmark of 22 controlled task families over rigid bodies, cables, textiles, and volumetric deformables, grounded in real-world trajectories with calibrated metadata, that jointly evaluates physics engines and generative video world models.

- **VIScore** — "VIScore: Diagnosing Planning-Relevant Quality in Latent World Models." *arXiv* 2608.11174 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.11174-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.11174)
  > Diagnoses which latent-space properties actually correlate with planning success, showing flexible VISReg isotropic regularization improves out-of-domain planning where the SSL-standard SIGReg does not.

- **Where World Models Break** — "Where World Models Break: Natural-Input Failure Discovery." *arXiv* 2608.22421 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.22421-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.22421)
  > Formalizes natural-input failure discovery for action-conditioned world models: under a finite query budget, finding environment-valid conditions and action prefixes that induce severe, seed-reproducible prediction failures.

- **Paired Exact-Reset Evaluation** — "Paired Exact-Reset Evaluation of a Prediction-Derived Medium-to-Full World-Model Cascade." *arXiv* 2608.14650 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.14650-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.14650)
  > Paired exact-reset audit protocol on a 1,600-state PushT bank that executes all candidate actions from identical reset states, defining when routing from a Medium to a frozen Full world-model predictor justifies its sequential overhead.
