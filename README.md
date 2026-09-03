# Experimental Results for LLMs on Kattis Programming Problems

This repository contains the experimental data used to evaluate recent Large Language Models (LLMs) on competitive programming problems from the [Kattis](https://open.kattis.com/) platform.

The dataset contains **60 existing Kattis problems**, divided into two groups according to their Kattis difficulty values:

- **G1**: 30 easier problems, with difficulty values between **1.3 and 1.9**.
- **G5**: 30 more difficult problems, with difficulty values between **5.1 and 7.6**.

The experiments compare the following seven models:

- ChatGPT-4o
- ChatGPT-o3
- ChatGPT-5
- Gemini-2.5-Flash
- Grok-3
- DeepSeek-V3
- DeepThink-R1

## File

The file contains the selected Kattis problems and the results obtained by the evaluated models.

The workbook includes information such as:

- problem number;
- source;
- problem name;
- Kattis problem ID;
- difficulty value;
- link to the problem;
- additional notes where available;
- evaluation results for each model.

For each evaluated model, the spreadsheet records three main fields:

- **Accepted** — indicates whether the submitted solution was fully accepted by Kattis;
- **Results** — the score reported by Kattis in the form `x/y`;
- **Score** — the normalized percentage score used in the analysis.

A score of **100** represents a fully accepted solution, a score between **0 and 100** represents a partial result, and a score of **0** represents a solution that received no points.

## Experimental protocol

All models were evaluated using the same set of programming problems and the same general request structure. Solutions were generated in C/C++ and evaluated using the Kattis online judge.

Each problem was tested in a new conversation using the default settings available in the web interface of each model. The model first generated one solution for the problem. An additional attempt was allowed only when the initial solution produced a compilation error. No judge feedback about wrong answers, failed test cases, execution time, or partial scores was used to improve a solution.

## Purpose of the dataset

The dataset can be used to reproduce or further analyze the descriptive and statistical results reported in the associated study, including:

- mean and median scores;
- standard deviations;
- acceptance and partial-result counts;
- comparisons between the G1 and G5 groups;
- correlations between Kattis difficulty and model score;
- statistical comparisons between the evaluated models.

## Notes

Kattis difficulty values are dynamic and may change over time. The values included in this dataset correspond to those observed when the problems were selected for the experiments.

The selected problems are publicly available on Kattis. Their inclusion in the training data of the evaluated models cannot be determined from this dataset.

## Citation

If you use this dataset, please cite the associated paper:

**Mirel Cosulschi, Mihai Gabroveanu, and Florin Slabu. _Exploring the limits of recent LLM reasoning on competitive programming tasks_. AIMSA 2026.**

