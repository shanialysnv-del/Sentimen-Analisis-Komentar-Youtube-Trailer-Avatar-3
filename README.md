## Deskripsi Proyek
Repository ini merupakan proyek Ujian Akhir Semester (UAS) mata kuliah Analisa Big Data yang bertujuan untuk melakukan analisis sentimen komentar YouTube terhadap video Trailer Avatar 3

Analisis dilakukan untuk mengetahui kecenderungan opini penonton (positif, netral, dan negatif) dengan memanfaatkan teknik text mining dan machine learning. Data diperoleh langsung dari platform YouTube menggunakan YouTube Data API, sehingga merepresentasikan opini asli pengguna.

---

## Metodologi
Proyek ini mengikuti tahapan CRISP-DM, yang meliputi:
1. Business Understanding
   Mengetahui respon dan persepsi penonton terhadap trailer Avatar 3.
2. Data Understanding
   Eksplorasi komentar YouTube dan karakteristik data teks.
3. Data Preparation
   Cleaning, tokenisasi, lemmatization, dan labeling sentimen.
4. Modeling  
   Klasifikasi sentimen menggunakan Naive Bayes dan Logistic Regression.
5. Evaluation  
   Evaluasi model menggunakan Accuracy, F1-score, dan Confusion Matrix.
6. Deployment 
   Implementasi model terbaik dalam aplikasi interaktif berbasis Gradio.

---

## Sumber Data
- Platform: YouTube  
- Metode Pengambilan: YouTube Data API  
- Objek Data: Komentar pengguna pada video trailer Avatar 3  
- Jenis Data: Data teks (unstructured text)

---

## Data Preparation
Tahapan preprocessing yang dilakukan:
- Case folding
- Cleaning (emoji, simbol, URL, tanda baca)
- Tokenisasi
- Lemmatization
- Pemberian label sentimen menggunakan TextBlob
- Penanganan ketidakseimbangan kelas menggunakan SMOTE

---

## Feature Extraction
- Metode: TF-IDF (Term Frequency–Inverse Document Frequency)
- Jumlah fitur maksimum: 5000

---

## Model yang Digunakan
- Naive Bayes
- Logistic Regression
- Split data: 90% data training : 10% data testing
- Hyperparameter tuning menggunakan GridSearchCV

---

## Evaluasi Model
Evaluasi dilakukan menggunakan:
- Accuracy
- F1-score (weighted)
- Confusion Matrix

Model Logistic Regression menunjukkan performa terbaik dan dipilih sebagai model akhir.

---

## Deployment
Model terbaik dan TF-IDF vectorizer disimpan menggunakan joblib, kemudian diimplementasikan dalam bentuk aplikasi prediksi sentimen sederhana menggunakan Gradio, sehingga pengguna dapat melakukan analisis sentimen secara interaktif.

---

## Tools & Library
- Python
- Pandas, NumPy
- Scikit-learn
- NLTK, TextBlob
- Imbalanced-learn (SMOTE)
- Matplotlib, Seaborn
- Gradio
