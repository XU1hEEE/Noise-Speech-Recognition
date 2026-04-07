# Noise-Robust-Digit-Recognition

**Group 3:** Marina (Yihe) Xu, Joseph Kung, Michelle Pan, Oliver Wang

This project trains a speech classification model to recognize spoken digits from audio recordings under clean and noisy conditions. Our final implementation uses a **BiLSTM classifier** with two alternative feature extraction pipelines:

1. **OpenSmile-based features** (**default**)
2. **Spectral subtraction + MFCC-based features**

Both methods performed well in our experiments. By default, the notebook runs with the **OpenSmile** feature pipeline, which gave slightly better results overall. We include both methods for completeness and to match our presentation/report.

---

## Repository Contents

- `Group3_FinalSubmission_Code.ipynb` — main notebook containing data loading, feature extraction, training, and evaluation
- `README.md` — instructions for setup and running the notebook

---

## Method Overview

### 1. OpenSmile Features (default)
This version uses:
- OpenSmile low-level descriptors with deltas
- Pre-emphasis
- Cepstral mean and variance normalization (CMVN)

Set:
```python
VERSION = 1
