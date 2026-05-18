<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0f1a,50:1a1040,100:4f17a8&height=120&section=header&text=Harsh%20Jain&fontSize=42&fontColor=ffffff&fontAlignY=65&animation=fadeIn" width="100%"/>

### Applied ML & AI Engineer · Adversarial RL · LLM Fine-Tuning · Production ML Systems

[![LinkedIn](https://img.shields.io/badge/LinkedIn-harsh--jain0621-0a66c2?style=flat-square&logo=linkedin)](https://linkedin.com/in/harsh-jain0621)
[![HuggingFace](https://img.shields.io/badge/🤗%20Hugging%20Face-Harsh--4210-ff9d00?style=flat-square)](https://huggingface.co/Harsh-4210)
[![Email](https://img.shields.io/badge/Email-harshjain0621@gmail.com-ea4335?style=flat-square&logo=gmail&logoColor=white)](mailto:harshjain0621@gmail.com)
![Profile views](https://komarev.com/ghpvc/?username=Harsh-4210&color=8b5cf6&style=flat-square&label=Profile+Views)

*B.E. Artificial Intelligence & Data Science @ SPPU · GPA 8.75/10*

*I train RL agents that learn what humans never state, and ship ML systems that survive production.*

</div>

---

## 🧠 Flagship Project — ConflictBench

> **Business instructions contradict. ConflictBench teaches LLMs to resolve them.**

ConflictBench is an RL environment that trains language models to resolve contradictory business directives by discovering an implicit 6-tier authority hierarchy — **Legal > C-Suite > VP > Director > Team Lead > IC** — entirely from reward signal. The hierarchy is never stated in the prompt; the model discovers it through episodes of 8–28 directives with 2–6 embedded conflict pairs.

```
┌──────────────────────────────────────────────────────────────────┐
│  Scenario Generator  →  8–28 directives, 2–6 conflict pairs     │
│  Reward Function     →  5-rubric deterministic (no LLM judge)   │
│  Training            →  GRPO + LoRA (r=32) on Qwen2.5-3B        │
│  Hardware            →  Single A100 48GB · 2 epochs · 400 scenes │
│  Output              →  Conflict-free resolution + JSON schema   │
└──────────────────────────────────────────────────────────────────┘
```

| Metric | Result |
|--------|--------|
| Composite reward lift | **0.14 → 0.50 (+257%)** over zero-shot baseline |
| Reward rubrics | Correctness · Contradiction-freedom · F1 · Efficiency · Schema |
| Training | GRPO + LoRA (r=32) on Qwen2.5-3B, A100 48GB |
| Recognition | **Finalist — Meta × PyTorch × HuggingFace OpenEnv Hackathon, Bangalore** |

[![GitHub](https://img.shields.io/badge/GitHub-Conflict__Bench-181717?style=flat-square&logo=github)](https://github.com/Harsh-4210/Conflict_Bench)
[![HuggingFace](https://img.shields.io/badge/🤗%20LoRA%20Adapter-live-ff9d00?style=flat-square)](https://huggingface.co/Harsh-4210)
[![Demo](https://img.shields.io/badge/🤗%20Base%20vs%20Fine--Tuned%20Demo-live-ff9d00?style=flat-square)](https://huggingface.co/Harsh-4210)

---

## 🔬 Projects

<table>
<tr>
<td width="50%" valign="top">

### [ARMSRACE — Adversarial Oversight Arena](https://github.com/Harsh-4210/LLM_HALLUCINATION_RL)

Two-agent zero-sum adversarial loop for hallucination detection — Red Agent generates plausible silent-failure hallucinations, Blue Agent acts as a factual gatekeeper.

- **Expert Correction Training (ECT):** converts failed RL steps into supervised signal, preventing policy collapse
- Hallucination detection: **25% → 100%** with **4% false-alarm rate**
- **96% OOD generalisation** across unseen domains
- Asymmetric rewards (TP+0.6, FP−2.0, FN−0.6) + zero-sum ELO tracking

`PPO` `LoRA` `PEFT` `REINFORCE` `SFT`

</td>
<td width="50%" valign="top">

### [TraceLink — Manufacturing Traceability](https://github.com/ruxir-ig/mccia-tracelink)

Production-deployed system for full forward/backward traceability across 6 entity types — raw material lots to customer dispatch orders.

- 6-role RBAC with Firebase ID-token verification
- CSV ingestion with full rollback + request-level audit trail
- Natural-language AI query endpoint for non-technical users
- Containerised (Bun + FastAPI) → deployed on Render with auto-deploy

`FastAPI` `React` `Firebase Auth` `SQLite` `Docker`

</td>
</tr>
<tr>
<td width="50%" valign="top">

### [Arivon — Adaptive Learning Platform](https://github.com/Harsh-4210/Arivon)

Detects metacognitive miscalibration — when a student's confidence diverges from actual performance — and dynamically adjusts learning paths.

- Bloom's taxonomy difficulty engine
- Voice-based exam interface via Groq Whisper
- RAG-powered study mentor (Haystack) + React Flow knowledge graph
- **🥉 3rd Place — Pragyantra, PES Modern College of Engineering**

`Next.js 15` `FastAPI` `Groq Whisper` `Haystack RAG` `MongoDB` `Redis`

</td>
<td width="50%" valign="top">

### [SO₂ Emission Prediction System](https://github.com/Harsh-4210/SO2-Emission-Prediction)

End-to-end ML pipeline predicting SO₂ emissions from Indian coal power plants, deployed as a containerised microservice.

- **85% accuracy** on held-out test data via cross-validation
- Optuna-based hyperparameter tuning on XGBoost
- **20% efficiency boost** through feature engineering + pipeline automation
- Comprehensive REST API with structured error handling

`XGBoost` `FastAPI` `Docker` `PostgreSQL` `Optuna`

</td>
</tr>
</table>

---

## 🏆 Hackathons & Awards

<table>
<tr>
<td>🥇</td>
<td><strong>Finalist</strong> — Meta × PyTorch × HuggingFace OpenEnv Hackathon, Bangalore</td>
<td><code>ConflictBench</code></td>
</tr>
<tr>
<td>🏅</td>
<td><strong>Top 100</strong> — Scaler School of Technology OpenEnv Pre-Selection</td>
<td><code>ConflictBench</code></td>
</tr>
<tr>
<td>🥉</td>
<td><strong>3rd Place</strong> — Pragyantra, PES Modern College of Engineering</td>
<td><code>Arivon</code></td>
</tr>
</table>

---

## ⚙️ Tech Stack

```python
LANGUAGES    = ["Python", "SQL", "JavaScript", "TypeScript"]

ML_RL        = ["PyTorch", "GRPO", "PPO", "LoRA/QLoRA", "TRL", "Unsloth",
                "Ray RLlib", "HuggingFace Transformers", "PEFT"]

VISION       = ["YOLOv8", "ONNX Runtime", "OpenCV", "Albumentations"]

LLM_INFRA    = ["RAG Pipelines", "RLHF", "Adversarial RL", "Agentic AI",
                "Haystack", "Groq Whisper"]

BACKEND      = ["FastAPI", "Next.js 15", "React"]

INFRA_DB     = ["Docker", "GitHub Actions", "Google Cloud",
                "PostgreSQL", "MongoDB", "Redis"]

CERTS        = ["Deep Learning Specialization (Andrew Ng)",
                "Generative AI with LLMs (AWS / Coursera)",
                "LLM Fundamentals (Hugging Face)"]
```

---

## 📊 GitHub Stats

<div align="center">

<img height="180" src="https://github-readme-stats.vercel.app/api?username=Harsh-4210&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=8b5cf6&icon_color=8b5cf6&text_color=c9d1d9&include_all_commits=true&count_private=true" />
<img height="180" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Harsh-4210&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=8b5cf6&text_color=c9d1d9&langs_count=8" />

</div>

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com?user=Harsh-4210&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=8b5cf6&ring=8b5cf6&fire=f97316&currStreakLabel=8b5cf6&dates=8b949e" />

</div>

<div align="center">

<img src="https://github-profile-trophy.vercel.app/?username=Harsh-4210&theme=algolia&no-frame=true&no-bg=true&column=6&margin-w=8" />

</div>

---

## 📈 Contribution Activity

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Harsh-4210&bg_color=0d1117&color=8b5cf6&line=4f17a8&point=8b5cf6&area=true&area_color=4f17a8&hide_border=true" width="100%"/>

---

## 🎯 Currently

- 🔬 Building adversarial RL systems and LLM fine-tuning pipelines
- 🏗️ Shipping production ML with FastAPI + Docker
- 📖 B.E. AI & Data Science @ SPPU · **Open to ML engineering roles & research internships**
- 📬 Reach me: [harshjain0621@gmail.com](mailto:harshjain0621@gmail.com) · [linkedin.com/in/harsh-jain0621](https://linkedin.com/in/harsh-jain0621)

---

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:4f17a8,50:1a1040,100:0a0f1a&height=80&section=footer" width="100%"/>

*"I don't just train models — I build systems that ship, scale, and survive production."*

![Profile views](https://komarev.com/ghpvc/?username=Harsh-4210&color=8b5cf6&style=flat-square&label=Profile+Views)

</div>