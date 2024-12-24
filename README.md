# UAS DEEP LEARNING
---
## 💻 SIAbot_UNIB (Chatbot Informasi Skripsi Informatika Universitas Bengkulu)
## Nama Kelompok :
1. RIMAYA DWI ATIKA (G1A021021)
2. RAHAYU NINGRUM PUSPA RIDHA (G1A021071)
---
# Deskripsi Proyek

SIAbot_UNIB adalah inovasi chatbot untuk mengetahui informasi terkait skripsi informatika Universitas Bengkulu dengan lebih efektif dan efisien dikarenakan mahasiswa tidak perlu membaca banyak halaman buku panduan untuk mencari informasi yang ingin diketahui. SIAbot_UNIB ini akan membantu mahasiswa dalam menjawab pertanyaan seputar skripsi informatika. Selain itu, SIAbot_UNIB ini dilengkapi dengan fitur Google Text To Speech, sehingga outputnya bisa didengarkan.

Proyek ini dikembangkan dengan menggunakan model Long Short Term Memory (LSTM) untuk membuat prediksi dan klasifikasi yang berhubungan dengan data teks.

---
## Langkah-Langkah Proyek

### Collecting Dataset
Dataset diambil secara manual melalui buku panduan skripsi informatika UNIB dan ditambah dengan informasi umum seputar skripsi.

### Pra-processing Data
![image](https://github.com/user-attachments/assets/ee87bdae-12dd-4f2c-a1ad-87a6bd983338)

Model dilatih dengan dataset yang telah melewati praproses seperti :
1.   Remove Punctuations (Menghapus Punktuasi)
2.   Lematization (Lematisasi)
3.   Tokenization (Tokenisasi)
4.   Apply Padding (Padding)
5.   Encoding the Outputs (Konversi Keluaran Enkoding)
   
### Arsitektur Model
Model ini menggunakan Long Short Term Memory (LSTM) dengan beberapa lapisan neural network sebagai berikut:
1. **Input Layer**: Menerima data input dengan bentuk `(input_shape)`.
2. **Embedding Layer**: Mengonversi kata-kata dalam data menjadi representasi vektor berdimensi 10.
3. **LSTM Layer**: Menggunakan 10 unit untuk menangkap hubungan jangka panjang dalam data urutan, dengan output berupa urutan dan dropout sebesar 20%.
4. **Flatten Layer**: Meratakan output LSTM menjadi satu dimensi.
5. **Dense Layer**: Lapisan output dengan fungsi aktivasi softmax untuk menghasilkan distribusi probabilitas dari kelas.

### Pelatihan Model
Menggunakan kompilasi model seperti :
1. Loss function : sparse categorical crossentropy
2. Optimizer : adam
3. Metrics : accuracy
4. Epochs : 450

### Hasil Pelatihan
![image](https://github.com/user-attachments/assets/eefda3db-54ec-430b-bcc1-f2be4e05e8ec)

### Hasil Pengujian
![Screenshots Hasil Pengujian dengan Voice](https://github.com/user-attachments/assets/971b1d7e-5646-4f49-ac22-9c1c5bb02214)

---
## 💡 Kesimpulan
Dari hasil pelatihan model menggunakan **LSTM (Long Short Term Memory)** menunjukan performa yang baik dalam mempelajari pola. Dapat dilihat dari grafik akurasi yang mencapai nilai mendekati 100% dengan loss  0.0321 di akhir pelatihan. Berdasarkan grafik, model bekerja sangat baik pada data latih. 

Setelah dianalisi lebih lanjut tidak ada terlihat bahwasannya model mengalami overfitting, dibuktikan dengan hasil pengujian yang akurat dalam menjawab pertanyaan, begitupun juga dengan hasil **Google text to speech**nya.

Model ini termasuk **Deep Learning** karena menggunakan **Long Short-Term Memory (LSTM)**, yang merupakan jenis jaringan saraf dalam (**Deep Neural Network**). LSTM digunakan untuk menangani data sekuensial seperti teks atau waktu. LSTM (Long Short-Term Memory) dikategorikan sebagai deep learning karena memiliki arsitektur berlapis yang mampu mempelajari representasi kompleks dari data urutan, seperti teks atau seri waktu. Sedangkan, Shallow learning seperti SVM, Random Forest, atau Regresi, bekerja baik pada data tabular yang sudah memiliki fitur terdefinisi dengan baik, tetapi tidak memiliki kemampuan hierarkis untuk mempelajari fitur dari data mentah. 

---
## 📚 Referensi
Medium - Going Merry With Tensorflow 2.0

---
## 📖 Cara Menjalankan
```bash
# Clone repository
git clone https://github.com/rimayadwiatika11/SIAbot_UNIB-Chatbot-Informasi-Skripsi-Informatika-UNIB.git
```

```bash
# Buka folder ipynb, upload data SIAbot_UNIB.json
running kode
