# Multi-Agent Code Review System

A Streamlit-based application that uses multiple AI agents to analyze, review, and improve Python code.

## 🚀 Overview

This project implements a multi-agent pipeline for automated code review. Instead of relying on a single AI, it combines specialized agents to improve accuracy, reduce hallucinations, and provide structured feedback.

## 🧠 Key Features

* Multi-agent review (Security + Correctness + Synthesizer)
* Static analysis (AST + pattern scanning)
* Ground truth evaluation (Precision, Recall, F1)
* LLM-as-Judge scoring (optional)
* Auto-fix agent for corrected code generation
* Ablation study to compare configurations

## 🏗️ Architecture

Pipeline:

1. Tool Agent (static analysis)
2. Security Reviewer
3. Correctness Reviewer
4. Synthesizer
5. Verifier (optional)
6. Fix Agent

## 📊 Evaluation

The system evaluates performance using:

* Precision
* Recall
* F1 Score
* Ground truth comparison (manually labeled bugs)

## 🧪 Sample Categories

* Vulnerable code (security issues)
* Data processing bugs
* ML scripts
* Clean utility code (false positive testing)
* API handlers
* Concurrent systems

## ⚙️ Setup

### 1. Clone repo

```bash
git clone https://github.com/anuj-dubay-max/Multi-agent-review_new.git
cd Multi-agent-review_new
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Add API key

Create `.env` file:

```
GROQ_API_KEY=your_key_here
```

### 4. Run app

```bash
streamlit run app.py
```

## 📁 Files

* `app.py` – main application
* `review_memory.json` – past runs
* `ablation_cache.json` – cached results

## 📈 Results

The system compares:

* Single-agent vs Multi-agent
* Synthetic vs Real-world code
* Different agent configurations

## ⚠️ Notes

* Ground truth is manually defined per sample
* Evaluation focuses on relative performance, not absolute correctness
* Designed for research and experimentation

## 📌 Future Work

* Larger real-world datasets
* Structured output (JSON-based findings)
* CI/CD integration
* Model comparison across providers

---

## 📄 License

For academic and research use.
