# Current Topics for Student Assistants

## Machine Unlearning

Machine unlearning is a growing area of research that focuses on how to effectively remove the influence of specific data points from a model that has already been trained. Instead of retraining a model from scratch, which can be computationally expensive and time-consuming, machine unlearning aims to “forget” selected pieces of data in a more efficient way while preserving the overall performance of the model.
This is particularly important in contexts where data must be removed after training, such as complying with privacy regulations (e.g., a user requesting deletion of their data), filtering out spam or corrupted inputs, or eliminating harmful, biased, or outdated information that may negatively affect model behavior.
Our current work specifically explores efficient and approximate approaches to machine unlearning in recommender systems. Since these systems often operate on large-scale, continuously evolving datasets, exact retraining is often impractical. Instead, we investigate methods that can approximate the removal of data influence with minimal computational overhead, while still maintaining high-quality recommendations and system stability.


---

## Task-Aware Data Validation

Task-aware data validation focuses on detecting data errors that actually matter for how the data is used. Instead of treating validation as purely statistical anomaly detection, which can flag harmless irregularities while missing errors that degrade downstream performance, task-aware data validation aims to ground error detection in the tasks that consume the data, making validation outcomes more actionable and less noisy.

Our current work specifically explores **LLM-based approaches** to task-aware data validation, using large language models to reason about data in context and identify errors with likely downstream consequences. On the core research side, we build pipelines that analyze downstream task code to automatically extract the data assumptions it depends on, and curate benchmark datasets that make it possible to systematically evaluate and compare validation methods. This project is inherently interdisciplinary, drawing on LLMs for code understanding, natural-language-to-query translation, and data validation.

Within this project, the student research assistant can contribute to one of several directions, and the exact focus can be adapted to the student's interests and background:

- **Automated error injection.** Develop methods for injecting meaningful data errors that simulate realistic failure cases — for instance, implementing and extending a library of error-injection operators covering modes such as value perturbations, schema drift, label noise, and plausible-but-wrong values, and building evaluation harnesses that measure how well existing validation methods catch these injected errors.
- **Downstream task curation.** Curate realistic downstream tasks whose code contains data assumptions, which serve as test cases for the assumption-extraction pipelines and as ingredients for the benchmarks.
