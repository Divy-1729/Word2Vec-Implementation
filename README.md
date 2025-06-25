# Word2Vec on Radiohead's "Let Down"

A playful, from-scratch implementation of Word2Vec using the lyrics of Radiohead’s *Let Down* as a tiny corpus.

---

## 🎸 What is this?

This notebook demonstrates how to build a simple neural network that learns word relationships from a real song. It covers:

- **Tokenization**: Splitting the lyrics into unique lowercase words.
- **Vocabulary mapping**: Creating fast lookup tables for words and their IDs.
- **One-hot encoding**: Representing words as vectors.
- **Context window**: Pairing each word with its neighbors for training.
- **Neural net**: A 2-layer model with softmax and cross-entropy loss.
- **Training loop**: Learning to predict context words.
- **Prediction**: Given a word, see which words the model thinks are most related.

---

## 📝 Example Usage
**
One-hot encode a word**
```
idx = letdown_to_id["transport"]
one_hot_vec = one_hot_encode(idx, len(letdown_to_id)).reshape(1, -1)
```
**Predict context words**
```
result = forward(model, one_hot_vec, return_cache=False)
for idx in np.argsort(result)[::-1]:
print(id_to_letdown[idx])
```

---

## 🚀 How to Run

1. Install Python 3 and NumPy.
2. Open the notebook (`word2vec.ipynb`) in Jupyter or Kaggle.
3. Run all cells, following the comments and markdown for explanations.

---

## 🧠 What You'll Learn

- How word embeddings work at a basic level
- How to implement a neural network with only NumPy
- The basics of natural language processing (NLP) with a fun dataset

---

## 📚 Credits

- Lyrics: Radiohead, "Let Down"
- Inspired by [Word2Vec (Mikolov et al., 2013)](https://arxiv.org/abs/1301.3781)

---

*Let down and hanging around...*
