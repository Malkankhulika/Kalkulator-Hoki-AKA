# <h1 align="center">Kalkulator Hoki</h1>
<p align="center">Khulika Malkan (2311110057)</p>
<p align="center">Rizal Wahyu Pratama (2311110029)</p>

## Daftar Isi

- [Studi Kasus](#GambaranumumMonkeyPox)
- [Struktur Program](#GambaranumumMonkeyPox)
- [Deskripsi Algoritma](#GambaranumumMonkeyPox)
- [Grafik Perbandingan Running Time](#Reference)
- [Performance Comparisom](#Reference)
- [Analisis Perbandingan Itetarive Vs Rekursive](#Reference)
- [Kesimpulan](#Conclusion)
- [Referensi](#Reference)
  
## Study Case
Kalkulator Hoki merupakan sebuah aplikasi interaktif yang dirancang untuk menghitung tingkat keberuntungan seseorang berdasarkan tiga huruf pertama dari nama panggilan mereka. Proses penghitungan dilakukan dengan menjumlahkan nilai numerik yang merepresentasikan huruf dalam alfabet (A=1, B=2, ..., Z=26), kemudian melibatkan operasi tambahan untuk menghasilkan skor keberuntungan (hoki) akhir.

Gagasan pengembangan aplikasi ini berakar dari fenomena rasa penasaran manusia terhadap hal-hal yang berkaitan dengan peramalan, seperti angka keberuntungan, zodiak, atau ramalan lainnya. Studi menunjukkan bahwa ramalan zodiak, misalnya, memiliki pengaruh signifikan terhadap kepercayaan remaja, terutama melalui media digital seperti video TikTok [1]. Selain itu, fenomena ramalan golongan darah di Jepang juga mencerminkan bagaimana masyarakat mengaitkan aspek-aspek kehidupan mereka dengan prediksi berbasis kepercayaan tradisional [2]. Hal ini menggambarkan ketertarikan alami manusia terhadap prediksi berbasis data atau simbolik.

Dengan menggunakan pendekatan sederhana berbasis penghitungan numerik, aplikasi ini tidak hanya menawarkan pengalaman yang menarik bagi pengguna, tetapi juga memberikan peluang untuk mengeksplorasi efisiensi algoritma dalam implementasi dunia nyata. Dalam konteks studi kasus ini, fokus utama adalah membandingkan efisiensi algoritma iteratif dan rekursif yang digunakan dalam penghitungan skor hoki. Perbandingan tersebut dilakukan melalui analisis kompleksitas waktu asimtotik serta pengukuran waktu eksekusi dengan berbagai ukuran masukan. Studi ini diharapkan dapat memberikan pemahaman yang lebih mendalam tentang pentingnya pemilihan algoritma yang efisien dalam menyelesaikan permasalahan komputasi.


## Struktur Program
![image](https://github.com/user-attachments/assets/b3ba1621-839b-4215-b41e-1381f14366fd)

Penjelasan struktur dan elemen dalam program kalkulator hoki
1. app.py
   
   app.py merupakan file utama dalam program yang bertanggung jawab untuk menjalankan backend menggunakan framework Flask. File ini mengatur logika perhitungan hoki dengan mengimplementasikan dua versi algoritma, yaitu iteratif dan rekursif. Selain itu, file ini mengatur rute untuk menerima input dari frontend, memprosesnya dengan algoritma yang sesuai berdasarkan konfigurasi, dan mengembalikan hasil perhitungan ke frontend dalam format JSON.

2. Folder static
   
   Folder static menyimpan sumber daya statis yang digunakan untuk meningkatkan estetika tampilan aplikasi. File utama di dalamnya adalah style.css, yang berisi definisi gaya visual seperti tata letak, warna, dan font. File ini bertujuan untuk memastikan pengalaman pengguna lebih menarik secara visual serta mendukung antarmuka yang responsif.

3. Folder templates
   
   Folder templates memuat file index.html, yaitu template HTML yang menjadi antarmuka utama pengguna. File ini menyediakan formulir input untuk memasukkan nama pengguna, tombol untuk menghitung tingkat hoki, dan area hasil yang dinamis untuk menampilkan skor hoki yang dihitung oleh backend. Struktur file ini mendukung komunikasi dengan backend melalui mekanisme asinkron.

4. File requirements.txt
   
   File ini mendokumentasikan semua pustaka yang diperlukan untuk menjalankan aplikasi, seperti Flask dan pustaka pendukung lainnya. Keberadaan file ini bertujuan untuk mempermudah instalasi dependensi dengan menggunakan perintah pip install -r requirements.txt, sehingga memastikan aplikasi dapat dijalankan pada lingkungan yang konsisten.

5. File credentials.json
    
   credentials.json merupakan file konfigurasi yang menyimpan data privat, seperti mode operasi (iteratif atau rekursif) yang digunakan oleh backend. File ini tidak dijelaskan secara rinci karena bersifat rahasia, namun berperan penting dalam menentukan perilaku algoritma yang diterapkan dalam app.py.


## Performance Comparisom
Pada Mei 20





## Itetarive Vs Rekursive
Pada Mei 20




## Conclusion
Pada Mei 20





## Reference
[1] https://www.researchgate.net/publication/376456580_Ramalan_Di_Era_Digital_Pengaruh_Video_Tiktok_Terkait_Kepercayaan_Remaja_Kepada

[2] https://journal.unair.ac.id/download-fullpapers-japanology87dbefda8b2full.pdf?utm_source=chatgpt.com
