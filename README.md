# EEG Motor Imagery Classification

A notebook to explore, preprocess, and train classification models on EEG data from 10 patients of the [EEG Motor Movement/Imagery Dataset (eegmmidb 1.0.0)](https://physionet.org/content/eegmmidb/1.0.0/).

## Dataset

The data used on this notebook is automatically installed during the notebook execution.
[Eegmidb](https://www.physionet.org/content/eegmmidb/1.0.0/)

## Setup

1. Create a virtual environment and activate it:

```bash
python -m venv .venv

# Windows
.venv\Scripts\activate

# Linux/Mac
source .venv/bin/activate
```

2. Install the dependencies:

```bash
pip install -r requirements.txt
```

3. Run the notebook:

````bash
jupyter notebook
```
or running with vscode

## What the notebook does

- Loads and preprocesses raw EEG data from 10 subjects
- Extracts epochs for motor imagery events (T1, T2), discarding rest (T0)
- Trains and evaluates multiple classifiers using Leave-One-Subject-Out cross validation:
  - Random Forest
  - Gaussian Naive Bayes
  - SVM
- Plots confusion matrices for each model
````
