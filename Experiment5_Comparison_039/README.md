# Experiment 5 — Deep Learning Lab Report

**CS3807 – Deep Learning Laboratory**
Comprehensive Study of CNN Training, Regularization, Optimization,
Hyperparameter Tuning, Transfer Learning and Cross-Validation

**Name:** Miruthula JMM
**Reg. No.:** 24011101039
**Class:** AI DS - A (Batch 2)
**Degree & Branch:** B.Tech Artificial Intelligence & Data Science, Semester V
**AY:** 2026–27

---

## Overview

This experiment uses **MobileNetV2** (ImageNet-pretrained) on the
**Oxford-IIIT Pet Dataset** (37 breeds, RGB, resized to 224×224) to
study the effect of:

- Weight initialization (Zero, Random, Xavier, He)
- Regularization (None, L2, Dropout, Batch Normalization)
- Optimizers (SGD, Momentum, RMSProp, Adam)
- CNN hyperparameters (learning rate, batch size, dropout rate)
- Transfer learning (feature extraction) vs. fine-tuning
- 5-fold cross-validation for final model selection

## Files in This Submission

| File | Description |
|---|---|
| `experiment5-dl.ipynb` | Executed Jupyter notebook with all code and outputs |
| `report.tex` | LaTeX source of the lab report |
| `report.pdf` | Compiled PDF report |
| `figures/` | All plots/images used in the report, extracted from the notebook |

## Dataset

- **Source:** Oxford-IIIT Pet Dataset (via `tensorflow_datasets`)
- **Split:** 3,312 training / 368 validation / 3,669 test images
- **Resolution:** 160×160 for exploratory sweeps (Sections 5–11), 224×224 for the final retrained model (Section 12)
- Test set was kept untouched until final evaluation, as required.

## Key Results Summary

| Stage | Best Configuration | Result |
|---|---|---|
| Initialization | He | 99.73% val. accuracy, most stable convergence |
| Regularization | Batch Normalization | Lowest val. loss, most stable curve |
| Optimizer | RMSProp | 100% val. accuracy, lowest final loss |
| Hyperparameters | lr=0.001, batch=16, dropout=0 | 100% val. accuracy |
| Transfer Learning | Fine-tuned (last block unfrozen) | Val. loss improved from 0.0011 → ~0.00048 |
| Cross-Validation | C1 (Best From Sweeps) | 97.93% ± 0.31% |
| **Final Test Evaluation** | **Retrained C1 @ 224×224** | **89.51% test accuracy**, F1 = 0.8949 |
