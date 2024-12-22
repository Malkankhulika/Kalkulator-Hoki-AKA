# <h1 align="center">Kalkulator Hoki</h1>
<p align="center">Khulika Malkan (2311110057)</p>
<p align="center">Rizal Wahyu Pratama (2311110029)</p>

## Daftar Isi

- [Studi Kasus](#Studi-Kasus)
- [Struktur Program](#Struktur-Program)
- [Deskripsi Algoritma yang dipilih untuk menyelesaikan permasalahan](#Deskripsi-Algoritma-yang-dipilih-untuk-menyelesaikan-permasalahan)
- [Grafik Perbandingan Running Time](#Grafik-Perbandingan-Running-Time)
- [Kompleksitas Algoritma Terbaik, Terburuk, Rata rata](#Kompleksitas-Algoritma-Terbaik,-Terburuk,-Rata-rata)
- [Analisis Perbandingan Iteratif dan Rekursif](#Analisis-Perbandingan-Iteratif-dan-Rekursif)
- [Kesimpulan](#Kesimpulan)
- [Referensi](#Referensi)
  
## Studi Kasus
Kalkulator Hoki merupakan sebuah aplikasi interaktif yang dirancang untuk menghitung tingkat keberuntungan seseorang berdasarkan tiga huruf pertama dari nama panggilan mereka. Proses penghitungan dilakukan dengan menjumlahkan nilai numerik yang merepresentasikan huruf dalam alfabet (A=1, B=2, ..., Z=26), kemudian melibatkan operasi tambahan untuk menghasilkan skor keberuntungan (hoki) akhir.

Gagasan ini berakar dari fenomena rasa penasaran manusia terhadap hal-hal yang berkaitan dengan peramalan, seperti angka keberuntungan, zodiak, atau ramalan lainnya. Studi menunjukkan bahwa ramalan zodiak, misalnya, memiliki pengaruh signifikan terhadap kepercayaan remaja, terutama melalui media digital seperti video TikTok [1]. Selain itu, fenomena ramalan golongan darah di Jepang juga mencerminkan bagaimana masyarakat mengaitkan aspek-aspek kehidupan mereka dengan prediksi berbasis kepercayaan tradisional [2]. Hal ini menggambarkan ketertarikan alami manusia terhadap prediksi berbasis data atau simbolik.

Dengan menggunakan pendekatan sederhana berbasis penghitungan numerik, aplikasi ini tidak hanya menawarkan pengalaman yang menarik bagi pengguna, tetapi juga memberikan peluang untuk mengeksplorasi efisiensi algoritma dalam implementasi dunia nyata. Dalam konteks studi kasus ini, fokus utama adalah membandingkan efisiensi algoritma iteratif dan rekursif yang digunakan dalam penghitungan skor hoki. Perbandingan tersebut dilakukan melalui analisis kompleksitas waktu asimtotik serta pengukuran waktu eksekusi dengan berbagai ukuran masukan. Studi ini diharapkan dapat memberikan pemahaman yang lebih mendalam tentang pentingnya pemilihan algoritma yang efisien dalam menyelesaikan permasalahan komputasi.

  **Hasil dan Manfaat**
  
![WhatsApp Image 2024-12-22 at 22 25 13_249684bb](https://github.com/user-attachments/assets/0fa0e3bf-b8f6-4f63-8825-b1c5b716b7d8)

- Pengalaman Pengguna: Program ini berhasil menciptakan pengalaman yang menyenangkan dan interaktif, meningkatkan keterlibatan pengguna.
- Statistik yang Berguna: Dengan menyimpan hasil sebelumnya, pengguna dapat melacak perkembangan hoki mereka, yang menambah nilai lebih pada program.
- Visualisasi yang Menarik: Penggunaan warna untuk menampilkan hasil hoki membuat informasi lebih mudah dipahami dan menarik secara visual.

## Struktur Program
![image](https://github.com/user-attachments/assets/b3ba1621-839b-4215-b41e-1381f14366fd)

Penjelasan struktur dan elemen dalam program kalkulator hoki
1. app.py
   
   app.py merupakan file utama dalam program untuk menjalankan backend menggunakan framework Flask. File ini mengatur logika perhitungan hoki dengan mengimplementasikan dua versi algoritma, yaitu iteratif dan rekursif. Selain itu, file ini mengatur rute untuk menerima input dari frontend, memprosesnya dengan algoritma yang sesuai berdasarkan konfigurasi, dan mengembalikan hasil perhitungan ke frontend dalam format JSON.

2. Folder static
   
   Folder static menyimpan sumber daya statis yang digunakan untuk meningkatkan estetika tampilan aplikasi. File utama di dalamnya adalah style.css, yang berisi definisi gaya visual seperti tata letak, warna, dan font. File ini bertujuan untuk memastikan pengalaman pengguna lebih menarik secara visual serta mendukung antarmuka yang responsif.

3. Folder templates
   
   Folder templates memuat file index.html, yaitu template HTML yang menjadi antarmuka utama pengguna. File ini menyediakan formulir input untuk memasukkan nama pengguna, tombol untuk menghitung tingkat hoki, dan area hasil yang dinamis untuk menampilkan skor hoki yang dihitung oleh backend. Struktur file ini mendukung komunikasi dengan backend melalui mekanisme asinkron.

4. File requirements.txt
   
   File ini mendokumentasikan semua pustaka yang diperlukan untuk menjalankan aplikasi, seperti Flask dan pustaka pendukung lainnya. Keberadaan file ini bertujuan untuk mempermudah instalasi dependensi dengan menggunakan perintah pip install -r requirements.txt, sehingga memastikan aplikasi dapat dijalankan pada lingkungan yang konsisten.

5. File credentials.json
    
   credentials.json merupakan file konfigurasi yang menyimpan data privat, seperti mode operasi (iteratif atau rekursif) yang digunakan oleh backend.

**Deskripsi Program**
![WhatsApp Image 2024-12-22 at 22 25 50_de181fab](https://github.com/user-attachments/assets/ab0ae6d2-74dc-419f-ae79-e4bc430f777b)

- Input Pengguna: Program meminta pengguna untuk memasukkan nama panggilan mereka.
- Perhitungan Hoki:
  - a. Mengambil tiga huruf pertama dari nama yang dimasukkan.
  - b. Menghitung nilai numerik untuk setiap huruf berdasarkan urutan abjad (A=1, B=2, ..., Z=26).
  - c. Menambahkan nilai dari tanggal dan bulan saat ini untuk mendapatkan total hoki.
- Visualisasi Hasil: Hasil hoki ditampilkan dengan warna:
  - a. Merah untuk hoki di bawah 50%.
  - b. Kuning untuk hoki antara 50% hingga 80%.
  - c. Hijau untuk hoki di atas 80%.
- Statistik Hoki: Program menyimpan hasil hoki sebelumnya, memungkinkan pengguna untuk melihat statistik seperti rata-rata hoki, hoki tertinggi, dan hoki terendah.
- Interaksi Pengguna: Setelah menampilkan hasil, pengguna diberikan opsi untuk bermain kembali atau tidak. Jika memilih untuk tidak bermain lagi, program menampilkan pesan perpisahan yang positif, berharap hoki mereka akan terus berkembang.

## Deskripsi Algoritma yang dipilih untuk menyelesaikan permasalahan
- Iteratif

  Algoritma iteratif menggunakan pendekatan berbasis perulangan (loop) untuk menghitung nilai hoki. Tiga huruf pertama dari nama panggilan pengguna diakses satu per satu, nilai numeriknya dihitung dengan rumus (ord(huruf.upper()) - 64), kemudian semua nilai dijumlahkan dalam sebuah variabel akumulator. Setelah itu, skor hoki dihitung dengan menerapkan modulasi sederhana atau operasi numerik lainnya pada hasil penjumlahan.
  Pendekatan iteratif dipilih karena efisien dalam penggunaan memori, dengan kompleksitas waktu sebesar 𝑂 (𝑛), di mana 𝑛 adalah panjang nama (maksimal 3 iterasi). Sehingga pendekatan ini cocok untuk penghitungan sederhana pada aplikasi interaktif seperti "Kalkulator Hoki," di mana kecepatan dan keandalan sangat penting untuk pengalaman pengguna.

- Rekursif
  
  Algoritma rekursif memanfaatkan pemanggilan fungsi berulang untuk menghitung nilai hoki. Fungsi ini secara rekursif menjumlahkan nilai huruf pertama dari nama panggilan pengguna dengan hasil pemanggilan fungsi yang sama pada substring nama tanpa huruf pertama, hingga mencapai kondisi dasar di mana nama kosong atau memiliki panjang 0. Operasi pada hasil akhir dilakukan untuk menghasilkan skor hoki.
  Pendekatan rekursif relevan untuk studi kasus ini karena memberikan solusi yang elegan dan modular. Kompleksitas waktu juga sebesar 𝑂 (𝑛), tetapi memiliki overhead memori tambahan akibat stack rekursi. Studi perbandingan antara iterasi dan rekursi menjadi penting untuk memahami bagaimana pilihan algoritma dapat memengaruhi performa pada penghitungan yang sederhana namun sering dilakukan, seperti pada "Kalkulator Hoki."

- Relevansi Studi Kasus

  Kedua algoritma dipilih berdasarkan kemampuan mereka untuk menyelesaikan perhitungan dengan efisiensi tinggi dan skalabilitas yang cukup baik. Pendekatan iteratif lebih sesuai untuk aplikasi yang menuntut efisiensi memori, sementara pendekatan rekursif memberikan perspektif tentang struktur algoritma yang lebih abstrak dan relevan untuk analisis kompleksitas. Studi perbandingan iterasi dan rekursi di "Kalkulator Hoki" memberikan gambaran nyata tentang dampak pemilihan algoritma pada performa sistem dalam tugas-tugas sehari-hari.


## Grafik Perbandingan Running Time
![image](https://github.com/user-attachments/assets/f70fdd15-d783-49b7-9aab-b5a28d08e1a9)

Grafik perbandingan waktu eksekusi (running time) antara algoritma rekursif dan iteratif pada "kalkulator hoki" menunjukkan variasi kinerja kedua metode dalam menyelesaikan tugas yang sama. Secara umum, hasil menunjukkan bahwa algoritma rekursif memiliki waktu eksekusi yang lebih rendah dibandingkan algoritma iteratif pada sebagian besar kasus. Hal ini mengindikasikan bahwa rekursi, dengan mekanisme pemanggilan fungsi berulang, lebih efisien dalam menyelesaikan perhitungan yang melibatkan submasalah yang berulang. Keunggulan rekursi ini terlihat terutama pada individu dengan waktu eksekusi yang lebih cepat, meskipun beberapa individu menunjukkan perbedaan waktu yang lebih kecil atau bahkan lebih tinggi pada algoritma iteratif [3]. Hal ini sejalan dengan temuan dari penelitian sebelumnya yang menunjukkan bahwa rekursi seringkali lebih cepat dalam kasus masalah yang terstruktur secara rekursif, seperti pada perhitungan pohon atau grafik [4].

Namun, meskipun rekursi menunjukkan keunggulan dalam hal waktu eksekusi, perbedaan yang terjadi pada data ini mengindikasikan bahwa faktor lain, seperti kompleksitas input dan implementasi algoritma, juga mempengaruhi kinerja masing-masing metode. Algoritma iteratif, meskipun lebih lambat secara umum dalam dataset ini, cenderung lebih stabil dan memiliki kontrol yang lebih baik terhadap alur eksekusi, serta lebih mudah dioptimalkan dalam beberapa kasus [5]. Oleh karena itu, pemilihan antara rekursif dan iteratif harus mempertimbangkan berbagai aspek, seperti efisiensi waktu, kebutuhan memori, dan kompleksitas implementasi, yang dapat berbeda tergantung pada konteks aplikasi dan karakteristik masalah yang dihadapi.

## Kompleksitas Algoritma Terbaik, Terburuk, Rata rata
Kompleksitas Waktu pada kasus terbaik, terburuk, dan rata-rata dari "Kalkulator Hoki" adalah semua sama, karena batasan maksimal yang dieksekusi selalu sama yaitu 3 Huruf sehingga Algoritma hanya akan memproses 3 huruf pertama yang diinputkan terlepas dari panjang nama, sehingga jumlah iterasi atau panggilan rekursif tidak pernah melebihi 3. Kemudian operasi konstan setiap hurufnya memerlukan waktu konstan untuk konversi ke nilai numerik dan penjumlahan. Dengan membatasi iterasi atau rekursi, algoritma 8memastikan stabilitas waktu eksekusi untuk nama pendek () maupun panjang (). 

Kompleksitas Konstan (O(1)): Pada implementasi ini, meskipun nama pengguna memiliki panjang yang berbeda, algoritma hanya memproses tiga huruf pertama. Oleh karena itu, waktu eksekusi tidak bergantung pada panjang input setelah mencapai tiga huruf, menjadikannya memiliki kelas efisiensi konstan.Dalam konteks besar, ini termasuk algoritma yang sangat efisien karena waktu eksekusinya tidak meningkat seiring bertambahnya ukuran input (selama batasan tiga huruf dipatuhi). Sehingga kelas efisiensi dari "Kalkulator Hoki" adalah O(1), atau dikenal sebagai algoritma dengan efisiensi konstan. Hal ini menunjukkan bahwa algoritma tersebut optimal untuk tujuan spesifiknya, yaitu menghitung skor hoki dengan pembatasan tiga huruf.


## Analisis Perbandingan Iteratif dan Rekursif
Pada aplikasi "Kalkulator Hoki", perbandingan antara algoritma rekursif dan iteratif menunjukkan bahwa tidak ada perbedaan yang signifikan dalam kinerja kedua algoritma ini. Meskipun kedua pendekatan tersebut berbeda dalam cara mereka menyelesaikan permasalahan, kompleksitas waktu pada kedua algoritma adalah O(1), yang berarti waktu eksekusinya tetap konstan, terlepas dari panjang input, selama input terbatas pada tiga huruf pertama nama. Hal ini terjadi karena dalam kedua metode, hanya tiga huruf pertama yang dihitung, dan setiap operasi pada huruf-huruf tersebut dilakukan dalam waktu konstan.

Dengan kompleksitas waktu yang O(1), baik algoritma iteratif maupun rekursif akan memiliki waktu running yang serupa untuk masalah ini. Tidak ada pengaruh signifikan terhadap kecepatan eksekusi ketika jumlah huruf input dibatasi hanya hingga tiga karakter. Oleh karena itu, baik algoritma rekursif maupun iteratif relevan dan memiliki performa yang hampir identik dalam konteks ini.

Selain itu, meskipun algoritma rekursif dapat menambah beban penggunaan memori karena memerlukan call stack tambahan, permasalahan terkait stack overflow sangat tidak mungkin terjadi dalam aplikasi ini, karena kedalaman rekursi dibatasi hanya sampai tiga kali (untuk tiga huruf pertama). Oleh karena itu, risiko terjadinya stack overflow hampir tidak ada dalam kasus ini.

Secara keseluruhan, meskipun algoritma rekursif menawarkan pendekatan yang lebih modular dan elegan, serta algoritma iteratif lebih sederhana dan langsung, perbedaan antara kedua metode tersebut dalam konteks "Kalkulator Hoki" sangat minim. Kedua algoritma ini memberikan hasil yang serupa dalam waktu eksekusi dan penggunaan memori, menjadikannya pilihan yang relevan dan efektif untuk masalah ini.


## Kesimpulan
Berdasarkan analisis yang telah dilakukan, algoritma rekursif terbukti lebih unggul dibandingkan dengan algoritma iteratif dalam konteks aplikasi "Kalkulator Hoki." Meskipun memiliki overhead memori tambahan, algoritma rekursif menawarkan kecepatan yang lebih tinggi dan fleksibilitas yang lebih baik untuk pengembangan aplikasi. Kelemahan yang melekat, seperti risiko stack overflow, dapat diabaikan karena ruang lingkup input yang terbatas pada tiga huruf.

Penggunaan algoritma rekursif memberikan bukti nyata bahwa pemilihan algoritma yang sesuai dapat memberikan dampak signifikan pada performa sistem. Hal ini menegaskan pentingnya evaluasi mendalam dalam memilih metode komputasi yang paling tepat, bahkan untuk aplikasi dengan tugas yang terbilang sederhana.

## Referensi
[1] S. Author, "Ramalan Di Era Digital: Pengaruh Video Tiktok Terkait Kepercayaan Remaja Kepada," ResearchGate. [Online]. Available: https://www.researchgate.net/publication/376456580_Ramalan_Di_Era_Digital_Pengaruh_Video_Tiktok_Terkait_Kepercayaan_Remaja_Kepada. [Accessed: Dec. 22, 2024].

[2] S. Author, "Analysis of Japanese Culture Through Modern Media," Japanology Journal. [Online]. Available: https://journal.unair.ac.id/download-fullpapers-japanology87dbefda8b2full.pdf. [Accessed: Dec. 22, 2024].

[3] D. E. Knuth, The Art of Computer Programming, Volume 1: Fundamental Algorithms, Addison-Wesley, 1973.

[4] T. H. Cormen, C. E. Leiserson, R. L. Rivest, and C. Stein, Introduction to Algorithms, 3rd ed. MIT Press, 2009.

[5] R. Sedgewick and K. Wayne, Algorithms, 4th ed. Addison-Wesley, 2011.
