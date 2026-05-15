# TG-TX-CellBender-Pipeline

CellBender preprocessing workflows for sorted and unsorted TG-TX single-cell RNA-seq datasets.

---

## Overview

This repository contains Colab-based CellBender preprocessing pipelines for:

- TG_TX_v44
- TG_TX_Sort_v44

The workflows include:

- Google Drive mounting
- Raw 10x matrix extraction
- CellBender installation
- Report patching for compatibility
- Background removal
- Output organization and export

---

## Environment

- Google Colab
- NVIDIA Tesla T4 GPU
- Python 3.12
- CellBender (Broad Institute)

---

## CellBender Parameters

```bash
cellbender remove-background \
    --expected-cells 5000 \
    --total-droplets-included 20000 \
    --epochs 150 \
    --fpr 0.01 \
    --cuda
```

---

## Repository Structure

```text
TG-TX-CellBender-Pipeline/
├── README.md
├── TG_TX_v44.ipynb
└── TG_TX_Sort_v44.ipynb
```

---

## Outputs

Generated outputs include:

- filtered h5 matrices
- posterior files
- HTML reports
- PDF summary plots
- Cell barcode CSVs
- metrics CSVs

---

## Notes

This workflow includes compatibility fixes for CellBender report generation under newer Python environments.
