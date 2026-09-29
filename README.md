# LLM Text Annotation Thesis

Repository for the Master's thesis project:

**Automatic Labeling of Text Data Using Large Language Models**

## Project goal

The project investigates whether Large Language Models (LLMs) can be used as automatic annotators for text classification tasks.

The workflow is:

1. Load a labeled text dataset.
2. Take an input text `X`.
3. Create a classification prompt.
4. Send the prompt to an LLM.
5. Receive the predicted label `ŷ`.
6. Compare `ŷ` with the ground-truth label `y`.
7. Evaluate the results using metrics such as accuracy, precision, recall, and F1-score.
8. Analyze errors and compare model behavior.

The thesis experiments use benchmark text-classification datasets such as **SST-2** and **AG News** and compare multiple LLMs under the same evaluation setup.
