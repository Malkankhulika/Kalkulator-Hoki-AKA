# Analisis-Kompleksitas-Algoritma
TUBES AKA
# <h1 align="center">Classification_MonkeyPox</h1>
<p align="center">Khulika Malkan</p>
<p align="center">2311110057</p>

## Features

- [Gambaran Umum MonkeyPox](#GambaranumumMonkeyPox)
- [About Dataset](#AboutDataset)
- [Code](#Code)
- [Output](#Output)
- [Kesimpulan](#Kesimpulan)

## Gambaran Umum MonkeyPox
![image](https://github.com/user-attachments/assets/caecf5dc-1c1a-42b5-87ca-7684067f2f56)

Pada Mei 2022, wabah monkeypox, sebuah penyakit virus, dikonfirmasi terjadi. Kasus pertama ditemukan di Inggris pada 6 Mei 2022, pada individu yang memiliki riwayat perjalanan ke Nigeria, tempat penyakit ini endemik. Wabah ini menandai pertama kalinya monkeypox menyebar secara luas di luar Afrika Tengah dan Barat. Mulai 18 Mei, kasus terus dilaporkan dari berbagai negara dan wilayah, terutama di Eropa, tetapi juga di Amerika Utara dan Selatan, Asia, Afrika, serta Oseania. Pada 23 Juli, Direktur Jenderal Organisasi Kesehatan Dunia (WHO), Tedros Adhanom Ghebreyesus, menyatakan wabah ini sebagai darurat kesehatan masyarakat yang menjadi perhatian internasional (PHEIC). Hingga 12 Agustus, tercatat 34.448 kasus terkonfirmasi di lebih dari 82 negara, dengan sebagian besar negara mengalami kasus pertama mereka.


Monkeypox adalah infeksi virus yang biasanya muncul sekitar satu hingga dua minggu setelah paparan. Gejalanya diawali dengan demam dan gejala tidak spesifik lainnya, diikuti dengan munculnya ruam dan lesi yang berlangsung selama 2–4 minggu sebelum kering, mengeras, dan terkelupas. Meski dapat menyebabkan banyak lesi, pada wabah saat ini beberapa pasien hanya mengalami satu lesi, biasanya di mulut atau area genital, sehingga lebih sulit dibedakan dari infeksi lainnya. Dalam infeksi sebelum wabah ini, sekitar 1–3 persen penderita yang terdiagnosis diketahui meninggal jika tidak mendapatkan pengobatan. Kasus pada anak-anak dan individu dengan gangguan kekebalan lebih berisiko menjadi parah.


## About Dataset
![image](https://github.com/user-attachments/assets/2b8fa5bf-42ee-41fa-b6b5-4f2f4235b177)

Dataset ini terdiri dari dua folder utama:
1.	Original Images:
Folder ini berisi subfolder bernama "FOLDS," yang terdiri dari lima fold (fold1 hingga fold5) yang digunakan untuk validasi silang 5-fold. Setiap fold memiliki subfolder terpisah untuk dataset test, train, dan validation.

3.	Augmented Images:
Folder ini memiliki subfolder bernama "FOLDS_AUG," yang berisi gambar augmented dari set train di setiap fold yang ada dalam subfolder "FOLDS" di "Original Images." Proses augmentasi ini meningkatkan jumlah gambar hingga sekitar 14 kali lipat dari jumlah aslinya.
