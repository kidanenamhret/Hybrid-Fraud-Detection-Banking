# Hybrid Machine Learning for Real-Time Fraud Detection in Digital Banking

This repository contains the LaTeX source code for a research proposal titled:

> **A Hybrid Machine Learning Approach for Real-Time Fraud Detection in Digital Banking Systems**

Submitted to the Department of Computer Science, Hawassa University IoT Campus, as part of the course *Research Methods in Computer Science (CoSc3101)*.

## Abstract

Digital banking systems face a critical trade-off between security and user experience. Current fraud detection largely relies on static rule‑based heuristics, leading to slow adaptation (2–4 weeks), high false‑positive rates (15–25 legitimate blocks per true fraud), and inference latency (200–500 ms) that exceeds real‑time requirements. Global fraud losses reached $7.3 billion in 2025, and customer churn due to false positives remains a major concern.

This proposal outlines a **hybrid machine learning system** that combines a stacking ensemble (Random Forest, Gradient Boosting, and Logistic Regression) with SMOTE‑ENN resampling to address extreme class imbalance. The system is designed to achieve:
- **F1‑score > 88%**
- **Sub‑100ms per‑transaction latency (p99)**
- Automated temporal adaptation to evolving fraud patterns

The methodology uses the IEEE‑CIS and IBM AML datasets (1M+ transactions) and is evaluated against single‑model baselines. The expected outcome is a lightweight, real‑time fraud detection pipeline suitable for deployment in digital banking gateways, especially in emerging markets.

## Repository Contents

| File | Description |
|------|-------------|
| `main.tex` | Main LaTeX document (proposal) |
| `references.bib` | BibTeX bibliography file |
| `logo.jpg` | University logo (institution emblem) |
| `system_arch.png` | System architecture diagram (Figure 1 in proposal) |

## Requirements

To compile the LaTeX document to PDF, you need a TeX distribution such as:

- **TeX Live** (Linux, Windows)
- **MiKTeX** (Windows)
- **MacTeX** (macOS)

Additionally, the following LaTeX packages are required (all are included in standard distributions):

- `geometry`, `amsmath`, `amsfonts`, `amssymb`, `graphicx`
- `booktabs`, `array`, `hyperref`, `setspace`
- `pgfgantt`, `float`, `url`

## Compilation Instructions

### Using a local LaTeX compiler

1. Clone or download this repository.
2. Open a terminal in the repository folder.
3. Run the following commands (requires BibTeX):

   ```bash
   pdflatex main.tex
   bibtex main
   pdflatex main.tex
   pdflatex main.tex
