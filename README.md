
# Hi, I'm Kartik Srivastava 👋

### AI/ML Engineer | Machine Learning | Backend Engineering | MLOps

I'm a final-year B.Tech Artificial Intelligence student at
Sardar Vallabhbhai National Institute of Technology (SVNIT).

My interests lie in designing, building, and deploying
production-oriented AI/ML systems that combine machine learning,
scalable backend infrastructure, and reliable engineering practices.

I enjoy working across the complete ML lifecycle — from
experimentation and model development to deployment,
evaluation, and continuous improvement.

---

## 🚀 About Me

- 🎓 B.Tech in Artificial Intelligence at SVNIT (2023–2027)
- 🤖 Focused on Machine Learning, Deep Learning, and AI Engineering
- ⚙️ Interested in production ML systems, backend APIs, and MLOps
- 🧠 Exploring model fine-tuning, multimodal AI, and intelligent retrieval
- 🔬 Research Lead for a multi-branch Dueling DQN project
- 💻 Practicing Data Structures & Algorithms
- 🌱 Continuously learning and building real-world AI applications

---

## 🛠️ Technical Skills

### Programming Languages

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![C++](https://img.shields.io/badge/C%2B%2B-00599C?style=flat&logo=cplusplus&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=flat&logo=postgresql&logoColor=white)

### Machine Learning & Deep Learning

- Machine Learning
- Deep Learning
- Computer Vision
- Natural Language Processing
- Model Fine-Tuning
- LoRA
- BLIP & CLIP
- Scikit-learn
- PyTorch

### Backend & Application Development

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=flat&logo=react&logoColor=61DAFB)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)

- Python Backend Development
- REST APIs
- WebSockets
- MongoDB
- React
- Playwright

### MLOps & Deployment

![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat&logo=github-actions&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat&logo=git&logoColor=white)

- Docker
- DVC
- MLflow
- GitHub Actions
- CI/CD
- Render
- Vercel
- Qdrant

---

# 🔥 Featured Projects

## 1. Nexa — Adaptive Behavioral Personalization Engine

> A production-deployed personalization platform combining behavioral
> profiling, hybrid retrieval, and real-time external product discovery.

### Overview

Nexa is a FastAPI and MongoDB-based platform designed to personalize
product discovery by modeling user behavior and adapting recommendations
to current user intent.

The system combines behavioral signals, evolving user embeddings,
and a hybrid retrieval architecture to support personalized catalog
search and external product discovery.

### Key Engineering Highlights

- Engineered a production-deployed FastAPI and MongoDB platform
  sustaining 50 concurrent users at 20 requests/sec, with a
  reported 0% failure rate and approximately 300 ms median latency
  for catalog searches.

- Designed a real-time behavioral profiling engine using dwell time,
  click frequency, and scroll depth as normalized signals.

- Implemented evolving user embeddings using exponential decay
  to align recommendations with changing user intent.

- Architected a hybrid retrieval system that routes unindexed
  queries to a decoupled Playwright scraper.

- Integrated WebSockets to stream external product results live.

### Technologies

`Python` `FastAPI` `MongoDB` `Qdrant Cloud`
`WebSockets` `Playwright` `React`

---

## 2. AeroForge ML — Route-Aware Predictive Pricing System

> An end-to-end MLOps pipeline for flight price prediction,
> reproducible experimentation, and automated deployment.

### Overview

AeroForge ML transforms flight price prediction from a notebook-based
experiment into a structured, deployable machine learning system.

The project focuses on route-aware validation, reproducible data
and model pipelines, automated CI/CD, and continuous training.

### Key Engineering Highlights

- Built a route-aware flight price prediction model using
  stratified splitting on source-destination pairs to prevent
  spatial data leakage.

- Achieved an R² score of 0.86 and Spearman correlation of 0.95
  under the reported evaluation setup.

- Designed a deterministic DVC execution DAG backed by DagsHub
  remote storage.

- Implemented MD5-hashed state tracking to support intelligent,
  stage-level caching and avoid redundant computation during CI cycles.

- Architected an automated CI/CD and continuous training pipeline
  using GitHub Actions.

- Integrated dynamic execution, persistent MLflow tracking,
  and strict artifact validation gates.

- Containerized the deployment workflow using Docker and
  deployed through Render.

### MLOps Architecture

Data → Validation → Feature Engineering → Model Training
→ Evaluation → Artifact Validation → Deployment

### Technologies

`Python` `Scikit-learn` `XGBoost` `FastAPI`
`DVC` `DagsHub` `MLflow` `Docker`
`GitHub Actions` `Render`

---

## 3. WildCaption — Wildlife Caption Refinement via
## LoRA-BLIP and CLIP Reranking

> A vision-language model fine-tuning and caption refinement
> pipeline combining LoRA, candidate generation, and CLIP reranking.

### Overview

WildCaption explores image caption refinement using a fine-tuned
BLIP text decoder and CLIP-based candidate evaluation.

The project combines parameter-efficient fine-tuning with
multi-candidate caption generation and semantic reranking.

### Key Engineering Highlights

- Fine-tuned BLIP's text decoder using LoRA with rank r=8,
  while keeping the vision encoder frozen.

- Used approximately 1–2% trainable parameters for
  parameter-efficient fine-tuning.

- Curated a 2,800-image wildlife subset from Flickr8k
  through dual-signal CLIP scoring and adaptive
  65th-percentile thresholding.

- Built a caption generation pipeline producing 12 candidates
  through grouped beam search and nucleus sampling.

- Applied diversity penalty of 0.8 and top_p of 0.92
  in the candidate generation pipeline.

- Deduplicated generated captions using MiniLM before
  applying CLIP-based reranking.

- Reported a 14% improvement in average CLIP score and
  a 94% caption improvement rate across held-out images.

### Technologies

`PyTorch` `BLIP` `CLIP` `LoRA`
`Sentence Transformers` `MiniLM`

---

# 🔬 Research Experience

## Research Lead — Multi-Branch Dueling DQN
### EEG Emotion Recognition

Research project based on FLD3QN (IEEE TNNLS 2024)
using the DEAP dataset.

### Contributions

- Led a 3-member team to replicate and extend the referenced
  reinforcement learning research.

- Managed experimental design, task allocation, and
  cross-team coordination.

- Co-designed a three-strategy reinforcement learning framework:
  - Paper-Anchored
  - Prioritized N-Step
  - Curriculum + Margin DDQN

- Investigated cross-subject overfitting, observing a reported
  training score of 0.71 versus validation score of 0.30.

- Developed an anti-overfitting variant using:
  - EEG Mixup
  - Channel Dropout
  - Spectral Noise Injection

- Consolidated research tracks into a unified multi-branch
  architecture that achieved 0.581 AUC-ROC under a
  strict subject-independent evaluation protocol.

---

# 💻 Coding Profiles

I regularly practice problem-solving and algorithmic thinking
through competitive programming and coding platforms.

## 💻 Coding Profiles

| Platform | Profile |
|---|---|
| LeetCode | [My LeetCode Profile](https://leetcode.com/u/Kartik_2005_/) |
| Codeforces | [My Codeforces Profile](https://codeforces.com/profile/kartiksri2005) |
| GitHub | [My GitHub Profile](https://github.com/kartik23481) |
---


# 🎯 Current Focus

- Building production-oriented AI/ML systems
- Improving machine learning system design
- Exploring Generative AI and multimodal models
- Strengthening DSA and problem-solving skills
- Learning scalable backend and MLOps architecture
- Researching reliable and generalizable ML pipelines

---

## 📫 Connect With Me

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=flat&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/kartik-srivastava-462609285/)

[![Email](https://img.shields.io/badge/Email-D14836?style=flat&logo=gmail&logoColor=white)](mailto:kartiksri2005@gmail.com)
---

⭐ Thanks for visiting my profile!

I'm always interested in learning, building, and exploring
interesting problems in AI/ML and software engineering.
