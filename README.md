AI vs Human Code Energy-Efficiency Evaluation

This repository contains all resources, scripts, and evaluation data for analyzing and comparing energy-efficiency patterns in code solutions authored by human developers (Stack Overflow) and AI models (ChatGPT, Gemini).
The project uses a structured evaluation framework based on 8 core deep-learning energy-efficiency patterns, with a scoring system from 1–5 for each pattern.

📂 Repository Structure

The repository contains 7 main items:

1. README.md

This documentation file (the one you are reading).
It explains the repository’s structure, purpose, usage, and methodology.

2. AnalysisScript/

A directory containing the Python analysis scripts used to:

Parse human-written and AI-generated code

Detect energy-efficiency–related patterns

Apply the 1–5 scoring rubric across 8 dimensions

Generate structured outputs per sample

Support reproducibility for all analysis experiments

This directory includes the core evaluation logic for the entire study.

3. EvaluationSheet/

This directory contains:

The final aggregated scores for every question–answer pair

Separate evaluation results from ChatGPT and Gemini

Metadata about which model assigned which score

The merged analysis-ready dataset

These sheets represent the final, post-analysis scoring outcome.

4. Data_AI.csv

This CSV file contains:

All AI-generated code solutions

Question IDs

Preprocessing metadata

Any notes captured before scoring

Useful if you want to trace how the AI response for each question was evaluated.

5. Data_Human.csv

This CSV file contains:

All human-generated (Stack Overflow) code solutions

Question IDs and mapping to the accepted answers

Pre-cleaning and preprocessing details

This parallels the AI dataset to support reproducible, paired comparison.

6. RawCode/

Directory containing the raw code snippets before any preprocessing:

Unmodified AI-generated code

Original Stack Overflow answers

Helpful for auditability and replication

7. ProcessedCode/

Directory containing cleaned, normalized versions of all code snippets:

Whitespace normalized

Comments removed (where needed)

Standard formatting applied

These are the versions fed into the scoring pipeline.

🧪 Evaluation Methodology

The project uses an 8-pattern scoring framework.
Each code sample is evaluated on:

Compute Minimization

Memory Optimization

Model Size Efficiency

Tensor Operation Efficiency

Data Pipeline Efficiency

Execution-Time Efficiency

Hardware-Aware Optimization

Redundancy & Overhead Reduction

Each dimension is scored 1 (poor) to 5 (excellent) by two LLM-based evaluators:

ChatGPT

Gemini

Final results are aggregated in the EvaluationSheet/ folder.

▶️ How to Run the Analysis

Place all raw human and AI code in RawCode/.

Run AnalysisScript/main.py
(or whichever script serves as the entry point).

Processed code will be saved in ProcessedCode/.

Generated scores will appear in EvaluationSheet/.

📈 Results & Insights

The evaluations support higher-level research questions such as:

When does AI generate more energy-efficient code?

In which cases do humans outperform AI?

How do different models (ChatGPT vs Gemini) assess the same code?

These insights contribute to ongoing research in sustainable software engineering.
