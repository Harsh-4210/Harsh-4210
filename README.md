<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0a0f1a,50:2d0a4e,100:8b5cf6&height=150&section=header&text=Harsh%20Jain&fontSize=44&fontColor=ffffff&fontAlignY=55&animation=fadeIn" width="100%"/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&size=20&duration=2800&pause=900&color=A78BFA&center=true&vCenter=true&width=720&lines=Applied+ML+%26+AI+Engineer+%C2%B7+Adversarial+RL;Training+agents+that+learn+what+humans+never+state;From+hackathon+prototypes+to+deployed+systems" alt="Typing SVG" />

[![GitHub](https://img.shields.io/badge/GitHub-Harsh--4210-181717?style=flat-square&logo=github)](https://github.com/Harsh-4210)
[![Portfolio](https://img.shields.io/badge/Portfolio-harsh--portfolio-8B5CF6?style=flat-square&logo=vercel&logoColor=white)](https://harsh-portfolio-delta-nine.vercel.app)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-harsh--jain0621-0A66C2?style=flat-square&logo=linkedin)](https://linkedin.com/in/harsh-jain0621)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20Hugging%20Face-Harsh--4210-FFD21E?style=flat-square)](https://huggingface.co/Harsh-4210)
[![Email](https://img.shields.io/badge/Email-harshjain0621%40gmail.com-EA4335?style=flat-square&logo=gmail&logoColor=white)](mailto:harshjain0621@gmail.com)

**BE Artificial Intelligence & Data Science @ SPPU · GPA 8.75/10**

*I train RL agents that learn what humans never state, and ship ML systems that survive production.*

</div>

---

## 🧠 ConflictBench

> **Business instructions contradict. ConflictBench teaches LLMs to resolve them.**

An RL environment that trains language models to resolve contradictory business directives by discovering an implicit 6-tier authority hierarchy — **Legal > C-Suite > VP > Director > Team Lead > IC** — entirely from reward signal. The hierarchy is never stated in the prompt; the model discovers it through episodes of 8–28 directives with 2–6 embedded conflict pairs.

<table>
<tr>
<td><b>Scenario Generator</b></td>
<td>8–28 directives per episode, 2–6 embedded conflict pairs</td>
</tr>
<tr>
<td><b>Reward Function</b></td>
<td>5-rubric deterministic — no LLM judge</td>
</tr>
<tr>
<td><b>Training</b></td>
<td>GRPO + LoRA (r=32) on Qwen2.5-3B, single A100 48GB, 2 epochs, 400 scenes</td>
</tr>
<tr>
<td><b>Output</b></td>
<td>Conflict-free resolution + structured JSON schema</td>
</tr>
</table>

| Evaluation | Result |
| :--- | :--- |
| Composite reward lift | **0.14 → 0.50 (+257%)** over zero-shot baseline |
| Reward rubrics | Correctness · Contradiction-freedom · F1 · Efficiency · Schema |
| Recognition | **Finalist — Meta × PyTorch × HuggingFace OpenEnv Hackathon, Bangalore** · Top 100, Scaler School of Technology Pre-Selection |

[![Repository](https://img.shields.io/badge/GitHub-Conflict__Bench-181717?style=flat-square&logo=github)](https://github.com/Harsh-4210/Conflict_Bench)
[![Hugging Face](https://img.shields.io/badge/%F0%9F%A4%97%20LoRA%20Adapter-live-FFD21E?style=flat-square)](https://huggingface.co/Harsh-4210)

---

## ⚔️ ARMS RACE — Adversarial Oversight Arena

> **Train AI to catch AI hallucinations — adversarially, continuously, at scale.**

A two-agent zero-sum adversarial RL loop for hallucination detection. A **Red-Team** agent learns to generate subtle, confident hallucinations; a **Blue-Team (Overseer)** agent learns to detect, probe, and flag them — both trained with real gradient updates (PPO/GRPO via Unsloth), not rule-based heuristics.

<table>
<tr>
<td><b>Core Loop</b></td>
<td>Zero-sum adversarial self-play, real gradient updates on both sides</td>
</tr>
<tr>
<td><b>V1 Innovation</b></td>
<td>Expert Correction Training (ECT) — converts failed RL steps into supervised signal, preventing policy collapse</td>
</tr>
<tr>
<td><b>V3.0 Innovations</b></td>
<td>Semantic similarity scoring · confidence calibration · difficulty curriculum · belief-state tracking · failure replay buffer</td>
</tr>
<tr>
<td><b>V3.0 Interface</b></td>
<td>3-line evaluation API (<code>ArmsRaceRunner</code>) — stress-test any LLM across pluggable model & domain adapters</td>
</tr>
</table>

| Evaluation | Result |
| :--- | :--- |
| Detection rate | **25% → 100%**, 4% false-alarm rate |
| Generalization | **96%** on out-of-domain scenarios |
| Reward design | Asymmetric (TP +0.6, FP −2.0, FN −0.6) + zero-sum ELO tracking |
| Models supported (V3) | OpenAI · Anthropic · HuggingFace · Custom |
| Domains supported (V3) | TriviaQA · Medical (PubMedQA) · Legal (CaseHold) · Custom JSON |

*Built for the Meta × PyTorch × HuggingFace OpenEnv Hackathon Grand Finale, Bangalore, April 2026.*

[![V1 Repository](https://img.shields.io/badge/GitHub-LLM__HALLUCINATION__RL%20(V1)-181717?style=flat-square&logo=github)](https://github.com/Harsh-4210/LLM_HALLUCINATION_RL)
[![V3 Repository](https://img.shields.io/badge/GitHub-Inquisitor%20(V3.0)-181717?style=flat-square&logo=github)](https://github.com/Harsh-4210/Inquisitor)
![PPO](https://img.shields.io/badge/RL-PPO%20%7C%20GRPO-orange?style=flat-square)

---

## 🔬 Selected Projects

<table>
<tr>
<td width="50%" valign="top">

### [AssetFlow](https://github.com/Harsh-4210/Team-Artemis-)

Enterprise asset & resource management system — built with Team Artemis for the **Odoo Hackathon**.

- Structured asset lifecycles: Available → Allocated → Under Maintenance → Retired
- Centralized resource booking with strict overlap prevention
- Approval-gated maintenance workflows, scheduled audit cycles with auto-generated discrepancy reports
- Role-based access — signup only creates a plain Employee; admins promote from the Employee Directory

<br/>

`TypeScript` `Node.js` `PostgreSQL` `React` `Vite`

</td>
<td width="50%" valign="top">

### [Self-Evolving Multi-Agent Governance](https://github.com/Harsh-4210/Self_Evolving_Multi_Agent_Governance)

Decentralized multi-agent governance simulation — built in 24 hours for **Fusion Hackathon 2025** with Yash Doke and Viraj Jadhao.

- RL agents autonomously propose, enforce, and evolve governance rules
- Reputation-Weighted Quadratic Voting for rule changes
- Game-theoretic Nash Bargaining for autonomous dispute resolution
- Real-time Dash/Plotly dashboard for governance metrics & reputations

<br/>

`Python` `PPO` `Ray RLlib` `PettingZoo` `PostgreSQL`

</td>
</tr>

<tr>
<td width="50%" valign="top">

### [AI-Generalist — DDR Report Generator](https://github.com/Harsh-4210/AI-Generalist)

Automated pipeline converting building inspection + thermal PDF reports into client-ready Detailed Diagnostic Reports.

- PyMuPDF extraction → Gemini 2.5 Flash multimodal analysis → ReportLab PDF generation
- Structured 7-section output with page-proximity image matching + deduplication
- Explicit "Not Available" flagging rather than fabricating missing data

<br/>

`React` `FastAPI` `PyMuPDF` `Gemini 2.5 Flash` `ReportLab`
[Live Demo](https://ai-generalist-rust.vercel.app)

</td>
<td width="50%" valign="top">

### [NutriSense AI](https://github.com/Harsh-4210/NutriClean)

AI-powered food & health app — built in under 3 hours for the **AMD Workshop Hackathon**.

- Multimodal food analyzer (Gemini 2.0 Flash) with an 80+ dish Indian food dataset for offline fallback
- Real-time AI nutritionist chat, macro/calorie dashboard, healthy-restaurant finder
- Multi-language (EN/HI/MR), WCAG AA accessible, <1MB repo size

<br/>

`JavaScript` `Vite` `Gemini API` `Firebase` `Docker`

</td>
</tr>

<tr>
<td width="50%" valign="top">

### [TraceLink](https://github.com/ruxir-ig/mccia-tracelink)

Manufacturing batch traceability platform — **AMD Slingshot Regional Ideathon**.

- Full forward/backward traceability across 6 entity types, raw material lots to customer dispatch
- 6-role RBAC with Firebase ID-token verification
- CSV ingestion with full rollback + request-level audit trail
- Natural-language AI query endpoint for non-technical users

<br/>

`FastAPI` `React` `Firebase Auth` `Docker`
[Live](https://trace-link-mccia.vercel.app)

</td>
<td width="50%" valign="top">

### [Arivon](https://github.com/Harsh-4210/Arivon)

Adaptive learning platform — **🥉 3rd Place, Pragyantra, PES Modern College of Engineering**.

- Detects metacognitive miscalibration between student confidence and actual performance
- Bloom's taxonomy difficulty engine, dynamically adjusted learning paths
- Voice-based exam interface (Groq Whisper) + RAG-powered study mentor (Haystack)

<br/>

`Next.js 15` `FastAPI` `Groq Whisper` `Haystack RAG` `MongoDB`

</td>
</tr>

<tr>
<td width="50%" valign="top">

### [SO₂ Emission Prediction](https://github.com/Harsh-4210/SO2-Emission-Prediction)

End-to-end ML pipeline predicting SO₂ emissions from Indian coal power plants.

- **85% accuracy** on held-out test data via cross-validation
- Optuna-based hyperparameter tuning on XGBoost, **20% efficiency boost** from pipeline automation
- Deployed as a containerized microservice with a structured REST API

<br/>

`XGBoost` `FastAPI` `Docker` `Optuna`

</td>
<td width="50%" valign="top">

### [Applied ML Foundations](https://github.com/Harsh-4210/PRODIGY_ML_PROJECTS)

Three applied ML projects — **Prodigy InfoTech, Machine Learning Intern**.

- **Regression:** house price prediction, R² = 0.52
- **Clustering:** K-Means customer segmentation, 5 segments via Elbow Method
- **Computer Vision:** SVM cat/dog classifier, 55% → 62% accuracy after PCA + GridSearchCV tuning

<br/>

`Python` `Pandas` `Scikit-learn`

</td>
</tr>
</table>

---

## 🤖 Robotics

### ABU Robocon 2026 · Team Vulcans

**Affiliate Member — Computer Vision & Detection**

Contributing to the perception and object detection stack for PESMCOE's ABU Robocon 2026 robot.

- Real-time object detection using OpenCV and YOLO models
- Deploying and optimizing detection models on Jetson Orin Nano hardware for on-robot inference
- Working within the team's broader ROS2-based control architecture and competition-rule-based strategy

`OpenCV` `YOLO` `Jetson Orin Nano` `ROS2` `Python`

---

## ⚙️ Technical Stack

<table>
<tr>
<td><b>Languages</b></td>
<td>Python · SQL · JavaScript · TypeScript</td>
</tr>
<tr>
<td><b>Machine Learning / RL</b></td>
<td>PyTorch · GRPO · PPO · LoRA/QLoRA · TRL · Unsloth · Ray RLlib · PettingZoo · HuggingFace Transformers · PEFT</td>
</tr>
<tr>
<td><b>Vision</b></td>
<td>YOLOv8 · ONNX Runtime · OpenCV · Albumentations</td>
</tr>
<tr>
<td><b>LLM Systems</b></td>
<td>RAG Pipelines · RLHF · Adversarial RL · Agentic AI · Haystack · Groq Whisper · Gemini API (2.0/2.5 Flash)</td>
</tr>
<tr>
<td><b>Backend</b></td>
<td>FastAPI · Next.js 15 · React · Node.js/Express</td>
</tr>
<tr>
<td><b>Infra & Data</b></td>
<td>Docker · GitHub Actions · Google Cloud Run · gRPC · Redis · PostgreSQL · MongoDB · Supabase · Firebase</td>
</tr>
<tr>
<td><b>Robotics</b></td>
<td>ROS2 · Gazebo · Jetson Orin Nano</td>
</tr>
<tr>
<td><b>Certifications</b></td>
<td>Deep Learning Specialization (Andrew Ng) · Generative AI with LLMs (AWS/Coursera) · LLM Fundamentals (Hugging Face)</td>
</tr>
</table>

---

## 📊 GitHub Activity

<div align="center">

<img height="175" src="https://github-readme-stats.vercel.app/api?username=Harsh-4210&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=a78bfa&icon_color=a78bfa&text_color=c9d1d9&include_all_commits=true&count_private=true" />

<img height="175" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Harsh-4210&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=a78bfa&text_color=c9d1d9&langs_count=8" />

</div>

<br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=Harsh-4210&bg_color=0d1117&color=a78bfa&line=8b5cf6&point=a78bfa&area=true&area_color=8b5cf6&hide_border=true" width="100%"/>

<div align="center">

<img src="https://github-readme-streak-stats.herokuapp.com?user=Harsh-4210&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=a78bfa&ring=a78bfa&fire=a78bfa&currStreakLabel=a78bfa&dates=8b949e" />

</div>

---

<div align="center">

[![Profile Views](https://komarev.com/ghpvc/?username=Harsh-4210&color=a78bfa&style=flat-square&label=Profile+Views)](https://github.com/Harsh-4210)

*"I don't just train models — I build systems that ship, scale, and survive production."*

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8b5cf6,100:0a0f1a&height=90&section=footer" width="100%"/>

</div>
