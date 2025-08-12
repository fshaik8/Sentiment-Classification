# Twitter Sentiment Analysis for Political Discourse

This repository contains the code and findings for a research project on sentiment classification of political tweets, completed for the CS583 Data Mining and Text Mining course. The project involves building an end-to-end pipeline to classify tweets about the 2012 U.S. presidential election candidates (Barack Obama and Mitt Romney) into positive, negative, or neutral sentiment.

The core of this project is a systematic comparison of baseline NLP models against modern, fine-tuned Transformer architectures to achieve the highest possible accuracy on this noisy, domain-specific dataset.

---

## Key Features & Achievements

*   **📈 High-Performance Model:** Engineered an end-to-end sentiment classification pipeline that achieved over **72% accuracy** on the final test set.
*   **🤖 State-of-the-Art Transformers:** Successfully fine-tuned a domain-specific **BERTweet** transformer model, which proved to be the most effective architecture for this social media-based task.
*   **🔬 Rigorous Model Comparison:** Led a comparative analysis of three distinct models (rule-based VADER, general-purpose RoBERTa, and domain-specific BERTweet) to scientifically select the best foundation for fine-tuning.
*   **🚀 Quantifiable Improvement:** The final fine-tuning methodology delivered a **16% performance improvement** over the best-performing baseline model, demonstrating the critical value of transfer learning.
*   **📊 Comprehensive Evaluation:** Evaluated all models against a full suite of metrics, including Accuracy, Precision, Recall, and F1-score for both positive and negative classes.

---

## Methodology

The project followed a structured, multi-stage methodology to arrive at the final, optimized model.

### 1. Data Preprocessing
The initial training dataset contained 14,398 tweets (7,198 for Obama, 7,200 for Romney). The following preprocessing steps were applied:
- **Class Filtering:** The "mixed" sentiment class (label 2) was removed to align with the project's three-class (positive, negative, neutral) objective.
- **Feature Pruning:** Non-textual columns like date and time were dropped.
- **Text Cleaning:** A standard NLP cleaning pipeline was implemented to remove irrelevant components like HTML tags, URLs, and usernames from the tweet text, preparing it for the models.

### 2. Baseline Model Benchmarking
Three different pre-trained models were evaluated on the raw training data to establish a performance baseline:
1.  **VADER:** A traditional, rule-based sentiment analyzer.
2.  **Twitter-RoBERTa:** A powerful Transformer model pre-trained on a massive corpus of tweets.
3.  **BERTweet:** A RoBERTa-based model specifically pre-trained on English tweets.

Based on this initial experiment, **BERTweet** was selected as the most promising model to carry forward for fine-tuning.

### 3. Fine-Tuning
The selected BERTweet model was then fine-tuned on the project's specific training data. A key strategic decision was made to train two separate, specialized models:
- An **Obama-specific model**, fine-tuned only on tweets about Barack Obama.
- A **Romney-specific model**, fine-tuned only on tweets about Mitt Romney.

This approach of creating tailored models for each candidate proved to be more effective than a single, general-purpose model. The number of training epochs (2-3) was carefully chosen to maximize accuracy while preventing overfitting.

---

## Key Results

### Baseline Model Performance (Accuracy)

| Model | Accuracy |
| :--- | :--- |
| VADER | 35.1% |
| Twitter-RoBERTa | 59.2% |
| **BERTweet** | **62.5%** |

### Final Fine-Tuned Model Performance (Accuracy on Test Set)

| Model | Accuracy |
| :--- | :--- |
| **Fine-Tuned Obama Model** | **72.9%** |
| **Fine-Tuned Romney Model**| **71.8%** |

The fine-tuning process resulted in a **~16% relative improvement in accuracy** over the baseline BERTweet model, confirming the effectiveness of the methodology.
