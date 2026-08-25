# Proposed Additions — Mind / Representational / Agentic World Models & Resources

**Search date:** 2026-08-25
**Prepared for:** README sections 0, 2, 3, Surveys & Position Papers, Benchmarks & Evaluation, Workshops & Challenges, Community Resources, Technical Blogs & Reports.
**Do not merge into README directly — curator review required.**

**Queries run (arXiv + web):** "JEPA world model" (2608 window), "DreamerV4", "model-based RL world model" (2608), "LLM world model / language world model agent" (2608), "text world model", "GUI world model / mobile agent world model" (2608), "multi-agent world model" (2608), "world model safety / adversarial" (2608), "world model benchmark" (2608), "world model survey / position paper" (2608), "occupancy / BEV world model" (2608), "world model memory / long-horizon video" (2608), "world models workshop NeurIPS 2026 / CoRL 2026", "world model lab blog posts July–August 2026", plus targeted classic-paper checks (Craik, Tolman, predictive coding, Dyna, PILCO, VPN, TDM, successor features, TransDreamer, DayDreamer, HarmonyDream, MWM, S4WM, SAVi, SlotFormer, G-SWM, C-SWM, WorldCoder, LeJEPA).

**Result counts:**
- **New entries proposed:** 68 (67 unique resources; WorldSimProbe is proposed for both §3.3 and the Benchmarks table, matching the README's cross-listing convention).
- **Duplicates found during search and skipped (already in README):** WebWorld (2602.14721), Qwen-AgentWorld (2606.24597), WAC / World-Model-Augmented Web Agents (2602.15384), MultiWorld (2604.18564), Drive-OccWorld (2408.14197), Cosmos 3 (2606.02800), DreamerV4 (2509.24527, present in §3.1 — cross-listing to §2.1 proposed below), WorldOlympiad (2606.11129), WBench (2605.25874), MobileWorldBench (2512.14014), ICLR 2026 2nd World Models Workshop, Mila 2026 World Modeling Workshop, World Labs RTFM & Marble blog posts.
- All arXiv IDs below were grepped against README.md — none are present.

---

## 0 · 🧠 Mind World Models — Biological Origins & Foundational Definitions

### → Target: 0.1 Foundational Cognitive & Neuroscientific Works

- **The Nature of Explanation (Craik)** — Craik, K.J.W. *The Nature of Explanation.* Cambridge University Press (1943). [![Paper](https://img.shields.io/badge/Paper-Link-4C566A?logo=readthedocs&logoColor=white)](https://archive.org/details/natureofexplanat0000crai)
  > **Origin of the concept.** First articulation that organisms carry a "small-scale model" of external reality in their heads, enabling them to try out alternatives and react to future situations before they arise.

- **Cognitive Maps in Rats and Men (Tolman)** — Tolman, E.C. "Cognitive Maps in Rats and Men." *Psychological Review* 55(4):189–208 (1948). [![Paper](https://img.shields.io/badge/Paper-Link-4C566A?logo=readthedocs&logoColor=white)](https://psychclassics.yorku.ca/Tolman/Maps/maps.htm)
  > Classic behavioral evidence that animals learn map-like internal representations of the environment rather than mere stimulus-response chains — the ancestral "world model" in psychology.

- **The Hippocampus as a Cognitive Map** — O'Keefe, J. & Nadel, L. *The Hippocampus as a Cognitive Map.* Oxford University Press (1978).
  > Landmark neuroscience synthesis identifying the hippocampus (place cells) as the neural substrate of Tolman's cognitive map; foundation for spatial world-model research.

- **Mental Models (Johnson-Laird)** — Johnson-Laird, P.N. *Mental Models: Towards a Cognitive Science of Language, Inference, and Consciousness.* Harvard University Press (1983).
  > Cognitive-science theory that reasoning operates over constructed internal models of situations rather than formal logic rules — a direct intellectual ancestor of "mental world modeling."

- **Internal Models for Sensorimotor Integration** — Wolpert, D.M., Ghahramani, Z. & Jordan, M.I. "An Internal Model for Sensorimotor Integration." *Science* 269(5232):1880–1882 (1995). [![Paper](https://img.shields.io/badge/Paper-Link-4C566A?logo=readthedocs&logoColor=white)](https://www.science.org/doi/10.1126/science.7569931)
  > Canonical evidence that the brain uses forward models to predict sensory consequences of motor commands — the neuroscience blueprint for action-conditioned prediction.

- **Predictive Coding in the Visual Cortex** — Rao, R.P.N. & Ballard, D.H. "Predictive Coding in the Visual Cortex: A Functional Interpretation of Some Extra-Classical Receptive-Field Effects." *Nature Neuroscience* 2:79–87 (1999). [![Paper](https://img.shields.io/badge/Paper-Link-4C566A?logo=readthedocs&logoColor=white)](https://www.nature.com/articles/nn0199_79)
  > The concrete computational predictive-coding model (predating Friston's free-energy generalization): higher cortical areas predict lower-level activity and feed back prediction errors.

### → Target: 0.2 Formative Computational World Model Papers

- **Making the World Differentiable (Schmidhuber)** — Schmidhuber, J. "Making the World Differentiable: On Using Self-Supervised Fully Recurrent Neural Networks for Dynamic Reinforcement Learning and Planning in Non-Stationary Environments." *TR FKI-126-90, TU Munich* (1990). [![Paper](https://img.shields.io/badge/Paper-Link-4C566A?logo=readthedocs&logoColor=white)](https://people.idsia.ch/~juergen/FKI-126-90_(revised)bw_ocr.pdf)
  > The 1990 recurrent controller–model architecture cited by Ha & Schmidhuber (2018) as the direct ancestor of learned neural world models for planning.

- **Dyna (Sutton)** — Sutton, R.S. "Dyna, an Integrated Architecture for Learning, Planning, and Reacting." *ACM SIGART Bulletin* 2(4):160–163 (1991). [![Paper](https://img.shields.io/badge/Paper-Link-4C566A?logo=readthedocs&logoColor=white)](https://dl.acm.org/doi/10.1145/122344.122377)
  > **Foundational MBRL architecture.** Interleaves real experience with simulated experience from a learned model — the template behind MBPO-style rollouts and modern "Dyna-style" agents.

- **PILCO** — Deisenroth, M.P. & Rasmussen, C.E. "PILCO: A Model-Based and Data-Efficient Approach to Policy Search." *ICML* 2011. [![Paper](https://img.shields.io/badge/Paper-Link-4C566A?logo=readthedocs&logoColor=white)](https://mlg.eng.cam.ac.uk/pub/pdf/DeiRas11.pdf)
  > Gaussian-process dynamics model with analytic uncertainty propagation; long-standing reference point for data-efficient model-based policy search.

- **Embed to Control (E2C)** — Watter, M. et al. "Embed to Control: A Locally Linear Latent Dynamics Model for Control from Raw Images." *NeurIPS* 2015. [![arXiv](https://img.shields.io/badge/arXiv-1506.07365-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1506.07365)
  > Early latent dynamics model learned from pixels with locally linear transitions enabling optimal control in latent space — a precursor of PlaNet-style latent planning.

- **Action-Conditional Video Prediction** — Oh, J. et al. "Action-Conditional Video Prediction using Deep Networks in Atari Games." *NeurIPS* 2015. [![arXiv](https://img.shields.io/badge/arXiv-1507.08750-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1507.08750)
  > First deep action-conditioned video prediction at scale (Atari); established the action-conditional next-frame formulation used by generative world models today.

- **Successor Features** — Barreto, A. et al. "Successor Features for Transfer in Reinforcement Learning." *NeurIPS* 2017. [![arXiv](https://img.shields.io/badge/arXiv-1606.05312-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1606.05312)
  > Generalizes Dayan's successor representation to deep features; decouples environment dynamics from rewards for transfer — a key representational world-model idea.

- **Value Prediction Network (VPN)** — Oh, J., Singh, S. & Lee, H. "Value Prediction Network." *NeurIPS* 2017. [![arXiv](https://img.shields.io/badge/arXiv-1707.03497-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1707.03497)
  > Plans with an abstract model that predicts future values and rewards rather than future observations — direct precursor of MuZero's value-equivalent world model.

- **Imagination-Augmented Agents (I2A)** — Racanière, S., Weber, T. et al. "Imagination-Augmented Agents for Deep Reinforcement Learning." *NeurIPS* 2017. [![arXiv](https://img.shields.io/badge/arXiv-1707.06203-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1707.06203)
  > Learns to interpret imperfect learned-model rollouts as additional context for a model-free policy — an early, influential template for "imagination" in agents.

- **Temporal Difference Models (TDM)** — Pong, V., Gu, S., Dalal, M. & Levine, S. "Temporal Difference Models: Model-Free Deep RL for Model-Based Control." *ICLR* 2018. [![arXiv](https://img.shields.io/badge/arXiv-1802.09081-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1802.09081)
  > Bridges model-free and model-based RL: goal-conditioned value functions trained model-free act as implicit horizon-varying dynamics models for planning.

- **Generative Query Networks (GQN)** — Eslami, S.M.A. et al. "Neural Scene Representation and Rendering." *Science* 360(6394):1204–1210 (2018). [![Paper](https://img.shields.io/badge/Paper-Link-4C566A?logo=readthedocs&logoColor=white)](https://www.science.org/doi/10.1126/science.aar6170)
  > Learns implicit 3D scene representations from posed observations and renders unseen viewpoints — formative for viewpoint-consistent neural scene world models.

- **SimPLe** — Kaiser, Ł. et al. "Model-Based Reinforcement Learning for Atari." *ICLR* 2020. [![arXiv](https://img.shields.io/badge/arXiv-1903.00374-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1903.00374)
  > First demonstration that a learned video-prediction world model supports sample-efficient Atari agents (~100k interactions); origin of the Atari 100k evaluation protocol.

- **The Value Equivalence Principle** — Grimm, C., Barreto, A., Singh, S. & Silver, D. "The Value Equivalence Principle for Model-Based Reinforcement Learning." *NeurIPS* 2020. [![arXiv](https://img.shields.io/badge/arXiv-2011.03506-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2011.03506)
  > Formalizes when a world model only needs to be accurate for value prediction rather than observation reconstruction — theoretical backbone of MuZero-style models.

---

## 2 · 🏗️ Representational World Models

### → Target: 2.1 Latent Dynamics Models (RSSM / Dreamer Family) — new table rows

| Model | Venue | Key Contribution | Links |
|-------|-------|-----------------|-------|
| **C-SWM** | ICLR 2020 | Contrastive structured world models: object-factored latent states and GNN transitions without pixel reconstruction | [![arXiv](https://img.shields.io/badge/arXiv-1911.12247-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1911.12247) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/tkipf/c-swm) |
| **G-SWM** | ICML 2020 | Generative structured world model unifying object interaction, occlusion, multimodal uncertainty, and situation-aware imagination | [![arXiv](https://img.shields.io/badge/arXiv-2010.02054-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2010.02054) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://sites.google.com/view/gswm) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/zhixuan-lin/G-SWM) |
| **SAVi** | ICLR 2022 | Conditional slot-attention on video; object-centric representations that track entities through time | [![arXiv](https://img.shields.io/badge/arXiv-2111.12594-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2111.12594) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/google-research/slot-attention-video) |
| **TransDreamer** | arXiv 2022 | Replaces the RSSM recurrence with a transformer state-space model (TSSM) for imagination-based RL | [![arXiv](https://img.shields.io/badge/arXiv-2202.09481-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2202.09481) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/changchencc/TransDreamer) |
| **DayDreamer** | CoRL 2022 | Dreamer trained directly on physical robots (quadruped walking in 1 hour) without simulators | [![arXiv](https://img.shields.io/badge/arXiv-2206.14176-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2206.14176) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://danijar.com/project/daydreamer/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/danijar/daydreamer) |
| **Masked World Models (MWM)** | CoRL 2022 | Decouples visual representation (masked autoencoding) from dynamics learning for visual robotic control | [![arXiv](https://img.shields.io/badge/arXiv-2206.14244-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2206.14244) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://sites.google.com/view/mwm-rl) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/younggyoseo/MWM) |
| **SlotFormer** | ICLR 2023 | Transformer dynamics over slot representations for unsupervised object-centric visual simulation | [![arXiv](https://img.shields.io/badge/arXiv-2210.05861-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2210.05861) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://slotformer.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/pairlab/SlotFormer) |
| **S4WM** | NeurIPS 2023 | Systematic face-off of RNN, transformer, and S4 world-model backbones; S4-based world model for long-range memory | [![arXiv](https://img.shields.io/badge/arXiv-2307.02064-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2307.02064) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/fdeng18/s4wm) |
| **HarmonyDream** | ICML 2024 | Automatically harmonizes observation-modeling vs. reward-modeling losses inside world-model learning | [![arXiv](https://img.shields.io/badge/arXiv-2310.00344-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2310.00344) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/thuml/HarmonyDream) |
| **DreamerV4** | arXiv 2025 | Scalable shortcut-forcing transformer world model; agents trained purely in imagination from offline data (*cross-list: already in §3.1, missing from this table*) | [![arXiv](https://img.shields.io/badge/arXiv-2509.24527-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2509.24527) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://danijar.com/project/dreamer4/) |

### → Target: 2.2 Joint Embedding Predictive Architectures (JEPA)

- **LeJEPA** — Balestriero, R. & LeCun, Y. "LeJEPA: Provable and Scalable Self-Supervised Learning Without the Heuristics." *arXiv* 2511.08544 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2511.08544-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2511.08544) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/rbalestr-lab/lejepa)
  > **The original LeJEPA paper** (referenced by several §2.2 entries but missing itself). Proves the isotropic Gaussian is the optimal JEPA embedding distribution and enforces it with SIGReg, removing stop-gradients, teacher-student EMA, and schedulers.

- **JEPA-WAM** — "JEPA-WAM: Learning Vision-Language-Action Policies with Joint-Embedding World Modeling." *arXiv* 2608.09381 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09381-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09381) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://spritewithoutice.github.io/JEPA_WAM/)
  > Latent world-action model built in pretrained V-JEPA space; a shared predictor couples latent transition prediction with continuous action generation, reaching 86.3% on LIBERO-Plus when instantiated in a pretrained VLA.

- **PSG-JEPA** — "Is Forward Prediction Enough? Physical State Grounding for JEPA World Models." *arXiv* 2608.06799 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.06799-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.06799)
  > Adds training-only grounding objectives that tie individual latents to robot proprioceptive state and latent pairs to multi-horizon joint-angle changes, improving probing, latent planning, and policy learning.

- **AC-MTM** — "No Gaussian Required: Contrastive Inverse Dynamics for JEPA World Models." *arXiv* 2608.17542 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.17542-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.17542) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/jackboyla/action-contrastive-jepa)
  > Replaces LeWM's SIGReg anti-collapse regularizer with a training-only Action-NCE inverse-dynamics head; a collapsed encoder provably fails the action-discrimination task, so no prescribed embedding geometry is needed.

- **Orthogonal JEPA** — "Orthogonal JEPA: Factorized Predictive States for Latent World Models." *arXiv* 2608.20065 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.20065-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.20065)
  > Replaces the monolithic JEPA target with orthogonally factorized predictive components synthesized back into a full latent state, evaluated across vision, control, health records, and molecular dynamics.

### → Target: 2.3 Occupancy & BEV Representations

- **CascadeOcc** — "CascadeOcc: Rethinking 3D Occupancy World Models with Cascaded VQ Representations." *arXiv* 2606.27644 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.27644-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.27644)
  > Cascaded coarse-to-fine vector-quantized occupancy tokens with a TimeMixer for multi-scale temporal dependencies; strong vision-centric 4D occupancy forecasting and planning without external foundation models.

### → Target: 2.4 Multimodal, Text, Acoustic & Memory-Oriented World Models

- **MemWM** — "MemWM: Memory-Augmented Text-Based World Model." *arXiv* 2608.07107 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.07107-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07107)
  > Conditions text-based next-state imagination on a curated world memory of transition rules, state caches, and hard-to-predict facts; introduces Structured State Fidelity and improves agent success on ALFWorld, WebShop, and ScienceWorld.

- **WorldTrace** — "Addressable Memory for Video World Models." *arXiv* 2608.07408 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.07408-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07408)
  > Training-free addressable KV-cache memory: fixed in-distribution virtual positions keep compressed history retrievable beyond the training horizon; ships LoopBench for return-to-scene evaluation after long detours.

### → Target: 2.5 Symbolic & Knowledge-Graph World Models

- **WorldCoder** — Tang, H., Key, D. & Ellis, K. "WorldCoder, a Model-Based LLM Agent: Building World Models by Writing Code and Interacting with the Environment." *NeurIPS* 2024. [![arXiv](https://img.shields.io/badge/arXiv-2402.12275-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2402.12275)
  > **Missing classic of code world models** (the README's WorldCoder-Bench builds on this line). An LLM agent represents its world model as a Python program synthesized and refined through environment interaction, far more sample-efficient than deep RL.

- **NeSy-WM** — "Towards Zero-Shot Task Transfer with Neurosymbolic World Models." *arXiv* 2608.17959 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.17959-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.17959)
  > Decouples observation reconstruction from reward prediction over learned symbolic state properties, letting a DreamerV3-style world model adapt zero-shot to new reward functions defined on the same symbolic space.

---

## 3 · 🤖 Agentic World Models

### → Target: 3.1 Model-Based Reinforcement Learning (MBRL) — new table row

| Model | Venue | Architecture | Domain | Links |
|-------|-------|-------------|--------|-------|
| **QWM** | arXiv 2026 | World-model test-time search on top of standard Q-learning; policy/value trained only on real transitions to avoid compounding model bias | Robot manipulation (Robomimic, LIBERO) | [![arXiv](https://img.shields.io/badge/arXiv-2608.17163-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.17163) |

### → Target: 3.2 World-Model-Guided Planning

- **DriveFuture** — "DriveFuture: Future-Aware Latent World Models for Autonomous Driving." *arXiv* 2605.09701 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.09701-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.09701)
  > Conditions driving decisions on compact future-aware latent states instead of dense observation- or occupancy-space rollouts, reducing modeling complexity and error accumulation in planner-coupled world models.

### → Target: 3.3 Closed-Loop Simulation & Evaluation

- **WorldSimProbe** — "WorldSimProbe: Diagnosing Simulator Faithfulness in Action-Conditioned World Models for Embodied Manipulation." *arXiv* 2608.09298 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09298-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09298) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://evophys.com/WorldSimProbe/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/pxxq25/WorldSimProbe)
  > Formalizes an "Observable Simulator Contract" (actions must induce agent motion; environment responses must be grounded in that motion) and probes it with five controlled suites over 18,000+ instances across RoboTwin, ManiSkill, and LIBERO.

- **WorldCycle** — "WorldCycle: Self-Verifiable Reinforcement Learning for Long-Horizon Video World Models." *arXiv* 2608.04964 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04964-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04964) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://nevsnev.github.io/Worldcycle/)
  > Turns reversible action cycles into annotation-free verification: a sequence composed with its inverse must return to the initial state, yielding spatial-closure and temporal-consistency rewards (plus the CycleBench diagnostic) that cut state-returning drift by up to 44%.

### → Target: 3.4 Multi-Agent World Models

- **MASS** — "MASS: Multiplayer World Models with Authoritative Shared State." *arXiv* 2608.06257 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.06257-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.06257)
  > Borrows multiplayer-game architecture: a learned Logic Engine advances a single authoritative typed world state from joint actions, while a Rendering Engine decodes consistent per-camera views — scaling to 1,024 concurrent players over 10,000 recurrent steps.

- **Khora** — "Population-Scalable Multi-Agent World Modeling." *arXiv* 2608.08600 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.08600-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.08600)
  > Decouples shared world-state evolution from view-conditioned rendering with a population-agnostic rendering interface, enabling inference-time expansion to arbitrary agent counts without retraining and near-linear scaling in queried views.

### → Target: 3.5 🛡️ Safety-Aware Agentic World Models

- **BadWAM** — "BadWAM: When World-Action Models Dream Right but Act Wrong." *arXiv* 2607.15207 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.15207-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.15207)
  > Introduces World-Action Drift Attacks: small visual perturbations that desynchronize what a world-action model imagines from what it executes, including stealthy imagination-preserving variants that defeat imagine-then-check verification.

- **False Prophets** — "False Prophets: On the Security of World Models in Agentic Systems." *arXiv* 2607.23147 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.23147-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.23147)
  > Systematizes world-model-specific vulnerabilities in LLM agent pipelines with a security benchmark for text-based world models; induced mispredictions reach 95% success and enable command execution, denial of service, and data extraction.

- **DreamGuard** — "DreamGuard: Efficient Runtime Guardrail for LLM Agents via Risk-Aware World Model." *arXiv* 2608.05695 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05695-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05695)
  > Proactive guardrail built on a recurrent risk-aware latent world model that forecasts multi-horizon hazard evidence before action execution, achieving the best safety-utility trade-off at ~25 ms per call.

### → Target: 3.6 LLM / VLM / GUI Agents with World Models

- **EnvACE** — "EnvACE: Internalizing Environment Dynamics via World Rehearsal for Agentic Reinforcement Learning." *arXiv* 2608.06197 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.06197-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.06197) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/Within-yao/EnvACE)
  > A single policy alternates between acting and rehearsing the environment's response to its own tool calls, internalizing an agent world model that also enables private test-time rehearsal before committed execution.

- **WMRL** — "Scaling Automatic Research Agents via World Models." *arXiv* 2608.12564 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.12564-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.12564)
  > Replaces sandboxed environment execution — the RL bottleneck for AutoResearch agents — with a world model, adding online debiasing and inverse-variance denoising with proven convergence gains and 3-4x training speedups.

- **AppDeltaWorld** — "AppDeltaWorld: Transition-Grounded Delta Code World Model for Mobile GUI Agents." *arXiv* 2608.05891 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05891-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05891)
  > Predicts the next GUI as a reachable delta code update (two-level HTML plus generated visual assets) under action-transition constraints; supports closed-loop SFT data construction and world-model-based test-time RL without touching real apps.

- **Mobile World Models for GUI Agents** — "How Mobile World Model Guides GUI Agents?" *arXiv* 2605.10347 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.10347-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.10347)
  > Trains mobile world models across four state representations (delta text, full text, diffusion images, renderable code) and measures downstream utility: code excels in-distribution, text is more robust for online OOD execution, and world models help more as priors than post-hoc verifiers.

---

## 📚 Surveys & Position Papers

### → Target: Autonomous Driving Surveys — new table row

| Paper | Venue | Scope | Link |
|-------|-------|-------|------|
| **Planning-Oriented End-to-End AD** | arXiv 2026 | Architectures, evaluation, and emerging paradigms for E2E driving, including BEV/latent world models (MILE, LAW, WoTE, World4Drive) as planning supervision | [![arXiv](https://img.shields.io/badge/arXiv-2608.20111-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.20111) |

---

## 📊 Benchmarks & Evaluation — new table rows

| Benchmark | Domain | Metric Focus | Links |
|-----------|--------|-------------|-------|
| **WorldExam** | Video world models | 1,474-case hierarchical diagnostic: visual quality, control adherence, spatial consistency, and inherent world reactivity across camera/action/language paradigms | [![arXiv](https://img.shields.io/badge/arXiv-2608.02603-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.02603) |
| **PlayWorld** | Interactive video | Agent Players pursue 171 long-horizon objectives; geometry consistency, interaction fidelity, out-of-sight and insight evolution | [![arXiv](https://img.shields.io/badge/arXiv-2608.13552-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13552) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://kxding.github.io/project/PlayWorld/) |
| **HarnessEval-W** | Visual world models | Agentified harness-style evaluation: 330 cases decomposed into sub-agent diagnoses with verifiable evidence trees over 18 world models | [![arXiv](https://img.shields.io/badge/arXiv-2608.16859-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.16859) |
| **WorldSimProbe** | Robotics / action-conditioned WMs | Simulator-faithfulness contract: action calibration, trajectory coverage, action-source preservation, interaction grounding and dynamics (18k+ instances) | [![arXiv](https://img.shields.io/badge/arXiv-2608.09298-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09298) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://evophys.com/WorldSimProbe/) [![HuggingFace](https://img.shields.io/badge/🤗-Dataset-FFD21E)](https://huggingface.co/datasets/petersonco/worldsimprobe) |
| **WorldOdysseyBench (WorldRoam-Bench)** | Interactive video | 600+ open-world cases, 10-60 s WASD interaction; per-frame action metric, segment drift, controllability-gated physics, trajectory-aware scene/subject memory | [![arXiv](https://img.shields.io/badge/arXiv-2606.31672-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.31672) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://worldroam.amap.com/) |

---

## 🔬 Workshops & Challenges

- **World Models in Physical AI @ NeurIPS 2026** — Sydney; latent dynamics, generative simulation, evaluation, planning/control; co-located AV Causal Reasoning Retrieval Challenge. [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://www.worldmodels-physicalai.com/)
- **Robot Learning with World Models: Capabilities, Frontiers, and Challenges @ NeurIPS 2026** — world models and WAMs for robot reasoning, learning, and evaluation. [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://robowm-ws.github.io/)
- **Continual World Models @ NeurIPS 2026** — Sydney; world models that keep learning after deployment from observation, memory, feedback, and interaction. [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://continual-world-models-workshop.github.io)
- **World Models for High-Stakes Health (WMHS) @ NeurIPS 2026** — Atlanta; patient world models, intervention-aware reasoning, and clinical trial simulation as a falsifiable world-model testbed. [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://wmhs-neurips.github.io/WMHS/)

---

## 🌐 Community Resources & Open Repositories

### → Target: 🛠️ Open Toolkits & Platforms — new table row

| Resource | Focus | Links |
| --- | --- | --- |
| **LeJEPA** | Lean, provable JEPA self-supervised training framework (SIGReg); ~50-line core, heuristics-free | [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/rbalestr-lab/lejepa) [![arXiv](https://img.shields.io/badge/arXiv-2511.08544-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2511.08544) |

### → Target: 📊 Leaderboards & Benchmark Hubs — new table rows

| Resource | Focus | Links |
| --- | --- | --- |
| **WorldRoam-Bench Leaderboard** | Long-horizon stability leaderboard for interactive world models (action, vision, physics, memory) | [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://worldroam.amap.com/) [![arXiv](https://img.shields.io/badge/arXiv-2606.31672-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.31672) |
| **WebWorld Model Collection (Qwen)** | Open WebWorld-8B/14B/32B web world-model checkpoints for agent training and lookahead search | [![HuggingFace](https://img.shields.io/badge/🤗-Models-FFD21E)](https://huggingface.co/Qwen/WebWorld-32B) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/QwenLM/WebWorld) |

### → Target: 🗃️ Datasets & Data Collections — new table rows

| Resource | Focus | Links |
| --- | --- | --- |
| **WorldSimProbe** | Public RoboTwin/LIBERO evaluation packages for action-conditioned world-model faithfulness probing | [![HuggingFace](https://img.shields.io/badge/🤗-Dataset-FFD21E)](https://huggingface.co/datasets/petersonco/worldsimprobe) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/pxxq25/WorldSimProbe) |
| **WebWorldData** | 1M+ open-web interaction trajectories behind the WebWorld world-model series | [![HuggingFace](https://img.shields.io/badge/🤗-Dataset-FFD21E)](https://huggingface.co/datasets/Qwen/WebWorldData) [![arXiv](https://img.shields.io/badge/arXiv-2602.14721-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2602.14721) |

---

## 📝 Selected Technical Blogs & Reports

### → Target: 🇺🇸 English — Official Labs & Primary Sources — new table rows

| Title | Author / Source | Year | Link |
|-------|----------------|------|------|
| **A Functional Taxonomy of World Models** | World Labs (Fei-Fei Li et al.) | 2026 | [![Blog](https://img.shields.io/badge/Blog-Post-F97316?logo=rss&logoColor=white)](https://www.worldlabs.ai/blog/taxonomy-of-world-models) |
| **Building Worlds That Train Robots (R2S2R)** | World Labs | 2026 | [![Blog](https://img.shields.io/badge/Blog-Post-F97316?logo=rss&logoColor=white)](https://www.worldlabs.ai/blog/real-to-sim-to-real) |
| **Into the Omniverse: How Open World Models Push the Frontier of Physical AI** | NVIDIA Blog | 2026 | [![Blog](https://img.shields.io/badge/Blog-Post-F97316?logo=rss&logoColor=white)](https://blogs.nvidia.com/blog/open-world-models-physical-ai/) |
| **State of World Models 2026: Taxonomy, Benchmarks and Open Challenges** | world-models.io (Zenodo) | 2026 | [![Report](https://img.shields.io/badge/Report-Link-4C566A?logo=readthedocs&logoColor=white)](https://world-models.io/reports/state-of-world-models-2026/) |

Notes on the blog rows: the World Labs taxonomy essay (renderers / simulators / planners) is already being cited by academic work such as *A Definition and Roadmap for World Models* (arXiv 2607.06401, in README) and is a primary-source definition piece. The R2S2R post (2026-07-28) documents real-to-sim-to-real world-model training/evaluation for robot policies, in the requested 2026-07-12 → 2026-08-25 window.

---

## Curator checklist

1. Entries above follow the badge and prose conventions of their target sections (bullets with `> ` one-liners for prose sections, table rows matching existing columns).
2. O'Keefe & Nadel (1978) and Johnson-Laird (1983) are book entries without link badges, following the precedent of the Dayan (1993) entry in §0.1; add publisher links if desired.
3. WorldSimProbe is intentionally proposed for both §3.3 and the Benchmarks table, matching how RoboWM-Bench / MiraBench / RoboTrustBench are cross-listed.
4. DreamerV4 is *not* a new entry — the proposal is to cross-list the existing §3.1 entry into the §2.1 table where the rest of the Dreamer family lives.
5. All 26xx arXiv IDs, project pages, GitHub repos, and HF links were resolved during the search session on 2026-08-25 (HTTP 200), except the ACM (Dyna) and science.org (Wolpert, GQN) DOIs, which block automated clients but are canonical publisher links.
