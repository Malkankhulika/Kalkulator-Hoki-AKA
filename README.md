# <h1 align="center">Kalkulator Hoki</h1>
<p align="center">Khulika Malkan (2311110057)</p>
<p align="center">Rizal Wahyu Pratama (2311110029)</p>

## Daftar Isi

- [Studi Kasus](#Studi-Kasus)
- [Struktur Program](#Struktur-Program)
- [Deskripsi Algoritma](#Deskripsi-Algoritma)
- [Grafik Perbandingan Running Time](#Grafik-Perbandingan-Running-Time)
- [Analisis Perbandingan Iteratif dan Rekursif](#Analisis-Perbandingan-Iteratif-dan-Rekursif)
- [Kesimpulan](#Kesimpulan)
- [Referensi](#Referensi)
  
## Studi Kasus
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


## Deskripsi Algoritma
- Iteratif

  Algoritma iteratif menggunakan pendekatan berbasis perulangan (loop) untuk menghitung nilai hoki. Tiga huruf pertama dari nama panggilan pengguna diakses satu per satu, nilai numeriknya dihitung dengan rumus (ord(huruf.upper()) - 64), kemudian semua nilai dijumlahkan dalam sebuah variabel akumulator. Setelah itu, skor hoki dihitung dengan menerapkan modulasi sederhana atau operasi numerik lainnya pada hasil penjumlahan.
  Pendekatan iteratif dipilih karena efisien dalam penggunaan memori, dengan kompleksitas waktu sebesar 𝑂 (𝑛), di mana 𝑛 adalah panjang nama (maksimal 3 iterasi). Pendekatan ini cocok untuk penghitungan sederhana pada aplikasi interaktif seperti "Kalkulator Hoki," di mana kecepatan dan keandalan sangat penting untuk pengalaman pengguna.

- Rekursif
  Algoritma rekursif memanfaatkan pemanggilan fungsi berulang untuk menghitung nilai hoki. Fungsi ini secara rekursif menjumlahkan nilai huruf pertama dari nama panggilan pengguna dengan hasil pemanggilan fungsi yang sama pada substring nama tanpa huruf pertama, hingga mencapai kondisi dasar di mana nama kosong atau memiliki panjang 0. Operasi pada hasil akhir dilakukan untuk menghasilkan skor hoki.
  Pendekatan rekursif relevan untuk studi kasus ini karena memberikan solusi yang elegan dan modular. Kompleksitas waktu juga sebesar  𝑂 (𝑛), tetapi memiliki overhead memori tambahan akibat stack rekursi. Studi perbandingan antara iterasi dan rekursi menjadi penting untuk memahami bagaimana pilihan algoritma dapat memengaruhi performa pada penghitungan yang sederhana namun sering dilakukan, seperti pada "Kalkulator Hoki."

- Relevansi Studi Kasus

  Kedua algoritma dipilih berdasarkan kemampuan mereka untuk menyelesaikan perhitungan dengan efisiensi tinggi dan skalabilitas yang cukup baik. Pendekatan iteratif lebih sesuai untuk aplikasi yang menuntut efisiensi memori, sementara pendekatan rekursif memberikan perspektif tentang struktur algoritma yang lebih abstrak dan relevan untuk analisis kompleksitas. Studi perbandingan iterasi dan rekursi di "Kalkulator Hoki" memberikan gambaran nyata tentang dampak pemilihan algoritma pada performa sistem dalam tugas-tugas sehari-hari.


## Grafik Perbandingan Running Timne
![image](https://github.com/user-attachments/assets/f70fdd15-d783-49b7-9aab-b5a28d08e1a9)

Grafik perbandingan waktu eksekusi (running time) antara algoritma rekursif dan iteratif pada "kalkulator hoki" menunjukkan variasi kinerja kedua metode dalam menyelesaikan tugas yang sama. Secara umum, hasil menunjukkan bahwa algoritma rekursif memiliki waktu eksekusi yang lebih rendah dibandingkan algoritma iteratif pada sebagian besar kasus. Hal ini mengindikasikan bahwa rekursi, dengan mekanisme pemanggilan fungsi berulang, lebih efisien dalam menyelesaikan perhitungan yang melibatkan submasalah yang berulang. Keunggulan rekursi ini terlihat terutama pada individu dengan waktu eksekusi yang lebih cepat, meskipun beberapa individu menunjukkan perbedaan waktu yang lebih kecil atau bahkan lebih tinggi pada algoritma iteratif [3]. Hal ini sejalan dengan temuan dari penelitian sebelumnya yang menunjukkan bahwa rekursi seringkali lebih cepat dalam kasus masalah yang terstruktur secara rekursif, seperti pada perhitungan pohon atau grafik [4].

Namun, meskipun rekursi menunjukkan keunggulan dalam hal waktu eksekusi, perbedaan yang terjadi pada data ini mengindikasikan bahwa faktor lain, seperti kompleksitas input dan implementasi algoritma, juga mempengaruhi kinerja masing-masing metode. Algoritma iteratif, meskipun lebih lambat secara umum dalam dataset ini, cenderung lebih stabil dan memiliki kontrol yang lebih baik terhadap alur eksekusi, serta lebih mudah dioptimalkan dalam beberapa kasus [5]. Oleh karena itu, pemilihan antara rekursif dan iteratif harus mempertimbangkan berbagai aspek, seperti efisiensi waktu, kebutuhan memori, dan kompleksitas implementasi, yang dapat berbeda tergantung pada konteks aplikasi dan karakteristik masalah yang dihadapi.


## Analisis Perbandingan Iteratif dan Rekursif
Pada Mei 20




## Kesimpulan
Pada Mei 20





## Reference
[1] https://www.researchgate.net/publication/376456580_Ramalan_Di_Era_Digital_Pengaruh_Video_Tiktok_Terkait_Kepercayaan_Remaja_Kepada

[2] https://journal.unair.ac.id/download-fullpapers-japanology87dbefda8b2full.pdf?utm_source=chatgpt.com

[3] D. E. Knuth, The Art of Computer Programming, Volume 1: Fundamental Algorithms, Addison-Wesley, 1973.

[4] T. H. Cormen, C. E. Leiserson, R. L. Rivest, and C. Stein, Introduction to Algorithms, 3rd ed. MIT Press, 2009.

[5] R. Sedgewick and K. Wayne, Algorithms, 4th ed. Addison-Wesley, 2011.
