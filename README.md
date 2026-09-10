<div align="center">

# Harsh Jain

<img src="./assets/harsh-jain-banner.svg" alt="Harsh Jain - Applied ML and AI Engineer" width="100%" />

### Applied ML & AI Engineer building systems that learn, reason, and ship

`Reinforcement Learning` · `LLM Systems` · `Production AI`

<img src="https://readme-typing-svg.demolab.com?font=Space+Grotesk&weight=600&size=20&pause=1200&color=0E75B6&center=true&vCenter=true&width=720&lines=Reinforcement+Learning+%C2%B7+LLM+Systems+%C2%B7+Production+AI;From+reward+functions+to+reliable+APIs;Building+systems+that+can+explain+how+they+decide" alt="Reinforcement Learning, LLM Systems, and Production AI" />

[![GitHub](https://img.shields.io/badge/GitHub-Harsh--4210-181717?style=for-the-badge&logo=github)](https://github.com/Harsh-4210)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Harsh%20Jain-0A66C2?style=for-the-badge&logo=linkedin)](https://www.linkedin.com/in/harsh-jain0621/)
[![Email](https://img.shields.io/badge/Email-Contact%20me-EA4335?style=for-the-badge&logo=gmail)](mailto:harshjain0621@gmail.com)

<sub>🎓 B.E. Artificial Intelligence & Data Science @ SPPU &nbsp;•&nbsp; GPA 8.75/10 &nbsp;•&nbsp; Pune, India</sub>

</div>

---

<div align="center">

<a href="#flagship-project">Flagship project</a> &nbsp;·&nbsp;
<a href="#selected-work">Selected work</a> &nbsp;·&nbsp;
<a href="#technical-stack">Technical stack</a> &nbsp;·&nbsp;
<a href="#github-activity">GitHub activity</a>

</div>

<br />

<table>
<tr>
<td width="33%" valign="top">

### ◉ Currently focused

Reliable AI with explicit evaluation, adversarial testing, and structured outputs.

</td>
<td width="33%" valign="top">

### ↗ Best fit

ML engineering, applied AI, reinforcement learning, LLM systems, and research-oriented collaborations.

</td>
<td width="33%" valign="top">

### ✦ North star

Systems that are useful beyond the demo: observable, testable, and ready to ship.

</td>
</tr>
</table>

## What I Work On

I turn research ideas into measurable, deployable systems. My work sits at the intersection of reinforcement learning, LLM systems, applied ML, and production engineering.

- **Reinforcement learning:** GRPO, PPO, reward design, environments, and agent evaluation
- **LLM systems:** fine-tuning, LoRA/QLoRA, RAG, structured generation, and agentic workflows
- **Applied ML:** computer vision, emissions prediction, feature engineering, and optimization
- **Production engineering:** FastAPI services, React applications, Docker, databases, and CI/CD

> **My approach:** design the evaluation first, make decisions traceable, and treat deployment as part of the research—not the final polish.

---

## Flagship Project

### ConflictBench &nbsp;·&nbsp; *Reward-driven authority resolution*

**Can an LLM learn authority resolution from reward alone?**

ConflictBench is a reinforcement-learning environment that teaches language models to resolve contradictory business instructions. The model infers an implicit six-tier authority hierarchy from reward signals rather than being given the rule directly:

`Legal > C-Suite > VP > Director > Team Lead > Individual Contributor`

Scenarios contain 8–28 directives and 2–6 embedded conflict pairs. The agent must detect conflicts, produce an executable plan, override lower-priority instructions, and remain consistent in structured JSON.

| Signal | Evidence |
|---|---|
| **Composite reward** | **0.14 → 0.50** — a 257% improvement over zero-shot |
| Reward design | Deterministic correctness, contradiction freedom, conflict-pair F1, efficiency, and JSON compliance |
| Training | GRPO + LoRA on Qwen2.5-3B, 400 scenarios, 2 epochs, single A100 48 GB |
| Recognition | Top 100 finalist, Meta × PyTorch × Hugging Face OpenEnv Hackathon |

[![Source Code](https://img.shields.io/badge/Source%20Code-ConflictBench-181717?style=flat-square&logo=github)](https://github.com/Harsh-4210/Conflict_Bench)
[![Live Demo](https://img.shields.io/badge/Live%20Demo-Hugging%20Face-FFD21E?style=flat-square&logo=huggingface)](https://huggingface.co/spaces/Harsh-9209/Conflict_Bench)
[![LoRA Adapter](https://img.shields.io/badge/LoRA%20Adapter-Hugging%20Face-FFD21E?style=flat-square&logo=huggingface)](https://huggingface.co/Harsh-9209/conflictbench-qwen2.5-3b-grpo-lora)

<img src="./assets/conflictbench-flow.svg" alt="ConflictBench training loop from contradictory directives through verification and reward into GRPO and LoRA training" width="100%" />

---

## Selected Work

<sub>A selection of systems spanning adversarial LLM evaluation, production traceability, adaptive learning, and applied forecasting.</sub>

### 01 — [Inquisitor / ARMS RACE V3](https://github.com/Harsh-4210/LLM_HALLUCINATION_RL)

A two-agent red/blue system for detecting silent-failure hallucinations. The Red Agent generates semantically plausible wrong answers while the Blue Agent returns structured `Pass`, `Flag`, or `Probe` decisions.

- Expert Correction Training turns failed RL steps into supervised learning signal
- Detection improved from **25% to 100%**, with a **4% false-alarm rate**
- **96% out-of-distribution generalisation** across unseen domains
- Asymmetric rewards and zero-sum ELO tracking discourage indiscriminate flagging

<img src="./assets/armsrace-loop.svg" alt="ARMS RACE loop connecting the Red Agent, Blue Agent, asymmetric reward, and correction training" width="100%" />

`PPO` &nbsp; `LoRA` &nbsp; `PEFT` &nbsp; `REINFORCE` &nbsp; `SFT`

### 02 — [TraceLink](https://github.com/ruxir-ig/mccia-tracelink)

A production-deployed manufacturing traceability platform for tracing dispatch orders backward through production batches, QC inspections, and raw-material lots, then forward from a flagged lot to affected customer orders.

- Six-entity traceability graph with forward, reverse, and blast-radius investigation
- Six-role RBAC with Firebase ID-token verification
- CSV ingestion with rollback support and request-level audit trails
- Natural-language AI query endpoint with Dockerised FastAPI and React deployment

<img src="./assets/tracelink-graph.svg" alt="TraceLink graph connecting raw lots, production batches, quality inspections, dispatch orders, and customer impact" width="100%" />

`FastAPI` &nbsp; `React` &nbsp; `Firebase Auth` &nbsp; `SQLite` &nbsp; `Docker`

### 03 — [Arivon](https://github.com/nishtha911/Pragyantra-ED14-ET-3)

An adaptive learning platform that detects when confidence diverges from actual performance and adjusts the learning path accordingly.

- Bloom's taxonomy-based difficulty adjustment
- React Flow knowledge graph and voice exam interface with Groq Whisper
- Haystack RAG study mentor backed by PostgreSQL, MongoDB, and Redis
- **3rd Place — Pragyantra, PES Modern College of Engineering**

`Next.js` &nbsp; `FastAPI` &nbsp; `Haystack` &nbsp; `MongoDB` &nbsp; `Redis`

### 04 — [SO2 Emission Prediction](https://github.com/Harsh-4210/SO2-Emission-Prediction)

An end-to-end ML pipeline for predicting SO2 emissions from Indian coal power plants.

- XGBoost with feature selection, cross-validation, and Optuna tuning
- Containerised FastAPI deployment with structured error handling
- Reproducible data-to-inference workflow

`XGBoost` &nbsp; `FastAPI` &nbsp; `Optuna` &nbsp; `Docker`

---

## Technical Stack

<table>
<tr>
<td valign="top" width="33%">

### 🧠 ML & AI

`Python` `PyTorch` `Transformers` `GRPO` `PPO` `LoRA/QLoRA` `TRL` `Unsloth` `PEFT` `Ray RLlib` `RAG` `OpenCV` `YOLOv8`

</td>
<td valign="top" width="33%">

### ⚙️ Backend & Data

`FastAPI` `React` `Next.js` `PostgreSQL` `MongoDB` `Redis` `SQL` `Firebase`

</td>
<td valign="top" width="33%">

### 🚀 Engineering

`Docker` `Docker Compose` `GitHub Actions` `GCP` `ONNX Runtime` `CI/CD` `OpenAPI`

</td>
</tr>
</table>

---

## Recognition

| ✦ | Milestone | Context |
|---|---|---|
| **Top 100 Finalist** | Meta × PyTorch × Hugging Face OpenEnv Hackathon | ConflictBench |
| **3rd Place** | Pragyantra, PES Modern College of Engineering | Arivon |
| **ML Intern** | Prodigy InfoTech · Nov 2025–Jan 2026 | Applied machine learning |

---

## GitHub Activity

<div align="center">

<a href="https://github.com/Harsh-4210">
  <img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/stats?username=Harsh-4210&theme=github_dark" alt="Harsh Jain's GitHub statistics" />
</a>
<a href="https://github.com/Harsh-4210?tab=repositories">
  <img height="180" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=Harsh-4210&theme=github_dark" alt="Harsh Jain's repositories by language" />
</a>

<br />

<img width="96%" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=Harsh-4210&theme=github_dark" alt="Harsh Jain's contribution activity graph" />

<br /><br />

[![GitHub Profile](https://img.shields.io/badge/View%20all%20repositories-Harsh--4210-0e75b6?style=for-the-badge&logo=github)](https://github.com/Harsh-4210?tab=repositories)

</div>

---

<div align="center">

### Building toward reliable AI

Explicit evaluation, adversarial testing, structured outputs, traceable decisions, and deployment paths that survive contact with real users.

[Email me](mailto:harshjain0621@gmail.com) &nbsp; · &nbsp; [Connect on LinkedIn](https://www.linkedin.com/in/harsh-jain0621/) &nbsp; · &nbsp; [Explore my repositories](https://github.com/Harsh-4210)

<br />

![Profile views](https://komarev.com/ghpvc/?username=Harsh-4210&style=flat-square&color=0e75b6&label=Profile+Views)

</div>
