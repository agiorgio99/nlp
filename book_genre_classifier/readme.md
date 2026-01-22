# BERT-based Book Genre Classifier

## Overview
This project provides a system to classify books into genres based on their plot summaries using **BERT** (Bidirectional Encoder Representations from Transformers).

## Dataset
The model uses a balanced subset of the **CMU Book Summary Dataset**, consisting of 3,000 summaries across 6 main genres:
* Crime Fiction
* Fantasy
* Historical Novel
* Horror
* Science Fiction
* Thriller  

## Architecture
The classifier fine-tunes a **BERT transformer model**. Key components include:
* **Input:** Tokenized summaries (padded/truncated to 512 tokens).
* **Representation:** Using the embedding of the first token (`[CLS]`) from the last layer.
* **Optimization:** Dynamic learning rate schedule and mixed-precision training (float16/float32) for efficiency.

## Experimental Results
Various experiments were conducted comparing raw text against preprocessed text (stop words removal, NER masking, lemmatization).
* **Best Performance:** The model performed best using **only BERT** without heavy preprocessing, reaching a **Validation Accuracy of 77.29%**.
* **Observations:** Preprocessing techniques tended to decrease performance, suggesting the model benefits from the full context of the raw summaries.