# Hybrid Machine Learning for Real-Time Banking Fraud Detection

**Author:** Mesfin Alemayehu (ID: 2920/16)  
**Course:** Research Methods in Computer Science (CoSc3101)  
**Instructor:** Mr. Birhane Bekele  
**Institution:** Hawassa University, Department of Computer Science  
**Submission Date:** April 28, 2026

## Abstract

Digital banking fraud caused global financial losses exceeding $32 billion USD in 2025. Current fraud detection systems face a fundamental technical trade-off: rule-based systems are fast (10-15ms) but miss 62% of sophisticated fraud, while deep learning models achieve higher accuracy but introduce 300-500ms latency per transaction. This research proposes a hybrid machine learning architecture combining Random Forest (supervised) and Autoencoder (unsupervised) operating in parallel. Using the IEEE-CIS Fraud Detection dataset (1.2 million transactions), the system targets sub-100ms latency with >95% recall. A dynamic fusion gate adjusts model weights based on recent false positive rates.

## Proposal Document

The full research proposal is available as [`proposal.pdf`](proposal.pdf).

## Repository Structure
Hybrid-Fraud-Detection-Banking/
├── README.md # This file
├── proposal.pdf # Complete research proposal
├── references.bib # BibTeX citations (5 peer-reviewed sources)
├── src/ # Source code directory
│ ├── preprocess.py # Data preprocessing with SMOTE-ENN
│ ├── kafka_producer.py # Transaction stream simulator
│ ├── random_forest_branch.py
│ ├── autoencoder.py # PyTorch implementation
│ ├── fusion_gate.py
│ └── benchmark.py
├── config/ # Configuration files
│ ├── model_params.yaml
│ └── kafka_config.yaml
├── results/ # Output directory
│ ├── metrics.csv
│ ├── confusion_matrix.png
│ └── latency_distribution.pdf
└── .github/workflows/
└── latex_compile.yml # Auto-compiles proposal on push


## Prerequisites

- Python 3.9 or higher
- 8GB RAM minimum (16GB recommended)
- NVIDIA GPU (optional, for faster training)
- Internet connection for dataset download

## Installation

```bash
# Clone the repository
git clone https://github.com/mesfin-2920/Hybrid-Fraud-Detection-Banking.git
cd Hybrid-Fraud-Detection-Banking

# Create virtual environment (recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install torch scikit-learn pandas numpy kafka-python redis matplotlib seaborn

Dataset
The IEEE-CIS Fraud Detection Dataset is available at:
https://ieee-dataport.org/open-access/ieee-cis-fraud-detection

Download and extract to ./data/raw/

Expected Output
Metric	Target
Precision	>0.85
Recall	>0.95
F1-Score	>0.89
AUC-ROC	>0.97
Latency (p95)	<95ms
Ethics Compliance
Data Privacy: No PII in dataset. GDPR compliant.

Bias Audit: Stratified sampling + demographic parity testing.

Environmental Impact: 500 GPU-hours offset with carbon donation.

License
Academic submission to Hawassa University. All rights reserved.

Contact
Mesfin Alemayehu - Student ID: 2920/16
Hawassa University Institute of Technology
Department of Computer Science

Submitted to Mr. Birhane Bekele - April 28, 2026

