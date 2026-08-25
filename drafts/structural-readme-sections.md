# Draft: Structural README Sections

> **Status:** draft for review. Nothing below has been merged into `README.md`.
> **Purpose:** add handbook-style front-matter and reference sections that turn the taxonomy into a complete field map, without adding a single new paper entry.

## Paste Notes (read before merging)

1. **Heading levels.** Every section below is a top-level `##` section, matching the existing README structure. Do not demote them.
2. **No raw arXiv links.** The CI duplicate check (`node scripts/check-arxiv-duplicates.mjs README.md`) is strict: every `arxiv.org/abs/...` occurrence in `README.md` counts, so repeating an arXiv URL that already appears in a taxonomy entry would fail CI. All sections below therefore reference papers **by name plus an internal section anchor**. If you deliberately add an arXiv link to any of these sections, add its ID to `.github/arxiv-duplicate-allowlist.json` with a reason.
3. **Anchors.** All internal links reuse the anchors already used by the existing Table of Contents and Start Here table. New headings were chosen so their GitHub-generated anchors match the Suggested TOC Insertions at the bottom of this file. In particular, `## ⭐ Why Star This Repo?` generates `#-why-star-this-repo`, which is the anchor the current TOC already links to (the section body has been missing until now).
4. **Suggested placement** (top to bottom of README):
   - `## ⭐ Why Star This Repo?` — immediately after `## 📰 News`, before `## 🚀 Start Here`.
   - `## 🧭 How to Use This List` — after `## 🗂️ Definition and Scope`, before the Table of Contents.
   - `## 🎓 Reading Roadmap` — after `## 🗺️ Taxonomic Overview`, before section 0.
   - `## ⏳ Historical Timeline` — after `## 🎓 Reading Roadmap`.
   - `## 🧩 Architecture Cheat Sheet` — after `## ⏳ Historical Timeline`.
   - `## 📘 Glossary` — after `## 📊 Benchmarks & Evaluation`, before `## 🔬 Workshops & Challenges` (it is a reference section, like benchmarks).
   - `## 🧪 Evaluation Dimensions` — immediately before `## 📊 Benchmarks & Evaluation` (it is the conceptual index into that table).
   - `## 🏭 Labs, Companies & Open Stacks` — inside or immediately after `## 🌐 Community Resources & Open Repositories`.
   - `## 🚧 Open Problems` — after `## 📚 Surveys & Position Papers`.
   - `## ❓ FAQ` — before `## 📖 Citation`.
   - `## 📊 List Statistics` — immediately before `## 📖 Citation`.
5. **Housekeeping when merging:** update the `Last Updated` badge (currently `July 2026`), the *"Latest curation pass verified against arXiv on July 11, 2026"* line, and add the News item at the bottom of this file.
6. **Flagged references.** Three historical works referenced in the Historical Timeline (Craik 1943, Tolman 1948, Sutton's Dyna 1991) and the Tesla row of the Labs table are **not currently entries in `README.md`** — they are flagged inline with *(not yet in this list — verify before linking)*. Either add them as proper §0.1 entries in a separate PR or keep them as plain-text mentions.

---

## ⭐ Why Star This Repo?

There are many world-model paper lists. This one makes five specific commitments that the others usually do not, and it is maintained against them.

| Commitment | What it means in practice |
| --- | --- |
| **Paradigm-first taxonomy** | Entries are organized by *what the model is* — [Generative](#1--generative-world-models), [Representational](#2--representational-world-models), or [Agentic](#3--agentic-world-models), grounded in [Mind World Models](#0--mind-world-models--biological-origins--foundational-definitions) — before domain. A driving paper and a Minecraft paper that share an architecture family sit near each other conceptually; domain-first lists cannot show that. |
| **Strict inclusion heuristics** | A paper enters only when it clears the [practical boundary](#definition-and-scope): at least two of *models state*, *predicts state evolution under action or intervention*, *supports imagination, planning, evaluation, or controllable simulation*. Generic video generation, perception-only, and forecasting-only work is deliberately deprioritized — see [Deliberate non-goals](#definition-and-scope). |
| **Paper-first, primary sources, official code only** | Every entry links arXiv/venue pages, official project pages, and official repositories. Unofficial reimplementations are not badged as `GitHub` code. Blog posts are quarantined into [Selected Technical Blogs & Reports](#-selected-technical-blogs--reports) rather than mixed into the paper taxonomy. |
| **Cross-domain coverage under one definition** | Driving ([1.2](#12-autonomous-driving--generative), [2.3](#23-occupancy--bev-representations)), robotics ([1.3](#13-embodied-ai--robotics--generative)), games and interactive simulation ([1.1](#11-game--interactive-world-simulation)), science ([1.5](#15-scientific--physical-world-modeling)), 3D/4D worlds ([1.4](#14-3d--4d-scene-generation)), and LLM/GUI agents ([3.6](#36-llm--vlm--gui-agents-with-world-models)) are all held to the same working definition instead of being separate lists stapled together. |
| **Duplicate-aware curation** | A CI check (`scripts/check-arxiv-duplicates.mjs`) rejects any arXiv ID that appears twice unless it is explicitly allowlisted with a reason. Each paper has exactly one home; intentional cross-references use plain-text pointers like *(see §1.2.3)*. Large lists rot through silent duplication; this one cannot. |

Two smaller things that compound over time: every curation pass is **dated** (see the badge and the verification line at the top), and every entry carries a one-line, factual reason it matters — no entry is a bare link.

If that is the kind of map you want of this field, a star helps others find it.

[⬆ Back to Top](#-table-of-contents)

---

## 🧭 How to Use This List

### Navigate by paradigm, then by domain

The taxonomy has one deliberate spine:

1. Decide **what kind of model** you care about. Synthesizing plausible futures → [1 · Generative](#1--generative-world-models). Learning structured internal state without pixel decoding → [2 · Representational](#2--representational-world-models). Coupling a world model to acting, planning, and evaluation → [3 · Agentic](#3--agentic-world-models). Cognitive and biological grounding → [0 · Mind World Models](#0--mind-world-models--biological-origins--foundational-definitions).
2. Then narrow by **domain or mechanism** inside that paradigm (e.g. 1.2 driving, 2.2 JEPA, 3.3 closed-loop evaluation).
3. When a paper is domain-specific, it is filed by its **main technical role first** and domain second. A JEPA-style LiDAR model lives under driving generative LiDAR (§1.2.3) with a cross-reference from JEPA (§2.2), not the other way around.

The [Start Here](#-start-here) table maps six common intents directly to sections. The [Taxonomic Overview](#-taxonomic-overview) shows the full tree at a glance.

### What the badges mean

| Badge | Meaning |
| --- | --- |
| `arXiv` | The arXiv paper; the badge label carries the full arXiv ID, so you can search the page for an ID you already know. |
| `GitHub` | **Official** code or the official project repository. Unofficial reimplementations are not badged. |
| `Project` | Official project page. |
| `HuggingFace` | Official model, dataset, space, or leaderboard. |
| `Blog` | Technical blog post or official research-lab write-up. |
| `Paper` | Non-arXiv primary source: DOI, OpenReview, or proceedings page. |

### Tables vs. bullets

Two entry formats coexist by design:

- **Tables** are used where a family is mature enough to compare on fixed columns: the [RSSM / Dreamer family](#21-latent-dynamics-models-rssm--dreamer-family), [MBRL](#31-model-based-reinforcement-learning-mbrl), [Surveys](#-surveys--position-papers), [Benchmarks](#-benchmarks--evaluation), and [Community Resources](#-community-resources--open-repositories).
- **Bullets with a one-line rationale** are used in fast-moving areas where entries do not yet share a comparable schema. The indented `>` line under each bullet states, factually, why the entry is in scope.

### Finding code and reproducible stacks

- Skim any section for `GitHub` badges — they always mean official code.
- For end-to-end stacks (training recipes, checkpoints, serving), go straight to [Open Toolkits & Platforms](#-community-resources--open-repositories), which collects Cosmos, minWM, Matrix-Game, Genie Envisioner, DreamerV3, TD-MPC2, V-JEPA 2, OpenDWM, and others.
- Leaderboards and datasets have their own subsections under [Community Resources](#-community-resources--open-repositories).

### What this list is not

This is **not a video-generation dump**. A video model appears only when it explicitly targets control, causality, memory, or world-model conversion — that boundary is stated at the top of [§1.6 General Video World Models & Rollout Backbones](#16-general-video-world-models--rollout-backbones) and enforced even more tightly in [§1.7 Persistent Narrative & Multi-Shot Video](#17--persistent-narrative--multi-shot-video-world-models), which requires documented state, memory, or structured planning that crosses a shot boundary. Length, resolution, visual quality, and identity consistency alone never qualify a paper. If you want a broad video-generation list, several are linked in [Curated Lists & Awesome Repos](#-community-resources--open-repositories).

[⬆ Back to Top](#-table-of-contents)

---

## 🎓 Reading Roadmap

Three tracks. Each step names papers that are already entries in this list; follow the section link to find full citations, badges, and code.

### Track 1 — Newcomer (build the concept from zero)

Goal: understand what a world model is, where the idea comes from, and what the modern instantiations look like — roughly 7 stops.

1. **The definition.** Read [Definition and Scope](#definition-and-scope) and the working definitions under [Taxonomic Overview](#-taxonomic-overview). Ten minutes that prevent months of terminology confusion.
2. **The seminal paper.** *World Models* (Ha & Schmidhuber, 2018) and its NeurIPS version *Recurrent World Models Facilitate Policy Evolution* — in [§0.1–0.2](#0--mind-world-models--biological-origins--foundational-definitions). Learn V-M-C: compress perception, predict in latent space, train a controller entirely inside the dream.
3. **Latent dynamics done right.** *PlaNet* (RSSM) and *Dream to Control* (Dreamer), then skim *DreamerV2/V3* — in [§0.2](#0--mind-world-models--biological-origins--foundational-definitions) and the comparison table in [§2.1](#21-latent-dynamics-models-rssm--dreamer-family). This is the reinforcement-learning lineage of the field.
4. **The generative-interactive turn.** *Genie: Generative Interactive Environments*, then the *Genie 2* and *Genie 3* lab reports — in [§1.1.2](#11-game--interactive-world-simulation). Latent actions learned from unlabeled video; playable worlds from a prompt.
5. **The non-generative counterpoint.** *V-JEPA* (and LeCun's *A Path Towards Autonomous Machine Intelligence*, [§0.1](#0--mind-world-models--biological-origins--foundational-definitions)) — in [§2.2](#22-joint-embedding-predictive-architectures-jepa). Predict representations, not pixels; understand why this is an argument, not just an architecture.
6. **One driving paper.** *GAIA-1* — in [§1.2.1](#12-autonomous-driving--generative). The first large-scale autoregressive driving world model; sets up everything that follows in §1.2. (*OccWorld* in [§1.2.2](#12-autonomous-driving--generative) is the natural second read for the geometry-first side.)
7. **One robotics paper.** *UniSim: Learning Interactive Real-World Simulators* — in [§1.3.1](#13-embodied-ai--robotics--generative). A learned action-conditioned simulator of real-world interaction; the conceptual bridge to WAMs.

After these seven, the [Historical Timeline](#-historical-timeline) and [Architecture Cheat Sheet](#-architecture-cheat-sheet) below will read as review rather than news.

### Track 2 — Practitioner (build something this quarter)

Goal: pick a stack with open weights or code and a known deployment story. All of these have `GitHub` badges and live under [Open Toolkits & Platforms](#-community-resources--open-repositories) plus their taxonomy homes.

| Stack | What it gives you | Where |
| --- | --- | --- |
| **NVIDIA Cosmos** (incl. Cosmos-Predict2.5, Cosmos 3) | Open world-foundation-model platform for Physical AI: pretrained video WFMs, post-training recipes, driving pipeline (Cosmos-Drive-Dreams) | [Toolkits](#-community-resources--open-repositories), [§1.6](#16-general-video-world-models--rollout-backbones) |
| **DreamerV3** | Reference latent-dynamics MBRL agent; single hyperparameter set across domains; the default baseline for imagination-based RL | [§2.1](#21-latent-dynamics-models-rssm--dreamer-family), [§3.1](#31-model-based-reinforcement-learning-mbrl) |
| **TD-MPC2** | Scalable latent MPC for continuous control (104 tasks); decoder-free, robust defaults | [§2.1](#21-latent-dynamics-models-rssm--dreamer-family), [§1.3.3](#13-embodied-ai--robotics--generative) |
| **V-JEPA 2** | Self-supervised video representation + action-conditioned latent planning; zero-shot manipulation recipes; official checkpoints on HuggingFace | [§2.2](#22-joint-embedding-predictive-architectures-jepa), [§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam) |
| **Matrix-Game** (1.0 → 3.0) | Open interactive game-world stack: real-time streaming rollouts, long-horizon memory in 3.0 | [§1.1.1](#11-game--interactive-world-simulation), [Toolkits](#-community-resources--open-repositories) |
| **Genie Envisioner** | Unified robotic-manipulation world platform: imagination, policy evaluation, and data generation in one loop (AgiBot) | [§1.3.1](#13-embodied-ai--robotics--generative), [Toolkits](#-community-resources--open-repositories) |

Supporting picks, depending on the problem: **minWM** and **Causal Forcing** for converting a video backbone into a real-time interactive world model ([§1.6](#16-general-video-world-models--rollout-backbones)); **OpenDWM** for driving; **stable-worldmodel** and **Nano World Models** for controlled research baselines (all under [Toolkits](#-community-resources--open-repositories)).

### Track 3 — Researcher (find the frontier)

1. **Surveys first.** From the [Surveys & Position Papers](#-surveys--position-papers) tables: *Understanding World or Predicting Future?* for the broad taxonomy, *Is Sora a World Simulator?* for the generative debate, *World Action Models: A Survey* and *World Action Models: The Next Frontier* for the WAM consolidation, plus the domain surveys for driving and embodied AI.
2. **Theory and safety.** The [Safety & Theory](#-surveys--position-papers) table (*When Does LeJEPA Learn a World Model?*, *General Agents Contain World Models*, *Critiques of World Models*, identifiability and value-equivalence results in [§2.1](#21-latent-dynamics-models-rssm--dreamer-family)–[§2.2](#22-joint-embedding-predictive-architectures-jepa)) and [§3.5 Safety-Aware Agentic World Models](#35-safety-aware-agentic-world-models) for the attack-surface literature.
3. **Benchmarks.** Read [Evaluation Dimensions](#-evaluation-dimensions) below as the index, then go metric-shopping in [Benchmarks & Evaluation](#-benchmarks--evaluation). Pay attention to closed-loop utility benchmarks (World-in-World, WorldGym, WorldEval) versus rollout-quality benchmarks — they disagree, and that disagreement is a research topic.
4. **Open problems.** The [Open Problems](#-open-problems) section below distills what the 2025–2026 surveys actually argue about, with entry points into the taxonomy for each.

[⬆ Back to Top](#-table-of-contents)

---

## ⏳ Historical Timeline

Two eras, compact by design. Every named work in the second table is an entry in this list; the first table flags the pre-history items that are context rather than entries.

### Cognitive and computational origins (1943–2018)

| Year | Milestone | Why it matters |
| --- | --- | --- |
| 1943 | Craik, *The Nature of Explanation* *(not yet in this list — verify before linking)* | First articulation of the mind carrying a "small-scale model" of external reality used to try out alternatives before acting — the sentence the whole field footnotes. |
| 1948 | Tolman, *Cognitive Maps in Rats and Men* *(not yet in this list — verify before linking)* | Latent spatial representations inferred from behavior; the empirical ancestor of learned internal state. |
| 1989 | **Occupancy Grids** (Elfes, *Computer*) — [§0.1](#0--mind-world-models--biological-origins--foundational-definitions) | First computational formalization of a spatial world model for a physical agent; the direct ancestor of [§2.3](#23-occupancy--bev-representations). |
| 1991 | Sutton, Dyna *(not yet in this list — verify before linking)* | Learning, planning, and reacting integrated through imagined experience; "Dyna-style rollouts" survive verbatim in the [MBRL table](#31-model-based-reinforcement-learning-mbrl). |
| 1993 | **Successor Representations** (Dayan, *Neural Computation*) — [§0.1](#0--mind-world-models--biological-origins--foundational-definitions) | Represent the future occupancy of states rather than immediate reward — predictive representation before deep learning. |
| 2010 | **Free-Energy Principle** (Friston, *Nature Reviews Neuroscience*) — [§0.1](#0--mind-world-models--biological-origins--foundational-definitions) | The brain as a hierarchical prediction-error-minimizing machine; the neuroscientific grounding for predictive world models. |
| 2013 | **Simulation as an engine of physical scene understanding** (Battaglia et al., *PNAS*) — [§0.1](#0--mind-world-models--biological-origins--foundational-definitions) | Humans run fast approximate physics simulations as a world model for intuitive physics. |
| 2018 | **World Models** (Ha & Schmidhuber) + **Recurrent World Models Facilitate Policy Evolution** (*NeurIPS*) — [§0.1–0.2](#0--mind-world-models--biological-origins--foundational-definitions) | The term enters modern machine learning: V-M-C decomposition, training a controller entirely inside the learned dream. |

### The scaling era (2018–2026)

| Year | Milestones (all entries in this list) | Where |
| --- | --- | --- |
| 2019 | **PlaNet** (*ICML*) introduces RSSM and latent-space planning; **MBPO** (*NeurIPS*) formalizes Dyna-style model-based policy optimization; **DPI-Net** (*ICLR*) brings graph-network particle physics. | [§0.2](#0--mind-world-models--biological-origins--foundational-definitions), [§3.1](#31-model-based-reinforcement-learning-mbrl), [§1.5.1](#15-scientific--physical-world-modeling) |
| 2020 | **Dreamer** (*ICLR*) trains actor-critic fully in imagination; **MuZero** (*Nature*) plans with a learned value-equivalent dynamics model, no rules given. | [§0.2](#0--mind-world-models--biological-origins--foundational-definitions), [§3.1](#31-model-based-reinforcement-learning-mbrl) |
| 2021 | **DreamerV2** (*ICLR*) makes discrete latents work; **EfficientZero** (*NeurIPS*) reaches Atari sample-efficiency milestones; **Pathdreamer** (*ICCV*) is an early visual world model for navigation. | [§0.2](#0--mind-world-models--biological-origins--foundational-definitions), [§3.1](#31-model-based-reinforcement-learning-mbrl), [§1.3.2](#13-embodied-ai--robotics--generative) |
| 2022 | **LeCun's position paper** proposes JEPA-centered autonomous machine intelligence; **TD-MPC** (*ICML*) fuses TD learning with latent MPC; **Iso-Dream** (*NeurIPS*) disentangles controllable dynamics. | [§0.1](#0--mind-world-models--biological-origins--foundational-definitions), [§2.1](#21-latent-dynamics-models-rssm--dreamer-family) |
| 2023 | **DreamerV3** generalizes across domains with fixed hyperparameters; **I-JEPA** (*CVPR*) lands the JEPA program in vision; **GAIA-1** (Wayve) is the first large-scale generative driving world model; **UniPi** turns text-guided video generation into policies; **Pangu-Weather** (*Nature*) and **GraphCast** (*Science*) show learned earth-system dynamics beating traditional simulation. | [§0.2](#0--mind-world-models--biological-origins--foundational-definitions), [§2.2](#22-joint-embedding-predictive-architectures-jepa), [§1.2.1](#12-autonomous-driving--generative), [§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam), [§1.5.2](#15-scientific--physical-world-modeling) |
| 2024 | OpenAI frames Sora as a "world simulator", igniting the debate (*Is Sora a World Simulator?* survey; *PhyWorld* physical-law critique); **Genie** learns latent actions from unlabeled video; **GameNGen** runs DOOM in a diffusion model in real time; **Oasis** generates Minecraft token-by-token; **V-JEPA** (*ICLR*) and **TD-MPC2** (*ICLR*) mature the representational side; **OccWorld** (*ECCV*) and **Copilot4D** (*ICLR*) establish occupancy/LiDAR world models; **Genie 2** (December) generates playable 3D worlds from one image; **DIAMOND** (*NeurIPS*) shows diffusion world models paying off for RL. | [Surveys](#-surveys--position-papers), [§1.5.1](#15-scientific--physical-world-modeling), [§1.1](#11-game--interactive-world-simulation), [§2.2](#22-joint-embedding-predictive-architectures-jepa), [§2.1](#21-latent-dynamics-models-rssm--dreamer-family), [§1.2.2–1.2.3](#12-autonomous-driving--generative), [§3.1](#31-model-based-reinforcement-learning-mbrl) |
| 2025 | **NVIDIA Cosmos** ships open world foundation models for Physical AI (January), extended by **Cosmos-Predict2.5** and **Cosmos-Drive-Dreams**; **GAIA-2** adds controllable multi-view driving; **V-JEPA 2** demonstrates zero-shot robot manipulation from internet-scale video pretraining; **Matrix-Game** and **Matrix-Game 2.0** open-source real-time interactive game worlds; **Genie 3** (August) reaches real-time 24 fps text-to-world generation; **Genie Envisioner** unifies robot imagination, evaluation, and data generation; **HunyuanWorld 1.0** generates explorable 3D worlds; **DreamerV4** scales agent-side world-model training; **PAN** targets general long-horizon interactive simulation. | [Toolkits](#-community-resources--open-repositories), [§1.2.1](#12-autonomous-driving--generative), [§2.2](#22-joint-embedding-predictive-architectures-jepa), [§1.1](#11-game--interactive-world-simulation), [§1.3.1](#13-embodied-ai--robotics--generative), [§1.4.1](#14-3d--4d-scene-generation), [§3.1](#31-model-based-reinforcement-learning-mbrl), [§1.6](#16-general-video-world-models--rollout-backbones) |
| 2026 | **Cosmos 3** unifies language, image, video, audio, and action in one omnimodal WFM family; **HY-World 2.0** and **Matrix-Game 3.0** push open 3D/interactive stacks; **V-JEPA 2.1** densifies JEPA video features; the **World Action Model (WAM)** wave consolidates — dedicated surveys (*World Action Models: A Survey*; *The Next Frontier*), open stacks (**DreamZero**), and a dense §1.3.4 of video-action models; memory, evaluation, and safety become first-class subfields (§1.1.3, §3.3, §3.5). | [§1.6](#16-general-video-world-models--rollout-backbones), [§1.4.1](#14-3d--4d-scene-generation), [§1.1.3](#11-game--interactive-world-simulation), [§2.2](#22-joint-embedding-predictive-architectures-jepa), [§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam), [Surveys](#-surveys--position-papers), [§3.3](#33-closed-loop-simulation--evaluation), [§3.5](#35-safety-aware-agentic-world-models) |

[⬆ Back to Top](#-table-of-contents)

---

## 🧩 Architecture Cheat Sheet

Eight architecture families that account for nearly every entry in this list. "State" is what the model carries between steps; "prediction target" is what it is trained to output; "failure modes" are the documented ones, not hypotheticals. Canonical papers are all entries here — follow the section links for citations and code.

| Family | State | Prediction target | Action conditioning | Strengths | Failure modes | Canonical papers (in this list) |
| --- | --- | --- | --- | --- | --- | --- |
| **Diffusion video WM** | Implicit — a window of recent frames or video latents | Future frames (pixel or VAE-latent), denoised | Actions/trajectories/text injected as conditioning; often weak by default | Visual fidelity; inherits video-generation pretraining; multimodal futures | Compounding error over long rollouts; action conditioning ignored under classifier-free guidance; slow sampling without distillation | GameNGen, DIAMOND ([§1.1.1](#11-game--interactive-world-simulation)); Vista ([§1.2.1](#12-autonomous-driving--generative)); Cosmos family ([§1.6](#16-general-video-world-models--rollout-backbones)) |
| **AR transformer WM** | Discrete token history (VQ codes) with KV cache | Next visual tokens / frames | Interleaved action tokens or learned latent actions | Streaming and real-time by construction; unified with LLM tooling; latent actions learnable from unlabeled video | Tokenizer artifacts; finite context → spatial forgetting; exposure bias | Genie, Oasis, MineWorld ([§1.1.2](#11-game--interactive-world-simulation)); iVideoGPT ([§1.6](#16-general-video-world-models--rollout-backbones)); DrivingGPT ([§1.2.4](#12-autonomous-driving--generative)) |
| **RSSM / Dreamer family** | Compact deterministic + stochastic latent | Next latent state (+ reward, value; decoder optional) | Explicit action input to the transition function | Extremely cheap rollouts → sample-efficient RL in imagination; stable training recipes | Limited visual capacity; mostly proven at simulator scale; latent hallucination outside the data manifold | PlaNet, Dreamer, DreamerV2/V3 ([§2.1](#21-latent-dynamics-models-rssm--dreamer-family)); DreamerV4 ([§3.1](#31-model-based-reinforcement-learning-mbrl)); TD-MPC2 (decoder-free relative, [§2.1](#21-latent-dynamics-models-rssm--dreamer-family)) |
| **JEPA** | Embedding produced by a target encoder | Representation of future/masked content — no pixel decoding (energy-based objective) | Optional: action-conditioned predictor (V-JEPA 2, AD-L-JEPA) | Ignores unpredictable pixel detail; strong transfer; cheap planning in representation space | No renderable output for humans; representation collapse without careful regularization; evaluation is indirect | I-JEPA, V-JEPA, V-JEPA 2/2.1, LeWorldModel ([§2.2](#22-joint-embedding-predictive-architectures-jepa)); AD-L-JEPA ([§1.2.3](#12-autonomous-driving--generative)) |
| **Occupancy / BEV WM** | Explicit 3D voxel occupancy or BEV grid | Future occupancy / BEV frames | Ego trajectory, agent commands, language (OccLLaMA) | Metric geometry; direct planner interface; sensor-fusion friendly | Resolution–memory trade-off; appearance-free (needs a renderer for photorealism); semantic sparsity | OccWorld, Drive-OccWorld, DOME ([§1.2.2](#12-autonomous-driving--generative)); OccSora, BEVWorld ([§2.3](#23-occupancy--bev-representations)) |
| **3DGS / NeRF worlds** | Explicit persistent 3D scene (Gaussians, fields, meshes) | Novel-view renders + scene evolution | Camera trajectory; object-level edits; physics add-ons | 3D consistency by construction; revisitable, editable, engine-loadable worlds | Dynamics usually bolted on; costly scene construction; closed-world assumption | EmerNeRF, 4D Gaussian Splatting, HunyuanWorld 1.0, LayerPano3D ([§1.4.1](#14-3d--4d-scene-generation)); GWM, GaussianWorld ([§1.3.1](#13-embodied-ai--robotics--generative), [§1.2.2](#12-autonomous-driving--generative)) |
| **LLM text WM** | Textual / symbolic state description | Next state description, transition validity, or executable program | Text actions; tool calls | Abstract and counterfactual reasoning; composable with agent frameworks; cheap | State drift and hallucination over steps; weak physical/spatial grounding; hard to verify | LLM-Sim ([§2.4](#24-multimodal-text-acoustic--memory-oriented-world-models)); RAP, WebDreamer, CWM ([§3.6](#36-llm--vlm--gui-agents-with-world-models)); Text2World, PoE-World ([§2.5](#25-symbolic--knowledge-graph-world-models)) |
| **WAM (world action model)** | Shared video–action latent | **Joint**: future video (or latent) *and* actions | Intrinsic — action is an output as much as an input | Policy and simulator in one model; transfers video pretraining into control; zero-shot policy results | Inference cost of imagining before acting; video-action generalization gap; evaluation protocols still immature | WorldVLA, UWM, UVA, DreamZero, LingBot-VA ([§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam)); WAM surveys ([Surveys](#-surveys--position-papers)) |

Reading the table: the top half trades **fidelity against control** (diffusion vs. AR), the middle trades **capacity against efficiency** (RSSM/JEPA vs. pixel models), and the bottom half trades **structure against openness** (occupancy/3D worlds vs. text vs. joint video-action). Most 2026 systems are hybrids that pick one row as a backbone and borrow mechanisms from two others.

[⬆ Back to Top](#-table-of-contents)

---

## 📘 Glossary

Precise working definitions, in the sense used throughout this list. Alphabetical. Terms in *italics* are cross-references within the glossary.

- **Action-conditioned rollout** — Generating a future trajectory (frames, latents, occupancy) where each step is conditioned on a supplied action, so different action sequences must produce different futures. The minimum bar separating a world model from a video generator; benchmarked by ACT-Bench and the VRAG Benchmark ([Benchmarks](#-benchmarks--evaluation)).
- **Agentic world model** — A *world foundation model* coupled with action selection, planning, memory, tool use, or policy optimization in a closed loop. The organizing idea of [Section 3](#3--agentic-world-models).
- **BEV (bird's-eye view)** — A top-down metric grid representation of a scene, standard in driving. BEV world models predict future BEV frames; see [§2.3](#23-occupancy--bev-representations).
- **Causal forcing** — A training/distillation recipe that converts bidirectional video diffusion into causal (past-only) autoregressive generation suitable for real-time interaction; named after the Causal Forcing line of work in [§1.6](#16-general-video-world-models--rollout-backbones).
- **Closed-loop vs. open-loop** — Open-loop: the model predicts a future once, from a fixed prompt/context, and is scored against ground truth. Closed-loop: the model's outputs feed back into its own inputs (or a policy acts inside it) over many steps, so errors can compound and interventions matter. Closed-loop evaluation is the stricter and more decision-relevant regime; see [§3.3](#33-closed-loop-simulation--evaluation).
- **Compounding error (rollout drift)** — Accumulation of small per-step prediction errors during autoregressive rollout, driving generated futures off the data manifold. The central engineering obstacle of §1.6; mitigations include *self-forcing*, history guidance, memory modules, and 3D anchoring.
- **Counterfactual** — A "what would have happened if" query: same initial state, different action or intervention. A world model with counterfactual fidelity produces futures that diverge correctly under such edits; benchmarked by What-If World and parts of RoboTrustBench ([Benchmarks](#-benchmarks--evaluation)).
- **Diffusion forcing** — A training objective mixing next-token-style causal prediction with full-sequence diffusion, giving per-frame noise levels; a backbone recipe for controllable causal video rollouts ([§1.6](#16-general-video-world-models--rollout-backbones)).
- **Digital twin vs. world model** — A digital twin is an instance-specific, engineered replica of one particular asset or site, kept synchronized with it. A world model is a *learned, generalizing* predictive model of environment dynamics. Twins can be built *from* world models (see Real2Sim, [§1.3.5](#13-embodied-ai--robotics--generative)) and world models can be trained from twins, but the terms are not interchangeable; see the *Digital Twin AI* survey ([Surveys](#-surveys--position-papers)).
- **Dyna-style rollout** — Using a learned model to generate imagined transitions that augment real experience for policy learning (after Sutton's Dyna architecture). MBPO in [§3.1](#31-model-based-reinforcement-learning-mbrl) is the canonical deep-RL instantiation.
- **Energy-based JEPA** — LeCun's formulation in which a predictor is trained to make representations of compatible (context, target) pairs low-energy, without reconstructing pixels — avoiding wasted capacity on unpredictable detail. The theoretical program behind [§2.2](#22-joint-embedding-predictive-architectures-jepa).
- **Generative world model** — Predicts or synthesizes plausible future *observations* (pixels, video, occupancy, point clouds), typically usable as a learned simulator or data engine. [Section 1](#1--generative-world-models).
- **Imagination** — Rolling the world model forward without touching the real environment, to train a policy (Dreamer), plan (MPC/MCTS), evaluate a policy, or synthesize data. "Training in imagination" means the policy never sees real transitions during optimization.
- **Inverse dynamics model (IDM)** — A model that infers the action connecting two observed states. Used to label action-free video, to ground *latent actions*, and to turn generated videos into executable robot commands ([§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam)).
- **Latent action** — An action representation learned from unlabeled video rather than recorded controls (Genie, AdaWorld). Enables interactive control of models trained on internet-scale data without action labels; must be mapped to executable controls for robotics.
- **Latent dynamics model** — A world model whose transition function operates on a compact learned state rather than observations; the RSSM/Dreamer family in [§2.1](#21-latent-dynamics-models-rssm--dreamer-family) is the reference implementation.
- **Long-horizon memory** — Mechanisms (explicit 3D state, retrieval, surfel/keyframe caches, state-space models) that keep a rollout consistent with content generated many steps ago, including content that left the field of view. See [§1.1.3](#11-game--interactive-world-simulation) and the memory benchmarks MBench, MIND, and STEVO-Bench ([Benchmarks](#-benchmarks--evaluation)).
- **MBRL (model-based reinforcement learning)** — RL that learns and exploits a dynamics model for sample efficiency, via imagined training, planning, or both. [§3.1](#31-model-based-reinforcement-learning-mbrl).
- **MPC (model-predictive control)** — At each step, optimize a short action sequence against the world model's predicted futures, execute the first action, re-plan. The standard way to use latent world models for control without a learned policy (PlaNet, TD-MPC2).
- **Neural simulator** — A learned model used *in place of* a hand-built simulator: action-in, observation-out, at interactive rates, with enough fidelity to train or evaluate policies (UniSim, RoboWorld, NVIDIA OmniDreams). The claim is functional, not architectural.
- **Occupancy (grid)** — A voxelized representation marking which regions of 3D space are occupied (optionally with semantics). The oldest world-model formalization in this list (Elfes 1989, [§0.1](#0--mind-world-models--biological-origins--foundational-definitions)) and a mainline of driving world models ([§1.2.2](#12-autonomous-driving--generative), [§2.3](#23-occupancy--bev-representations)).
- **Open-loop evaluation** — See *closed-loop vs. open-loop*.
- **Physical plausibility vs. photorealism** — Orthogonal axes: a rollout can look real while violating conservation laws, object permanence, or contact dynamics. PhyWorld, Physics-IQ Verified, and VideoPhy-2 ([Benchmarks](#-benchmarks--evaluation)) measure the physics axis specifically.
- **Policy-in-the-loop evaluation** — Scoring a world model by how well a policy trained or evaluated *inside* it transfers to the real environment — the utility-centric alternative to visual metrics. WorldGym, WorldEval, PiL-World, World-in-World ([§3.3](#33-closed-loop-simulation--evaluation), [Benchmarks](#-benchmarks--evaluation)).
- **Real2Sim / Sim-to-Real** — Real2Sim: constructing simulation-ready scene twins from real recordings ([§1.3.5](#13-embodied-ai--robotics--generative)). Sim-to-Real: transferring a policy or model trained in simulation (or imagination) to the physical world. World models sit on both bridges.
- **Representational world model** — Predicts future *state or latent structure* without requiring photorealistic decoding. [Section 2](#2--representational-world-models).
- **RSSM (recurrent state-space model)** — The PlaNet/Dreamer transition architecture: a deterministic recurrent path plus a stochastic latent path, trained with variational objectives; supports fast latent-space planning and imagination.
- **Self-forcing** — Training an autoregressive video model on its *own* generated prefixes rather than ground-truth frames, closing the train–test gap that causes rollout drift. Contrast *teacher forcing*; see [§1.6](#16-general-video-world-models--rollout-backbones).
- **Streaming / real-time interactivity** — The system accepts new user input *after* a generated prefix already exists and continues from it at interactive latency. Stricter than autoregression or generation speed alone — this is the §1.7 bar for "interactive".
- **Teacher forcing** — Training a sequence model with ground-truth history as input at every step. Efficient, but the model never learns to recover from its own mistakes — the root cause of exposure bias in rollouts.
- **VLA vs. WAM** — A VLA (vision-language-action model) maps observations and language *directly* to actions; any world knowledge is implicit. A WAM (world action model) explicitly couples future prediction and action generation — it can imagine, then act, or co-generate both. The boundary cases (VLAs with latent world-model regularizers) live in [§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam); see also *Do World Action Models Generalize Better than VLAs?* ([Surveys](#-surveys--position-papers)).
- **WAM (world action model)** — A model that jointly learns environment dynamics and action generation in one backbone, typically initialized from video generation. The fastest-growing family in this list ([§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam)).
- **WFM (world foundation model)** — A pretrained model of environment structure and dynamics reusable across downstream tasks (simulation, planning, forecasting, data generation) — e.g. Cosmos, Genie, V-JEPA 2. "Foundation" refers to pretraining breadth, not architecture.
- **World model** — An internal predictive model of an environment that helps an agent answer: *what will happen if I act, wait, intervene, or imagine an alternative future?* Intentionally broader than model-based RL and narrower than "any model that understands the world" — see [Definition and Scope](#definition-and-scope).

[⬆ Back to Top](#-table-of-contents)

---

## 🧪 Evaluation Dimensions

"Evaluating a world model" means at least nine different things, and a single leaderboard number conflates them. This section is the conceptual index into [Benchmarks & Evaluation](#-benchmarks--evaluation); every benchmark named below is an entry in that table or in [§3.3](#33-closed-loop-simulation--evaluation).

| Dimension | Question it answers | Typical measurements | Where to look in this list |
| --- | --- | --- | --- |
| **1. Visual fidelity** | Do rollouts look like real observations? | FVD/FID-style distances, human preference, per-frame quality | WorldModelBench, DrivingGen, EWMBench, WorldSimBench |
| **2. Action controllability** | Do different actions produce correctly different futures? | Action-following accuracy, instruction adherence, trajectory-conditioned error | ACT-Bench, VRAG Benchmark, MiraBench, iWorld-Bench, MIND (control axis) |
| **3. 3D / geometric consistency** | Is the implied 3D world stable across viewpoints and revisits? | Reprojection/loop-closure error, multi-view consistency, camera-controlled probing | ViewBench, WRBench, 4DWorldBench, WorldScore, Toward Memory-Aided World Models (LoopNav) |
| **4. Physical plausibility** | Does the rollout obey mechanics, permanence, and conservation? | Physics-law probes, intuitive-physics batteries, commonsense violation rates | Physics-IQ Verified, VideoPhy-2, WorldBench, PDI-Bench, PhysicsMind, Tailor-Bench, WorldOlympiad |
| **5. Long-horizon memory** | Does content that left the view come back correct? | Revisit consistency, occlusion probes, minute-scale drift metrics | MBench, MIND, STEVO-Bench, Toward Stable World Models, Omni-WorldBench |
| **6. Closed-loop policy utility** | Does the model actually help an agent act? | Real-task success of policies trained/evaluated inside the model; sim-vs-real ranking agreement | World-in-World, WorldGym, WorldEval, PiL-World, GigaWorld-1 / WMBench, ReactSim-Bench, RoboWM-Bench ([§3.3](#33-closed-loop-simulation--evaluation)) |
| **7. Sample efficiency** | How little real experience does model-based learning need? | Score at fixed interaction budget | Atari 100k, DMControl Suite, ProcGen, Minecraft Diamond (DreamerV3) |
| **8. Safety & robustness** | Does the model resist perturbations, misuse, and optimistic bias? | Adversarial-context degradation, unsafe-instruction rejection, poisoning detection, optimism-bias probes | RoboTrustBench, ARB4WM, MiraBench (optimism bias), MMBench2 (hallucination), plus the attack literature in [§3.5](#35-safety-aware-agentic-world-models) |
| **9. Counterfactual fidelity** | Do intervention-edited rollouts diverge the way the world would? | Intervention/counterfactual probe accuracy, causal-consistency scoring | What-If World, RoboTrustBench (counterfactual axis), WM-ABench (atomic internal-model probes) |

Three cautions, all documented in entries here:

- **Dimensions 1 and 4 dissociate.** High visual fidelity with broken physics is the normal failure mode, not the exception (*PhyWorld*, [§1.5.1](#15-scientific--physical-world-modeling)).
- **Dimensions 1–5 do not predict dimension 6.** Rollout-quality metrics and policy-utility outcomes can rank models differently; this is why [§3.3](#33-closed-loop-simulation--evaluation) exists as its own subsection, and why *Validate the Dream* argues for admissibility checks before trusting simulator verdicts.
- **Reference-free evaluation is still open.** Most metrics need ground-truth futures that interventions make unavailable; see *Reference-Free Physical Consistency* in [§3.3](#33-closed-loop-simulation--evaluation).

[⬆ Back to Top](#-table-of-contents)

---

## 🏭 Labs, Companies & Open Stacks

Who is building what, restricted to public, primary-source material already linked in this list. "Representative entries" point to sections where the full citations and badges live. Claims about unpublished internal systems are deliberately excluded.

| Organization | Focus | Representative entries in this list | Openness |
| --- | --- | --- | --- |
| **NVIDIA (Cosmos)** | World foundation model platform for Physical AI: video WFMs, driving data engines, real-time closed-loop simulation, omnimodal Cosmos 3 | Cosmos, Cosmos-Predict2.5, Cosmos 3 ([§1.6](#16-general-video-world-models--rollout-backbones), [Toolkits](#-community-resources--open-repositories)); Cosmos-Drive-Dreams, NVIDIA OmniDreams ([§1.2.1](#12-autonomous-driving--generative)); DreamGen, FLARE ([§1.3.1](#13-embodied-ai--robotics--generative)); SANA-WM, FlashDreams, Causal-rCM ([§1.1.3](#11-game--interactive-world-simulation), [§1.6](#16-general-video-world-models--rollout-backbones), [Toolkits](#-community-resources--open-repositories)) | Open weights + code for the Cosmos family |
| **Google DeepMind (Genie)** | Foundation world models for playable environments; generalist 3D agents | Genie, Genie 2, Genie 3 ([§1.1.2](#11-game--interactive-world-simulation)); SIMA ([§1.3.2](#13-embodied-ai--robotics--generative)); MuZero ([§3.1](#31-model-based-reinforcement-learning-mbrl)); GraphCast ([§1.5.2](#15-scientific--physical-world-modeling)); Physics-IQ Verified ([Benchmarks](#-benchmarks--evaluation)) | Papers + lab reports; Genie 2/3 are blog-documented, not open-weight |
| **Meta AI (JEPA)** | Non-generative predictive representation program; video JEPA world models with robot planning | I-JEPA, V-JEPA, V-JEPA 2, V-JEPA 2.1 ([§2.2](#22-joint-embedding-predictive-architectures-jepa)); LeCun's position paper ([§0.1](#0--mind-world-models--biological-origins--foundational-definitions)); CWM code world model ([§3.6](#36-llm--vlm--gui-agents-with-world-models)) | Open code + checkpoints (HuggingFace collection linked in [Leaderboards](#-community-resources--open-repositories)) |
| **Wayve (GAIA)** | Generative driving world models with fine-grained controllability | GAIA-1, GAIA-2 ([§1.2.1](#12-autonomous-driving--generative)); lab write-ups in [Blogs](#-selected-technical-blogs--reports) | Papers + technical blogs; models not released |
| **World Labs** | Spatially grounded multimodal 3D world generation | Marble ([§1.4.1](#14-3d--4d-scene-generation)); RTFM real-time frame model ([Blogs](#-selected-technical-blogs--reports)) | Product + blog reports; limited technical disclosure |
| **1X Technologies** | Humanoid robotics; world models for real-robot video prediction and policy evaluation | 1x World Model Challenge ([Benchmarks](#-benchmarks--evaluation)); OpenDriveLab WM Track co-listing | Public challenge + data; no full model paper in this list |
| **AgiBot** | Robotic manipulation world platforms, embodied data engines, embodied evaluation | EnerVerse, EnerVerse-AC, Genie Envisioner, AgiBot World Colosseo ([§1.3.1](#13-embodied-ai--robotics--generative)); EWMBench ([Benchmarks](#-benchmarks--evaluation)) | Open code, datasets, and benchmarks |
| **Skywork AI (Matrix)** | Open real-time interactive game/world stacks; 3D world generation | Matrix-Game 1.0/2.0 ([§1.1.1](#11-game--interactive-world-simulation)); Matrix-Game 3.0 ([§1.1.3](#11-game--interactive-world-simulation)); Matrix-3D ([§1.4.1](#14-3d--4d-scene-generation)) | Open code + weights |
| **Tencent (Hunyuan)** | Explorable, mesh-based, and simulatable 3D world generation | HunyuanWorld 1.0, HY-World 2.0 ([§1.4.1](#14-3d--4d-scene-generation), [Toolkits](#-community-resources--open-repositories)) | Open code + weights |
| **OpenAI (Sora)** | Video generation framed as world simulation — the claim that started the 2024 debate | *Video generation models as world simulators* ([Blogs](#-selected-technical-blogs--reports)); the debate itself: *Is Sora a World Simulator?*, *PhyWorld* ([Surveys](#-surveys--position-papers), [§1.5.1](#15-scientific--physical-world-modeling)) | Blog post; no open model; treated here as a position, not a system entry |
| **Tesla** | Occupancy networks for planning, presented publicly in engineering talks *(no primary paper; not an entry in this list — verify before linking)* | Conceptual lineage is covered by the occupancy sections: [§1.2.2](#12-autonomous-driving--generative), [§2.3](#23-occupancy--bev-representations) | Public talks only; nothing citable to list-standard |

Also tracked across the taxonomy, without dedicated rows: **Xiaomi** (Xiaomi EV World Model, Xiaomi-Robotics-U0, MiLA, DGGT), **Microsoft** (MineWorld, Latent Spatial Memory), **Alibaba/Qwen and DAMO** (WorldVLA, Qwen-RobotWorld, Qwen-AgentWorld, WorldOlympiad), **SenseTime** (OpenDWM, MaskGWM, UniMLVG), **GigaAI** (ReconDreamer, GigaWorld, GigaBrain), **Meituan** (WBench), and **Ant/Robbyant** (LingBot-VA, LingBot-World). Use repository search on the name; each has entries with badges in the relevant sections.

[⬆ Back to Top](#-table-of-contents)

---

## 🚧 Open Problems

Twelve questions the 2025–2026 surveys and position papers in this list actually argue about — not a wish list. Each problem names its entry points here.

1. **Compounding error over long horizons.** Autoregressive rollouts drift off-manifold; every mitigation (self-forcing, history guidance, rolling windows, distillation) trades something else away. When is drift a training-objective artifact versus a fundamental limit of learned single-step dynamics? Entry points: the forcing-family recipes and long-context models in [§1.6](#16-general-video-world-models--rollout-backbones); *Orbis* ([§1.2.1](#12-autonomous-driving--generative)).
2. **Action controllability and grounding.** Video backbones absorb actions as weak conditioning and often ignore them; latent actions learned from unlabeled video may not align with executable controls. How do we guarantee — and measure — that actions cause futures? Entry points: ACT-Bench, VRAG Benchmark ([Benchmarks](#-benchmarks--evaluation)); Genie's latent actions ([§1.1.2](#11-game--interactive-world-simulation)); AdaWorld, WALA ([§1.3.1](#13-embodied-ai--robotics--generative), [§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam)).
3. **Physical grounding vs. photorealism.** Scaling improves appearance faster than physics; models interpolate visual statistics rather than learning laws. Does physical competence require explicit structure (Hamiltonian latents, differentiable simulators, occupancy) or only better data and probes? Entry points: *PhyWorld*, *Physically Native World Models*, *PhysCoRe* ([§1.5.1](#15-scientific--physical-world-modeling), [§1.3.1](#13-embodied-ai--robotics--generative)); *Physical Grounding in World Models* ([Surveys](#-surveys--position-papers)).
4. **Memory and persistent state.** Pixel-history context is not a world state: off-screen content decays, revisits contradict earlier generations. Explicit 3D state, retrieval, and hierarchical memory all help and all cost; none is settled. Entry points: [§1.1.3](#11-game--interactive-world-simulation) as a whole; *Beyond Pixel Histories* ([§1.4.2](#14-3d--4d-scene-generation)); *On Memory* ([§2.4](#24-multimodal-text-acoustic--memory-oriented-world-models)); MBench, STEVO-Bench ([Benchmarks](#-benchmarks--evaluation)).
5. **Evaluation itself.** Benchmarks have multiplied faster than agreement on what they measure; rollout-quality metrics and closed-loop utility rank models differently, and most metrics need ground-truth futures that interventions destroy. Entry points: [Evaluation Dimensions](#-evaluation-dimensions); *Validate the Dream*, *Reference-Free Physical Consistency* ([§3.3](#33-closed-loop-simulation--evaluation)); World-in-World ([Benchmarks](#-benchmarks--evaluation)).
6. **Safety, robustness, and the trusted-imagination attack surface.** Imagined futures now gate real actions, which makes the world model itself a target: adversarial contexts, data poisoning that only manifests downstream, and optimistic rollouts that hide failures. Entry points: BadWorld, *World-Model Supply-Chain Poisoning*, *Trusted Imagination Attacks*, *World Models in Pieces* ([§3.5](#35-safety-aware-agentic-world-models)); RoboTrustBench ([Benchmarks](#-benchmarks--evaluation)).
7. **Data: action labels are the bottleneck.** Internet video is abundant but action-free; robot data is labeled but tiny and embodiment-specific. Latent actions, inverse dynamics, human-video transfer, and synthetic data engines each cover part of the gap. Entry points: WALA, EgoWAM, LaST-HD ([§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam)); DreamDojo, PlayWorld ([§1.3.1](#13-embodied-ai--robotics--generative)); *Geographic Diversity for JEPA Driving WMs* ([§1.2.4](#12-autonomous-driving--generative)).
8. **Sim-to-real and real-to-sim closure.** When can a policy trained or validated inside a learned world model be trusted on hardware — and can real recordings be lifted into simulation-ready twins automatically? Entry points: [§1.3.5](#13-embodied-ai--robotics--generative); *Efficient Sim-to-Real WAM* ([§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam)); RWM-O, *Robotic World Model* ([§1.3.3](#13-embodied-ai--robotics--generative)); *Quadrotor WM Generalization* ([§1.3.2](#13-embodied-ai--robotics--generative)).
9. **Multi-agent shared worlds.** Almost everything in this list models one agent's view; shared, jointly consistent worlds with other goal-directed agents (traffic, multiplayer, social dynamics) are barely started. Entry points: [§3.4](#34-multi-agent-world-models); Solaris, *Multiplayer Interactive World Models* ([§1.1.2](#11-game--interactive-world-simulation)); SceneDiffuser++ ([§1.2.4](#12-autonomous-driving--generative)).
10. **Are video generators world models?** The Sora debate, still unresolved: implicit dynamics demonstrably emerge, and demonstrably violate physical law out of distribution. The productive version of the question is *what additional structure converts one into the other*. Entry points: *Is Sora a World Simulator?*, *Mechanistic View on Video Generation as WMs*, *Critiques of World Models* ([Surveys](#-surveys--position-papers)); the §1.6/§1.7 boundary notes ([§1.6](#16-general-video-world-models--rollout-backbones), [§1.7](#17--persistent-narrative--multi-shot-video-world-models)).
11. **Reconstruction vs. representation.** Should the model predict pixels at all? Decoder-free (JEPA, TD-MPC2) and decoder-optional designs are cheaper and sometimes plan better, but are harder to inspect and evaluate. Entry points: *Reconstruction or Semantics?* ([Surveys](#-surveys--position-papers)); *ImageWAM*, *Fast-WAM* ([§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam)); [§2.2](#22-joint-embedding-predictive-architectures-jepa) theory entries.
12. **Real-time inference economics.** Interactive world models must generate under strict latency budgets; distillation, delta tokens, keyframe sparsity, and flash-style serving all exist because full-fidelity imagination is currently too slow to act on. Entry points: *A Frame is Worth One Token* ([§1.1.1](#11-game--interactive-world-simulation)); SKIP, LaWAM ([§1.3.1](#13-embodied-ai--robotics--generative), [§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam)); minWM, MoWorld, FlashDreams ([§1.6](#16-general-video-world-models--rollout-backbones), [Toolkits](#-community-resources--open-repositories)).

[⬆ Back to Top](#-table-of-contents)

---

## ❓ FAQ

**Q1. Is Sora a world model?**
Unresolved, and this list treats it that way. OpenAI's 2024 report frames video generation models as world simulators ([Blogs](#-selected-technical-blogs--reports)); the survey *Is Sora a World Simulator?* and the physical-law study *PhyWorld* ([Surveys](#-surveys--position-papers), [§1.5.1](#15-scientific--physical-world-modeling)) document both the emergent dynamics and the systematic violations. Operationally: a video generator qualifies for the taxonomy here only when it demonstrates action conditioning, state persistence, or evaluable world-model use — the boundary stated at the top of [§1.6](#16-general-video-world-models--rollout-backbones).

**Q2. What is the difference between a VLA, a world model, and a WAM?**
A VLA maps observation + language directly to actions; a world model predicts what happens next under actions or interventions; a WAM does both in one backbone — it jointly predicts futures and actions. See the *VLA vs. WAM* glossary entry, [§1.3.4](#134-world-model-based-vision-language-action-vla--world-action-models-wam), and the empirical comparison *Do World Action Models Generalize Better than VLAs?* ([Surveys](#-surveys--position-papers)).

**Q3. Why are generic video-generation papers excluded?**
Because implicit visual dynamics alone are below the bar. An entry needs at least two of: models state; predicts state evolution under action/intervention; supports imagination, planning, evaluation, or controllable simulation ([Definition and Scope](#definition-and-scope)). Video length, resolution, identity consistency, and multi-shot output do not qualify by themselves — [§1.7](#17--persistent-narrative--multi-shot-video-world-models) spells this out for the hardest boundary cases.

**Q4. How are duplicates handled?**
Every paper has exactly one home section, chosen by main technical role. Intentional cross-references are plain-text pointers like *(see §1.2.3)*, not repeated links. CI runs `node scripts/check-arxiv-duplicates.mjs README.md`, which fails on any arXiv ID appearing twice unless it is allowlisted in `.github/arxiv-duplicate-allowlist.json` with a reason.

**Q5. How do I add a paper?**
For a lightweight suggestion, open a paper-suggestion issue. For a curated addition, open a PR following [CONTRIBUTING.md](CONTRIBUTING.md): use the existing entry format, link primary sources, place it in the most appropriate section, keep the one-line description factual, and run the lint commands in the checklist. Taxonomy changes need their own justification (which entries move, and why the current tree fails them).

**Q6. A paper fits both Generative and Representational — where does it go?**
By its **main technical contribution**, not its outputs. A model that predicts latents and *optionally* decodes pixels is representational; a model whose contribution is the synthesized observation stream is generative; a model wrapped in planning/acting machinery is agentic. Domain placement comes second — see the routing rule in [Definition and Scope](#definition-and-scope).

**Q7. Is my perception / segmentation / trajectory-forecasting paper in scope?**
Usually not on its own. Pure perception answers "what is in the scene now", not "what happens if". It enters when it carries a genuine world-modeling role — e.g. occupancy *forecasting* under ego action ([§1.2.2](#12-autonomous-driving--generative)) rather than occupancy estimation.

**Q8. Is a physics simulator or a digital twin a world model?**
Not by default. Hand-built simulators execute engineered dynamics; digital twins mirror one specific asset. This list includes them when they are *learned*, when they are constructed automatically from observation (Real2Sim, [§1.3.5](#13-embodied-ai--robotics--generative)), or when a learned model plays the simulator's role (neural simulators — see the Glossary). The *Digital Twin AI* survey ([Surveys](#-surveys--position-papers)) covers the relationship.

**Q9. What exactly is a "World Foundation Model"?**
A pretrained model of environment structure and dynamics that supports multiple downstream uses — simulation, planning, forecasting, data generation — as defined in the [working definitions](#-taxonomic-overview). Cosmos, Genie, and V-JEPA 2 are the canonical examples here. It is a claim about pretraining breadth and reusability, not about any particular architecture.

**Q10. Why is a famous paper missing?**
Three common reasons: it is out of scope under the two-of-three boundary (most video generation and most VLAs); it is a secondary source (commentary, re-implementations, news); or it genuinely slipped through — in which case, see Q5. Absence is a scope judgment before it is an omission.

**Q11. What do the `GitHub` badges guarantee?**
Official code or the official project repository only. Unofficial reimplementations are deliberately not badged, per [CONTRIBUTING.md](CONTRIBUTING.md). If an official repo appears later, PRs updating the badge are welcome.

**Q12. How often is the list updated, and what does a "curation pass" mean?**
The header states the date of the last full pass (e.g. *verified against arXiv on July 11, 2026*). A pass means links and IDs were re-checked against arXiv and the duplicate check was run — not merely that entries were appended. The [News](#-news) section records structural changes.

[⬆ Back to Top](#-table-of-contents)

---

## 📊 List Statistics

<!-- The placeholders below are meant to be filled (and periodically re-filled) by a maintainer or a script.
     Counting rules — keep these stable so numbers are comparable across passes:
     - unique arXiv papers:   count of distinct arXiv IDs, exactly as computed by
                              `node scripts/check-arxiv-duplicates.mjs README.md` (it prints "N unique IDs").
                              Equivalent: rg -o 'arxiv\.org/abs/[0-9]{4}\.[0-9]{4,5}' README.md | sort -u | wc -l
     - total entries:         count of taxonomy bullets and table rows that name a work, i.e. lines matching
                              `^- \*\*` plus paper rows in the §2.1, §3.1, Surveys, and Benchmarks tables.
     - official-code links:   rg -c 'img.shields.io/badge/GitHub' README.md   (badge occurrences; official code only, per badge policy)
     - project pages:         rg -c 'img.shields.io/badge/Project' README.md
     - taxonomy sections:     numbered `##`/`###`/`####` headings inside sections 0–3 (subsections included).
     - benchmarks:            rows in the Benchmarks & Evaluation table.
     - surveys:               rows across the four Surveys & Position Papers tables.
     - last verified:         date of the latest full curation pass (must match the header line).
-->

| Statistic | Value |
| --- | --- |
| Unique arXiv papers | <!-- STATS: unique-arxiv-ids --> |
| Total curated entries (papers + resources) | <!-- STATS: total-entries --> |
| Entries with official code (`GitHub` badges) | <!-- STATS: github-code-badges --> |
| Official project pages (`Project` badges) | <!-- STATS: project-page-badges --> |
| Taxonomy sections and subsections | <!-- STATS: taxonomy-sections --> |
| Benchmarks tracked | <!-- STATS: benchmarks --> |
| Surveys & position papers tracked | <!-- STATS: surveys --> |
| Last full curation pass | <!-- STATS: last-verified --> |

Counts follow the rules in the comment above; the arXiv figure is definitionally consistent with the CI duplicate check, so the two can never disagree. For calibration: on the 2026-08-25 snapshot the raw counts were ~730 unique arXiv IDs, ~239 `GitHub` badges, and 772 total arXiv link occurrences — recompute rather than reuse these.

[⬆ Back to Top](#-table-of-contents)

---

## Suggested TOC Insertions

The TOC already contains `- [⭐ Why Star This Repo?](#-why-star-this-repo)` (the section body was missing; this draft supplies it — no TOC change needed for that line). Insert the following new entries:

Immediately after `- [⭐ Why Star This Repo?](#-why-star-this-repo)`:

```markdown
- [🧭 How to Use This List](#-how-to-use-this-list)
- [🎓 Reading Roadmap](#-reading-roadmap)
```

Immediately after `- [🗺️ Taxonomic Overview](#-taxonomic-overview)`:

```markdown
- [⏳ Historical Timeline](#-historical-timeline)
- [🧩 Architecture Cheat Sheet](#-architecture-cheat-sheet)
```

Immediately after `- [📚 Surveys & Position Papers](#-surveys--position-papers)`:

```markdown
- [🚧 Open Problems](#-open-problems)
```

Immediately before `- [📊 Benchmarks & Evaluation](#-benchmarks--evaluation)`:

```markdown
- [🧪 Evaluation Dimensions](#-evaluation-dimensions)
```

Immediately after `- [📊 Benchmarks & Evaluation](#-benchmarks--evaluation)`:

```markdown
- [📘 Glossary](#-glossary)
```

Immediately after `- [🌐 Community Resources & Open Repositories](#-community-resources--open-repositories)`:

```markdown
- [🏭 Labs, Companies & Open Stacks](#-labs-companies--open-stacks)
```

Immediately before `- [📖 Citation](#-citation)`:

```markdown
- [❓ FAQ](#-faq)
- [📊 List Statistics](#-list-statistics)
```

Anchor sanity check (GitHub slug rules — emoji stripped, spaces to hyphens, punctuation dropped): `#-why-star-this-repo`, `#-how-to-use-this-list`, `#-reading-roadmap`, `#-historical-timeline`, `#-architecture-cheat-sheet`, `#-glossary`, `#-evaluation-dimensions`, `#-labs-companies--open-stacks` (comma dropped, `&` becomes a double hyphen), `#-open-problems`, `#-faq`, `#-list-statistics`. None collide with existing anchors (`#-list-statistics` vs. `#-benchmarks--evaluation` share the 📊 emoji but slugs differ).

---

## Suggested News Item (2026-08-25)

Add at the top of `## 📰 News`:

```markdown
- **[2026-08-25]** 🧭 Structural refresh: the README now carries full handbook front-matter — [Why Star This Repo?](#-why-star-this-repo) (previously TOC-linked but missing), [How to Use This List](#-how-to-use-this-list), a three-track [Reading Roadmap](#-reading-roadmap), a [Historical Timeline](#-historical-timeline) (1943–2026), an [Architecture Cheat Sheet](#-architecture-cheat-sheet), a [Glossary](#-glossary), [Evaluation Dimensions](#-evaluation-dimensions), [Labs, Companies & Open Stacks](#-labs-companies--open-stacks), [Open Problems](#-open-problems), an [FAQ](#-faq), and [List Statistics](#-list-statistics). No taxonomy changes; no paper entries added or moved.
```

Also update, in the same commit: the `Last Updated` badge (`Updated-July%202026` → `Updated-August%202026`) and — only if a link/ID re-verification is actually performed — the *"Latest curation pass verified against arXiv on July 11, 2026"* line.

---

## Verification Notes (for the reviewer; delete before merging)

- **Not currently entries in `README.md`** (mentioned as flagged context only): Craik 1943 (*The Nature of Explanation*), Tolman 1948 (*Cognitive Maps in Rats and Men*), Sutton 1991 (Dyna), and any Tesla occupancy material. Verify before turning any of these into linked entries; the timeline and labs table already mark them inline.
- Every other paper, benchmark, toolkit, and blog named in this draft was checked against the 2026-08-25 snapshot of `README.md` and is an existing entry under the section it is linked to.
- No arXiv URLs appear anywhere in these sections, by design (see Paste Note 2), so merging them cannot break `check-arxiv-duplicates.mjs`.
