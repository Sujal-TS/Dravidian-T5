# 🌐 Dravidian-T5: A Neural Machine Translation Approach for Dravidian Languages

Dravidian-T5 is a multilingual NMT model fine-tuned for low-resource Dravidian languages (Kannada, Tamil, Telugu, Malayalam). It is built using a **pivot-based data augmentation framework** and a compressed, language-specific version of **mT5**. This project also introduces **DraPara**, a 100k parallel corpus, and a lightweight translation model for inclusive NLP.

---

## 📌 Highlights

- 🔁 Pivot-based augmentation using English as an intermediary
- 🔤 Multilingual translation for 4 Dravidian languages
- 🧠 Dravidian-specific T5 model (~20% smaller than original mT5)
- 📂 Dataset & Model available on Hugging Face

---

## 🧠 Abstract

Neural Machine Translation (NMT) in low-resource settings struggles due to lack of high-quality parallel data. This project overcomes that using English as a pivot between Kannada and target languages (Tamil, Telugu, Malayalam), creating a synthetic yet semantically-rich corpus. The mT5 model is reduced and fine-tuned to yield the **Dravidian-T5**, optimized for these languages.

---

## 📊 Dataset: DraPara

- 📚 Source: [Samanantar Kn-En Dataset](https://arxiv.org/abs/2104.05596)
- 🔁 Translated from English → Tamil, Telugu, Malayalam using **NLLB-200**
- 🧹 Filtered using BLEU > 0.5 and Similarity > 0.8
- 📦 Final size: **107,057** high-quality sentence pairs
- 📍 Hosted on Hugging Face: [DraPara Dataset](https://huggingface.co/datasets/Sujalts/DraPara)

---

## 🤖 Model: Dravidian-T5

- Base: `google/mt5-small`
- Vocabulary reduced to top Dravidian language tokens
- Language-tagged sentences (e.g., `<tamil>`, `<kannada>`)
- Trained using joint multilingual fine-tuning
- 🚀 Hosted at: [Dravidian-T5 Model](https://huggingface.co/Sujalts/Dravidian-T5)

---

## 🧪 Evaluation

| Language Pair   | BLEU   | Similarity |
|------------------|--------|------------|
| Kannada ↔ Tamil  | 6.52   | 0.7203     |
| Kannada ↔ Telugu | 6.75   | 0.7484     |
| Kannada ↔ Malayalam | 6.39 | 0.7168     |
| Tamil ↔ Telugu   | 5.98   | 0.7146     |

- 🧮 Average BLEU: **0.69**
- 🤝 Avg Similarity: **0.7764** (on 1000 unseen sentences/language)
- 🔬 Evaluation via Indic-SBERT and sentence-BLEU

---

## 💡 Example

**Input (Kannada):**
