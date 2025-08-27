# NVIDIA Stock Forecasting with Deep Learning & Sentiment Integration

This open-source project implements an **end-to-end reproducible machine learning pipeline** for **time series forecasting of NVIDIA stock prices**, combining deep learning sequence models, multi-lookback training, ensemble meta-modeling, and integration of **news sentiment via FinBERT**.  

The work was developed as a staged, multi-week pipeline culminating in a full **capstone system** with exogenous confidence scoring.

---

## 📂 Project Structure

The repository follows a week-by-week build-up:

- **Week 1 – Repository & EDA Foundations**  
  - Repository hygiene, README/LICENSE/CITATION setup  
  - Exploratory Data Analysis (EDA) and feature engineering notebooks  

- **Week 2 – Ethical & Licensing Foundations**  
  - Open-source software compliance and citation practices  
  - Instructor notes on licenses (Apache 2.0, CC0)  

- **Week 3 – Sequential Modeling Foundations**  
  - Literature review: RNNs, LSTMs, Attention  
  - Simple Attention notebooks for 1D and 365D lookbacks  
  - Instructor lecture notes and slides on RNN/Attention  

- **Week 4 – Multi-Lookback Base Models**  
  - Training Conv1D + BiGRU + Attention models across multiple lookbacks (14D–365D)  
  - Exploration of *Attention is All You Need*  

- **Week 5 – Meta-Model Ensembling**  
  - Ridge regression meta-model stacking base lookback predictions  
  - Ensemble learning slides  

- **Week 6 – Sentiment Integration with FinBERT**  
  - Extension of the meta-model pipeline with **NewsAPI + FinBERT sentiment**  
  - Logging predictions with appended sentiment confidence  

- **Week 7 – Capstone End-to-End Pipeline**  
  - Eight lookback base models (365D → 1D) trained and ensembled  
  - Strict artifact structure with timestamped runs  
  - Pluggable **Exogenous Confidence API** for sentiment/macro signals  

- **Week 7.5 – Final Presentation**  
  - 10-minute recorded presentation explaining design choices, reproducibility, and ethical considerations  

---

## 📊 Data

- **NVIDIA Stock Dataset**  
  - Source: [Kaggle – Adil Shamim](https://www.kaggle.com/datasets/adilshamim8/nvidia-stock-market-history)  
  - License: [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)  
  - Notes: Public domain dataset, used for supervised forecasting with sliding windows.  

---

## 🤖 Models

- **Base Models**: TensorFlow Sequential models with BiGRU, Conv1D, and Attention layers (varied by lookback).  
- **Meta-Model**: Ridge regression (baseline), with support for Lasso/ElasticNet and optional tree ensembles.  
- **Sentiment Model**: FinBERT (ProsusAI) — BERT fine-tuned for financial sentiment.  

---

## 🔑 Key Features

- Multi-lookback design (1D, 14D, 30D, 60D, 90D, 180D, 270D, 365D)  
- Strict artifact saving conventions with timestamped runs  
- Ensemble meta-model with feature order contracts  
- Exogenous sentiment integration (NewsAPI + FinBERT)  
- Confidence labeling (STRONG / NEUTRAL / WEAK) based on sentiment scores  
- End-to-end reproducibility across Google Colab + Drive  

---

## 📜 License

This project’s original code is released under the **Apache 2.0 License**.  
Third-party components are included under their respective licenses:  

- NVIDIA Stock Dataset — [CC0 1.0 Universal](https://creativecommons.org/publicdomain/zero/1.0/)  
- FinBERT — [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)  

See [LICENSE.txt](./License.txt) and [CITATION.cff](./CITATION.cff) for details.  

---

## ✍️ Citation

If you use this project, please cite:

- Shamim, Adil. *NVIDIA Stock Dataset*. Kaggle. CC0 1.0 Universal.  
- Araci, Dogu & Genc, Zulkuf. *FinBERT*. ProsusAI. Apache License 2.0.  
- Hill, Patrick. *NVIDIA Stock Forecasting with FinBERT* (Capstone Project, 2025).  
