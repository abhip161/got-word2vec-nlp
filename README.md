
# Game of Thrones Word2Vec NLP Project

This project trains a **Word2Vec model on Game of Thrones text data** to learn semantic relationships between characters, locations, and concepts in the series.

The model learns vector embeddings for words and can capture relationships such as:

* `daenerys → khaleesi`
* `stark → winterfell`
* `jon → snow`

These embeddings allow us to perform **semantic similarity, word analogies, and character relationship analysis**.

---

## 📌 Features

* Text preprocessing using **NLTK**
* Tokenization and normalization of GOT scripts
* Training **Word2Vec (Skip-Gram)** model using **Gensim**
* Word similarity analysis
* Character relationship discovery
* Vector arithmetic with embeddings

---

## 📊 Example Results

```
model.wv.most_similar("daenerys")

stormborn   0.72
targaryen   0.68
princess    0.64
khaleesi    0.60
```

```
model.wv.most_similar("stark")

winterfell  0.59
eddard      0.58
benjen      0.55
```

---

## ⚙️ Tech Stack

* Python
* Gensim
* NLTK
* NumPy
* Matplotlib

---

## 📂 Dataset

The dataset consists of **Game of Thrones text files containing story content**.
Each file is processed to extract sentences which are then tokenized into words.

---

## 🧠 Model

Word2Vec model configuration:

```
vector_size = 200
window = 10
min_count = 1
epochs = 50
sg = 1 (Skip-Gram)
```

Skip-Gram is used because it performs better on **smaller datasets and rare words**.

---

## 📈 Example Usage

```
model.wv.most_similar("jon")
model.wv.similarity("stark","winterfell")
```

---

## 🚀 Future Improvements

* Phrase detection (`jon_snow`, `iron_throne`)
* Embedding visualization using **PCA / t-SNE**
* Character clustering
* Transformer embedding comparison

---
