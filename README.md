﻿# Anonymizer Lib Fetcher

This project captures execution times for different data anonymization techniques applied to a chosen dataset based on the specified payload parameter using a custom Anonymizer library.

## Introduction

The purpose of this project is to showcase the execution times of various data anonymization techniques applied to a given dataset using a custom Anonymizer library. The project supports three different payload configurations: 1, 2, and 3. Each payload configuration corresponds to a specific set of data anonymization techniques.

## Result Example

In this example, we use the dataset "1kB_100objects_dataset.json" and run the data anonymization process with different execution parameters.

Execution Parameters 1 Results:

| Propriedade              | Antes        | Depois      |
|--------------------------|--------------|-------------|
| k-anonymity              | 1.0          | 100.0       |
| l-diversity              | 1.0          | 8.0         |
| t-closeness (latitude)   | 4.907627     | 4.907627    |
| t-closeness (longitude)  | 13.131974    | 13.131974   |
| t-closeness (renda)      | 24024.258748 | 24024.258748|

Execution Parameters 2 Results:

| Propriedade              | Antes        | Depois      |
|--------------------------|--------------|-------------|
| k-anonymity              | 1.0          | 100.0       |
| l-diversity              | 1.0          | 8.0         |
| t-closeness (latitude)   | 4.907627     | 5.732671    |
| t-closeness (longitude)  | 13.131974    | 13.286883   |
| t-closeness (renda)      | 24024.258748 | 20725.841869|


Execution Parameters 3 Results:

| Propriedade              | Antes        | Depois      |
|--------------------------|--------------|-------------|
| k-anonymity              | 1.0          | 1.0         |
| l-diversity              | 1.0          | 1.0         |
| t-closeness (latitude)   | 4.907627     | 4.897002    |
| t-closeness (longitude)  | 13.131974    | 13.137886   |
| t-closeness (renda)      | 24024.258748 | 24024.247941|


## Usage

To use this project, follow these steps:

1. Configure ./src/settings.py:

```bash
  [...]
  RESULTS_PATH = "./tests/results/"
  [...]
```

2. On the root of the repository run:

```bash
  [...]
    python -m venv venv
    venv/scripts/activate
    python -m pip install --upgrade pip
    pip install -r requirements.txt

    python .\fecth_results.py -h
  [...]
```

3.1 .bat Execution:

```bash
  [...]
    .\fetch_results.bat
  [...]
```

3.2 Manual Execution:

```bash
  [...]
    python .\fecth_results.py -a ".\tests\datasets\1kB_100objects_dataset.json" -t 5 -p 1 
  [...]
```

