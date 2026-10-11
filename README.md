# 📄 Research Paper NLP Classification

An NLP pipeline for **multi-label research paper classification, keyword extraction,
and SDG mapping** using traditional Machine Learning and Transformer-based models.

---

## 🎯 Project Overview

The system analyzes research titles and abstracts to:

- Predict academic domains
- Extract representative keywords
- Map research content to relevant UN Sustainable Development Goals (SDGs)

The project is aligned with **SDG 4: Quality Education**.

---

## 📊 Dataset

The project uses the **arXiv Scientific Abstracts Dataset** from Kaggle.

Main inputs:

- Research titles and abstracts
- Academic domain labels

The data pipeline included text cleaning, normalization, tokenization,
lemmatization, duplicate removal, and multi-label target preparation.

---

## 🤖 Models

Three approaches were evaluated for multi-label domain classification:

- **TF-IDF + Linear SVM**
- **BERT Embeddings + Logistic Regression**
- **DistilBERT Embeddings + Logistic Regression**

A **One-vs-Rest** strategy was used for classification.

Keyword extraction was performed using **YAKE**, while SDG mapping used
a rule-based dictionary approach.

---

## 📈 Results

| Model | Subset Accuracy | Micro-F1 |
|---|---:|---:|
| **TF-IDF + Linear SVM** | 0.274 | **0.679** |
| **BERT + Logistic Regression** | **0.287** | 0.675 |
| **DistilBERT + Logistic Regression** | 0.184 | 0.611 |

**TF-IDF + Linear SVM achieved the highest Micro-F1**, while  
**BERT + Logistic Regression achieved the highest Subset Accuracy**.

---

## 🔍 Explainability

**LIME** was used to explain model predictions by identifying which words
contributed positively or negatively to each predicted research domain.

---

## 🛠️ Methods & Technologies

- Natural Language Processing
- TF-IDF
- Linear SVM
- Logistic Regression
- BERT
- DistilBERT
- YAKE
- LIME
- Multi-label Classification
- Explainable AI

---

## ⚠️ Limitations

- Long-tail class imbalance affects rare domains
- Abstract-only input may provide limited context
- Related domains may contain overlapping terminology
- SDG mapping currently relies on rule-based matching

---

Academic team project – Princess Nourah bint Abdulrahman University
