# ARES: Autonomous Resilience & Exploration System 🚀
**A Multimodal Reinforcement Learning Approach to Self-Healing Mobile UI Testing**

## 🌐 Live Interactive Demo
[**🔗 Launch ARES AI Dashboard**](https://SDET-Hamad-KMughal.github.io/ARES-Framework/Phase_4_Reporting/code/index.html)
*Test the autonomous script generation engine directly in your browser.*

---

## 📌 Abstract
The ARES Framework addresses the fragility of traditional automated testing by combining **Computer Vision (YOLOv8)**, **Natural Language Processing (BERT)**, and **Reinforcement Learning (PPO)**. This repository provides the full implementation of an agent capable of perceiving UI elements, understanding their semantic intent, and discovering navigational paths that self-heal when the UI changes.

---

## 🛠️ The 4-Phase Architecture

### 🛡️ Phase 1 & 2: Perception Engine (Vision)
* **Module:** `Phase_1_Training/` & `Phase_2_Inference/`
* **Tech:** YOLOv8 (Object Detection)
* **Result:** Real-time identification of UI nodes (Buttons, Inputs, Icons) with high-confidence bounding boxes.

### 🧠 Phase 3: Logic & Semantic Engine (The Brain)
* **Module:** `Phase_3_Logic/`
* **Tech:** BERT (Sentence-Transformers) + PPO (Proximal Policy Optimization)
* **Result:** Elements are mapped into 384-dimensional semantic vectors. The PPO agent learns optimal navigation strategies through a reward-based system.

### 🛠️ Phase 4: Self-Healing & Reporting (Execution)
* **Module:** `Phase_4_Reporting/`
* **Tech:** Selenium + Python FPDF + HTML5/Tailwind
* **Result:** Automated recovery from "UI Drift." If a locator fails, the system re-calculates the target. Final execution results are exported as professional PDF reports.

---

## 📂 Repository Structure
```text
├── Phase_1_Training/         # YOLO training data and weights
├── Phase_2_Inference/        # UI detection on live app screens
├── Phase_3_Logic/            
│   ├── code/                 # BERT Embeddings & PPO Training Notebooks
│   └── results/              # Decision verification logs
└── Phase_4_Reporting/        
    ├── code/                 # index.html (Interactive Dashboard)
    └── reports/              # ARES_Final_Test_Report.pdf
