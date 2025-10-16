# Data-Classification-IBM
# Analisis Sentimen Ulasan Aplikasi Travoy

## Project Overview
[cite_start]Proyek ini adalah sebuah analisis sentimen terhadap ulasan pengguna aplikasi Travoy yang dipublikasikan di Google Play Store[cite: 7]. [cite_start]Tujuannya adalah untuk mengklasifikasikan opini pengguna ke dalam sentimen **Positif**, **Negatif**, atau **Netral**[cite: 37]. [cite_start]Dengan memanfaatkan AI, proyek ini mengubah data kualitatif (teks ulasan) menjadi wawasan kuantitatif yang dapat digunakan untuk memberikan rekomendasi konkret kepada pengembang aplikasi[cite: 11, 33].

---

## Proses Analisis & Sumber Data
[cite_start]Proses kerja dalam proyek ini dilakukan sepenuhnya di Google Colab Notebook[cite: 15, 23]. Berikut adalah langkah-langkah yang dijalankan:

1.  **Setup Environment**: Menginstal library Python yang dibutuhkan, yaitu `google-play-scraper` untuk pengambilan data, serta `pandas` dan `matplotlib`/`seaborn` untuk manipulasi dan visualisasi data.

2.  **Pengambilan Data (Data Scraping)**: Alih-alih menggunakan dataset statis, data ulasan diambil secara *real-time* dari Google Play Store. Kode mengambil 200 ulasan terbaru aplikasi Travoy untuk memastikan data yang dianalisis adalah yang paling relevan. [cite_start]Karena metode ini, tidak ada file "Raw Dataset" yang dilampirkan[cite: 25]; data dibuat langsung oleh kode.

3.  [cite_start]**Analisis Sentimen dengan AI**: Setiap teks ulasan yang telah dikumpulkan kemudian dianalisis satu per satu menggunakan model AI dari **IBM Granite**[cite: 3]. Model AI diberi instruksi untuk membaca setiap ulasan dan mengklasifikasikannya sebagai 'Positif', 'Negatif', atau 'Netral'.

4.  **Visualisasi Hasil**: Setelah semua ulasan diklasifikasikan, hasilnya diagregasi untuk menghitung jumlah total setiap kategori sentimen. [cite_start]Data ini kemudian divisualisasikan menggunakan diagram lingkaran (*pie chart*) untuk menunjukkan distribusi sentimen secara jelas[cite: 32].

---

## Insight & Findings
Berdasarkan visualisasi dan analisis data, ditemukan beberapa wawasan utama:

* **Sentimen Dominan Negatif**: Hasil analisis menunjukkan bahwa mayoritas ulasan pengguna memiliki sentimen **Negatif**. Ini adalah indikator kuat adanya masalah signifikan terkait pengalaman pengguna (*user experience*).
* **Keluhan Utama Pengguna**: Dari ulasan negatif, tema keluhan yang paling sering muncul adalah seputar masalah teknis, terutama pada **kesulitan saat login**, **aplikasi yang sering *error***, dan **antarmuka (UI/UX) yang dinilai tidak intuitif**.
* **Apresiasi Pengguna**: Di sisi lain, ulasan positif yang ada umumnya memuji fitur-fitur informatif seperti **akurasi informasi tarif tol** dan kemudahan **fitur cek saldo e-money**.

---

## AI Support Explanation
[cite_start]Peran AI dalam proyek ini sangat sentral, yaitu sebagai **mesin klasifikasi sentimen otomatis**[cite: 37]. Model AI (IBM Granite) digunakan untuk:
* **Membaca dan Memahami Konteks**: AI membaca setiap kalimat ulasan untuk memahami makna dan sentimen di baliknya.
* **Mengklasifikasi secara Objektif**: AI memberikan label sentimen ('Positif', 'Negatif', 'Netral') secara konsisten dan objektif, menghilangkan bias yang mungkin terjadi jika dilakukan secara manual.
* **Efisiensi**: Proses analisis ratusan ulasan dapat diselesaikan dalam hitungan menit, bukan jam.

[cite_start]Penggunaan AI memungkinkan analisis data teks tidak terstruktur menjadi wawasan yang terukur dan dapat ditindaklanjuti[cite: 8].
