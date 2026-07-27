# MA-Thesis-WHO-repository-CU
This repository contains the custom computational pipeline and empirical analysis code accompanying the thesis investigating the World Health Organization's (WHO) crisis communication during the COVID-19 pandemic (2020–2023).

## Project Overview

To operationalise the dual-track framework—distinguishing between the technical track (scientific shielding, epidemiological metrics, clinical procedures) and the moral track (political-moral coordination, global solidarity, health equity)—this pipeline executes a hybrid approach:
1. **Dictionary-Based Regex Matching:** Computes word-boundary-safe frequency scores normalised per 10,000 words for technical keywords, moral keywords, and epistemic uncertainty diagnostics.
2. **Unsupervised Topic Modelling:** Implements `BERTopic` combined with `SentenceTransformers` (`all-MiniLM-L6-v2`) to capture semantic clusters and cross-validate dictionary findings across 1,390 institutional documents.
3. **Statistical Validation:** Automatically computes independent samples t-tests (p < 0.05) across pooled temporal, spatial, and audience categories to ensure observed variances reflect true structural shifts rather than random corpus noise.

## Repository Structure

analysis_script.py                 # Main Python execution pipeline
README.md                          # Project documentation
dataset                            # Local directory for PDF corpus ingestion
