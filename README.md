# News Summarization using T5 and BART Models
This repository contains code and resources for news summarization using T5 and BART models, along with the evaluation based on ROUGE metrics.

## Overview
News summarization plays a crucial role in condensing lengthy news articles into concise yet informative summaries. In this project, we explore the effectiveness of T5 and BART models for generating accurate and coherent news summaries.

## Prerequisites
* Python 3.x
* TensorFlow
* Hugging Face Transformers Library
* ROUGE Metric

## Dataset Description
The "news_summary.csv" dataset is a comprehensive collection of news articles and their corresponding summaries. It contains a diverse range of news topics and serves as an ideal resource for training and evaluating automatic summarization models.

## Models Used
### T5 (Text-to-Text Transfer Transformer):
* T5, which stands for Text-to-Text Transfer Transformer, is a versatile transformer-based model introduced by Google Research. Unlike many other transformer models that were designed for specific tasks like translation or classification, T5 is designed with a unified "text-to-text" framework. This means that it can handle various NLP tasks, including summarization, translation, question answering, and more, by converting all tasks into a text-to-text format.

* In the context of summarization, T5 frames the summarization task as converting a given source text (e.g., a news article) into a target text (e.g., a concise summary). It achieves this by using a sequence-to-sequence architecture, where the source text is encoded into a fixed-size vector, and then the model generates the target text from this vector. T5 can be fine-tuned on summarization data to generate coherent and concise summaries.

### BART (Bidirectional and AutoRegressive Transformers):
* BART, short for Bidirectional and AutoRegressive Transformers, is another powerful transformer-based model developed by Facebook AI. It's designed to handle sequence-to-sequence tasks, including text generation tasks like summarization. BART's architecture combines bidirectional and autoregressive approaches to leverage the strengths of both.

* For summarization, BART's bidirectional nature helps it understand the context of the source text more effectively, capturing important information from both directions. Then, its autoregressive decoding process allows it to generate target text one token at a time, considering the generated tokens in a left-to-right manner to ensure coherence.

* BART is pretrained on a denoising autoencoder task, which involves corrupting and then reconstructing sentences. This pretraining helps the model capture the structure and content of text. Fine-tuning BART on summarization tasks refines its ability to generate coherent and informative summaries.

## Evaluation Metrics
* ROUGE Scores:
  
1. The ROUGE scores for the BART model's summarization are as follows:

- ROUGE-1:
  - Recall (R): 0.6154
  - Precision (P): 0.1667
  - F1-Score (F): 0.2623

- ROUGE-2:
  - Recall (R): 0.2500
  - Precision (P): 0.0588
  - F1-Score (F): 0.0952

- ROUGE-L:
  - Recall (R): 0.5385
  - Precision (P): 0.1458
  - F1-Score (F): 0.2295

These ROUGE scores provide an evaluation of the quality of the generated summaries produced by the BART model. They assess how well the generated summaries match the reference summaries in terms of recall, precision, and F1-score for different n-gram levels and the longest common subsequence. Higher ROUGE scores generally indicate better summarization performance. Keep in mind that the specific threshold for good scores can vary based on the specific task and dataset.

2. The ROUGE scores for the T5 model's summarization are as follows:

- ROUGE-1:
  - Recall (R): 0.4615
  - Precision (P): 0.2400
  - F1-Score (F): 0.3158

- ROUGE-2:
  - Recall (R): 0.2500
  - Precision (P): 0.1250
  - F1-Score (F): 0.1667

- ROUGE-L:
  - Recall (R): 0.3846
  - Precision (P): 0.2000
  - F1-Score (F): 0.2632

Similar to the BART model, these ROUGE scores provide an evaluation of the quality of the generated summaries produced by the T5 model. They assess how well the generated summaries match the reference summaries in terms of recall, precision, and F1-score for different n-gram levels and the longest common subsequence. Higher ROUGE scores generally indicate better summarization performance, but the interpretation of what constitutes a "good" score can depend on the specific context and task.
