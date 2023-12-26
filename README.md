# Malware Analysis Dataset Exploration

## Overview

This repository contains a Jupyter Notebook (ExpoAnalysis_21pc06.ipynb) that explores a dataset related to system metrics and behavior, particularly in the context of malware analysis. The dataset comprises approximately 58,000 samples, categorized as "Benign," offering insights into normal system behavior. Various attributes cover diverse aspects such as processes, DLLs, handles, and more.

## Dataset Description

- **File:** Obfuscated-MalMem2022.csv
- **Attributes:** 
  - Categorical (e.g., 'Category', 'Class')
  - Numerical (e.g., 'pslist.nproc', 'dlllist.ndlls', 'handles.nhandles')
  - Others detailing processes, DLLs, handles, injections, services, and callbacks.

## Data Exploration

The Jupyter Notebook includes:

1. **Scatter Plots:** Visualizes relationships between attributes, aiding in understanding data distribution.
2. **Histograms:** Displays distributions of numerical attributes ('dlllist.ndlls', 'dlllist.avg_dlls_per_proc', 'handles.nhandles').
3. **Attribute Analysis:** Examines the spread and distribution of a specific numerical attribute ('pslist.avg_threads').
4. **Boxplot:** Illustrates the distribution of 'dlllist.avg_dlls_per_proc' using a boxplot.
5. **Supervised Scatter Plots:** Explores relationships between attributes and the class variable ('Class').

## Classification Challenge

- **Observations:**
  - Class imbalance, diverse numerical attributes, and feature-rich dataset.
  - Limited information from the last 3 attributes ('callbacks.ncallbacks', 'callbacks.nanonymous', 'callbacks.ngeneric') for classification.

- **Summary:**
  - Classification challenge demands a nuanced approach.
  - Potential techniques: Random Forests, Gradient Boosting, Support Vector Machines.
  - Gradient Boosting (e.g., XGBoost) identified as promising for its ability to handle complex relationships.

## Usage

1. **Setup:**
   - Ensure Python and necessary libraries (NumPy, Matplotlib, Pandas, Seaborn) are installed.
   - Jupyter Notebook: ExpoAnalysis_21pc06.ipynb.

2. **Data Loading:**
   - Use the provided dataset file 'Obfuscated-MalMem2022.csv'.

3. **Exploration:**
   - Execute notebook cells for visualization and analysis.

## Visualization Libraries

Explore alternative libraries for data visualization:
- Plotly
- Bokeh
- Altair
- ggplot
- Pygal
- Plotnine
- Holoviews

## Feature Selection Methods

Feature selection is crucial for model performance. Three main types:
1. **Filter Methods:** Statistical evaluation of feature relevance.
2. **Wrapper Methods:** Model-centric assessment using techniques like recursive feature elimination.
3. **Embedded Methods:** Integration into the model training process, e.g., L1 regularization, decision tree-based methods.
