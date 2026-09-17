<div align="center">

# Harsh Jain

**Applied ML & AI Engineer** — building systems that learn, reason, and ship.

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=500&size=15&pause=3000&color=8B949E&center=true&vCenter=true&width=620&height=36&lines=Reinforcement+Learning+%C2%B7+LLM+Systems+%C2%B7+Production+AI" alt="Specialization" />

[![GitHub](https://img.shields.io/badge/GitHub-Harsh--4210-161b22?style=flat-square&logo=github&logoColor=white)](https://github.com/Harsh-4210)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Harsh%20Jain-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/harsh-jain0621/)
[![Email](https://img.shields.io/badge/Email-harshjain0621%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:harshjain0621@gmail.com)
[![Hugging Face](https://img.shields.io/badge/HuggingFace-Harsh--9209-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/Harsh-9209)

<sub>B.E. Artificial Intelligence &amp; Data Science · SPPU · GPA 8.75/10 · Pune, India</sub>

</div>

---

## About

I turn research ideas into measurable, deployable systems — at the intersection of reinforcement learning, LLM systems, applied ML, and production engineering.

- **Reinforcement learning** — GRPO, PPO, reward design, environments, and agent evaluation
- **LLM systems** — fine-tuning, LoRA/QLoRA, RAG, structured generation, and agentic workflows
- **Applied ML** — computer vision, emissions prediction, feature engineering, and optimization
- **Production** — FastAPI, React, Docker, PostgreSQL, MongoDB, CI/CD

> Design the evaluation first. Make decisions traceable. Treat deployment as part of the research.

---

## GitHub Stats

<div align="center">

<img height="160" src="https://github-readme-stats.vercel.app/api?username=Harsh-4210&show_icons=true&theme=github_dark&hide_border=true&include_all_commits=true&bg_color=0d1117&title_color=c9d1d9&icon_color=58a6ff&text_color=8b949e&cache_seconds=21600" alt="GitHub Stats" />
<img height="160" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Harsh-4210&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=c9d1d9&text_color=8b949e&langs_count=6&cache_seconds=21600" alt="Top Languages" />

<img width="90%" src="https://streak-stats.demolab.com/?user=Harsh-4210&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=21262d&ring=58a6ff&fire=58a6ff&currStreakLabel=c9d1d9&sideLabels=8b949e&dates=8b949e" alt="Streak Stats" />

</div>

---

## Flagship Project

### ConflictBench — *Reward-driven authority resolution*

**Can an LLM learn authority resolution from reward alone?**

ConflictBench is a reinforcement-learning environment that teaches language models to resolve contradictory business instructions. The model infers an implicit six-tier authority hierarchy from reward signals rather than being given the rule directly:

```
Legal > C-Suite > VP > Director > Team Lead > Individual Contributor
```

Scenarios contain 8–28 directives and 2–6 embedded conflict pairs. The agent must detect conflicts, produce an executable plan, override lower-priority instructions, and remain consistent in structured JSON.

| Signal | Evidence |
|---|---|
| **Composite reward** | **0.14 → 0.50** — a 257% improvement over zero-shot |
| Reward design | Deterministic correctness, contradiction freedom, conflict-pair F1, efficiency, JSON compliance |
| Training | GRPO + LoRA on Qwen2.5-3B · 400 scenarios · 2 epochs · single A100 48 GB |
| Recognition | Top 100 finalist, Meta × PyTorch × Hugging Face OpenEnv Hackathon |

[![Source](https://img.shields.io/badge/Source-ConflictBench-161b22?style=flat-square&logo=github)](https://github.com/Harsh-4210/Conflict_Bench)
[![Demo](https://img.shields.io/badge/Demo-HF%20Spaces-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/spaces/Harsh-9209/Conflict_Bench)
[![Adapter](https://img.shields.io/badge/LoRA%20Adapter-HF%20Hub-FFD21E?style=flat-square&logo=huggingface&logoColor=black)](https://huggingface.co/Harsh-9209/conflictbench-qwen2.5-3b-grpo-lora)

<img src="./assets/conflictbench-flow.svg" alt="ConflictBench training loop" width="100%" />

---

## Selected Work

### [Inquisitor / ARMS RACE V3](https://github.com/Harsh-4210/LLM_HALLUCINATION_RL)

A two-agent red/blue system for detecting silent-failure hallucinations. The Red Agent generates semantically plausible wrong answers; the Blue Agent returns structured `Pass`, `Flag`, or `Probe` decisions.

- Expert Correction Training turns failed RL steps into supervised learning signal
- Detection improved from **25% to 100%** with a **4% false-alarm rate**
- **96% out-of-distribution generalisation** across unseen domains
- Asymmetric rewards and zero-sum ELO tracking discourage indiscriminate flagging

<img src="./assets/armsrace-loop.svg" alt="ARMS RACE loop" width="100%" />

`PPO` · `LoRA` · `PEFT` · `REINFORCE` · `SFT`

---

### [TraceLink](https://github.com/ruxir-ig/mccia-tracelink)

A production-deployed manufacturing traceability platform for tracing dispatch orders backward through production batches, QC inspections, and raw-material lots.

- Six-entity traceability graph with forward, reverse, and blast-radius investigation
- Six-role RBAC with Firebase ID-token verification
- CSV ingestion with rollback support and request-level audit trails
- Natural-language AI query endpoint with Dockerised FastAPI and React deployment

<img src="./assets/tracelink-graph.svg" alt="TraceLink graph" width="100%" />

`FastAPI` · `React` · `Firebase Auth` · `SQLite` · `Docker`

---

### [Arivon](https://github.com/nishtha911/Pragyantra-ED14-ET-3)

An adaptive learning platform that detects when confidence diverges from actual performance and adjusts the learning path accordingly.

- Bloom's taxonomy-based difficulty adjustment
- React Flow knowledge graph and voice exam interface with Groq Whisper
- Haystack RAG study mentor backed by PostgreSQL, MongoDB, and Redis
- **3rd Place — Pragyantra, PES Modern College of Engineering**

`Next.js` · `FastAPI` · `Haystack` · `MongoDB` · `Redis`

---

### [SO2 Emission Prediction](https://github.com/Harsh-4210/SO2-Emission-Prediction)

End-to-end ML pipeline for predicting SO2 emissions from Indian coal power plants.

- XGBoost with feature selection, cross-validation, and Optuna tuning
- Containerised FastAPI deployment with structured error handling
- Reproducible data-to-inference workflow

`XGBoost` · `FastAPI` · `Optuna` · `Docker`

---

## Stack

**ML / AI** — Python · PyTorch · Transformers · GRPO · PPO · LoRA/QLoRA · TRL · Unsloth · PEFT · Ray RLlib · RAG · OpenCV · YOLOv8

**Backend & Data** — FastAPI · React · Next.js · PostgreSQL · MongoDB · Redis · Firebase · SQLite

**Engineering** — Docker · Docker Compose · GitHub Actions · GCP · ONNX Runtime · CI/CD · OpenAPI

---

## Recognition

| Milestone | Context |
|---|---|
| **Top 100 Finalist** — Meta × PyTorch × Hugging Face OpenEnv Hackathon | ConflictBench |
| **3rd Place** — Pragyantra, PES Modern College of Engineering | Arivon |
| **ML Intern** — Prodigy InfoTech · Nov 2025–Jan 2026 | Applied machine learning |

---

<div align="center">

[harshjain0621@gmail.com](mailto:harshjain0621@gmail.com) &nbsp;·&nbsp; [linkedin.com/in/harsh-jain0621](https://www.linkedin.com/in/harsh-jain0621/) &nbsp;·&nbsp; [github.com/Harsh-4210](https://github.com/Harsh-4210)

![](https://komarev.com/ghpvc/?username=Harsh-4210&style=flat-square&color=8b949e&label=views)

</div>
