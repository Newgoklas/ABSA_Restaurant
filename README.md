# 🍽️ Aspect Based Sentiment Analysis (ABSA) Review Restoran Bahasa Indonesia

## 📌 Deskripsi

Project ini merupakan implementasi **Aspect Based Sentiment Analysis (ABSA)** pada review restoran berbahasa Indonesia menggunakan pendekatan hybrid:

- Named Entity Recognition (NER) menggunakan **Conditional Random Field (CRF)**
- Aspect Sentiment Classification menggunakan **TF-IDF + Multinomial Naive Bayes**

Sistem mampu mengidentifikasi aspek yang dibahas pada sebuah review kemudian menentukan sentimen pada setiap aspek tersebut.

---

# Struktur Project

```
ABSA_Restaurant/

│
├── app.py
├── requirements.txt
├── README.md
├── ner_model.pkl
├── absa_model.pkl
├── dataset/
│      ├── restaurant_review.csv
│      ├── ner_dataset.csv
│      └── absa_dataset.csv
│
└── notebook/
       ├── Notebook1.ipynb
       ├── Notebook2.ipynb
       ├── Notebook3A.ipynb
       ├── Notebook3B.ipynb
       ├── Notebook4.ipynb
       └── Notebook5.ipynb
```

---

# Dataset

Dataset yang digunakan meliputi:

1. Dataset Review Restoran
2. Dataset NER (BIO Tagging)
3. Dataset ABSA

---

# Algoritma

## Named Entity Recognition

Model:

- Conditional Random Field (CRF)

Entity:

- FOOD
- SERVICE
- PRICE
- AMBIENCE
- MISCELLANEOUS

---

## Sentiment Classification

Model:

- TF-IDF
- Multinomial Naive Bayes

Kelas Sentimen:

- Positive
- Neutral
- Negative

---

# Tahapan Sistem

```
Review

↓

Preprocessing

↓

NER (CRF)

↓

Aspect Extraction

↓

TF-IDF

↓

Naive Bayes

↓

Sentiment Prediction

↓

Output
```

---

# Install

Install dependency

```bash
pip install -r requirements.txt
```

---

# Menjalankan Aplikasi

```bash
streamlit run app.py
```

---

# Tampilan

Masukkan review restoran, kemudian klik tombol **Analisis**.

Contoh:

```
Makanannya enak,
pelayanannya lambat,
harga cukup mahal.
```

Output

| Aspect | Context | Sentiment |
|---------|---------|-----------|
| FOOD | makanan enak | Positive |
| SERVICE | pelayanan lambat | Negative |
| PRICE | harga mahal | Negative |

---

# Library

- Python 3.x
- Streamlit
- Pandas
- NumPy
- Scikit-Learn
- sklearn-crfsuite
- Joblib

---

# Evaluasi

Evaluasi dilakukan menggunakan:

- Accuracy
- Precision
- Recall
- F1-Score
- Classification Report
- Confusion Matrix

---

# Author

Nama :

NIM :

Universitas :

Program Studi :

---

# Lisensi

Project ini dibuat untuk keperluan akademik sebagai tugas UAS.
