This repository contains the data, scripts, and evaluation outputs used to compare energy-efficiency patterns between human (Stack Overflow) and AI-generated code.

## CSV Files

### **1. DL_Energy_Patterns.csv**

This file contains the raw curated dataset used in the study. It includes:

* Stack Overflow questions and other metadata
* Accepted human answers
* Corresponding ChatGPT-generated responses

This file forms the primary input for all analyses conducted in this work.

### **2. developer_survey.csv**

This file contains the developer survey results collected by the authors who originally released the curated Stack Overflow dataset. The survey includes responses from deep-learning practitioners regarding the usefulness and applicability of the dataset.

---

## Folders

### **1. prompt_refinement/**

Contains all the prompt versions and refinements explored during the study. These prompts were used to compare the human and AI responses.

### **2. analysis_script/**

Contains the scripts used to evaluate human and AI code using the final prompt.
This folder includes:

* Python scripts for three models: **Cohere**, **ChatGPT**, and **Gemini**
* API-based evaluation scripts for Cohere and Gemini
* A script for processing ChatGPT’s JSON-formatted output (from a shared conversation link) into a structured CSV format

These scripts take both Stack Overflow and AI answers as input and generate model-specific evaluation outputs.

### **3. evaluation_sheet/**

Contains the evaluation results produced by the analysis scripts.
This includes the results from the comparative evaluation of AI and Human code as evaluated by ChatGPT and Gemini

Each sheet summarizes the model’s judgments on the energy-efficiency patterns for each question–answer pair, along with numerical scores for the finalized patterns.

### **4. statistical_results/**

Contains the statistical analyses performed on the evaluation outputs.
This includes correlation tests and significance analyses to understand the agreement between the models (e.g., ChatGPT vs. Gemini).

---
