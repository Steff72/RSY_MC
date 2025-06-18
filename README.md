# 🎯 RSY Mini-Challenge FS25

This repository contains the solution to the RSY Mini-Challenge FS25, which focuses on the evaluation and comparison of various recommender systems using a movie rating dataset.

## 📦 Contents

- `RSY_MiniChallenge_FS25.ipynb`: Jupyter notebook containing all models, evaluations, visualizations, and conclusions.
- Multiple recommenders implemented and compared:
  - Random baseline
  - Global mean + user/item bias (Baseline)
  - User-/Item-based Collaborative Filtering (Cosine & Pearson)
  - Matrix Factorization (SVD with folding-in)
  - Neural Network Recommender
  - Diversity-aware SVD (re-ranking)
  - LLM-based (GPT-4) recommender — conceptually discussed

## 🧪 Evaluation

Each model is evaluated on a hold-out test set using:
- **RMSE**, **MAE**: For rating prediction accuracy
- **Precision@15**, **Recall@15**: For Top-N recommendation quality
  (now computed properly using ranked lists of unseen items)

A fair comparison is ensured using consistent masking and observed ratings per user.

## ⚙️ Requirements

- Python ≥ 3.8
- Jupyter Notebook
- `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `surprise`, `tensorflow` (for NN)
- `.env` file (see below)

## 🔐 OpenAI API (optional)

If you want to generate recommendations using the LLM-based (ChatGPT) recommender:

> Create a `.env` file in the root directory and add your API key:

```bash
OPENAI_API_KEY=your-api-key-here
```
