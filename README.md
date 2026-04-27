# IEA-SCALE Educational Implementation (Three-Tower Weak-Signal Intelligence)

This repository provides supplementary educational material inspired by the IEA-SCALE architecture described in Case 2 (“Democratizing Foresight for SME Networks: the IEA-SCALE Model”).

It is designed to support teaching, reproducibility, and conceptual understanding of AI-augmented weak signal interpretation, without exposing any proprietary or production-level implementation.

---

## What this repository is

This repository contains a minimal, didactic pipeline that transforms a small set of documents into a structured, multi-level output inspired by the SCALE “three-tower” logic:

- **Tower 1:** a concise strategic insight
- **Tower 2:** thematic contexts and intermediate interpretation
- **Tower 3:** traceable evidence fragments with source metadata

The goal is to illustrate how weak-signal interpretation can be structured in a transparent, reproducible, and human-centered way.

---

## What this repository is not

This repository is intentionally limited in scope:

- It is **not** the production IEA-SCALE system
- It is **not** a deployable product: no database, no scraping infrastructure, no private prompts
- It does **not** claim full automation

In line with the conceptual foundation of SCALE, weak-signal meaning does not emerge automatically from data, but through the interaction between human interpretation and AI-supported structuring.

---

## Software environment and dependencies

To run the examples locally, the following environment is recommended:

- Python 3.10 or higher
- pip package manager

Install dependencies with:

```bash
pip install -r requirements.txt
```

Main libraries used:

- sentence-transformers
- scikit-learn
- numpy
- pandas

Optional libraries, only if the reader wants to connect real LLMs instead of the offline stub:

- openai
- google-generativeai

---

## Quick start

1. Install Python 3.10 or higher.

2. Create a virtual environment, if desired.

3. Install dependencies:

```bash
pip install -r requirements.txt
```

4. Run the demo pipeline:

```bash
python -m src.pipeline --input data/sample_docs --out out
```

The default configuration uses a stub LLM, so the pipeline runs offline without requiring API keys.

If a reader wants to connect a real LLM provider, they can set environment variables such as:

```bash
LLM_PROVIDER=...
LLM_API_KEY=...
```

and adjust the configuration in `src/llm.py`.

---

## Reproducing the results presented in the chapter

To reproduce the simplified workflow described in the chapter:

1. Clone or download this repository.
2. Install the dependencies listed above.
3. Run the demo pipeline.
4. Inspect the generated outputs.

The outputs will be saved in:

- `out/tower1.md` → strategic insight
- `out/tower2.md` → thematic contexts
- `out/tower3.json` → evidence fragments with traceability

These outputs follow the same conceptual structure presented in the chapter. They are intended to reproduce the logic of the educational workflow, not the production SCALE system.

Results may vary depending on:

- input documents
- model configuration
- parameter choices
- API provider, if an external LLM is used

---

## Data sources

The examples in the chapter and this repository are inspired by open-access weak-signal datasets, particularly:

**European Commission – Joint Research Centre (JRC)**  
**Weak signals in Science and Technologies (2024)**

Repository:  
https://publications.jrc.ec.europa.eu/repository/handle/JRC140959

The JRC dataset includes weak signals identified through:

- text mining
- clustering
- scientometric indicators
- Scopus publications
- PATSTAT patent data

Additionally, this repository includes a small set of sample documents for demonstration purposes:

```text
data/sample_docs/
```

These files are illustrative only and are not intended to replicate the full dataset.

---

## Outputs

Running the pipeline generates:

- `out/tower1.md`
- `out/tower2.md`
- `out/tower3.json`

These outputs demonstrate how weak signals can be structured into layered, traceable insights.

---

## How to cite

If you use this material:

- Please cite the associated Springer book chapter.
- You may also cite this repository using its URL or release version.
- A `CITATION.cff` file is included for convenience.

---

## License

MIT License, for educational use.  
See the LICENSE file for details.

---

## Contact

IEA Future Lab / UFRGS  
For academic inquiries and collaboration.
