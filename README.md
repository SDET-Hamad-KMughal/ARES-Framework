# ARES-Framework
# ARES Framework: Autonomous Resilience & Exploration System 🚀
**A Multimodal Reinforcement Learning Approach to Self-Healing Mobile UI Testing**

## 📌 Overview
The ARES Framework is a four-phase autonomous engine designed to navigate mobile applications using computer vision and semantic understanding. This repository contains the implementation of the framework as described in the research paper, focusing on the **Airbnb iOS** ecosystem as a case study.

---

## 🛠️ System Architecture (The 4 Phases)

### 📂 Phase 1 & 2: The Perception Engine
* **Folder:** `Phase_1_Training/` & `Phase_2_Inference/`
* **Technology:** YOLOv8 (Deep Learning)
* **Function:** The "Eyes" of the system. It detects interactive elements (Buttons, Inputs, Icons) with high precision.
* **Key File:** `best.pt` (Trained weights for UI detection).

### 📂 Phase 3: The Logic Engine (The Brain)
* **Folder:** `Phase_3_Logic/code/`
* **Technology:** PPO (Reinforcement Learning) + BERT (NLP)
* **Function:** This is where the AI "decides" where to click. It uses BERT to read text on buttons and PPO to learn the most efficient path to a goal.
* **Results:** Verification logs confirm successful prioritization of 'Input' elements.


### 📂 Phase 4: Self-Healing & Reporting
* **Folder:** `Phase_4_Reporting/code/`
* **Technology:** Python FPDF + Custom Healer Logic
* **Function:** Monitors UI stability. If the UI changes, the "Self-Healing" mechanism re-maps coordinates automatically. Generates a formal PDF report.
* **Key File:** `ARES_Final_Test_Report.pdf`.

---

## 🚀 How the System Works
1.  **Detection:** YOLOv8 identifies interactive UI nodes.
2.  **Semantic Mapping:** BERT converts labels into 384-dimensional vectors to "understand" intent.
3.  **Strategic Learning:** The PPO agent navigates the app, earning rewards for reaching target nodes (e.g., Search/Input).
4.  **Resilience:** If a button moves, the Self-Healer detects the "UI Drift" and updates the test path.

---

## 📂 Repository Structure
```text
├── Phase_1_Training/         # YOLO model training scripts
├── Phase_2_Inference/        # UI detection on live screens
├── Phase_3_Logic/            # RL training and BERT semantic engine
│   ├── code/                 # Notebooks for PPO & Mapping
│   └── results/              # Verification success logs
└── Phase_4_Reporting/        # Self-healing logic and automated PDF reports
