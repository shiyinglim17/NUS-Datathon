# Decision-Conditioned Company Intelligence  
**NUS SDS Datathon 2026 – Cat A (Data Warriors)**

## Problem Statement

This project addresses the challenge of extracting **meaningful, explainable insights from firm-level data**. Traditional company segmentation assumes a single definition of similarity, which often leads to weak benchmarking and misleading comparisons.

The goal is to build a **data-driven company intelligence prototype** that:
- Groups companies into relevant peer sets  
- Highlights similarities, differences, and anomalies  
- Supports benchmarking, risk assessment, and decision-making  
- Produces **interpretable, data-grounded insights** rather than black-box outputs

---

## Dataset Overview

The analysis uses the **CHAMPIONS Group dataset**, containing **8,559 companies** and **74 variables**.

At a high level, the data covers:
- Firmographic attributes (size, age, industry, entity type)  
- Technology and operational indicators (IT spend, infrastructure proxies)  
- Ownership and organisational structure (parent–subsidiary relationships, corporate family size)

The dataset is sparse and highly skewed, requiring careful preprocessing and peer-relative analysis. No sensitive or proprietary information is exposed.

---

## Approach & Solution

Instead of a single segmentation, our solution adopts a **multi-lens, decision-conditioned framework**, where each lens answers a different business question:

- **Firmographic Lens** – structural and organisational similarity  
- **Technology Intensity Lens** – digital maturity and IT investment patterns  
- **Corporate Complexity Lens** – ownership depth and governance structure  

Each lens independently:
- Engineers interpretable features  
- Discovers structure using unsupervised learning  
- Produces peer groups and relative scores  

Cross-lens comparisons are then used to surface **mismatches and potential risks** (e.g. scale vs technology gaps, complexity vs operational size). Final outputs are translated into **explainable, rule-based risk archetypes**, with an LLM used only for narrative explanation — not decision-making.

---

## Key Skills & Techniques

- Exploratory data analysis on large, sparse datasets  
- Feature engineering & domain-informed preprocessing  
- PCA, KMeans, and HDBSCAN clustering  
- Peer-relative scoring and percentile ranking  
- Cross-segment comparison and anomaly detection  
- Explainable, rule-based insight generation  
- Controlled use of LLMs for interpretation  

---

## Repository Structure

- `CAT_A_Data_Warriors.ipynb` – End-to-end analysis pipeline  
- `requirements.txt` – Dependencies  
- `README.md` – Project overview\
Note: dataset is not uploaded
---

## Key Takeaway

Company similarity is **decision-dependent, not absolute**.  
This project demonstrates how a single dataset can support multiple business questions by redefining similarity through structured, explainable analytical lenses.
