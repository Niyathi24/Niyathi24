# Fairness Analysis of Pre-Trained NLP Models for Toxicity Detection
[Paper - "A Comparative Analysis of Pre-Trained NLP Models for Toxicity Detection and Unintended Bias"](Sreeniyathi_Kasireddy_paper.pdf)
## Overview

**A Comparative Analysis of Pre-Trained NLP Models for Toxicity Detection and Unintended Bias**

This project evaluates the fairness and accuracy of three state-of-the-art NLP models for toxicity detection, with a focus on identifying and quantifying unintended bias against protected identity groups. The research combines automated evaluation metrics with bias analysis across gender and racial identities to assess real-world implications for content moderation systems.

## Problem Statement

**Do pre-trained toxicity detection models exhibit systematic bias against comments mentioning protected identities?**

This project investigates whether models trained to detect toxic language disproportionately flag non-toxic comments containing identity references (gender, race), potentially silencing marginalized voices in online spaces.

## Dataset

**Source:** Jigsaw Unintended Bias in Toxicity Classification Dataset (2019)  
**Size:** ~180,000 comments from Civil Comments platform  
**Features Used:** Comment text, toxicity labels, identity mention annotations  
**Balanced Subsets Created:**  
- Gender-focused: ~10,000 comments (male, female, transgender, other_gender)  
- Race-focused: ~34,000 comments (Asian, Black, Latino, White, other_race_or_ethnicity)

## Approach

### Model Selection & Implementation

Three transformer-based models were evaluated without fine-tuning:

1. **Detoxify Original** – Wikipedia-trained toxicity classifier  
2. **roberta-hate-speech-dynabench-r4-target** – Hate speech detection from dynamic adversarial data  
3. **Twitter-RoBERTa Offensive** – Social media offensive language detection

**Implementation:** HuggingFace Transformers pipeline with 0.5 toxicity threshold

### Evaluation Methodology

**Primary Metrics:**
- Accuracy, Precision, Recall, F1-Score
- **False Positive Rate (FPR)** – Key fairness metric for identity groups

**Bias Analysis:**
- Subgroup performance comparison across identities
- Trade-off analysis between precision and recall
- Cross-model fairness comparison

## Results

### Key Findings

| Model | Accuracy Range | FPR Range (Gender) | FPR Range (Race) | Bias Pattern |
|-------|----------------|---------------------|------------------|-------------|
| **Detoxify** | 80-89% | 2.8-3.9% | 2.1-3.2% | Most balanced, conservative |
| **Dynabench R4** | 66-76% | 13.9-21.9% | 18.4-27.9% | Moderate bias, recall-focused |
| **Twitter-RoBERTa** | 41-47% | 62.6-65.0% | 63.1-76.0% | High bias, over-flagging |

### Critical Insights

1. **Twitter-RoBERTa showed the highest bias** – FPRs exceeding 60% indicate strong association between identity mentions and toxicity predictions
2. **Detoxify demonstrated the best fairness-performance balance** – Low FPRs across all subgroups while maintaining reasonable detection
3. **Transgender and Asian identities consistently showed highest FPRs** across models, indicating amplified bias against underrepresented groups
4. **Race-related bias exceeded gender-related bias** in all models, with wider FPR disparities

## Technologies

**NLP & ML:** HuggingFace Transformers, PyTorch, Scikit-learn  
**Data Processing:** Pandas, NumPy  
**Visualization:** Matplotlib, Seaborn  
**Evaluation:** Custom fairness metrics, statistical analysis

## Impact

This analysis provides:
- Quantitative evidence of bias in widely-used toxicity detection models
- Framework for evaluating fairness in NLP systems
- Guidance for selecting appropriate models based on use-case requirements
- Evidence for the need for bias mitigation techniques in content moderation

## Team

**Sreeniyathi Kasireddy**

**Mantra Burugu**

**Farhana Rahman**
