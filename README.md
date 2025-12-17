# 🚀 Text Generation with RNN, GRU & Mini‑GPT (Transformer)

> **An end‑to‑end NLP project that builds, analyzes, and compares classic sequence models (RNN, LSTM, GRU) with a Transformer‑based Mini‑GPT for word‑level text generation.**

This project is designed to **show real engineering maturity**:

* handling large text datasets safely
* understanding *why* certain models fail
* and upgrading to better architectures for the right reasons

---

## 📌 Project Motivation

Text generation looks simple on the surface, but different deep learning models behave **very differently** when generating language.

This project answers three important questions:

1. ❓ *Can RNNs really generate meaningful long text?*
2. ❓ *Do GRU/LSTM fix repetition and semantic drift?*
3. ❓ *Why do Transformers (GPT‑style models) work so much better?*

Instead of jumping straight to Transformers, this project **intentionally starts with RNNs**, hits their limits, and then **moves to a Mini‑GPT**.

---

## 🧠 Models Implemented

### 1️⃣ RNN / LSTM (Baseline)

* Word‑level language model
* Next‑word prediction
* Demonstrates:

  * repetition issues
  * short‑term coherence
  * loss of meaning over long sequences

### 2️⃣ GRU (Improved RNN)

* Fewer parameters than LSTM
* Faster convergence
* Reduced repetition
* Still suffers from **semantic drift**

### 3️⃣ Mini‑GPT (Transformer) ⭐

* Decoder‑only Transformer
* Masked multi‑head self‑attention
* Positional embeddings
* Maintains topic coherence
* Produces **significantly cleaner text**

---

## 🧩 Key Learning Outcome (IMPORTANT)

> This project proves that **text generation quality is limited by model architecture, not training tricks**.

Even with:

* more data
* more epochs
* sampling tricks

RNN/GRU models hit a **theoretical ceiling**.

Transformers break that ceiling using **self‑attention**.

---

## 📂 Project Structure

```text
text_generation_rnn/
│
├── dataset/
│   ├── raw/                # original text (ignored in git)
│   └── processed/          # tokenized & sequence data (ignored in git)
│
├── models/                 # trained models (ignored in git)
│
├── src/
│   ├── preprocess.py       # dataset preprocessing
│   ├── train_rnn.py        # RNN / LSTM training
│   ├── train_gru.py        # GRU training
│   └── train_transformer.py# Mini‑GPT training
│
├── .gitignore
└── README.md
```

> ⚠️ Large datasets and trained weights are intentionally excluded from GitHub.

---

## 📊 Dataset

* **Source:** Wikipedia text corpus (Kaggle)
* **Type:** Plain text
* **Learning style:** Self‑supervised

### Preprocessing Highlights

* Word‑level tokenization
* Vocabulary limited to **20,000 words**
* Sliding window sequences
* Memory‑safe chunk loading (Colab friendly)

---

## ⚙️ Training Setup

| Component       | Value                           |
| --------------- | ------------------------------- |
| Vocabulary      | 20,000                          |
| Sequence length | 10–20                           |
| Batch size      | 128                             |
| Optimizer       | Adam                            |
| Loss            | Sparse Categorical Crossentropy |
| Platform        | Google Colab (GPU)              |

---

## ✨ Sample Outputs

### ❌ RNN / GRU Output (Expected Limitation)

```
deep learning is a field of artificial intelligence that the university of the journal of the prize of the university of
```

### ✅ Mini‑GPT Output

```
deep learning is a field of artificial intelligence that enables systems to learn from data and improve performance without explicit programming
```

---

## 🔍 Why Transformers Win

| Aspect             | RNN / GRU | Transformer |
| ------------------ | --------- | ----------- |
| Long‑range context | ❌         | ✅           |
| Repetition control | ❌         | ✅           |
| Topic coherence    | ❌         | ✅           |
| Parallelism        | ❌         | ✅           |

---

## 🛠️ Technologies Used

* **Python**
* **TensorFlow / Keras**
* **NumPy**
* **Google Colab (GPU)**
* **Git & GitHub**

---

## 🧪 How to Run (Quick Start)

```bash
pip install tensorflow numpy
```

1. Add your text file to `dataset/raw/`
2. Run preprocessing
3. Train model of choice
4. Generate text from a seed prompt

---

## 🧠 What This Project Demonstrates

# ✔ Deep understanding of NLP pipelines
# ✔ Memory‑aware dataset handling
# ✔ Model comparison & failure analysis
# ✔ Correct use of Transformers
# ✔ End‑to‑end ML engineering workflow

---


## 🚀 Future Work

* SentencePiece / BPE tokenization
* Character‑level vs subword comparison
* Fine‑tuning pre‑trained GPT models
* Web demo using Streamlit

---

## 🙌 Final Note

This project was intentionally built **the hard way** — starting from RNNs — to truly understand *why* modern NLP uses Transformers.

