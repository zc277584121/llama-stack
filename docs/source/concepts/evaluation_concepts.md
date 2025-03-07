# Evaluation Concepts

The Llama Stack Evaluation flow allows you to run evaluations on your GenAI application datasets or pre-registered benchmarks.

We introduce a set of APIs in Llama Stack for supporting running evaluations of LLM applications.
- `/datasetio` + `/datasets` API
- `/scoring` + `/scoring_functions` API
- `/eval` + `/benchmarks` API

This guide goes over the sets of APIs and developer experience flow of using Llama Stack to run evaluations for different use cases. Checkout our Colab notebook on working examples with evaluations [here](https://colab.research.google.com/drive/10CHyykee9j2OigaIcRv47BKG9mrNm0tJ?usp=sharing).


## Evaluation Concepts

The Evaluation APIs are associated with a set of Resources as shown in the following diagram. Please visit the Resources section in our [Core Concepts](../concepts/index.md) guide for better high-level understanding.

![Eval Concepts](../references/evals_reference/resources/eval-concept.png)

- **DatasetIO**: defines interface with datasets and data loaders.
  - Associated with `Dataset` resource.
- **Scoring**: evaluate outputs of the system.
  - Associated with `ScoringFunction` resource. We provide a suite of out-of-the box scoring functions and also the ability for you to add custom evaluators. These scoring functions are the core part of defining an evaluation task to output evaluation metrics.
- **Eval**: generate outputs (via Inference or Agents) and perform scoring.
  - Associated with `Benchmark` resource.


## What's Next?

- Check out our Colab notebook on working examples with running benchmark evaluations [here](https://colab.research.google.com/github/meta-llama/llama-stack/blob/main/docs/notebooks/Llama_Stack_Benchmark_Evals.ipynb#scrollTo=mxLCsP4MvFqP).
- Check out our [Building Applications - Evaluation](../building_applications/evals.md) guide for more details on how to use the Evaluation APIs to evaluate your applications.
- Check out our [Evaluation Reference](../references/evals_reference/index.md) for more details on the APIs.
