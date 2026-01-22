# Homework 2: Word Sense Disambiguation (WSD)

## Overview
This project, titled **"POS-itive Disambiguation"**, implements a system for Word Sense Disambiguation using **Transformer-based models** (BERT) combined with **POS tagging** information.

## Methodology
The system utilizes the **BERT Encoder** to generate embeddings. The core architecture involves:
* **Tokenization:** Handling word-to-token mapping to isolate target words.
* **Feature Extraction:** Averaging the last 4 hidden states of BERT to create target embeddings.
* **POS Integration:** Enhancing the model by concatenating or summing POS embeddings with the transformer output.
* **Classification:** A linear layer with dropout and candidate masking to predict the correct sense ID.

## Dataset
The model is trained on a coarse-grained dataset containing words, lemmas, POS tags, and candidate senses from WordNet.

## Results
The experiments demonstrated that using **words** as input (rather than lemmas) combined with **POS embeddings** yielded the best performance, achieving a **Test Accuracy of 0.8956**.