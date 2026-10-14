---
language:
- en
license: mit
tags:
- sentiment-analysis
- text-classification
- bert
datasets:
- imdb
metrics:
- f1-score
pipeline_tag: text-classification
---

# BERT-Base Fine-Tuned for IMDb Sentiment Analysis 🎬🤖

This model is a fine-tuned version of **`bert-base-uncased`** trained on the [IMDb dataset](https://huggingface.co) for binary sentiment classification (Positive/Negative). 

It was built as a lightweight, efficient project to demonstrate transfer learning using the Hugging Face `transformers` ecosystem.

## 📌 Model Description
- **Developed by:** Rohith A K
- **Model type:** Transformer-based text classification
- **Language(s) (NLP):** English
- **License:** MIT
- **Finetuned from model:** `bert-base-uncased`

## 🚀 How to Use

You can use this model directly with a Hugging Face pipeline for inference:

```python
from transformers import pipeline

# Load the model and tokenizer from the hub
classifier = pipeline("text-classification", model="your-username/your-model-name")

# Test a review
review = "I absolutely loved this movie! The acting was incredible and the plot kept me hooked."
print(classifier(review))
# Output: [{'label': 'LABEL_1', 'score': 0.998}] (Note: LABEL_1 is Positive, LABEL_0 is Negative)
```

## 📊 Dataset & Training Details
- **Dataset:** IMDb Movie Reviews (25,000 training samples, 25,000 testing samples)
- **Task:** Binary Sentiment Analysis (Classifying movie reviews into positive or negative sentiment).
- **Training Framework:** Hugging Face `Trainer` API & PyTorch.

## 🎛️ Intended Uses & Limitations
- **Intended Use:** Analyzing user reviews, feedback, or short textual commentary for movie or entertainment-related content.
- **Limitations:** The model is trained specifically on movie reviews and may not perform as accurately on other domains (e.g., financial news, medical feedback, or product reviews with highly technical jargon).
