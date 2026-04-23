# 🐠 Data Mining for Marine Conservation

### Mining 247MB of Reef Life Survey data to identify the invisible species holding Australia's reefs together.

> *"We do not need to monitor every rare or elusive species to understand the health of a reef. We just need to protect the right ones."*

---

## 👉 Start Here: [main_notebook.ipynb](main_notebook.ipynb)

---

## 🌊 What Is This?

This project applies high-dimensional data mining to the **Reef Life Survey (RLS) Australia Dataset** — over 700,000 observations across 10,705 surveys — to identify **Topological Anchors**: the specific species that hold reef ecosystems together through network connectivity rather than raw abundance.

Traditional marine conservation focuses on biomass and apex predators. This project challenges that paradigm by treating the reef as a **complex network** and using unsupervised machine learning to find the species that, if lost, would cause the entire system to unravel.

---

## 🔬 The Four-Pillar Framework

The analysis is structured around four research pillars that build toward a single unified conservation ranking:

| Pillar | Method | Output |
|--------|--------|--------|
| **1. Hidden Keystones** | PageRank Centrality on a 1,424 × 1,424 species co-occurrence graph | Species with high influence but low abundance |
| **2. Biological Indicators** | FP-Growth Association Rule Mining (Lift > 11.0) | Proxy species that statistically predict shark & turtle presence |
| **3. Ecological Fingerprinting** | Triangle counting & clustering coefficients across 26.9M network motifs | Structural resilience score per species |
| **4. Topological Anchors** | Louvain community detection + Conservation Priority Index (CPI) | Regional priority leaderboard of the 20 most critical species |

The final **Validation Handshake** synthesizes all four pillars using a proportional seat allocation formula to produce the **Topological Anchor Leaderboard** — a data-driven blueprint for reef protection.

---

## 🏆 Key Findings

- **26.9 million structural triangles** mapped across the Australian reef network — a novel metric for ecosystem resilience
- **Global Clustering Coefficient of 0.7721**, meaning a 77.21% probability that a species' neighbors remain connected even after it is lost
- Top indicator rule: **Chrysiptera notialis → Carcharhinus galapagensis** with a **Lift of 12.08** and 82.5% confidence
- **20 Topological Anchors** identified across 4 biogeographic modules: Tropical North, Coral Sea, Temperate South, and Offshore Hubs
- **Labroides dimidiatus** (Bluestreak Cleaner Wrasse) achieved the maximum possible PageRank of 1.0 despite being in the bottom 5% of abundance — the strongest validation of the network model

---

## 🗂 Repository Structure

```
data-mining-for-marine-conservation/
├── main_notebook.ipynb          ← Final curated analysis (start here)
├── requirements.txt             ← Python dependencies
├── README.md
├── .gitignore
├── checkpoints/
│   ├── checkpoint_1.ipynb       ← Project Checkpoint 1
│   └── checkpoint_2.ipynb       ← Project Checkpoint 2
└── data/
    └── README.md                ← Dataset download instructions
```

---

## 🚀 How to Run

This project was built and run entirely in **Google Colab**.

### 1. Get the Dataset
The RLS dataset (~247MB) is too large to include in this repo. See [`data/README.md`](data/README.md) for download instructions from the AODN portal.

### 2. Open in Colab
[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/)

Upload `main_notebook.ipynb` to Google Colab and place the dataset at the path specified in **Section 1** of the notebook.

### 3. Install Dependencies
All required libraries are installed in the first cell of the notebook. Alternatively:
```bash
pip install -r requirements.txt
```

### 4. Run All Cells
Runtime → Run All. Total runtime is approximately **8–12 minutes** depending on Colab resources.

---

## 📦 Dependencies

Key libraries used:
- `networkx` — graph construction and PageRank
- `mlxtend` — FP-Growth association rule mining
- `python-louvain` — community detection
- `pandas`, `numpy` — data processing
- `matplotlib`, `seaborn` — visualization

Full list in [`requirements.txt`](requirements.txt).

---

## 📊 Dataset

**Reef Life Survey (RLS) — Australia Ecosystem Subset**
- Source: [AODN Portal](https://portal.aodn.org.au/)
- Timespan: 2016–2026
- Scale: 700,000+ observations, 1,424 species, 10,705 surveys
- Matrix sparsity: 98.22%

See [`data/README.md`](data/README.md) for exact download and setup instructions.

---

## 👤 Author

**Yash Patel**
UIN: 131009796
Data Mining & Analysis — Final Project
