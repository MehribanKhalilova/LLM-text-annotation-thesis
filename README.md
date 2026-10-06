# Automatic Labeling of Text Data Using Large Language Models

This repository supports the practical part of the master's thesis
"Automatic Labeling of Text Data Using Large Language Models".

## 1.2 Project as an End-to-End Solution

The purpose of the project is to investigate how Large Language Models
(LLMs) can be used as automatic annotators for text classification.

The system receives unlabeled text together with a predefined set of
possible class labels. An LLM is prompted to analyze the text and assign
one of the available labels.

The overall workflow is:

Raw text → LLM → Predicted label → Evaluation → Labeled dataset

During the experimental evaluation, benchmark datasets containing
human-annotated ground-truth labels are used. The LLM-generated labels
are compared with these reference labels using classification metrics
such as accuracy, precision, recall, and F1-score.

### Definition of X and y

In the context of this thesis:

- **X** represents the input text that should be classified.
- **y** represents the expected ground-truth class label assigned to
  that text.
- **ŷ (y-hat)** represents the label predicted by the LLM.

In the example CSV files:

- `x_text` corresponds to **X**
- `y_label` corresponds to **y**

Therefore, one sample can be represented as:

(X, y)

Example for SST-2:

X = "A charming and beautifully acted film."
y = positive

Example for AG News:

X = "Microsoft announced a new artificial intelligence model for developers."
y = Sci/Tech

The objective of the experimental system is to produce a prediction ŷ
that matches the ground-truth label y as accurately and consistently as
possible.

## Example Data

Example (X, y) pairs are available in the `data/` directory:

- `data/sst2_examples.csv` – binary sentiment classification examples
- `data/ag_news_examples.csv` – four-class news topic classification examples