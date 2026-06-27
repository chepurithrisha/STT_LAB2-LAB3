# STT_LAB2-LAB3

# Automated Bug-Fix Commit Mining and Context Analysis

## 📖 Overview

This project presents an end-to-end framework for **mining, analyzing, and evaluating bug-fixing commits** from large-scale open-source software repositories. The system combines **software repository mining**, **Large Language Models (LLMs)**, **static code analysis**, and **software quality metrics** to understand the characteristics of bug fixes and improve commit message quality.

Developed as part of the **CS202 – Software Tools and Techniques** course at **IIT Gandhinagar**, the project integrates the objectives of **Lab Assignment 2** and **Lab Assignment 3** into a unified software analytics pipeline.

---

## 🎯 Objectives

- Mine bug-fixing commits from real-world GitHub repositories.
- Extract file-level source code revisions and diffs.
- Analyze commit messages using pretrained Large Language Models.
- Rectify imprecise commit messages for improved contextual understanding.
- Compute structural software quality metrics before and after bug fixes.
- Measure semantic and token-level similarity between source code versions.
- Classify bug fixes as **Major** or **Minor** based on multiple software metrics.
- Compare semantic and structural analyses to identify agreement between different evaluation techniques.

---

## ✨ Features

### 🔹 Repository Mining

- Extracts bug-fixing commits from GitHub repositories.
- Collects commit metadata including:
  - Commit Hash
  - Parent Commits
  - Modified Files
  - Commit Messages

---

### 🔹 File-Level Diff Analysis

For every modified source file:

- Extracts source code before modification
- Extracts source code after modification
- Generates Git diffs
- Creates structured datasets for further analysis

---

### 🔹 Commit Message Rectification

Uses pretrained transformer models to:

- Infer bug-fix categories
- Evaluate developer commit messages
- Generate rectified file-level commit messages
- Improve contextual representation of software changes

---

### 🔹 Structural Code Analysis

Computes software quality metrics using **Radon**:

- Maintainability Index (MI)
- Cyclomatic Complexity (CC)
- Lines of Code (LOC)

Also computes:

- MI Change
- CC Change
- LOC Change

to measure the impact of each bug fix.

---

### 🔹 Semantic Code Analysis

Measures code change magnitude using:

- **CodeBERT Semantic Similarity**
- **BLEU Token Similarity**

These metrics quantify semantic and syntactic differences between source code versions.

---

### 🔹 Bug Classification

Automatically classifies bug fixes into:

- Major Fix
- Minor Fix

using configurable similarity thresholds.

---

### 🔹 Agreement Detection

Compares classifications obtained from semantic similarity and token similarity to determine whether multiple evaluation techniques agree on the significance of each software change.

---

## 🏗️ Project Workflow

```text
GitHub Repository
        │
        ▼
Repository Mining (PyDriller)
        │
        ▼
Bug-Fix Commit Identification
        │
        ▼
File-Level Diff Extraction
        │
        ▼
Commit Message Rectification
        │
        ▼
Structural Metric Analysis
(MI • CC • LOC)
        │
        ▼
Semantic & Token Similarity
(CodeBERT • BLEU)
        │
        ▼
Major / Minor Classification
        │
        ▼
Agreement Detection
        │
        ▼
Final Software Analytics Report
```

---

## 🛠️ Technologies Used

### Programming Language

- Python

### Libraries & Frameworks

- PyDriller
- Hugging Face Transformers
- CommitPredictorT5
- CodeBERT
- Radon
- SacreBLEU
- Pandas
- NumPy

### Development Tools

- Git
- GitHub
- Jupyter Notebook

---

## 📊 Evaluation Metrics

The framework evaluates software changes using:

- Maintainability Index (MI)
- Cyclomatic Complexity (CC)
- Lines of Code (LOC)
- Semantic Similarity
- Token Similarity (BLEU Score)
- Major/Minor Bug Classification
- Agreement Detection

---

## 📂 Project Structure

```
.
├── data/
│   ├── raw_dataset.csv
│   ├── processed_dataset.csv
│
├── scripts/
│   ├── repository_mining.py
│   ├── diff_analysis.py
│   ├── commit_rectification.py
│   ├── structural_metrics.py
│   ├── semantic_analysis.py
│   └── classification.py
│
├── results/
│   ├── metrics.csv
│   ├── plots/
│   └── reports/
│
├── notebooks/
│
├── README.md
│
└── requirements.txt
```

*(Modify the project structure above if your folder organization differs.)*

---

## 🚀 Key Highlights

- Automated mining of bug-fixing commits from open-source repositories.
- File-level source code comparison and diff extraction.
- LLM-assisted commit message rectification.
- Structural software quality analysis using Radon.
- Semantic code comparison using CodeBERT.
- Token similarity analysis using BLEU.
- Automated classification of bug fixes.
- Agreement analysis across multiple software quality metrics.

---

**Course:** CS202 – Software Tools and Techniques  
**Institute:** Indian Institute of Technology Gandhinagar
