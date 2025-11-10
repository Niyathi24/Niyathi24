# LLM Movie Title Generator

## Overview

Evaluates LLM capability to generate creative and contextually appropriate movie titles from genre and plot overview. This project implements an automated evaluation system combining semantic analysis, human ratings, and statistical correlation to assess title quality across creativity, content alignment, and linguistic quality dimensions.

## Problem Statement

Can LLMs generate movie titles that balance creativity with semantic relevance to the source material? This project evaluates the strengths and limitations of LLM-based creative content generation.

## Dataset

- **Source:** [HuggingFace IMDB Movies Dataset](https://huggingface.co/datasets/drossi/EDA_on_IMDB_Movies_Dataset)
- **Size:** 1,000 top-rated IMDB movies
- **Features Used:** Genre, Overview, Original Title, IMDB Rating

## Approach

### Title Generation
- **Model:** OpenAI GPT-4o-mini
- **Prompt:** Structured prompt requesting genre and overview-aware title generation
- **Parameters:** Max 20 tokens per response

**Example:**
```
Input: Genre: Drama | Overview: Two imprisoned men bond over years...
Output: "Beyond the Bars of Hope"
Original: "The Shawshank Redemption"
```

### Evaluation Methodology
Three-part evaluation combining:

1. **Automated Metrics** (SentenceTransformers, NLTK)
   - Content alignment (overview & genre relevance)
   - Creativity (novelty, surprise, difference from original)
   - Title quality (length, readability, word choice)

2. **Human Evaluation** (Interactive CLI)
   - User ratings on 1-10 scale
   - Comparison with automated scores

3. **Visualization**
   - Correlation analysis between metrics
   - Performance distribution histograms

## Results

| Metric | Score |
|--------|-------|
| Overall Score | 0.658 |
| Content Alignment | 0.480 |
| Creativity | 0.706 |
| Title Quality | 0.808 |
| Novelty | 0.998 |

**Key Insight:** LLM shows strong linguistic quality (0.808) and novelty (0.998) but weaker content alignment (0.480), indicating titles are grammatically sound but may lack semantic depth.

## Technologies

- **Backend:** Python, OpenAI API
- **NLP:** SentenceTransformers, NLTK, Hugging Face
- **Data:** Pandas, Scikit-learn
- **Visualization:** Matplotlib, Seaborn

## Team

- **Sreeniyathi Kasireddy** - Evaluation metrics, Exploratory Data Analysis, Prompt engineering
- **Nathan Chen** - Dataset analysis, human evaluation
- **Samanvay Upadhyay** - Prompt engineering, title generation
