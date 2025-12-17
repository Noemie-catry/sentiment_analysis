# 🤖 Sentiment Analysis POC: BERT Model vs. Gemini LLM

**Project Type:** Data Science / NLP (Natural Language Processing)  
**Context:** HR Ticket Analysis - Proof of Concept (POC)  
**File:** `final_sentiment_analysis.ipynb`

### 📥 Download Model

The model file is hosted via GitHub Releases due to its size.
[**Click here to download the .bin file**](https://github.com/Noemie-catry/sentiment_analysis/releases/download/v1.0/pytorch_model.1.zip)

---

## 📋 Overview

This notebook documents a comparative study conducted to analyze qualitative feedback from employee HR tickets. The goal was to move beyond simple quantitative scores (NPS) and automatically classify the **sentiment** (Positive, Negative, Neutral) of textual comments.

Given strict internal security constraints and a need for innovation, two approaches were tested and compared:
1.  **Classical NLP Approach:** Using a pre-trained **BERT** model (via Hugging Face Transformers).
2.  **GenAI Approach:** Using **Google Gemini** via API with prompt engineering.

## ⚙️ Methodology & Notebook Structure

The notebook is organized into the following logical steps:

### 1. Data Preprocessing
* Importing raw data (CSV/Excel).
* **Data Cleaning:** Removing HTML tags, special characters, and normalizing text using `pandas` and `re` (RegEx).
* **Anonymization:** Ensuring no PII (Personally Identifiable Information) is processed.

### 2. Approach A: BERT Model (Machine Learning)
* **Tokenization:** processing text for the BERT model.
* **Inference:** Running the model to classify sentiments.
* **Challenges:** Required significant data cleaning and computational resources.

### 3. Approach B: Gemini (Generative AI)
* **Prompt Engineering:** Designing a specific system prompt to instruct Gemini to act as a data analyst and output structured JSON/Labels.
* **API Calls:** Batch processing the comments through the model.
* **Advantages:** Better understanding of context, sarcasm, and nuances without heavy training.

### 4. Comparative Analysis & Visualization
* Comparison of accuracy between the two models.
* Visualizing the distribution of sentiments using `matplotlib` / `seaborn`.
* **Result:** The study highlighted the trade-offs between cost/latency (BERT) and accuracy/nuance (Gemini).

---

## 🛠 Libraries Used

To run this notebook, the following Python libraries are required:

```python
pip install pandas numpy torch transformers scikit-learn matplotlib seaborn
# For the GenAI part (depending on the specific SDK version used)
pip install google-generativeai
