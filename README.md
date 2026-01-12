# Assignment 1 - Sexism Detection on Twitter – EXIST 2023 Task 2

This repository contains the code developed for the EXIST 2023 Task 2 on sexism detection. The project focuses on multi-class classification of tweets according to the sexist intention expressed by the author.

## Task Description
The task consists of classifying tweets into four categories:
- Non-sexist
- Direct sexist
- Judgemental
- Reported sexist

Only English tweets are considered, following the official EXIST task setup.

## Models
Three architectures are evaluated:
- **Baseline**: Bidirectional LSTM with GloVe embeddings
- **Stacked**: Two-layer Bidirectional LSTM with GloVe embeddings
- **Transformer**: Twitter-RoBERTa-base fine-tuned for sexism detection

All models are trained using multiple random seeds, and results are reported using an ensemble strategy based on prediction confidence.

## Implementation
Experiments are implemented using Python, Keras/TensorFlow, PyTorch, and the HuggingFace Transformers library. All preprocessing, training, evaluation, and analysis steps are documented in the provided notebooks.

# Assignment 2 - Sexism Detection with LLMs

## Task Description
This project implements a multi-class classification system for sexism detection using open-source Large Language Models (LLMs) [file:1]. It addresses the **EDOS Task B**, classifying text into one of five categories:
1. **Non-sexist**
2. **Threats**
3. **Derogation**
4. **Animosity**
5. **Prejudiced Discussion**

## Methodology
The approach relies on **prompt engineering** rather than fine-tuning. The pipeline includes:
- **Model Setup**: Loading and quantizing open-source models (e.g., Mistral, Llama) using Hugging Face.
- **Prompting**: Implementing both **Zero-Shot** and **Few-Shot** strategies with specific instruction templates.
- **Inference**: Generating and parsing responses to map textual outputs to numerical labels (0-4).
- **Evaluation**: Measuring performance via **Macro F1-score** and **Fail-ratio** (percentage of invalid responses).

## Dataset
- **`a2_test.csv`**: Balanced test set of 300 samples for evaluation.
- **`demonstrations.csv`**: Collection of 1000 samples used to build few-shot examples.

## Notes
This repository accompanies an academic report submitted as part of an NLP course assignment.


