
# 🧠 Kidney Stone Detection using IBM Watson AutoAI

This project predicts the presence of kidney stones using an automated machine learning pipeline developed in **IBM Watson Studio** with **AutoAI**. AutoAI automates data preprocessing, model selection, feature engineering, and hyperparameter tuning, helping build high-performing models with minimal manual effort.

---

## 📁 Dataset

- **File:** `Kidney Stone Detection.csv`
- **Description:** Contains medical records of patients with a binary `target` variable indicating the presence (1) or absence (0) of kidney stones.

---

## ⚙️ Project Workflow

### 1. Dataset Upload
- The dataset was uploaded to the IBM Watson Studio project.
- The `target` column was selected as the prediction label.

### 2. AutoAI Experiment
AutoAI handled the end-to-end ML lifecycle:
- Data preprocessing
- Feature transformation
- Model selection
- Pipeline tuning

### 3. Pipeline Generation
AutoAI generated **8 pipelines** using different algorithms and enhancement strategies:
- Algorithms used: **Extra Trees Classifier**, **Snap Boosting Machine Classifier**
- Enhancements included:
  - **HPO** – Hyperparameter Optimization
  - **FE** – Feature Engineering

### 4. Pipeline Leaderboard

| Rank | Pipeline | Accuracy | Enhancements         | Algorithm                      |
|------|----------|----------|----------------------|--------------------------------|
| 1    | Pipeline 4 | 0.934    | HPO-1 → FE → HPO-2   | Extra Trees Classifier         |
| 2    | Pipeline 3 | 0.934    | HPO-1 → FE           | Extra Trees Classifier         |
| 3    | Pipeline 8 | 0.890    | HPO-1 → FE → HPO-2   | Snap Boosting Machine Classifier |
| 4    | Pipeline 7 | 0.890    | HPO-1 → FE           | Snap Boosting Machine Classifier |
| 5    | Pipeline 6 | 0.890    | HPO-1                | Snap Boosting Machine Classifier |
| 6    | Pipeline 2 | 0.880    | HPO-1                | Extra Trees Classifier         |
| 7    | Pipeline 1 | 0.880    | None                 | Extra Trees Classifier         |
| 8    | Pipeline 5 | 0.879    | None                 | Snap Boosting Machine Classifier |

- **Top performer:** Pipeline 4 with an accuracy of **93.4%**
- **Best algorithm:** Extra Trees Classifier
- **Time elapsed for training:** ~3 minutes

---

## 📊 Visual Tools

### 🧭 AutoAI Relationship Map
- Graphical flow showing feature transformers, estimators, and enhancements.

### 📋 Progress Map
- Illustrates data flow: input → preprocessing → model → output

### 🏁 Experiment Completed
- Total Pipelines: 8
- Ranking criteria: **Optimized Accuracy (Cross-validation score)**

---

## 📦 Assets Included

| Asset | Description |
|-------|-------------|
| `Kidney Stone Detection.csv` | Dataset file |
| `kidney stone detection - P4 Extra Trees Classifier - Notebook.ipynb` | Auto-generated notebook |
| `kidney stone detection - P4 Extra Trees Classifier - Model` | Trained model |
| `IBM Cloud Pak for Data.pdf` | Pipeline leaderboard and visual summary |

---

## 🧪 Reproduce This Project

1. Sign in to IBM Watson Studio.
2. Create a new project and upload the dataset.
3. Start a new AutoAI experiment.
4. Select the `target` column.
5. Let AutoAI build and rank pipelines.
6. Save/export the top model and notebook.

---

## 🛠️ Tools & Technologies

- IBM Watson Studio
- IBM AutoAI
- Scikit-learn (via AutoAI backend)
- Jupyter Notebooks
- CSV data format

---

## ✨ Outcome

By using IBM AutoAI, a high-accuracy kidney stone detection model was created with minimal manual coding. AutoAI's pipeline ranking system ensured the most optimized model was selected for deployment or further analysis.

---
