<div align="center">

# Hi, I'm Harsh

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://readme-typing-svg.demolab.com?font=Montserrat&weight=600&size=20&pause=1800&color=A9BCD6&center=true&vCenter=true&width=640&height=40&lines=Machine+learning+engineer+%C2%B7+LLM+post-training;I+build+RL+environments+and+reward+functions;Multi-agent+pipelines+with+a+quality+gate;Final-year+AI+%26+Data+Science+student%2C+Pune" />
  <img src="https://readme-typing-svg.demolab.com?font=Montserrat&weight=600&size=20&pause=1800&color=35557A&center=true&vCenter=true&width=640&height=40&lines=Machine+learning+engineer+%C2%B7+LLM+post-training;I+build+RL+environments+and+reward+functions;Multi-agent+pipelines+with+a+quality+gate;Final-year+AI+%26+Data+Science+student%2C+Pune" alt="Machine learning engineer, LLM post-training" />
</picture>

[![LinkedIn](https://img.shields.io/badge/LinkedIn-harsh--jain0621-1b1b1b?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/harsh-jain0621/)
[![Hugging Face](https://img.shields.io/badge/Hugging_Face-Harsh--9209-1b1b1b?style=flat-square&logo=huggingface&logoColor=white)](https://huggingface.co/Harsh-9209)
[![Email](https://img.shields.io/badge/Email-harshjain0621%40gmail.com-1b1b1b?style=flat-square&logo=gmail&logoColor=white)](mailto:harshjain0621@gmail.com)
[![Portfolio](https://img.shields.io/badge/Portfolio-source-35557a?style=flat-square&logo=nextdotjs&logoColor=white)](https://github.com/Harsh-4210/harsh-portfolio)

</div>

## About me

I build training environments, reward functions and evaluation harnesses for language models, plus the backend services that put them in front of users. Most of my recent work comes back to one question: **how do you get a small model to make a decision that a program can check?**

- Final-year **B.E. in Artificial Intelligence & Data Science** at SPPU, Pune (GPA 8.75/10)
- **Top 100 finalist** at the Meta × PyTorch × Hugging Face OpenEnv Hackathon, and **3rd place** at Pragyantra
- Open to **ML engineering internships** and **2027 full-time roles**

## Featured projects

### [ConflictBench](https://github.com/Harsh-4210/Conflict_Bench) · RL environment for LLMs

Language models handed a document of contradictory instructions (Legal vs. a VP vs. a team lead) tend to trust the latest message or try to satisfy both sides. ConflictBench is an OpenEnv environment that trains them to return **one executable JSON plan** instead.

- Scenario generator with 6–16 directives and 2–6 embedded conflicts across 10 business domains, each with ground truth
- **Deterministic five-rubric reward, no LLM judge:** correctness, contradiction-freedom, conflict-pair F1, efficiency, JSON validity
- Fine-tuned **Qwen2.5-3B with GRPO + LoRA** (Unsloth, 4-bit): composite reward **0.14 → 0.50** on held-out scenarios; instruction-following 0.11 → 0.48
- Top 100 finalist, Meta × PyTorch × Hugging Face OpenEnv Hackathon

[![Source](https://img.shields.io/badge/Source-GitHub-1b1b1b?style=flat-square&logo=github)](https://github.com/Harsh-4210/Conflict_Bench)
[![Demo](https://img.shields.io/badge/Live_demo-HF_Space-35557a?style=flat-square&logo=huggingface&logoColor=white)](https://huggingface.co/spaces/Harsh-9209/Conflict_Bench)
[![Adapter](https://img.shields.io/badge/LoRA_adapter-HF_Hub-35557a?style=flat-square&logo=huggingface&logoColor=white)](https://huggingface.co/Harsh-9209/conflictbench-qwen2.5-3b-grpo-lora)
&nbsp;`Python` `TRL` `Unsloth` `PEFT` `OpenEnv` `FastAPI` `Gradio` `W&B`

### [InsureClear](https://github.com/Harsh-4210/Insureclear) · Multi-agent LLM pipeline

Turns a rejected Indian health-insurance claim into a reviewable appeal package.

- Five agents in sequence: **Auditor → Policy Analyst → IRDAI Checker → Appeal Writer → Judge**
- The Judge acts as a quality gate: drafts scoring below **0.75** go back with concrete changes, for up to two revisions
- FastAPI job API on a **SQLite-backed queue with checkpoints**, so jobs survive restarts; the React UI streams per-agent progress
- Uploaded PDFs are deleted after processing, and every regulatory citation is flagged for manual verification

[![Source](https://img.shields.io/badge/Source-GitHub-1b1b1b?style=flat-square&logo=github)](https://github.com/Harsh-4210/Insureclear)
&nbsp;`Python` `Gemini` `FastAPI` `React` `SQLite` `Docker` `pytest`

### [DealFlow360](https://github.com/orion-catchers/dealflow) · B2B quote-to-cash (team of four)

Catalog → quote → approval → customer portal → fulfilment → billing, on a single PostgreSQL database. I was the top committer and built the customer portal, payment recording and catalog search.

- Revisioned quotes with **optimistic concurrency**: a stale revision is rejected with `409 STALE_REVISION`
- **Idempotency keys** on fulfilment, portal and payment writes, so a retried request cannot double-allocate stock or double-bill
- CI against a real Postgres 16: migrations, double-seed idempotency check, typecheck, lint, 43 test files, production build

[![Source](https://img.shields.io/badge/Source-GitHub-1b1b1b?style=flat-square&logo=github)](https://github.com/orion-catchers/dealflow)
&nbsp;`TypeScript` `Next.js` `PostgreSQL` `Prisma` `Vitest` `GitHub Actions`

## More projects

| Project | What it does | Stack |
|---|---|---|
| [**Inquisitor**](https://github.com/Harsh-4210/Inquisitor) | Red/blue self-play for hallucination detection: one model writes plausible wrong answers, the other passes, flags or probes them. *In progress.* | GRPO, Unsloth, MiniLM |
| [**SilentFailureDetector**](https://github.com/Harsh-4210/LLM_HALLUCINATION_RL) | OpenEnv environment that rewards flagging answers that are confident *and* wrong, while leaving correct ones alone. [Live on HF Spaces](https://huggingface.co/spaces/Harsh-9209/silent-failure-detector). | OpenEnv, Pydantic, FastAPI |
| [**TraceLink**](https://github.com/ruxir-ig/mccia-tracelink) | Lot traceability for an auto-parts manufacturer: backward/forward tracing, recall blast radius, CSV import with SHA-256 de-duplication and rollback. *Team of three, MCCIA program.* | FastAPI, React, SQLite, Docker |
| [**Arivon**](https://github.com/nishtha911/Pragyantra-ED14-ET-3) | Adaptive learning that treats "sure and wrong" differently from "unsure and wrong", with a knowledge graph, voice answers and a document-grounded tutor. *Team, 3rd place at Pragyantra.* | Next.js, FastAPI, MongoDB |
| [**AssetFlow**](https://github.com/Harsh-4210/Team-Artemis-) | Asset allocation, bookings, maintenance and audits with RBAC, overlap-safe bookings and atomic transfers. *Team, Odoo Hackathon.* | Express, Prisma, PostgreSQL, React |
| [**Batwa**](https://github.com/Harsh-4210/Batwa) | Assisted payments with a printed QR card and PIN for agents and merchants. I built the core API. *Team, Cognizant simulation.* | FastAPI, SQLite, React |
| [**AutoStream**](https://github.com/Harsh-4210/Autostream-Langgraph-agent) | LangGraph agent with intent routing, retrieval over FAISS and slot-filling lead capture behind a controlled tool call. | LangGraph, FAISS, OpenAI |
| [**AI DDR Generator**](https://github.com/Harsh-4210/AI-Generalist) | Reads inspection and thermal-imaging PDFs and writes a structured defect report PDF. | FastAPI, PyMuPDF, Gemini, ReportLab |
| [**NutriSense**](https://github.com/Harsh-4210/NutriClean) | Multimodal nutrition PWA: food-photo analysis, an offline lookup of 80+ Indian dishes, deployed on Cloud Run. *Built in a 3-hour AMD workshop.* | Gemini, Firebase, Express, Docker |
| [**Self-Evolving Governance**](https://github.com/Harsh-4210/Self_Evolving_Multi_Agent_Governance) | Multi-agent RL in which market agents trade and vote on tax rules. *Fusion Hackathon 2025.* | RLlib (PPO), PettingZoo, React |
| [**Prodigy ML tasks**](https://github.com/Harsh-4210/PRODIGY_ML_PROJECTS) | Internship work: regression, K-Means segmentation, SVM image classification, CNN gesture recognition, food calorie estimation. | scikit-learn, TensorFlow |

<sub>Also contributed to: [Advocai](https://github.com/Viraj281105/Advocai) (multi-agent insurance-appeal swarm, Kaggle Agents Intensive) · [ClimateX](https://github.com/Viraj281105/ClimateX) (causal climate-policy dashboard, PCCOE IGC)</sub>

## Tech stack

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://skillicons.dev/icons?i=py%2Cpytorch%2Ctensorflow%2Csklearn%2Cfastapi%2Cts%2Cnextjs%2Creact%2Cnodejs%2Cpostgres%2Cmongodb%2Csqlite%2Cprisma%2Cdocker%2Cgithubactions%2Cgcp%2Cgit%2Cvercel&theme=dark&perline=9" />
    <img src="https://skillicons.dev/icons?i=py%2Cpytorch%2Ctensorflow%2Csklearn%2Cfastapi%2Cts%2Cnextjs%2Creact%2Cnodejs%2Cpostgres%2Cmongodb%2Csqlite%2Cprisma%2Cdocker%2Cgithubactions%2Cgcp%2Cgit%2Cvercel&theme=light&perline=9" alt="Python, PyTorch, TensorFlow, scikit-learn, FastAPI, TypeScript, Next.js, React, Node.js, PostgreSQL, MongoDB, SQLite, Prisma, Docker, GitHub Actions, Google Cloud, Git, Vercel" />
  </picture>
</p>

| Area | Tools |
|---|---|
| LLM post-training | Hugging Face Transformers, TRL (GRPO), PEFT / LoRA, Unsloth, W&B |
| RL & evaluation | OpenEnv, reward design, RLlib (PPO), PettingZoo |
| LLM applications | Multi-agent pipelines, LangGraph, RAG (FAISS), structured output, Gemini / OpenAI APIs |
| Backend & data | FastAPI, Next.js, PostgreSQL, Prisma, SQLite, MongoDB |

## GitHub stats

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api?username=Harsh-4210&show_icons=true&hide_border=true&include_all_commits=true&rank_icon=github&bg_color=1b1b1b&title_color=f5f5f5&text_color=a3a3a3&icon_color=a9bcd6&cache_seconds=21600" />
    <img height="165" src="https://github-readme-stats.vercel.app/api?username=Harsh-4210&show_icons=true&hide_border=true&include_all_commits=true&rank_icon=github&bg_color=f5f5f5&title_color=1b1b1b&text_color=555555&icon_color=35557a&cache_seconds=21600" alt="GitHub stats" />
  </picture>
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://github-readme-stats.vercel.app/api/top-langs/?username=Harsh-4210&layout=compact&langs_count=6&hide_border=true&bg_color=1b1b1b&title_color=f5f5f5&text_color=a3a3a3&cache_seconds=21600" />
    <img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Harsh-4210&layout=compact&langs_count=6&hide_border=true&bg_color=f5f5f5&title_color=1b1b1b&text_color=555555&cache_seconds=21600" alt="Top languages" />
  </picture>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://streak-stats.demolab.com/?user=Harsh-4210&hide_border=true&background=1b1b1b&stroke=3a3a3a&ring=a9bcd6&fire=a9bcd6&currStreakNum=f5f5f5&sideNums=f5f5f5&currStreakLabel=a9bcd6&sideLabels=a3a3a3&dates=8a8a8a" />
    <img src="https://streak-stats.demolab.com/?user=Harsh-4210&hide_border=true&background=f5f5f5&stroke=d6d3d1&ring=35557a&fire=35557a&currStreakNum=1b1b1b&sideNums=1b1b1b&currStreakLabel=35557a&sideLabels=555555&dates=777777" alt="Contribution streak" />
  </picture>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Harsh-4210/Harsh-4210/output/github-contribution-grid-snake-dark.svg" />
    <img src="https://raw.githubusercontent.com/Harsh-4210/Harsh-4210/output/github-contribution-grid-snake.svg" alt="Contribution graph being eaten by a snake" />
  </picture>
</p>

<div align="center">

<img src="https://komarev.com/ghpvc/?username=Harsh-4210&style=flat-square&color=1b1b1b&label=profile+views" alt="Profile views" />

</div>
