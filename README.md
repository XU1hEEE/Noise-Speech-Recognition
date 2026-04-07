# Enhancing Noise Robustness in Spoken Digit Recognition



**Group 3:**  Yihe Xu, Michelle Pan, Joseph Kung, Oliver Wang  

This project studies **noise-robust spoken digit recognition** using deep learning and speech feature engineering. We classify spoken digits from **0–9** using an **LSTM-based classifier**, and compare multiple feature extraction and preprocessing strategies under **clean**, **10 dB noisy**, and **5 dB noisy** conditions.

Our final work explores two main approaches:

1. **Spectral subtraction + pre-emphasis + MFCC-based features**
2. **OpenSmile low-level descriptors (LLDs) + deltas + pre-emphasis + CMVN**

Among the methods we tested, the **OpenSmile IS11 LLD delta pipeline** achieved the best overall performance, while the **spectral subtraction → pre-emphasis** pipeline also produced strong results and offered useful insight into how preprocessing order affects noise robustness.

---

## Files

- `Group3_FinalSubmission_Code.ipynb` — main notebook for training and evaluation
- `README.md` — instructions for setup and running the code

---

## Project Overview

Spoken digit recognition is a classic speech processing task with applications such as automated phone systems and constrained-vocabulary speech interfaces. A major challenge is maintaining good recognition accuracy when speech is corrupted by background noise.

In this project, we trained a classifier on clean spoken digit recordings and evaluated it on:
- clean speech
- speech corrupted by babble noise at **10 dB SNR**
- speech corrupted by babble noise at **5 dB SNR**

We compared standard MFCC-based processing against two more noise-robust feature pipelines.

---

## Dataset

We use the **Free Spoken Digit Dataset (FSDD)**, which contains spoken digits from 0 to 9 recorded by multiple speakers.

The notebook expects the dataset to be organized as:

```text
M214_project_data/
├── train_clean/
├── test_clean/
├── test_snr_5db_babble/
└── test_snr_10db_babble/
