---
title: Streamlit - LLM - BERT and BART AI models
date: 2024-05-08
categories: [llm]
tags: [general]
author: perspectives1000
---

## BERT and BART AI models

BERT - Bidirectional Encoder Representations from Transformers

BART - Bidirectional and Auto-Regressive Transformers

BERT and BART  are two popular transformers used in natural language processing (NLP) tasks. Although they share some similarities, they have different architectures and are designed for different purposes. Let's explore the differences:

**BERT:**

- **Architecture:** BERT uses a **bidirectional encoder architecture** that allows it to capture context **from both the left and right sides of a word** or token in a sentence.
- **Purpose:** BERT is designed to learn contextualized representations of words or tokens in a sentence, which can be used for various NLP tasks such as **sentiment analysis, text classification, and question answering.**
- **Pre-training:** BERT is pre-trained using two tasks: **masked language modeling (MLM) and next sentence prediction (NSP)**. This pre-training allows BERT to learn the context and relationships between words in a sentence.

**BART:**

- **Architecture:** BART combines both bidirectional encoder and autoregressive decoder architectures.
- **Purpose:** BART is designed for sequence-to-sequence tasks, **such as text generation, summarization, and translation**. The autoregressive decoder in BART enables it to generate output sequences given input sequences.
- **Pre-training:** BART is pre-trained **using a denoising objective,** which involves reconstructing corrupted input sequences. During pre-training, BART **randomly corrupts the input** text by deleting tokens, masking spans, or permuting sentences, and then learns to reconstruct the original text.

**Key differences:**

1. **Architecture:** BERT is a bidirectional encoder-only model, while BART combines bidirectional encoder and autoregressive decoder architectures.
2. **Purpose:** BERT is primarily used for learning contextualized representations, while BART is designed for text generation and sequence-to-sequence tasks.
3. **Pre-training:** BERT uses masked language modeling and next sentence prediction, whereas BART employs a denoising objective for pre-training.

In summary, BERT and BART are both powerful transformer-based models with different specializations. BERT excels at capturing contextual information for various NLP tasks, while BART is particularly suited for text generation and sequence-to-sequence tasks. The choice between BERT and BART depends on the specific requirements of your project or application.

----
**Reference**:  https://haystack.deepset.ai/blog/generative-vs-extractive-models
