# TinyBayes
# Closed-Form Bayesian Inference via Jacobi Prior for Real-Time Image Classification on Edge Devices
#---------------------------------------------------------------------------------------------------

## Overview

This repository implements the **Jacobi-DMR classifier**, a closed-form Bayesian classification framework designed for **real-time, low-resource edge deployment**.

Unlike conventional deep learning pipelines, Jacobi-DMR:

* Requires **no iterative training**
* Uses a **closed-form posterior update**
* Achieves **fast CPU inference**
* Maintains competitive accuracy with minimal compute

---

## Key Contributions

* **Closed-form Bayesian classifier** using Jacobi prior
* Eliminates gradient-based training loops
* Extremely lightweight (<10MB total pipeline)
* Fast inference (~150 ms/image on CPU)
* Robust performance across hyperparameter settings

---

## Repository Structure

```
jacobi-dmr-classifier/
│
├── src/                # Core implementation
├── notebooks/          # Experiments and validation
├── data/               # Dataset instructions (no raw data)
├── results/            # Sample outputs and evaluation
├── paper/              # Research paper PDF
│
├── README.md
├── requirements.txt
├── LICENSE
└── .gitignore
```

---

## Installation

Clone the repository:

```bash
git clone https://github.com/shouvik-sardar/TinyBayes.git
cd TinyBayes
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

##  Usage

### Run the pipeline


### Using the notebook

Open:

```
notebooks/TinyBayes-Closed-Form Bayesian Inference via Jacobi Prior for Real-Time Image Classification on Edge Devices.ipynb
```

This notebook includes:

* Data preprocessing
* Feature extraction
* Jacobi posterior computation
* Classification and evaluation

NOTE: You must change the cell 1 for relevant Google Drive locations. under Step 1: Mount Google Drive, Set paths, Install libraries starting from "#Define paths"

---

## Method Summary

The Jacobi-DMR classifier applies a **Jacobi prior** to derive a **closed-form posterior estimate** for classification.

For a binary response:

[
\log \left( \frac{y + a}{1 + \frac{k}{b}} \right)
]

This formulation enables:

* Analytical computation of class scores
* Stability under sparse observations
* Independence from iterative optimization

---

## Results

| Model      | Accuracy | Inference Time |
| ---------- | -------- | -------------- |
| Jacobi-DMR | 78.7%    | ~150 ms/image  |

Dataset: Amini Cocoa Contamination Challenge

---

## Data

⚠️ Raw datasets are **not included**.

To reproduce results:

1. Obtain dataset from the original source and unzip it. 
2. Place folder "dataset" as per the BASE_DIR in cell 1. 
3. create a empty folder "val" as per IMAGE_DIR_VAL. 
4. Follow preprocessing steps in notebook

---

## Reproducibility

* All experiments are contained in the notebook
* Results can be reproduced using:

  * Provided pipeline
  * Fixed random seeds
  * Defined preprocessing steps
  * Expect slight variation in runtime since it's a new session 

---

## Paper

The full paper is available in:

```
arxiv link will be shared soon. 
```

---

## Citation

will be shared when the arxiv version is shared 
---

## License

This project is licensed under the MIT License.

---

## Notes

* This repository focuses on the **final inference pipeline**
* Experimental models (e.g., deep learning baselines) are not required for core reproduction
* Designed for **clarity, reproducibility, and edge deployment**

---

## Future Work

* Large-rate regime extension of Jacobi-DMR
* Integration with much more lightweight feature extractors
* Deployment on embedded hardware 

---
