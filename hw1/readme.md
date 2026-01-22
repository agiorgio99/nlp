# Homework 1: Event Detection

## Overview
This project focuses on **Event Detection** using **Bi-LSTM** (Bidirectional Long Short-Term Memory) architectures. The goal is to identify event triggers within sentences and classify them into specific categories.

## Methodology
The approach explores three incremental architectures:
1.  **Word Embeddings:** Using a Bi-LSTM layer taking word embeddings (e.g., GloVe) as input.
2.  **Word + POS Embeddings:** Concatenating Part-Of-Speech (POS) embeddings with word embeddings to add syntactic information.
3.  **CRF Layer:** Adding a Conditional Random Field (CRF) layer on top of the Bi-LSTM to model dependencies between adjacent tags.

## Dataset
The dataset consists of sentences annotated with event triggers in **BIO format**. The target event classes are:
* `SENTIMENT`
* `CHANGE`
* `ACTION`
* `SCENARIO`
* `POSSESSION` 
## Results
Experiments showed that adding POS embeddings improved performance, while the CRF layer did not significantly enhance detection for this specific task. The best models achieved a Test F1-Score around **0.70**.