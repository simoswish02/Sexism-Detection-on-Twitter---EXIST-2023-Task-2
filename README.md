# Sexism Detection on Twitter – EXIST 2023 Task 2

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

## Notes
This repository accompanies an academic report submitted as part of an NLP course assignment.
