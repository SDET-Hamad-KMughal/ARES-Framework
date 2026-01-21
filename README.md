# ARES: Autonomous Resilience & Exploration System 🚀
**A Multimodal Reinforcement Learning Approach to Self-Healing Mobile UI Testing**


---

## 📌 Abstract
The ARES Framework addresses the fragility of traditional automated testing by combining **Computer Vision (YOLOv8)**, **Natural Language Processing (BERT)**, and **Reinforcement Learning (PPO)**. This repository provides the full implementation of an agent capable of perceiving UI elements, understanding their semantic intent, and discovering navigational paths that automatically "heal" when the UI changes.

---

## 🛠️ The 4-Phase Architecture

### 🛡️ Phase 1 & 2: Perception Engine (Vision)
* **Module:** `Phase_1_Training/` & `Phase_2_Inference/`
* **Tech:** YOLOv8 (Deep Learning)
* **Result:** Real-time identification of 11 distinct UI nodes (Buttons, Inputs, Icons) with 90%+ confidence.
* **Key Output:** `best.pt` model weights.

### 🧠 Phase 3: Logic & Semantic Engine (The Brain)
* **Module:** `Phase_3_Logic/`
* **Tech:** BERT (Sentence-Transformers) + PPO (Proximal Policy Optimization)
* **Result:** UI labels are mapped into 384-dimensional semantic vectors. The PPO agent is trained for 10,000+ steps to learn optimal navigation strategies based on reward signals.

### 🛠️ Phase 4: Self-Healing & Reporting (Execution)
* **Module:** `Phase_4_Reporting/`
* **Tech:** Selenium + Python FPDF + HTML5/Tailwind
* **Result:** Monitors UI stability. If a locator fails due to "UI Drift," the system re-calculates the target using the BERT logic. Final results are exported as professional PDF reports.

---

## 📂 Repository Structure
```text
├── index.html                # Live Interactive Demo (Root)
├── Phase_1_Training/         # YOLO training data and weights
├── Phase_2_Inference/        # UI detection on live app screens
├── Phase_3_Logic/            
│   ├── code/                 # BERT Embeddings & PPO Training Notebooks
│   └── results/              # Decision verification logs
└── Phase_4_Reporting/        
    ├── code/                 # Self-healing logic verification
    └── reports/              # ARES_Final_Test_Report.pdf
