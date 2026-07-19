[![](https://capsule-render.vercel.app/api?type=waving&color=0:0a0f1a,50:1a1040,100:4f17a8&height=120&section=header&text=Harsh%20Jain&fontSize=42&fontColor=ffffff&fontAlignY=65&animation=fadeIn)](https://camo.githubusercontent.com/45bdcca6487d7eb359d9198352fc14ce5ecec07a00a1f128306b4bc98f8a3258/68747470733a2f2f63617073756c652d72656e6465722e76657263656c2e6170702f6170693f747970653d776176696e6726636f6c6f723d303a3061306631612c35303a3161313034302c3130303a346631376138266865696768743d3132302673656374696f6e3d68656164657226746578743d48617273682532304a61696e26666f6e7453697a653d343226666f6e74436f6c6f723d66666666666626666f6e74416c69676e593d363526616e696d6174696f6e3d66616465496e)

### Applied ML & AI Engineer · Adversarial RL · LLM Fine-Tuning · Production ML Systems

[![LinkedIn](https://img.shields.io/badge/LinkedIn-harsh--jain0621-0a66c2?style=flat-square&logo=linkedin)](https://linkedin.com/in/harsh-jain0621)
[![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97%20HuggingFace-Harsh--4210-ff9d00?style=flat-square)](https://huggingface.co/Harsh-4210)
[![Email](https://img.shields.io/badge/Email-harshjain0621%40gmail.com-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:harshjain0621@gmail.com)
[![Profile views](https://komarev.com/ghpvc/?username=Harsh-4210&color=8b5cf6&style=flat-square&label=Profile+Views)](https://github.com/Harsh-4210)

*B.E. Artificial Intelligence & Data Science @ SPPU · GPA 8.75/10*

*I train RL agents that learn what humans never state, and ship ML systems that survive production.*

---

## 🧠 Flagship Project — ConflictBench

> **Business instructions contradict. ConflictBench teaches LLMs to resolve them.**

ConflictBench is an RL environment that trains language models to resolve contradictory business directives by discovering an implicit 6-tier authority hierarchy — **Legal > C-Suite > VP > Director > Team Lead > IC** — entirely from reward signal. The hierarchy is never stated in the prompt; the model discovers it through episodes of 8–28 directives with 2–6 embedded conflict pairs.

```
┌──────────────────────────────────────────────────────────────────┐
│  Scenario Generator  →  8–28 directives, 2–6 conflict pairs      │
│  Reward Function     →  5-rubric deterministic (no LLM judge)    │
│  Training            →  GRPO + LoRA (r=32) on Qwen2.5-3B         │
│  Hardware            →  Single A100 48GB · 2 epochs · 400 scenes │
│  Output              →  Conflict-free resolution + JSON schema   │
└──────────────────────────────────────────────────────────────────┘
```

| Metric                | Result                                                                   |
| ---------------------- | ------------------------------------------------------------------------ |
| Composite reward lift  | **0.14 → 0.50 (+257%)** over zero-shot baseline                          |
| Reward rubrics         | Correctness · Contradiction-freedom · F1 · Efficiency · Schema           |
| Training               | GRPO + LoRA (r=32) on Qwen2.5-3B, A100 48GB                              |
| Recognition            | **Finalist — Meta × PyTorch × HuggingFace OpenEnv Hackathon, Bangalore** |

[![GitHub](https://img.shields.io/badge/GitHub-Conflict__Bench-181717?style=flat-square&logo=github)](https://github.com/Harsh-4210/Conflict_Bench)
[![HuggingFace](https://img.shields.io/badge/%F0%9F%A4%97%20LoRA%20Adapter-live-ff9d00?style=flat-square)](https://huggingface.co/Harsh-4210)

---

## ⚔️ ARMS RACE — Adversarial Oversight Arena

> **Train AI to catch AI hallucinations — adversarially, continuously, at scale.**

A two-agent zero-sum adversarial RL loop for hallucination detection: a **Red-Team** agent learns to generate subtle, confident hallucinations; a **Blue-Team (Overseer)** agent learns to detect, probe, and flag them — both trained with real gradient updates (PPO/GRPO via Unsloth), not rule-based heuristics.

**Two versions exist, reflecting the project's evolution:**

| | **V1 — Hackathon Build** | **V3.0 — Grand Finale Rebuild** |
|---|---|---|
| Repo | [`LLM_HALLUCINATION_RL`](https://github.com/Harsh-4210/LLM_HALLUCINATION_RL) | [`Inquisitor`](https://github.com/Harsh-4210/Inquisitor) |
| Scope | Original red/blue adversarial loop, Expert Correction Training (ECT) | Full rebuild: pluggable model adapters, domain adapters, curriculum learning, semantic similarity scoring, confidence calibration, belief-state tracking, failure replay buffer |
| Result | 25% → 100% detection, 4% false-alarm rate, 96% OOD generalization | Adds a 3-line evaluation API (`ArmsRaceRunner`) to stress-test any LLM (OpenAI/Anthropic/HuggingFace/Custom) across Trivia/Medical/Legal domains |

**Key results (V1):**
- **Expert Correction Training (ECT):** converts failed RL steps into supervised signal, preventing policy collapse
- Hallucination detection: **25% → 100%** with **4% false-alarm rate**
- **96% OOD generalisation** across unseen domains
- Asymmetric rewards (TP+0.6, FP−2.0, FN−0.6) + zero-sum ELO tracking

**V3.0 innovations:** semantic similarity scoring (forces subtler deception from red-team), confidence calibration (rewards honest uncertainty), difficulty curriculum, belief-state accumulation across evidence signals, failure replay buffer (300–500 stored failures, replayed at 40% of each batch).

*Built for the Meta × PyTorch × HuggingFace OpenEnv Hackathon Grand Finale, Bangalore, April 2026.*

`PPO` `GRPO` `LoRA` `PEFT` `REINFORCE` `SFT` `Unsloth`

---

## 🔬 Projects

### AssetFlow — Enterprise Asset & Resource Management
*Built with Team Artemis for the Odoo Hackathon*

A general-purpose ERP module for organizations managing physical assets — structured asset lifecycles (Available → Allocated → Under Maintenance → Retired), centralized resource booking with strict overlap prevention, approval-gated maintenance workflows, and scheduled audit cycles with auto-generated discrepancy reports.

- Role-based workflows: signup only creates a plain Employee; admins promote from the Employee Directory
- Deliberately scoped — no purchasing/invoicing/accounting, just a clean, well-modelled asset module
- **Team:** [Harsh Jain](https://github.com/Harsh-4210) + Team Artemis

`TypeScript` `Node.js` `PostgreSQL` `React` `Vite`
[GitHub](https://github.com/Harsh-4210/Team-Artemis-)

### Self-Evolving Multi-Agent Governance
*Built in 24 hours for Fusion Hackathon 2025, with Yash Doke and Viraj Jadhao*

A decentralized multi-agent system where RL agents autonomously propose, enforce, and evolve governance rules — token policies, transaction regulations, market mechanisms — exhibiting emergent economic behavior without centralized control.

- Agents propose/modify rules via Reputation-Weighted Quadratic Voting
- Disputes resolved through game-theoretic Nash Bargaining negotiation
- Adaptive agents trained via PPO in Ray RLlib across a PettingZoo multi-agent environment
- Real-time visualization dashboard (Dash/Plotly) for governance metrics, reputations, proposals

`Python` `PPO` `Ray RLlib` `PettingZoo` `Supabase` `PostgreSQL` `gRPC` `Redis`
[GitHub](https://github.com/Harsh-4210/Self_Evolving_Multi_Agent_Governance)

### AI-Generalist — Automated DDR Report Generator

An automated pipeline converting building inspection + thermal imaging PDF reports into professional, client-ready Detailed Diagnostic Reports using multimodal AI.

- Extracts text + images from paired PDFs via PyMuPDF, analyzes with Gemini 2.5 Flash, generates a structured 7-section DDR (issue summary, area-wise observations, root cause, severity, recommended actions) as a formatted PDF via ReportLab
- Page-proximity image matching with deduplication; explicit "Not Available" flagging rather than fabricating missing data
- Full pipeline: React + Vite (upload UI) → FastAPI (orchestration) → Gemini 2.5 Flash → ReportLab (PDF output)

`React` `FastAPI` `PyMuPDF` `Gemini 2.5 Flash` `ReportLab`
[GitHub](https://github.com/Harsh-4210/AI-Generalist) · [Live Demo](https://ai-generalist-rust.vercel.app)

### NutriSense AI
*Built in under 3 hours for the AMD Workshop Hackathon*

An AI-powered food & health app that analyzes meals via photo or text and delivers personalized dietary recommendations.

- Multimodal food analyzer (Gemini 2.0 Flash) with a local dataset of 80+ Indian dishes for instant offline-fallback recognition
- Real-time AI nutritionist chat, dynamic macro/calorie dashboard, healthy-restaurant finder via Google Maps
- Multi-language support (English, Hindi, Marathi); WCAG AA accessible; zero third-party UI libraries, <1MB repo size
- Dockerized for Google Cloud Run deployment

`JavaScript` `Vite` `Node.js/Express` `Gemini API` `Firebase` `Docker`
[GitHub](https://github.com/Harsh-4210/NutriClean)

### TraceLink — Manufacturing Traceability
*AMD Slingshot Regional Ideathon*

Full forward/backward traceability across 6 entity types — raw material lots to customer dispatch orders.

- 6-role RBAC with Firebase ID-token verification
- CSV ingestion with full rollback + request-level audit trail
- Natural-language AI query endpoint for non-technical users
- Containerized (Bun + FastAPI), deployed on Render with auto-deploy

`FastAPI` `React` `Firebase Auth` `SQLite` `Docker`
[GitHub](https://github.com/ruxir-ig/mccia-tracelink) · [Live](https://trace-link-mccia.vercel.app)

### Arivon — Adaptive Learning Platform
*🥉 3rd Place — Pragyantra, PES Modern College of Engineering*

Detects metacognitive miscalibration — when a student's confidence diverges from actual performance — and dynamically adjusts learning paths.

- Bloom's taxonomy difficulty engine
- Voice-based exam interface via Groq Whisper
- RAG-powered study mentor (Haystack) + React Flow knowledge graph

`Next.js 15` `FastAPI` `Groq Whisper` `Haystack RAG` `MongoDB` `Redis`
[GitHub](https://github.com/Harsh-4210/Arivon)

### SO₂ Emission Prediction System

End-to-end ML pipeline predicting SO₂ emissions from Indian coal power plants, deployed as a containerised microservice.

- **85% accuracy** on held-out test data via cross-validation
- Optuna-based hyperparameter tuning on XGBoost
- **20% efficiency boost** through feature engineering + pipeline automation
- Comprehensive REST API with structured error handling

`XGBoost` `FastAPI` `Docker` `PostgreSQL` `Optuna`
[GitHub](https://github.com/Harsh-4210/SO2-Emission-Prediction)

### Applied ML Foundations — Prodigy InfoTech Internship

Three applied ML projects spanning regression, clustering, and computer vision:

- **Regression:** Linear regression predicting house prices from structured property data, R² = 0.52
- **Clustering:** K-Means customer segmentation (Elbow Method), identifying 5 distinct customer segments
- **Computer Vision:** SVM-based cat/dog classifier with PCA + GridSearchCV tuning, 55% → 62% accuracy after tuning

`Python` `Pandas` `Scikit-learn`
[GitHub](https://github.com/Harsh-4210/PRODIGY_ML_PROJECTS)

---

## 🏆 Hackathons & Awards

| | Result | Event | Project |
| --- | --- | --- | --- |
| 🥇 | **Finalist** | Meta × PyTorch × HuggingFace OpenEnv Hackathon, Bangalore | `ConflictBench` |
| 🏅 | **Top 100** | Scaler School of Technology OpenEnv Pre-Selection | `ConflictBench` |
| 🚀 | **Built** | Meta × PyTorch × HuggingFace OpenEnv Hackathon Grand Finale | `ARMS RACE V3.0` |
| 🏗️ | **Built (Team)** | Odoo Hackathon | `AssetFlow` |
| 🧬 | **Built (Team)** | Fusion Hackathon 2025 | `Self-Evolving Multi-Agent Governance` |
| ⚡ | **Built** | AMD Workshop Hackathon | `NutriSense AI` |
| 🥉 | **3rd Place** | Pragyantra, PES Modern College of Engineering | `Arivon` |

---

## ⚙️ Tech Stack

```
LANGUAGES    = ["Python", "SQL", "JavaScript", "TypeScript"]

ML_RL        = ["PyTorch", "GRPO", "PPO", "LoRA/QLoRA", "TRL", "Unsloth",
                "Ray RLlib", "PettingZoo", "HuggingFace Transformers", "PEFT"]

VISION       = ["YOLOv8", "ONNX Runtime", "OpenCV", "Albumentations"]

LLM_INFRA    = ["RAG Pipelines", "RLHF", "Adversarial RL", "Agentic AI",
                "Haystack", "Groq Whisper", "Gemini API (2.0/2.5 Flash)"]

BACKEND      = ["FastAPI", "Next.js 15", "React", "Node.js/Express"]

INFRA_DB     = ["Docker", "GitHub Actions", "Google Cloud Run", "gRPC", "Redis",
                "PostgreSQL", "MongoDB", "Supabase", "Firebase"]

ROBOTICS     = ["ROS2", "Gazebo", "Jetson Orin Nano"]

CERTS        = ["Deep Learning Specialization (Andrew Ng)",
                "Generative AI with LLMs (AWS / Coursera)",
                "LLM Fundamentals (Hugging Face)"]
```

---

## 📊 GitHub Stats

![](https://github-readme-stats.vercel.app/api?username=Harsh-4210&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=8b5cf6&icon_color=8b5cf6&text_color=c9d1d9&include_all_commits=true&count_private=true)
![](https://github-readme-stats.vercel.app/api/top-langs/?username=Harsh-4210&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=8b5cf6&text_color=c9d1d9&langs_count=8)

![](https://github-readme-streak-stats.herokuapp.com?user=Harsh-4210&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=8b5cf6&ring=8b5cf6&fire=8b5cf6&currStreakLabel=8b5cf6&dates=8b949e)

![](https://github-profile-trophy.vercel.app/?username=Harsh-4210&theme=algolia&no-frame=true&no-bg=true&column=6&margin-w=8)

---

## 📈 Contribution Activity

![](https://github-readme-activity-graph.vercel.app/graph?username=Harsh-4210&bg_color=0d1117&color=8b5cf6&line=4f17a8&point=8b5cf6&area=true&area_color=4f17a8&hide_border=true)

---

## 🎯 Currently

- 🔬 Building adversarial RL systems and LLM fine-tuning pipelines
- 🤖 Working on the computer vision & object detection stack (OpenCV + YOLO, on Jetson Orin Nano) for **Team Vulcans**, ABU Robocon 2026
- 🏗️ Shipping production ML and full-stack systems with FastAPI, React, and Docker
- 📖 B.E. AI & Data Science @ SPPU · **Open to ML engineering roles & research internships**
- 📬 Reach me: <harshjain0621@gmail.com> · [linkedin.com/in/harsh-jain0621](https://linkedin.com/in/harsh-jain0621)

---

*"I don't just train models — I build systems that ship, scale, and survive production."*

[![Profile views](https://komarev.com/ghpvc/?username=Harsh-4210&color=8b5cf6&style=flat-square&label=Profile+Views)](https://github.com/Harsh-4210)
