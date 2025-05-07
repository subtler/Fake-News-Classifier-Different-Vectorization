# 📰 Fake News Classifier (BoW, TF-IDF, Word Embeddings)

This NLP project classifies news articles as **Real** or **Fake** using three powerful vectorization techniques:  
**Bag of Words**, **TF-IDF**, and **Word2Vec**. It demonstrates the evolution from basic count-based methods to semantic-aware embeddings.

---

## 🚀 Project Structure

FakeNewsClassifier/
├── data/
│   ├── Fake.csv
│   └── True.csv
├── notebooks/
│   ├── 1_BoW_FakeNews.ipynb
│   ├── 2_TFIDF_FakeNews.ipynb
│   └── 3_Embeddings_FakeNews.ipynb
├── models/
│   └── (optional: saved models)
├── utils/
│   └── preprocessing.py (optional)
├── README.md

---

## 📂 Dataset

- **Source**: [Fake and Real News Dataset on Kaggle](https://www.kaggle.com/datasets/clmentbisaillon/fake-and-real-news-dataset)
- Combined and cleaned `Fake.csv` and `True.csv`
- Removed duplicates and retained only the `text` and `label` columns

---

## 🧪 Model Comparison Results

| Vectorization | Accuracy | F1 Score (Real / Fake) | Notes |
|---------------|----------|------------------------|-------|
| **BoW**       | **99.47%** | 1.00 / 0.99 | Best overall performer |
| **TF-IDF**    | 98.70%   | 0.99 / 0.99 | Slightly lower, but robust |
| **Word2Vec**  | 97.89%   | 0.98 / 0.98 | Captures semantic relationships |

✔️ All models used **Logistic Regression**  
✔️ All preprocessing: lowercasing, punctuation removal, stop words  
❌ No deep learning — yet powerful results!

---

## 📊 Embedding Visualization

Used **t-SNE** to visualize Word2Vec embeddings of top 300 frequent terms. Similar words cluster close together (e.g., politics, economy, war).

---

## 🔧 Installation

pip install -r requirements.txt