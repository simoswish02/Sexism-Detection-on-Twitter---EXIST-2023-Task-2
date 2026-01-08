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

## Experimental Pipeline
The main steps of the pipeline are:
1. Dataset loading and cleaning
2. Text preprocessing
3. Vocabulary construction and embedding initialization
4. Model training and evaluation
5. Ensemble creation
6. Error analysis

## Evaluation
Models are evaluated using accuracy, macro precision, macro recall, and macro F1-score on validation and test sets.

## Repository Structure
data/ # Dataset files
notebooks/ # Jupyter notebooks for experiments
models/ # Model definitions and training scripts
results/ # Evaluation outputs


## Requirements
The experiments rely on the following libraries:
- Python
- Keras / TensorFlow
- PyTorch
- HuggingFace Transformers
- Scikit-learn

## Notes
This repository accompanies an academic report submitted as part of an NLP course assignment.
