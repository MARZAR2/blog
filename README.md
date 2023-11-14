
# BioWiC: An Evaluation Benchmark for Biomedical Concept Representation

## Introduction
Repository for the manuscript entitled "BioWiC: An Evaluation Benchmark for Biomedical Concept Representation".

In this manuscript, we present the BioWiC benchmark, a new dataset designed to assess the performance of both discriminative and generative language models in representing biomedical terms in context. 
BioWiC is formulated as binary classification task where each instance involves a pair of biomedical terms along with their corresponding sentences. 
The task is to classify each instance as True if the target terms carry the same meaning across both sentences or False if they do not.

## Table of Contents
- [Introduction](#introduction)
- [Getting Started](#getting-started)
- [Repository Structure](#repository-structure)
- [Installation](#installation)
- [Codes](#Codes)
- [BioWiC on Hugging Face](#hugging-face) 🤗
- [Contact](#contact)

## Getting Started
This section offers a guide on what you need to kick-start the project on your local machine, whether for development or testing purposes.

## Repository Structure
This repository is organized into several key sections:
- `UMLS`: Scripts for preprocessing Unified Medical Language System (UMLS) data, crucial to build the BioWiC dataset.
- `BioWiC_construction`: Scripts for assembling the BioWiC dataset.
- `data`: BioWiC splits, i.e., train set, validation set, and test set.
- `models`: Scripts for training and evaluating BioWiC baseline models.


## Installation
Follow these instructions to install the necessary dependencies for the project
```bash
git clone https://github.com/hrouhizadeh/BioWiC
cd BioWiC
pip install -r requirements.txt
```

## Codes
To reproduce construction of BioWiC, you need to perform the following steps:
1. Extracting UMLS information: In the `UMLS` directory, you will find the procedures to reproduce files containing UMLS information that are necessary for construction of the BioWiC dataset.
2. Building BioWiC dataset:  Follow the instructions in the `BioWiC_construction` directory to reconstruct the BioWiC dataset.
3. Train and evaluate models: The `models` folder contains scripts that enable you to train and assess various discriminative and generative large language models using the BioWiC dataset.

Additionally, the dataset is available for direct download in the `data` folder.



<a name="hugging-face"></a>
## Accessing BioWiC on Hugging Face 🤗

1. **Install the Hugging Face `datasets` Library:**
   If not already installed, you can add the `datasets` library from Hugging Face.
   ```bash
   pip install datasets
   ```

2. **Load the BioWiC Dataset:**
   To load the BioWiC dataset, execute the following Python code.
   ```python
   from datasets import load_dataset

   dataset = load_dataset("hrouhizadeh/BioWiC")
   ```
   This command will automatically download and cache the dataset.


## Contact
Should you have any inquiries, feel free to contact us at _hossein.rouhizadeh@unige.ch_.
