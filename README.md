# SENTINEX — GitHub README Insert Guide

## WHERE TO INSERT EACH SECTION

### 1. After the Flagship I (ArchitectAI) block, insert the SENTINEX block below.
### 2. Rename existing Flagship II → III, III → IV, IV → V (see bottom of this file).
### 3. Add tech stack entries to your existing sections.
### 4. Update the stats badges.

---

## ════════════════════════════════════════════════════════════
## INSERT THIS AFTER FLAGSHIP I (ArchitectAI) — BEFORE current Flagship II
## ════════════════════════════════════════════════════════════

<!-- ════════════════════════════════════════════════════════════
     FLAGSHIP 02 — SENTINEX
     ════════════════════════════════════════════════════════════ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=cylinder&color=gradient&customColorList=0,4,12,20&height=80&text=%F0%9F%A5%88%20%20FLAGSHIP%20II%20%E2%80%94%20Industrial%20AI%20%2F%20MLOps%20%20%F0%9F%A5%88&fontSize=26&fontColor=ffffff&animation=blinking"/>

### 🔧 SENTINEX — Diesel Engine Air-Path Leak Detection System

[![Repo](https://img.shields.io/badge/%F0%9F%94%97_View_on_GitHub-SENTINEX-00FFD4?style=for-the-badge&logo=github&logoColor=black)](https://github.com/Akash-2615/SENTINEX)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat-square&logo=typescript&logoColor=white)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=flat-square&logo=xgboost&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![SHAP](https://img.shields.io/badge/SHAP-TreeExplainer-8B5CF6?style=flat-square)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat-square&logo=threedotjs&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![AWS](https://img.shields.io/badge/AWS_EC2%2FECR-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Claude](https://img.shields.io/badge/Claude_API_(ARIA)-D97757?style=flat-square&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=flat-square&logo=supabase&logoColor=white)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=flat-square&logo=tailwindcss&logoColor=white)
![Recharts](https://img.shields.io/badge/Recharts-22B5E5?style=flat-square&logoColor=white)

</div>

<br/>

**What it does:** A **production-grade real-time physics-ML hybrid system** for detecting, locating, quantifying, and explaining diesel engine air-path leaks in Caterpillar test cells — built for the **Caterpillar Tech Challenge 2026 Grand Finale (Top 10 National Finalist, Team DECODERZZ)**.

Monitors **42 live sensor streams** through a 7-stage pipeline and delivers sub-second leak detection with full explainability, multi-leak capability, and a 3D Digital Twin — **zero new hardware required**.

| Stage | Component | What It Does |
|:---:|---|---|
| **1** | Data Quality Pipeline (DQP) | 5-stage cascade: bounds validation · null imputation · spike detection · EMA smoothing · drift flagging |
| **2** | Steady State Guard (SSG) | Suppresses detection during RPM/load transitions — eliminates transient false alarms |
| **3** | XGBoost + Multi-label NN | Single-leak: 99.95% accuracy across 8 scenarios · Multi-leak: sigmoid heads, BCEWithLogitsLoss, 7 valid combinations |
| **4** | SHAP TreeExplainer | Exact top-5 sensor attribution per prediction with deviation %, impact score, and plain-language interpretation |
| **5** | Sensor Fault Isolator (SFI) | 3-mechanism: health divergence tracking · DQP flag integration · physics cascade validation |
| **6** | Dynamic Baseline Engine | Physics-expected values at any operating point — CPR formula (K₁=1.5867) + T_exhaust formula (T_BASE=906.7°C) |
| **7** | FastAPI + React Dashboard | 10 REST endpoints · real-time streaming · session logging · multi-engine switching |

- 🤖 **ARIA AI Copilot** — Claude-powered diagnostic assistant with live context injection per message: current prediction + SHAP top-5 drivers + RCA ranked causes + live sensor readings + engine state — answers what standard chatbots never could
- 🔬 **Root Cause Analysis Engine** — deterministic per-scenario knowledge base (7 scenarios × 3 ranked hypotheses) with inspection actions, tools, and visual signs; disambiguation rules adjust probabilities from SHAP patterns
- 🌐 **3D Digital Twin** — Three.js procedural engine for C7/C13/C15 with SHAP-driven sensor sphere colouring, intake/exhaust flow particle animation, GNN edge overlay, real-time leak FX, and cutaway/X-ray view modes
- 📡 **Federated Learning** — FedAvg simulation across 4 Caterpillar India test facilities (Hosur/Bengaluru/Pune/Chennai) with attention-weighted aggregation (α_k), privacy compression >5000×, and live convergence chart
- 🏥 **Sensor Health Tracker** — per-sensor drift monitoring (rolling 20-sample window), calibration age tracking, FAULT/WATCH/STALE/OK status, fleet health score 0–100
- 🔍 **Multi-Leak Detection** — 17,500 training rows across 7 thermodynamically valid combinations using multiplicative superposition; ensemble confidence routing at 0.85 threshold between XGBoost and multi-label NN
- 📄 **Auto PDF Reports** — jsPDF one-click session reports with SFI confirmation, SHAP drivers, leak timeline, sensor fault events, and SMTP email delivery
- 🚀 **AWS Production Deployment** — Dockerised dual-container stack (backend + frontend), ECR registry, EC2 t3.large, single-command deploy

<div align="center">

```
42 Sensors ──► DQP (5-stage) ──► SSG (steady state guard) ──► XGBoost + SHAP
    ──► SFI (3-mechanism isolation) ──► Dynamic Baseline ──► FastAPI ──► React Dashboard
               ↕                              ↕                         ↕
        Sensor Health              Physics CPR + T_exhaust         ARIA Copilot
        Tracker (42 sensors)       K₁=1.5867 · T_BASE=906.7°C    (Claude API)
               ↕                              ↕                         ↕
      Multi-label NN             Dynamic Operating Point          3D Digital Twin
      (sigmoid · BCE)            Baseline for C7/C13/C15          (Three.js · GNN)
               ↕                                                         ↕
     Federated Learning                                         PDF Session Report
     (4 India Facilities)                                       + SMTP Email
```

![Sensors](https://img.shields.io/badge/Sensors-42_Live_Streams-00FFD4?style=flat-square&logoColor=black)
![Locations](https://img.shields.io/badge/Leak_Locations-7_Classified-FF6EC7?style=flat-square)
![Latency](https://img.shields.io/badge/Detection-<1s_Real--Time-00FF94?style=flat-square&logoColor=black)
![Training](https://img.shields.io/badge/Training_Rows-31%2C900-FFB347?style=flat-square)
![Accuracy](https://img.shields.io/badge/XGBoost-99.95%25_Accuracy-00FF94?style=flat-square&logoColor=black)
![Tests](https://img.shields.io/badge/Automated_Tests-85%2B_Passing-8B5CF6?style=flat-square)
![Multileak](https://img.shields.io/badge/Multi--Leak-7_Valid_Combos-FF6EC7?style=flat-square)
![Deploy](https://img.shields.io/badge/AWS_EC2-Live_Production-FF9900?style=flat-square&logo=amazonaws&logoColor=white)
![Challenge](https://img.shields.io/badge/CAT_Tech_Challenge_2026-Top_10_National_Finalist-FFFF00?style=flat-square&logoColor=black)
![Engines](https://img.shields.io/badge/Engines-C7_%C2%B7_C13_%C2%B7_C15-00FFD4?style=flat-square&logoColor=black)

</div>

<br/>

---


## ════════════════════════════════════════════════════════════
## RENAMING — Change these in your existing flagship headers
## ════════════════════════════════════════════════════════════

### Current Flagship II (Forensic Financial Suite) → Change to Flagship III
FIND:    FLAGSHIP II — Applied GenAI / RAG
REPLACE: FLAGSHIP III — Applied GenAI / RAG

FIND:    customColorList=6,11,19
KEEP AS IS (color stays)

FIND:    🥈  FLAGSHIP II — Applied GenAI / RAG  🥈
REPLACE: 🥉  FLAGSHIP III — Applied GenAI / RAG  🥉
(URL encode: %F0%9F%A5%89 for 🥉)

---

### Current Flagship III (6G SAGIN) → Change to Flagship IV
FIND:    FLAGSHIP III — Autonomous Networks
REPLACE: FLAGSHIP IV — Autonomous Networks

FIND:    🥉  FLAGSHIP III — Autonomous Networks  🥉
REPLACE: 🏅  FLAGSHIP IV — Autonomous Networks  🏅
(URL encode: %F0%9F%8F%85 for 🏅)

---

### Current Flagship IV (O-RAN) → Change to Flagship V
FIND:    FLAGSHIP IV — DRL + XAI Research
REPLACE: FLAGSHIP V — DRL + XAI Research

FIND:    🏅  FLAGSHIP IV — DRL + XAI Research  🏅
REPLACE: 🏆  FLAGSHIP V — DRL + XAI Research  🏆
(URL encode: %F0%9F%8F%86 for 🏆)

---

## ════════════════════════════════════════════════════════════
## TECH STACK ADDITIONS — Add to existing ⚡ Tech Stack section
## ════════════════════════════════════════════════════════════

### Under "Backend & Infrastructure" — add Supabase:
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)

### Add new subsection "🏭 Industrial AI & MLOps Stack" after existing sections:

**🏭 Industrial AI & MLOps**

![SHAP](https://img.shields.io/badge/SHAP-TreeExplainer-8B5CF6?style=for-the-badge)
![XGBoost](https://img.shields.io/badge/XGBoost-FF6600?style=for-the-badge&logo=xgboost&logoColor=white)
![Three.js](https://img.shields.io/badge/Three.js-000000?style=for-the-badge&logo=threedotjs&logoColor=white)
![Recharts](https://img.shields.io/badge/Recharts-22B5E5?style=for-the-badge&logoColor=white)
![Supabase](https://img.shields.io/badge/Supabase-3ECF8E?style=for-the-badge&logo=supabase&logoColor=white)
![jsPDF](https://img.shields.io/badge/jsPDF-Report_Generation-FF6EC7?style=for-the-badge)
![Tailwind](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

---

## ════════════════════════════════════════════════════════════
## STATS ADDITIONS — Add to "AI Engineering by the Numbers"
## ════════════════════════════════════════════════════════════

Add these badges to your existing stats block:

![Sensors](https://img.shields.io/badge/Test_Cell_Sensors-42_Live_Streams-00FFD4?style=for-the-badge&logoColor=black)
![Pipeline](https://img.shields.io/badge/Production_Pipeline-7_Stage_Physics--ML-FF6EC7?style=for-the-badge)
![MultiLeak](https://img.shields.io/badge/Multi--Leak_Combos-7_Thermodynamic-00FF94?style=for-the-badge&logoColor=black)
![TestRows](https://img.shields.io/badge/Training_Dataset-31%2C900_Physics_Rows-FFB347?style=for-the-badge)
![CAT](https://img.shields.io/badge/CAT_Tech_Challenge-Top_10_National-FFFF00?style=for-the-badge&logoColor=black)

---

## ════════════════════════════════════════════════════════════
## RESEARCH INTERESTS — Add row to table
## ════════════════════════════════════════════════════════════

Add this row to your Research Interests table:

| 🏭 Industrial AI | Physics-ML Hybrid Systems · Sensor Fusion · Predictive Maintenance · XAI for Engineering |

---

## ════════════════════════════════════════════════════════════
## COLLABORATE ON — Add badges
## ════════════════════════════════════════════════════════════

Add these to your "Open to Collaborate On" section:

![IndustrialAI](https://img.shields.io/badge/Industrial_AI_Systems-FF6EC7?style=flat-square)
![SensorFusion](https://img.shields.io/badge/Sensor_Fusion_%26_Anomaly_Detection-00FFD4?style=flat-square&logoColor=black)
![PhysicsML](https://img.shields.io/badge/Physics--ML_Hybrid_Systems-8B5CF6?style=flat-square)
![PredictiveMaint](https://img.shields.io/badge/Predictive_Maintenance-00FF94?style=flat-square&logoColor=black)
