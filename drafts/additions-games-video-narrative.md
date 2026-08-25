# Proposed additions — §1.1 Games / §1.6 Video World Models / §1.7 Persistent Narrative

**Status:** Draft for parent-agent integration. Do **not** merge into README.md as-is; each entry lists its recommended exact insertion subsection.

- **Search date:** 2026-08-25
- **Sources searched:** arXiv export API (`export.arxiv.org/api/query`, sorted by `submittedDate`, paged), targeted `id_list` metadata fetches for every proposed entry, and web verification of non-arXiv primary sources.
- **Queries used:** `"world model"`, `"world models"`, `"interactive world"`, `"neural game engine"`, `"action-conditioned video"`, `"video world model"`, `"streaming world model"`, `"multi-shot video"`, `"persistent narrative"`, `"game engine" AND diffusion`, `"playable" AND "world model"`, `"self forcing"`, `"autoregressive video diffusion"`, `"long video generation" AND memory`, `"world simulator"`, plus targeted title searches (`GameGAN`, `Playable Video Generation`, `Promptable Game Models`, `Cosmos-Predict`, `Cosmos-Transfer`, `RLVR-World`, `MovieAgent`, `Jasmine`, `World and Human Action Model`).
- **Counts:** 1,223 unique arXiv hits collected → 188 skipped as already present in README (any section) → **81 proposed NEW arXiv entries + 7 proposed non-arXiv primary resources (Nature paper + 6 official lab posts) = 88 proposed entries.** ~35 further candidates considered and excluded (see "Considered but excluded" at the bottom).
- **Recency coverage:** every arXiv ID > 2607.27201 and all 2608.xxxxx matching the queries were triaged; 2024–mid-2026 gaps vs the README were also filled.
- **Scope tags used in the index:** `S` = models explicit state / latent state; `D` = predicts evolution under action / intervention / waiting / imagination; `P` = supports planning, policy, evaluation, controllable simulation, or executable rollouts. Every entry carries ≥2 tags per the inclusion rule.

## Index of proposed entries

| arXiv ID | ShortName | Target subsection | In-scope |
|---|---|---|---|
| 1507.08750 | Action-Conditional Video Prediction | 1.1.1 | D+P |
| 2003.10520 | Neural Game Engine | 1.1.1 | D+P |
| 2005.12126 | GameGAN | 1.1.1 | S+D |
| 2411.00769 | GameGen-X | 1.1.1 | D+P |
| 2412.00887 | PlayGen | 1.1.1 | D+P |
| 2412.03568 | The Matrix | 1.1.1 | D+P |
| 2506.01380 | Next-Frame Diffusion | 1.1.1 | D+P |
| 2506.09995 | PlayerOne | 1.1.1 | S+D |
| 2506.17201 | Hunyuan-GameCraft | 1.1.1 | D+P |
| — (blog) | Mirage (Dynamics Lab) | 1.1.1 | D+P |
| 2101.12195 | Playable Video Generation | 1.1.2 | S+D |
| 2303.13472 | Promptable Game Models | 1.1.2 | S+D+P |
| — (Nature) | WHAM / Muse | 1.1.2 | S+D+P |
| 2510.27002 | Jasmine | 1.1.2 | D+P |
| 2604.02330 | ActionParty | 1.1.2 | S+D |
| 2607.12592 | WanToFight | 1.1.2 | D+P |
| 2607.21594 | WorldWeaver (W²) | 1.1.2 | S+D |
| 2608.06257 | MASS | 1.1.2 | S+D+P |
| 2608.13492 | AlayaWorld v1.1 report | 1.1.2 (update flag) | S+D+P |
| — (blog) | Odyssey-1 / Odyssey-2 | 1.1.2 | D+P |
| — (blog) | Oasis 2.0 (Decart) | 1.1.2 | D+P |
| — (blog) | Oasis 3 (Decart) | 1.1.2 | D+P |
| 2502.00466 | EDELINE | 1.1.3 | S+D+P |
| 2507.17744 | Yume | 1.1.3 | D+P |
| 2510.03198 | Memory Forcing | 1.1.3 | S+D |
| 2512.04040 | RELIC | 1.1.3 | S+D+P |
| 2512.14614 | WorldPlay | 1.1.3 | S+D+P |
| 2512.22096 | Yume-1.5 | 1.1.3 | D+P |
| 2603.06679 | MultiGen | 1.1.3 | S+D+P |
| 2605.18601 | Incantation | 1.1.3 | D+P |
| 2606.30045 | NeuWorld | 1.1.3 | S+D |
| 2607.07534 | LingBot-World 2.0 | 1.1.3 | D+P |
| 2607.18703 | AlayaRenderer-Flash | 1.1.3 | S+P |
| 2608.05070 | HelloWorld | 1.1.3 | D+P |
| 2608.13546 | Alaya-EVOKE | 1.1.3 | S+D+P |
| 2608.14530 | Marionette | 1.1.3 | S+D+P |
| 2608.21439 | WorldMind | 1.1.3 | S+D+P |
| 2608.23565 | ReWorld | 1.1.3 | S+D+P |
| 2410.23277 | SlowFast-VGen | 1.6 | S+D |
| 2412.07772 | CausVid | 1.6 | D+P |
| 2502.07825 | DWS | 1.6 | D+P |
| 2502.12632 | MALT Diffusion | 1.6 | S+P |
| 2503.14492 | Cosmos-Transfer1 | 1.6 | D+P |
| 2503.19325 | FAR | 1.6 | S+P |
| 2504.05298 | TTT-Video | 1.6 | S+P |
| 2504.12626 | FramePack | 1.6 | S+P |
| 2504.13074 | SkyReels-V2 | 1.6 | D+P |
| 2505.13211 | MAGI-1 | 1.6 | D+P |
| 2508.15720 | WorldWeaver | 1.6 | S+P |
| 2509.23958 | RLIR | 1.6 | D+P |
| 2510.02283 | Self-Forcing++ | 1.6 | D+P |
| 2511.12940 | RAD | 1.6 | S+P |
| 2512.04519 | VideoSSM | 1.6 | S+P |
| 2603.07145 | LiveWorld | 1.6 | S+D |
| 2603.13405 | Anchor Forcing | 1.6 | D+P |
| 2603.17117 | MosaicMem | 1.6 | S+D |
| 2605.16003 | Echo-Forcing | 1.6 | S+D |
| 2605.25333 | ReMind | 1.6 | S+D |
| 2606.07967 | DisCo | 1.6 | D+P |
| 2607.11836 | Cycle-World | 1.6 | D+P |
| 2607.20368 | Self Gradient Forcing | 1.6 | S+P |
| 2607.26694 | Visko Orbis 1.0 | 1.6 | D+P |
| 2607.27110 | FreqForcing | 1.6 | D+P |
| 2607.28362 | ShadowDancer | 1.6 | D+P |
| 2608.01127 | MiniWorld | 1.6 | D+P |
| 2608.04653 | CoCo | 1.6 | D+P |
| 2608.04964 | WorldCycle | 1.6 | D+P |
| 2608.07408 | WorldTrace | 1.6 | S+P |
| 2608.07981 | PhyS | 1.6 | D+P |
| 2608.09926 | LDR | 1.6 | S+D |
| 2608.10439 | Stream Forcing | 1.6 | D+P |
| 2608.14022 | ForgeWM | 1.6 | D+P |
| 2608.23189 | EchoWM | 1.6 | D+P |
| — (blog) | Sora 2 (OpenAI) | 1.6 | D+P |
| 2605.12496 | CausalCine | 1.7.1 | S+D+P |
| 2608.04956 | ContextMaster | 1.7.1 | S+D+P |
| 2608.05776 | Vorch-Director | 1.7.1 | S+D |
| 2605.23610 | EM-Vid | 1.7.2 | S+D |
| 2606.20799 | GroundShot | 1.7.2 | S+P |
| 2606.21661 | UnityShots | 1.7.2 | S+D |
| 2607.15772 | SlotMem | 1.7.2 | S+D |
| 2608.23383 | JoyAI-Echo-1.5 | 1.7.2 | S+D+P |
| 2412.02259 | VideoGen-of-Thought | 1.7.3 | S+P |
| 2503.07314 | MovieAgent | 1.7.3 | S+P |
| 2507.18634 | Captain Cinema | 1.7.3 | S+P |
| 2510.22431 | Hollywood Town | 1.7.3 | S+P |
| 2605.26525 | ReCA | 1.7.3 | S+D+P |

**Name-clash warnings for the integrator:**
- *WorldWeaver* appears twice: 2508.15720 (ByteDance/HKU, rich-perception long video, → 1.6) and 2607.21594 (UCLA/Adobe, multi-agent world state registers, → 1.1.2). Disambiguate as "WorldWeaver" and "WorldWeaver (W²)".
- README already contains a game entry named **SCOPE** (2605.23345, §1.1.3) and a §2.4 entry named **Mirage / Latent Spatial Memory** (2606.09828). The proposed *Mirage* below is the unrelated Dynamics Lab game engine; the arXiv paper "SCOPE: Score-Isolated Agentic Optimization" (2608.15043) was excluded (see bottom).
- **AlayaWorld v1.1 report** (2608.13492) is an updated technical report of the AlayaWorld entry already in §1.1.2 (2607.06291); the integrator may prefer updating the existing entry rather than adding a new row. An earlier v1.0 full report also exists (2607.18367).

---

## Proposed entries

### Target section: 1.1.1 Pixel-Space Diffusion Models

*(the first three are pre-diffusion classics; recommended for the top of 1.1.1 as historical precursors, or for §0.2 if the curator prefers)*

- **Action-Conditional Video Prediction** — Oh, J. et al. "Action-Conditional Video Prediction using Deep Networks in Atari Games." *NeurIPS* 2015. [![arXiv](https://img.shields.io/badge/arXiv-1507.08750-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/1507.08750)
  > Foundational neural game simulator: encoding–action-transformation–decoding networks generate ~100-step action-conditional Atari futures that remain useful for control, predating all modern neural game engines.

- **Neural Game Engine** — Bamford, C. & Lucas, S. "Neural Game Engine: Accurate learning of generalizable forward models from pixels." *arXiv* 2003.10520 (2020). [![arXiv](https://img.shields.io/badge/arXiv-2003.10520-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2003.10520) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/Bam4d/Neural-Game-Engine)
  > Coined the "neural game engine" framing: learns pixel-level forward models of GVGAI games (with reward prediction) that generalize to unseen level sizes and plug into MCTS and model-based RL.

- **GameGAN** — Kim, S.W. et al. "Learning to Simulate Dynamic Environments with GameGAN." *CVPR* 2020. [![arXiv](https://img.shields.io/badge/arXiv-2005.12126-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2005.12126) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://nv-tlabs.github.io/gameGAN/)
  > GAN-era neural game engine (Pac-Man) that renders the next screen from key presses, with a memory module building an internal environment map and disentangled static/dynamic components.

- **GameGen-X** — Che, H. et al. "GameGen-X: Interactive Open-world Game Video Generation." *arXiv* 2411.00769 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2411.00769-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2411.00769) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://gamegen-x.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/GameGen-X/GameGen-X)
  > Diffusion transformer for open-world game video that predicts and alters future content from the current clip via InstructNet control experts, trained on the 1M-clip OGameData corpus from 150+ games.

- **PlayGen** — Yang, M. et al. "Playable Game Generation." *arXiv* 2412.00887 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2412.00887-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.00887) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/GreatX3/Playable-Game-Generation)
  > Autoregressive DiT-based diffusion game engine with a playability-based evaluation framework; sustains real-time interactive mechanics simulation past 1000 frames on an RTX 2060.

- **The Matrix** — Feng, R. et al. "The Matrix: Infinite-Horizon World Generation with Real-Time Moving Control." *arXiv* 2412.03568 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2412.03568-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.03568) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://thematrix1999.github.io/)
  > Trained on AAA games (Forza Horizon 5, Cyberpunk 2077) plus real footage, it streams hour-long 720p rollouts at 16 FPS with real-time movement control and zero-shot game-to-real transfer.

- **Next-Frame Diffusion** — Cheng, X. et al. "Playing with Transformer at 30+ FPS via Next-Frame Diffusion." *arXiv* 2506.01380 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.01380-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.01380) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://nextframed.github.io/)
  > Block-wise causal diffusion transformer with consistency distillation and action-aware speculative sampling, reaching 30+ FPS action-conditioned Minecraft generation on a single A100.

- **PlayerOne** — Tu, Y. et al. "PlayerOne: Egocentric World Simulator." *arXiv* 2506.09995 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.09995-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.09995) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://playerone-hku.github.io/)
  > Egocentric world simulator driven by the user's real body motion (part-disentangled motion injection) with joint 4D-scene/video reconstruction to keep the simulated world consistent over long rollouts.

- **Hunyuan-GameCraft** — Li, J. et al. "Hunyuan-GameCraft: High-dynamic Interactive Game Video Generation with Hybrid History Condition." *arXiv* 2506.17201 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2506.17201-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2506.17201) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://hunyuan-gamecraft.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/Tencent-Hunyuan/Hunyuan-GameCraft-1.0)
  > Unifies keyboard/mouse input into a shared camera-action space and extends rollouts autoregressively with hybrid history conditioning; distilled for real-time play, trained on 1M+ clips from 100+ AAA games.

- **Mirage** — "Research Preview: The World's First AI-Native UGC Game Engine Powered by Real-Time World Model." *Dynamics Lab Blog* (2025). [![Blog](https://img.shields.io/badge/Blog-Post-F97316?logo=rss&logoColor=white)](https://blog.dynamicslab.ai/)
  > Real-time transformer-based autoregressive diffusion game engine playable at 16 FPS with frame-level prompt processing, letting players reshape the ongoing world via text, keyboard, or controller mid-rollout. (Unrelated to the §2.4 "Mirage / Latent Spatial Memory" paper.)

### Target section: 1.1.2 Autoregressive Transformer Models

- **Playable Video Generation** — Menapace, W. et al. "Playable Video Generation." *CVPR* 2021. [![arXiv](https://img.shields.io/badge/arXiv-2101.12195-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2101.12195) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://willi-menapace.github.io/playable-video-generation-website/)
  > Learns a discrete latent action space from unlabeled video so a user selects an action at every step of generation — the direct precursor of Genie's latent-action interface.

- **Promptable Game Models** — Menapace, W. et al. "Promptable Game Models: Text-Guided Game Simulation via Masked Diffusion Models." *ACM TOG* 2023. [![arXiv](https://img.shields.io/badge/arXiv-2303.13472-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2303.13472) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://snap-research.github.io/promptable-game-models/)
  > Represents a game as an environment state evolved by agent actions, adds text-promptable high- and low-level control, and learns an animation "game AI" enabling a goal-directed director's mode.

- **WHAM / Muse** — Kanervisto, A. et al. "World and Human Action Models towards gameplay ideation." *Nature* 638 (2025). [![Paper](https://img.shields.io/badge/Nature-Paper-006400?logo=springer&logoColor=white)](https://www.nature.com/articles/s41586-025-08600-3) [![Blog](https://img.shields.io/badge/Blog-Post-F97316?logo=rss&logoColor=white)](https://www.microsoft.com/en-us/research/blog/introducing-muse-our-first-generative-ai-model-designed-for-gameplay-ideation/) [![Project](https://img.shields.io/badge/HF-Weights-0A66C2?logo=huggingface&logoColor=white)](https://huggingface.co/microsoft/wham)
  > Microsoft's 1.6B autoregressive transformer over tokenized Bleeding Edge visuals and controller actions; runs as a world model, a behavior policy, or both, and persists user mid-sequence edits — open weights plus the WHAM Demonstrator.

- **Jasmine** — Mahajan, M. et al. "Jasmine: A Simple, Performant and Scalable JAX-based World Modeling Codebase." *arXiv* 2510.27002 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.27002-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.27002) [![Blog](https://img.shields.io/badge/Blog-Post-F97316?logo=rss&logoColor=white)](https://pdoom.org/jasmine.html)
  > Open, fully reproducible training infrastructure for Genie-style interactive world models, reproducing the Genie CoinRun case study an order of magnitude faster than prior open implementations. (Could alternatively live under Community Resources → Open Toolkits.)

- **ActionParty** — Pondaven, A. et al. "ActionParty: Multi-Subject Action Binding in Generative Video Games." *ECCV* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2604.02330-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2604.02330) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://action-party.github.io/)
  > Introduces persistent subject state tokens that bind each action to its subject, disentangling global frame rendering from per-subject updates; controls up to seven players simultaneously across 46 Melting Pot environments.

- **WanToFight** — Hu, L. et al. "WanToFight: Real-Time Generative Game Engine for Multi-Player Combat Interaction." *arXiv* 2607.12592 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.12592-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.12592) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://humanaigc.github.io/wantofight/)
  > First generative game engine combining two-player adversarial control, real-time inference, and contact physics: a streaming block-causal DiT with player-association modules binding each keyboard stream to a KOF '97 character at 30 FPS.

- **WorldWeaver (W²)** — Mo, S. et al. "Streaming Multi-Agent Autoregressive Diffusion Model with World State Registers." *arXiv* 2607.21594 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.21594-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.21594) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://vail-ucla.github.io/worldweaver/)
  > Augments streaming rollout with learnable cross-agent world-state registers — shared world information and per-agent status updated after every generated chunk — improving logical consistency in two-agent Minecraft. (Distinct from the 1.6 WorldWeaver, 2508.15720.)

- **MASS** — Cai, Z. et al. "MASS: Multiplayer World Models with Authoritative Shared State." *arXiv* 2608.06257 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.06257-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.06257) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://alaya-lab.github.io/MASS/)
  > A learned Logic Engine advances a global authoritative typed state from joint actions (the sole recurrent memory) while a Rendering Engine synthesizes any requested camera view — scaling to 1,024 concurrent players over 10,000 recurrent steps.

- **AlayaWorld v1.1 Technical Report** — "AlayaWorld: Interactive Long-Horizon World Modeling — Full Technical Report (v1.1)." *arXiv* 2608.13492 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.13492-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13492)
  > Update of the AlayaWorld entry already in §1.1.2 (2607.06291): replaces depth-warped spatial memory with a streaming 3D point-cache renderer and re-encodes all conditions in the causal-VAE latent space. **Integrator note:** consider updating the existing row instead of adding a new one; a v1.0 full report also exists (2607.18367).

- **Odyssey-1 / Odyssey-2** — "Introducing Odyssey-2: A General-Purpose World Model." *Odyssey Blog* (2026). [![Blog](https://img.shields.io/badge/Blog-Post-F97316?logo=rss&logoColor=white)](https://odyssey.ml/introducing-odyssey-2) [![Blog](https://img.shields.io/badge/Odyssey1-Post-F97316?logo=rss&logoColor=white)](https://odyssey.ml/introducing-odyssey-1)
  > Frontier-lab playable world models: causal autoregressive frame prediction conditioned on state, action, and history, streaming a new frame every 40–50 ms for multi-minute interactive rollouts steered by text mid-stream.

- **Oasis 2.0** — "Oasis 2.0." *Decart* (2026). [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://oasis2.decart.ai/)
  > Follow-up to the Oasis entry already in §1.1.2: 1080p/30fps real-time generative Minecraft shipped as a playable mod that restyles and regenerates the live game world frame-by-frame.

- **Oasis 3** — "Oasis 3: The Interactive World Model for Physical AI." *Decart* (2026). [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://decart.ai/oasis)
  > First API-accessible interactive world model: robot/vehicle actions in, multi-camera photorealistic views out, with unbounded-length real-time generation targeted at policy training and evaluation.

### Target section: 1.1.3 Memory-Augmented & Long-Horizon Game Worlds

- **EDELINE** — Lee, J.-H. et al. "EDELINE: Enhancing Memory in Diffusion-based World Models via Linear-Time Sequence Modeling." *arXiv* 2502.00466 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2502.00466-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.00466)
  > Direct DIAMOND follow-up: unifies state-space sequence models with diffusion world models to lift the fixed-context memory limit, improving RL agents on Atari-100k, memory-demanding Crafter, and ViZDoom.

- **Yume** — Mao, X. et al. "Yume: An Interactive World Generation Model." *arXiv* 2507.17744 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2507.17744-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2507.17744) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://stdstu12.github.io/YUME-Project/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/stdstu12/YUME)
  > Creates an explorable dynamic world from one image with quantized keyboard camera actions and a Masked Video Diffusion Transformer carrying a memory module for infinite autoregressive rollouts.

- **Memory Forcing** — Huang, J. et al. "Memory Forcing: Spatio-Temporal Memory for Consistent Scene Generation on Minecraft." *arXiv* 2510.03198 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.03198-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.03198)
  > Pairs hybrid/chained-rollout training with geometry-indexed spatial memory (point-to-frame retrieval over an incrementally reconstructed 3D cache) so Minecraft rollouts explore freely yet stay consistent on revisits.

- **RELIC** — Hong, Y. et al. "RELIC: Interactive Video World Model with Long-Horizon Memory." *arXiv* 2512.04040 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.04040-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.04040)
  > 14B real-time (16 FPS) interactive model storing the entire history as highly compressed camera-aware latent tokens in the KV cache, trained with a memory-efficient self-forcing paradigm for full-context distillation over long rollouts.

- **WorldPlay** — Sun, W. et al. "WorldPlay: Towards Long-Term Geometric Consistency for Real-Time Interactive World Modeling." *arXiv* 2512.14614 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.14614-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.14614) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://3d-models.hunyuan.tencent.com/world/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/Tencent-Hunyuan/HY-WorldPlay)
  > Tencent's streaming world model with dual action representation, reconstituted context memory (temporal reframing keeps geometrically important past frames addressable), and memory-aligned "context forcing" distillation for 720p/24 FPS rollouts.

- **Yume-1.5** — Mao, X. et al. "Yume-1.5: A Text-Controlled Interactive World Generation Model." *arXiv* 2512.22096 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.22096-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.22096)
  > Adds unified context compression with linear attention, bidirectional-attention distillation for real-time streaming, and text-controlled in-world events to the Yume line of keyboard-explorable worlds.

- **MultiGen** — Po, R. et al. "MultiGen: Level-Design for Editable Multiplayer Worlds in Diffusion Game Engines." *arXiv* 2603.06679 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2603.06679-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2603.06679) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://ryanpo.com/multigen/)
  > Decomposes the diffusion game engine into Memory/Observation/Dynamics modules around a persistent, user-editable external memory, enabling reproducible level design and coherent real-time multiplayer rollouts.

- **Incantation** — Zhu, S. et al. "Incantation: Natural Language as the Action Interface for Multi-Entity Video World Models." *arXiv* 2605.18601 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.18601-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.18601)
  > Per-latent-frame (0.25 s) natural-language action conditioning gives simultaneous multi-entity control and cross-entity concept transfer in Elden Ring and KOF worlds, streaming at 19.7 FPS with stable two-hour rollouts.

- **NeuWorld** — Li, Z. et al. "Walking in the Implicit: Interactive World Exploration via Neural Scene Representation." *ECCV* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2606.30045-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.30045)
  > Changes the rollout variable from frame latents to a fixed-length renderable Neural Implicit Scene state: a diffusion transformer stochastically evolves the scene state under camera actions while rendering is deterministic and pose-conditioned.

- **LingBot-World 2.0** — Gao, Z. et al. "Infinite Worlds with Versatile Interactions." *arXiv* 2607.07534 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.07534-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.07534) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://technology.robbyant.com/lingbot-world-v2) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/robbyant/lingbot-world-v2)
  > Open interactive world model with unbounded interaction horizon via causal pretraining, a 60 fps/720p real-time distilled variant, rich action and text-event interfaces, a pilot/director agentic harness, and a multiplayer interface. (LingBot-World v1 already appears under Open Toolkits.)

- **AlayaRenderer-Flash** — Lin, G. et al. "Generative World Renderer at the Speed of Play." *arXiv* 2607.18703 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.18703-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.18703) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://alaya-renderer-flash.alayalab.ai/)
  > Few-step autoregressive streaming renderer that synthesizes RGB from structured physics-engine world states at 31.5 FPS, composing with a real engine into a fully playable generative world where dynamics live in explicit state.

- **HelloWorld** — Ouyang, L. et al. "HelloWorld: Enabling Socially Interactive Characters in Video World Models." *arXiv* 2608.05070 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05070-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05070) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/AlayaLab/HelloWorld)
  > Adds button-press social interventions on in-world characters during an ongoing rollout, using self-distilled interaction data and press-window cross-attention masking to localize the character's response in time.

- **Alaya-EVOKE** — Yin, Y. et al. "Alaya-EVOKE: From Linear-Scaling Supervision to Endless World." *arXiv* 2608.13546 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.13546-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.13546)
  > Externalizes persistent world state into a camera-indexed bank with view-relevant retrieval and redesigns the teacher for linear-scaling long-horizon supervision, yielding a 3-step student supporting open-ended, prompt/event-controllable generation.

- **Marionette** — Meng, Z. et al. "Marionette: Predicting World States, Rendering Geometry, Painting Appearance." *arXiv* 2608.14530 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.14530-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.14530) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://alayalab.github.io/Marionette/)
  > Autoregressively predicts an explicit, interpretable 276-dim 3D world state (articulated skeletons, metric trajectories), renders geometry with a zero-parameter graphics bridge, and paints appearance with control-conditioned diffusion — long-horizon behavior can be repaired by rules imposed directly on the state.

- **WorldMind** — Deng, Z. et al. "WorldMind: Decoupled Game World Model for State-Aware NPC Behavior." *arXiv* 2608.21439 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.21439-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.21439) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://teawhite.cn/worldmind_projectpage/)
  > Decouples interactive world modeling into understanding/decision/control/generation layers reconnected in a closed loop, grounding NPC actions in an explicit compact game state; ships the BOSS-140K gameplay+state dataset.

- **ReWorld** — Chen, Z. et al. "ReWorld: An Interactive World Model with Long-Horizon Memory." *arXiv* 2608.23565 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.23565-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.23565) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://zhifeichen097.github.io/ReWorld/)
  > Separates control (windowed heads) from memory (global heads over a bounded, pose-indexed landmark KV bank) with a metric-scale-aligned data engine; regenerates the starting view after minute-long out-and-back rollouts where sliding windows have evicted the evidence.

### Target section: 1.6 General Video World Models & Rollout Backbones

- **SlowFast-VGen** — Hong, Y. et al. "SlowFast-VGen: Slow-Fast Learning for Action-Driven Long Video Generation." *ICLR* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2410.23277-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2410.23277) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://slowfast-vgen.github.io)
  > Action-driven long-video world model that complements slow-learned dynamics with inference-time fast learning: a temporal LoRA stores episodic memory of the ongoing rollout, improving long-horizon planning tasks.

- **CausVid** — Yin, T. et al. "From Slow Bidirectional to Fast Autoregressive Video Diffusion Models." *CVPR* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2412.07772-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.07772) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://causvid.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/tianweiy/CausVid)
  > The asymmetric bidirectional-teacher → causal-student DMD recipe (with KV caching and dynamic prompting) that Self-Forcing and most real-time interactive world models descend from.

- **DWS** — He, H. et al. "Pre-Trained Video Generative Models as World Simulators." *arXiv* 2502.07825 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2502.07825-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.07825)
  > Early Vid2World-style conversion recipe: a universal action-conditioned module plus a motion-reinforced loss turn pretrained video generators into action-executing simulators, with prioritized imagination for downstream model-based RL.

- **MALT Diffusion** — Yu, S. et al. "MALT Diffusion: Memory-Augmented Latent Transformers for Any-Length Video Generation." *CVPR Workshops* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2502.12632-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2502.12632)
  > Recurrent attention layers compress prior segments into a memory latent that conditions segment-level autoregressive generation, keeping quality stable over long temporal contexts.

- **Cosmos-Transfer1** — NVIDIA. "Cosmos-Transfer1: Conditional World Generation with Adaptive Multimodal Control." *arXiv* 2503.14492 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2503.14492-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.14492) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/nvidia-cosmos/cosmos-transfer1)
  > Conditional world generation with spatially adaptive multimodal control (segmentation/depth/edge) for world-to-world and Sim2Real transfer in Physical AI, with a demonstrated real-time inference-scaling deployment. (Complements the Cosmos platform and Cosmos-Predict2.5 entries already in the README.)

- **FAR** — Gu, Y. et al. "Long-Context Autoregressive Video Modeling with Next-Frame Prediction." *arXiv* 2503.19325 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2503.19325-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.19325) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://farlongctx.github.io/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/showlab/FAR)
  > Frame-autoregressive baseline explicitly motivated by world simulation: asymmetric patchify kernels keep distant frames as coarse context memory and nearby frames fine-grained, making long-context rollout training tractable.

- **TTT-Video** — Dalal, K. et al. "One-Minute Video Generation with Test-Time Training." *CVPR* 2025. [![arXiv](https://img.shields.io/badge/arXiv-2504.05298-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2504.05298) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://test-time-training.github.io/video-dit)
  > Test-Time Training layers whose hidden state is itself a neural network carry scene and story state across a one-minute multi-scene rollout — an expressive hidden-state memory mechanism for long-horizon world models.

- **FramePack** — Zhang, L. et al. "Frame Context Packing and Drift Prevention in Next-Frame-Prediction Video Diffusion Models." *arXiv* 2504.12626 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2504.12626-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2504.12626) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/lllyasviel/FramePack)
  > Importance-weighted frame-context packing plus anti-drifting sampling (early-established endpoints, discrete history) let next-frame-prediction models roll out thousands of frames without error accumulation — a widely reused open rollout backbone.

- **SkyReels-V2** — Chen, G. et al. "SkyReels-V2: Infinite-length Film Generative Model." *arXiv* 2504.13074 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2504.13074-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2504.13074) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/SkyworkAI/SkyReels-V2)
  > Open diffusion-forcing framework (non-decreasing noise schedules) for infinite-length autoregressive synthesis — one of the standard open backbones downstream interactive world models are converted from.

- **MAGI-1** — Sand.ai. "MAGI-1: Autoregressive Video Generation at Scale." *arXiv* 2505.13211 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2505.13211-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.13211) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/SandAI-org/MAGI-1)
  > 24B open chunk-wise autoregressive world model with monotonically increasing per-chunk noise: causal temporal modeling, streaming generation at constant peak inference cost, and chunk-wise prompting for controllable rollouts.

- **WorldWeaver** — Liu, Z. et al. "WorldWeaver: Generating Long-Horizon Video Worlds via Rich Perception." *arXiv* 2508.15720 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2508.15720-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2508.15720) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://johanan528.github.io/worldweaver_web/)
  > Jointly predicts RGB and perceptual conditions from a unified representation and maintains a drift-resistant depth-based memory bank, cutting structural drift in long-horizon world generation. (Distinct from the multi-agent WorldWeaver W², 2607.21594.)

- **RLIR** — Ye, Y. et al. "Reinforcement Learning with Inverse Rewards for World Model Post-training." *arXiv* 2509.23958 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2509.23958-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2509.23958)
  > Recovers input actions from generated video with an inverse dynamics model to obtain verifiable rewards, then GRPO post-training improves action-following of video world models by 5–10% across AR and diffusion paradigms.

- **Self-Forcing++** — Cui, J. et al. "Self-Forcing++: Towards Minute-Scale High-Quality Video Generation." *arXiv* 2510.02283 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.02283-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.02283) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://self-forcing-plus-plus.github.io/)
  > Direct Self-Forcing descendant: teacher guidance on segments sampled from the student's own long rollouts extends generation ~20× beyond the teacher horizon (4+ minutes) without long-video supervision.

- **RAD** — Chen, T. et al. "Recurrent Autoregressive Diffusion: Global Memory Meets Local Attention." *ECCV* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2511.12940-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2511.12940) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://yeyutaihan.github.io/recurrent-autoregressive-diffusion/)
  > Inserts recurrent (LSTM) memory layers into the diffusion transformer for global memory under a fixed budget while overlapping-window attention preserves local detail, validated on Memory Maze and Minecraft world modeling.

- **VideoSSM** — Yu, Y. et al. "VideoSSM: Autoregressive Long Video Generation with Hybrid State-Space Memory." *arXiv* 2512.04519 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2512.04519-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2512.04519)
  > Treats streaming synthesis as a recurrent dynamical process: an SSM carries an evolving global memory of scene dynamics while a local context window keeps motion cues, scaling linearly to minute-scale interactive prompt-controlled rollouts.

- **LiveWorld** — Duan, Z. et al. "LiveWorld: Simulating Out-of-Sight Dynamics in Generative Video World Models." *arXiv* 2603.07145 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2603.07145-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2603.07145) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://zichengduan.github.io/LiveWorld/index.html)
  > Formalizes the out-of-sight-dynamics problem: a persistent global state (static 3D background + dynamic entities) keeps evolving while unobserved and is synchronized upon revisit, with the LiveBench evaluation suite.

- **Anchor Forcing** — Yang, Y. et al. "Anchor Forcing: Anchor Memory and Tri-Region RoPE for Interactive Streaming Video Diffusion." *arXiv* 2603.13405 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2603.13405-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2603.13405) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/vivoCameraResearch/Anchor-Forcing)
  > Anchor-cache warm-started re-caching and tri-region RoPE re-alignment stabilize quality and motion when new prompts are injected into an ongoing streaming rollout.

- **MosaicMem** — Yu, W. et al. "MosaicMem: Hybrid Spatial Memory for Controllable Video World Models." *arXiv* 2603.17117 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2603.17117-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2603.17117) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://mosaicmem.github.io/mosaicmem/)
  > Hybrid memory lifts patches into 3D for reliable localization and targeted retrieval while native conditioning preserves generation, keeping rollouts consistent under camera motion, revisits, and intervention (including memory-based scene editing).

- **Echo-Forcing** — Wu, M. et al. "Echo-Forcing: A Scene Memory Framework for Interactive Long Video Generation." *arXiv* 2605.16003 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.16003-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.16003) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/mingqiangWu/Echo-Forcing)
  > Training-free hierarchical scene memory (stable anchors / compressed history / recent window) with scene-recall frames and difference-aware decay, uniformly supporting smooth transitions, hard cuts, and long-range scene recall during interactive prompt switching.

- **ReMind** — Xu, T. et al. "Teaching Video Generators to Remember: Eliciting Dynamic Memory for Out-of-Sight State Evolution." *arXiv* 2605.25333 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.25333-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.25333) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://remind-applied.github.io/)
  > Event-aware node-structured curriculum and camera-phase RoPE train pretrained DiTs to use their KV caches as dynamic memory, retrieving evolved past states across interruptions instead of freezing hidden state.

- **DisCo** — Huang, H. et al. "DisCo: World Models with Discrete Camera Motion Control." *arXiv* 2606.07967 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.07967-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.07967)
  > Identifies action-representation entanglement in continuous camera conditioning and conditions rollouts on a compact set of discrete action primitives instead, with DisCoBench covering short-term, long-horizon, and highly dynamic exploration.

- **Cycle-World** — Su, Z. et al. "Cycle-World: Mitigating Error Accumulation in Long-term Video World Models via Reverse-Prediction Cycle Consistency." *ECCV* 2026. [![arXiv](https://img.shields.io/badge/arXiv-2607.11836-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.11836)
  > Proves forward generative drift is bounded by a cycle-consistency objective; a reverse-prediction model embeds the constraint at training and doubles as a runtime gradient corrector that suppresses errors before they enter the rollout history.

- **Self Gradient Forcing** — Zhuang, J. et al. "Self Gradient Forcing: Native Long Video Extrapolation." *arXiv* 2607.20368 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.20368-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.20368) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://zhuang2002.github.io/SelfGradientForcing/)
  > Closes the historical context-gradient gap in self-forcing: a two-pass scheme lets future losses supervise how earlier latents are written into the KV memory, extrapolating minutes-long rollouts from 5-second training windows.

- **Visko Orbis 1.0** — Gao, X. et al. "Visko Orbis 1.0: A Live Model for Real-Time Interactive Long Video Generation." *arXiv* 2607.26694 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.26694-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.26694)
  > "Live model" whose prompt can be changed at any moment with the update visible in real time; bounded multi-scale memory preserves subjects and scenes across chunks over hour-scale 4K/24 FPS rollouts.

- **FreqForcing** — Li, J. et al. "FreqForcing: Autoregressive Long Video Generation via Spectral Self-Anchoring." *arXiv* 2607.27110 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.27110-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.27110) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/jiatongli2024/FreqForcing)
  > Characterizes rollout error accumulation as low-frequency spectral energy drift and counters it training-free with spectral self-anchoring, extending 5-second self-forcing models to two-minute (24×) streaming rollouts.

- **ShadowDancer** — "ShadowDancer: Teaching Video World Models Any Action by Learning Unified Dynamics Representations from a Video and Its Shadow." *arXiv* 2607.28362 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.28362-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.28362) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://shadowdancer-1.github.io)
  > Learns appearance-invariant dynamics representations from "shadow pairs" (same dynamics, independently resampled appearance), enabling any-action, frame-level control of interactive world models from demonstration videos.

- **MiniWorld** — Zhao, Y. et al. "MiniWorld: Democratizing the Training of Video World Models from Scratch." *arXiv* 2608.01127 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.01127-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.01127)
  > Lightweight, fully reproducible from-scratch recipe for streaming block-causal video world models (diffusion-forcing noise schedule, rolling KV cache, pipelined asynchronous denoising) trainable in days on one 8-GPU server, with released code and checkpoints.

- **CoCo** — Shi, Y. et al. "Overcoming Statistical Bias in Action-Controllable World Models." *arXiv* 2608.04653 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04653-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04653)
  > Enforces counterfactual consistency (inverse-action, zero-action, and mirrored-scene rollouts) so predicted dynamics genuinely depend on actions rather than visual inertia, with new controllability metrics and top average success on VP2 visual planning.

- **WorldCycle** — Gu, B. et al. "WorldCycle: Self-Verifiable Reinforcement Learning for Long-Horizon Video World Models." *arXiv* 2608.04964 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04964-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04964) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://nevsnev.github.io/Worldcycle/)
  > Reversible action cycles (a sequence composed with its inverse must return to the initial state) provide annotation-free verifiable rewards on long-horizon drift, cutting state-return drift by up to 44% and teaching actions as consistent state operators.

- **WorldTrace** — Wu, X. et al. "Addressable Memory for Video World Models." *arXiv* 2608.07408 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.07408-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07408) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://research.nvidia.com/labs/sil/projects/WorldTrace/)
  > Training-free addressable compressed KV memory assigning each summary slot an in-distribution virtual RoPE position, with Field (temporal coherence) and Landmark (episodic recall) variants and the LoopBench revisit benchmark.

- **PhyS** — Zhao, L. et al. "Distilling Physical Priors into Streaming World Models." *arXiv* 2608.07981 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.07981-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.07981) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://lyongo.github.io/PhyS/)
  > Three-stage pipeline (physics-aware SFT on the 120K-video PhyS-120K corpus, causal distillation, online RL with temporal credit routing) that makes few-step streaming world-model rollouts obey physical constraints, improving PhysicsIQ by 18.2% over its teacher.

- **LDR** — Li, H. et al. "Learning How the World Evolves: Extrapolative Video World Models via Latent Dynamics Reasoning." *arXiv* 2608.09926 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.09926-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.09926) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://lat-dyn-reason.github.io/)
  > Casts latent transitions as explicit kinematic integration over structured latents (the model regresses only higher-order residuals), achieving out-of-distribution dynamics extrapolation with a 20× smaller ID–OOD gap at a fraction of the compute.

- **Stream Forcing** — Zhu, Y. et al. "Stream Forcing: Constructing Unified Training Trajectory for Robust Streaming Video Generation." *arXiv* 2608.10439 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.10439-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.10439)
  > Reformulates video diffusion sampling as a frame-indexed stochastic noise process and builds a continuous training trajectory toward inference-consistent sampling, closing the streaming train–inference mismatch that world-model rollouts inherit.

- **ForgeWM** — Li, X. et al. "ForgeWM: Progressive Causal Training for Few-Step Action-Conditioned Video World Models." *arXiv* 2608.14022 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.14022-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.14022)
  > Four-stage progressive causal distillation turns bidirectional action-conditioned generators into 1/2/4-step world models that keep keyboard/mouse actions aligned with compressed latent chunks (Minecraft and gamepad FPS), plus a latency/replay-refinement dual-path deployment protocol.

- **EchoWM** — Zhang, S. et al. "EchoWM: Open and Enterable Omnimodal World Models." *arXiv* 2608.23189 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.23189-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.23189)
  > Open "enterable" world model responding to continuous navigation via a shared metric-scale 6-DoF trajectory interface while jointly generating 720p video with synchronized environmental sound, music, and speech over long-horizon autoregressive rollouts.

- **Sora 2** — "Sora 2 is here." *OpenAI* (September 2025). [![Blog](https://img.shields.io/badge/Blog-Post-F97316?logo=rss&logoColor=white)](https://openai.com/index/sora-2/) [![Blog](https://img.shields.io/badge/System_Card-Post-F97316?logo=rss&logoColor=white)](https://openai.com/index/sora-2-system-card/)
  > OpenAI's follow-up to the Sora world-simulator report with explicit dynamics claims: improved physical-law adherence, modeling of failure outcomes (e.g., missed shots rebound instead of teleporting), and positioning as a step toward general-purpose world simulators. (Alternative placement: Selected Technical Blogs, next to the existing Sora entry.)

### Target section: 1.7.1 Online Streaming & Intervenable Narrative Rollouts

- **CausalCine** — Meng, Y. et al. "CausalCine: Real-Time Autoregressive Generation for Multi-Shot Video Narratives." *arXiv* 2605.12496 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.12496-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.12496) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://yihao-meng.github.io/CausalCine/)
  > Turns multi-shot generation into an online directing process: a causal model trained on native multi-shot sequences accepts dynamic prompts on the fly, generates across shot boundaries, and routes cross-shot memory by attention relevance (CAMR) under a bounded active cache.

- **ContextMaster** — Guo, X. et al. "ContextMaster: Interactive Multi-Shot Video Creation via Fixed-Budget Sparse Context Routing." *arXiv* 2608.04956 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.04956-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.04956) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://guoxu1233.github.io/ContextMaster/)
  > Formalizes interactive multi-shot video creation: one model generates, follows references, or edits footage while maintaining a shared expanding history accessed through fixed-budget sparse context routing, running at 16 FPS after privileged context distillation.

- **Vorch-Director** — Zhang, L. et al. "Vorch-Director: Interactive World Story Model via Noise-Aware Error Rectification." *arXiv* 2608.05776 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.05776-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.05776) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://vorch-project.github.io/Vorch-Director-project)
  > Continues a world story by conditioning each extension on its own previously generated audio-visual history, with noise-level-aware residual correction to keep multi-shot, multi-subject, reference-guided rollouts stable at minute scale.

### Target section: 1.7.2 Persistent Cross-Shot State & Memory

- **EM-Vid** — Vandersanden, J. et al. "EM-Vid: Training-Free Entity-Centric Memory for Efficient and Consistent Multi-Shot Video Generation." *arXiv* 2605.23610 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.23610-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.23610)
  > Replaces full-frame history with an entity-indexed bank of latent patches under a budgeted update strategy; each new shot attends sparsely only to entity-relevant memory tokens, disentangling persistent entity state from transient scene context.

- **GroundShot** — Lai, Y. et al. "GroundShot: Visually Consistent Multi-Shot Long Video Generation via Entity-Grounded Shot Scheduling." *arXiv* 2606.20799 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.20799-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.20799)
  > Builds an entity-level visual memory online from accepted generated shots — grounding, verifying, and retrieving entity references — and schedules shot generation order by expected reference usefulness, with the GroundBench entity-consistency diagnostic.

- **UnityShots** — Huang, J. et al. "UnityShots: Memory-Driven Multi-Shot Audio-Video Generation with Boundary-Aware Gating." *arXiv* 2606.21661 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2606.21661-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2606.21661) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://jackailab.github.io/Projects/UnityShots)
  > Maintains fixed-size long-term (opening-shot anchor) and short-term (previous tail) memory slots updated at every cut by a boundary-conditioned gate fusing cut probability and beat signals, with a speaker token persisting voice identity across shots.

- **SlotMem** — Liu, Y. et al. "SlotMem: Character-Addressable Internal Memory for Narrative Long Video Generation." *arXiv* 2607.15772 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2607.15772-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2607.15772) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/YilaiLiu-HKU/SlotMem)
  > Character-addressable slot memory: a semantic probe localizes character tokens, a memory writer conservatively updates each character's compact slot as generation proceeds, and character-wise cross-attention re-injects the right memory across scene transitions and long temporal gaps.

- **JoyAI-Echo-1.5** — Duan, N. et al. "Long-Horizon Audio-Visual Generation for Persistent Stories and Interactive Worlds." *arXiv* 2608.23383 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2608.23383-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2608.23383) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://echo-team-joy-future-academy-jd.github.io/Echo-1.5-Page/)
  > Unified system whose long-video variant aggregates composable cross-shot memory (multi-shot visual evidence plus speech-filtered speaker cues) for persistent character appearance and voice, while a world-model variant adds calibrated metric 6-DoF navigation control (ranked first on WBench).

### Target section: 1.7.3 State-Aware Narrative Planning & Rendering

- **VideoGen-of-Thought (VGoT)** — Zheng, M. et al. "VideoGen-of-Thought: Step-by-step generating multi-shot video with minimal manual intervention." *arXiv* 2412.02259 (2024). [![arXiv](https://img.shields.io/badge/arXiv-2412.02259-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2412.02259) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://cheliosoops.github.io/VGoT/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/DuNGEOnmassster/VideoGen-of-Thought)
  > Dynamic storyline modeling expands one sentence into self-validated five-domain shot specifications (character dynamics, background continuity, relationship evolution, camera, lighting) and propagates controlled character-state changes across shots via identity-preserving portrait tokens.

- **MovieAgent** — Wu, W. et al. "Automated Movie Generation via Multi-Agent CoT Planning." *arXiv* 2503.07314 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2503.07314-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2503.07314) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://weijiawu.github.io/MovieAgent/) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/showlab/MovieAgent)
  > Hierarchical multi-agent CoT planning (director, screenwriter, storyboard artist, location manager roles) structures scenes, shots, and camera settings from a script and character bank before rendering, coordinating multi-scene narratives through the shared plan.

- **Captain Cinema** — Xiao, J. et al. "Captain Cinema: Towards Short Movie Generation." *arXiv* 2507.18634 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2507.18634-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2507.18634) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://thecinema.ai)
  > Top-down keyframe planning fixes the narrative's scene and character state for the whole storyline, then bottom-up long-context synthesis with interleaved MM-DiT conditioning renders each shot while consuming the planned cross-scene history.

- **Hollywood Town** — Wei, Z. et al. "Hollywood Town: Long-Video Generation via Cross-Modal Multi-Agent Orchestration." *arXiv* 2510.22431 (2025). [![arXiv](https://img.shields.io/badge/arXiv-2510.22431-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2510.22431)
  > Film-production-inspired hierarchical graph of agents with hypergraph group-discussion nodes for shared context and directed-cyclic retry loops, so later production stages feed corrections back into earlier narrative planning.

- **ReCA** — Liu, A. et al. "ReCA: Multi-Shot Long Video Extrapolation via Recursive Context Allocation." *arXiv* 2605.26525 (2026). [![arXiv](https://img.shields.io/badge/arXiv-2605.26525-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2605.26525) [![Project](https://img.shields.io/badge/Project-Page-0A66C2?logo=googlechrome&logoColor=white)](https://reca.vmv.re) [![GitHub](https://img.shields.io/badge/GitHub-Code-181717?logo=github&logoColor=white)](https://github.com/ali-vilab/ReCA)
  > Defines multi-shot video extrapolation — continuing an observed anchor state through cinematically structured shots — and solves it with recursive context allocation that decomposes planning/generation into context-bounded subproblems and propagates structured state updates across frozen-generator calls.

---

## Considered but excluded (for the integrator's reference)

- **Benchmarks / evaluation-only** (README has a dedicated Benchmarks section): PersonaShot 2608.16717, CaliBench 2608.16829, PlayWorld 2608.13552, WorldExam 2608.02603, GAUGE 2608.05948, WorldRoamBench 2606.31672, From Generation to Simulation 2608.23070, HarnessEval-W 2608.16859, WorldReasonBench 2605.10434.
- **Datasets** (README has a Datasets section): Sekai2 2608.09449, WildWorld 2603.23497. Survey-flavored analysis: "From Pixels to States" 2607.14076 (recommend Surveys; also ships a Black Myth: Wukong state-annotated data engine).
- **Position/no-experiments notes:** Twin Rollouts 2608.08982 (exact counterfactual-branching formalism for interactive world models, but experiments explicitly forthcoming — revisit when updated), Quo Vadis World Modeling 2608.02713.
- **Below the §1.6/§1.7 bar** (generic efficiency/KV-cache/identity machinery without world-state, memory-across-shots, or intervention claims): In-Context Forcing 2608.05237, Progressive AR VDM 2410.08151, Ms. Forcing 2607.20940, Surprise Forcing 2607.18436, Sparse/Focused/Pyramid/Head/Light/Pack/Relax-Forcing family, DySink 2605.21028, Rolling Sink 2602.07775, TokensGen 2507.15728, SlotMemory 2605.31033, OmniMem 2605.30519, FadeMem 2606.10671, TetherCache 2606.13035, LongLive-RAG 2606.02553, SWIFT 2605.09442, WorldCache 2603.22286/2603.06331, WorldDynCache 2608.01845, Partition-the-Support 2608.18484, SCOPE (agentic optimization) 2608.15043; multi-shot identity/cinematography-only: MultiShotMaster 2512.03041, ShotDirector 2512.10286, CineWeaver 2607.26529, CineTrans 2508.11484, EchoShot 2506.15838, ShotAdapter 2505.07652, HoloCine 2510.20822, Long Context Tuning 2503.10589, identity-aware memory 2605.18733, MSEditor 2608.17559; avatar/human-animation streaming: DynaForcing 2608.17707, LiveAnimate 2608.11745, MIDAS 2508.19320, Vorch-Streamer 2608.05663, Wan-Animate-2 2608.06009.
- **Out of target sections** (other README sections are the right home): Twin (ARC-AGI-3 executable world models) 2608.14490 and Tycho 2607.28287 → §2.5/§3.x; Latent Video Prediction Learns Better World Models 2605.15618 → §2.2; EgoForge 2603.20169 → §1.3.2; robotics/driving WAM papers (GeniWorld, XEWorld, DreamX-Phi, CosmosAlign, etc.) → §1.2/§1.3.
- **Verified already present (examples):** Cosmos WFM platform 2501.03575, Cosmos-Predict2.5 2511.00062, RLVR-World 2505.13934, AdaWorld 2503.18938, Pandora 2406.09455, Navigation World Models 2412.03572, Mixture of Contexts 2508.21058, DeepVerse 2506.01103, RTFM (World Labs) and Marble blogs, LingBot-World v1 2601.20540.
