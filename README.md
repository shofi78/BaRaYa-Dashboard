# BaRaYa (Bayi Juara Wargi Sadaya)-Dashboard

## **Latar Belakang**
Anak - anak indonesia adalah aset bangsa yang paling berharga, yang akan menentukan masa depan bangsa. Pilihan kebijakan dan investasi pemerintah untuk anak Indonesia yang diambil pada hari ini akan berdampak besar terhadap masa depan Indonesia. Di provinsi Jawa Barat, angka kelahiran bayi tercatat mencapai 2.5 persen, sementara jumlah penduduk Jawa Barat juga menduduki peringkat tertinggi di Indonesia.

Dalam kaitannya dengan angka kelahiran bayi yang tinggi, pemerintah Jawa Barat perlu melakukan planning yang tepat untuk membentuk generasi masa depan yang lebih baik, untuk itu pemerintah membutuhkan suatu sarana untuk memetakan kondisi bayi di Jawa Barat berdasarkan urutan prioritas berupa:
1. Daerah mana saja yang perlu menjadi fokus peningkatan kondisi dan gizi bayi
2. Penanganan secara preventif dan korektif yang perlu dilakukan di tiap daerah dengan berfokus pada faktor-faktor yang berpengaruh terhadap kondisi kesehatan bayi

## **Tujuan**
Bedasarkan latar belakang tersebut, akan dilakukan ‘Project Baraya’ dengan tujuan:
a. Merangking kondisi bayi berdasarkan faktor-faktor pengaruhnya di tiap kota & kabupaten di Jawa Barat
b. Menentukan faktor yang menjadi prioritas kebijakan di setiap rangking yang diperoleh suatu kota/ kabupaten di wilayah Jawa Barat

Hasil dari analisis tersebut akan disajikan dalan sebuah dashboard dengan sasaran user:
Pemerintah daerah/ Pemda Jawa Barat yang meliputi:
- Gubernur
- Walikota
- Bupati
- Kepala Desa
- Dinas Kesehatan

Dan dari dashboard tersebut dapat diperoleh insight berupa:
- Ranking/ pengurutan suatu daerah dengan kondisi bayi & balita ideal berdasarkan :
- Persebaran kondisi gizi bayi & balita di Jawa Barat
- Persebaran indeks kesehatan masyarakat & keluhan kesehatan masyarakat di Jawa Barat
- Persebaran pernikahan dini di Jawa Barat
- Ketersediaan layanan kesehatan berupa jumlah posyandu dan puskesmas di daerah tersebut

## **Overview dari Proses**

Project BaRaYa diawali dengan penentuan faktor-faktor apa saja yang berpengaruh 	terhadap kondisi bayi. Dari hasil diskusi, diperoleh beberapa faktor, yaitu:
Kondisi gizi bayi, Indeks kesehatan masyarakat, Jumlah pernikahan dini dan Ketersediaan layanan kesehatan.

Dari data set yang diperoleh, kemudian dilakukan EDA sebagai berikut;
1. Data Persebaran gizi bayi & balita, Persebaran kondisi kesehatan, Persebaran usia pernikahan dini, Jumlah fasilitas pelayanan kesehatan di tiap wilayah Jawa Barat menggunakan sorting.
    - Dalam proses ini dilakukan alignment data diurutkan berdasarkan tahun
    - Setelah dilakukan pembersihan data, data dikelompokkan berdasarkan kota & kabupaten
    - Dataset - dataset yang diperoleh disatukan berdasarkan nama kota/ kabupaten, dan tahun
    
2. Ranking bayi juara yang diperoleh dari indexing faktor gizi bayi, index kesehatan masyarakat, jumlah pernikahan dini, dan jumlah fasilitas pelayanan kesehatan di tiap wilayah Jawa barat, sebagai indikator wilayah mana yang menjadi prioritas kebijakan & yang menjadi achievement/ panutan.
    - Perangkingan dilakukan menggunakan modul pandas scikit criteria, yaitu modul perangkingan menggunakan multi criteria decision making yang menghasilkan score yang disebut bayi juara score (bj score).
    - Perangkingan dilakukan dengan mengurutkan BJ Score yang diperoleh, dimana BJ Score terbesar akan memperoleh rangking pertama, yang berarti kondisi bayi di daerah tersebut merupakan yang terbaik.
    - Rangking yang diperoleh dikelompokan kembali berdasarkan quartile, untuk memperoleh kriteria berdasarkan urutan rangking, berupa kelompok ‘Tinggi’, ‘Sedang’, dan ‘Rendah’.

Hasil EDA kemudian divisualisasikan menggunakan Tableau, dengan rancangan user flow sebagai berikut:

1. Sebagai seorang PNS ingin melihat overview ranking Bayi Juara di Jawa Barat & menentukan fokus kebijakan yang diperlukan
2. Membuka dashboard Bayi Juara Jabar
3. Melihat overview berupa peta wilayah ranking bayi juara berdasarkan pembobotan faktor gizi bayi dan balita, persebaran jumlah pernikahan dini, indeks kesehatan dan keluhan penyakit masyarakat, dan ketersediaan layanan kesehatan di tiap wilayah bagian Jawa barat.
4. Melihat detail hasil pembobotan nilai
5. Memilih satu atau lebih variabel yang mempengaruhi rangking Bayi Juara di Jawa barat berupa: jumlah persebaran gizi buruk bayi di tiap wilayah Jawa Barat, index nilai persebaran kondisi kesehatan di tiap wilayah di Jawa Barat, jumlah persebaran pernikahan dini di wilayah Jawa Barat, dan jumlah fasilitas pelayanan kesehatan di wilayah Jawa Barat
6. Setelah melihat detail indikator bayi juara, PNS dapat menentukan kebijakan yang sesuai sebagai langkah preventif dan korektif

Visualisasi user flow dapat dilihat pada [**link**](https://www.figma.com/file/Rwyx0yiboAYeepwh7IzoYz/User-Flow-PLBI-1---Grup-N?node-id=0%3A1) berikut.

Setelah memiliki user flow, langkah selanjut nya adalah membuat prototype. Pada tahap ini kita menyusun informasi apa yang perlu dilihat, dan interaksi apa yang dibutuhkan, untuk membantu user dalam merangking kondisi bayi berdasarkan faktor-faktor pengaruhnya dan memprioritaskan kebijakan pada rangking kab/kota yang diperoleh. Hi-Fi Prototype yang dibuat dapat dilihat pada [**link**](https://www.figma.com/file/2WG2ov0aagcRnTAT159xiq/Prototype-BaRaYa-Dashboard?node-id=0%3A1).

Dashboard ini mencakup:
* Simple overview untuk melihat rangking kab/kota yang menempati kelompok peringkat tinggi, medium, rendah.
* Menampilkan 5 kab/kota teratas dan terendah pada perangkingan Bayi Juara
* Persebaran distribusi Bayi Juara di Jabar
* Indikator yang dapat dipilih berdasarkan faktor-faktor pengaruhnya di tiap kota & kabupaten
* Rekomendasi sebagai langkah preventif dan korektif untuk setiap indikator yang dipilih

Dengan dashboard yang kami buat, diharapkan stakeholder mendapatkan informasi sebagai berikut:
* Mengetahui kab/kota mana yang harus diprioritaskan terlebih dahulu untuk fokus peningkatan kondisi dan gizi bayi
* Dapat melakukan penanganan secara preventif dan korektif di daerah yang memiliki rangking terendah dengan berfokus pada faktor-faktor yang berpengaruh terhadap kondisi kesehatan bayi

Secara umum, hambatan-hambatan yang kami hadapi dalam pembuatan dashboard ini adalah:
1. Ketersediaan data tidak terupdate setiap tahun sehingga sulit mendapatkan data yang align antara satu sama lain.
2. Adanya format data yang tidak terstandarisasi sehingga perlu penyeragaman.

## **MVP Demonstration**
Visualisasi di Tableau dibuat sebagai MVP (Minimum Viable Product) Dashboard, yang mana ke depannya akan dilakukan improvement sesuai dengan feedback dan kebutuhan user. Tampilan dashboard pada Tableau dapat dilihat pada [**link**](https://public.tableau.com/app/profile/shofi.f.ilmi/viz/BaRaYaDashboard-GroupN-PLBI1-Pacmann/Dashboard1) berikut.


![Dashboard 1](https://user-images.githubusercontent.com/102605912/189572139-c13e51cf-d57a-4467-92db-4115748a275e.png)

Pada bagian atas, terdapat hasil pengelompokan hasil rangking BJ Score menjadi 2 kelompok, dengan jumlah kota & kabupaten yang termasuk ke dalam kelompok tersebut, yaitu 7 kab/ kota yang termasuk kelompok ‘Tinggi’, 13 kab/ kota yang termasuk kelompok ‘Sedang’, dan 7 kab/ kota yang termasuk ke dalam kelompok ‘Rendah’.

**Fitur unggulan** dari dashboard kami tombol filter pilihan kab/kota dan pilihan indikator di **pojok kanan atas**. Melalui tombol tersebut, user dapat mengetahui faktor mana saja yang perlu menjadi prioritas penanganan untuk peningkatan kondisi bayi di wilayah tersebut. Selain itu, tombol tersebut dapat menampilkan rekomendasi sesuai dengan indikator yang dipilih.

## **Kesimpulan dan Analisis**
### Mengapa Bayi Juara?
Karena dashboard ini dapat memberikan insight terhadap prioritas daerah yang menggambarkan kondisi bayi yang dipengaruhi oleh beberapa faktor dalam hal ini faktor yang dipilih adalah persebaran gizi buruk bayi, jumlah pernikahan dini, indeks kesehatan masyarakat dan ketersediaan layanan kesehatan di tiap wilayah Jawa Barat. Sehingga kepala daerah, policy maker dan lembaga terkait dapat melakukan screening pertama untuk pencegahan kondisi stunting di masa depan untuk mengoptimalkan aspek-aspek tumbuh kembang anak di tiap-tiap daerah.

Ranking bayi juara yang diperoleh dari indexing faktor gizi bayi, index kesehatan masyarakat, jumlah pernikahan dini, dan jumlah fasilitas pelayanan kesehatan di tiap wilayah Jawa barat, sebagai indikator wilayah mana yang menjadi prioritas kebijakan & yang menjadi achievement/panutan di wilayah Jawa Barat.

## **Room for Improvement:**
* Perlu dilakukan analisis lebih lanjut untuk hasil BJ score di tahun-tahun yang belum tersedia
* Jumlah bayi bergizi buruk pada tiap daerah perlu dilakukan analisis lebih jauh dengan membandingkannya terhadap populasi jumlah bayi di daerah tersebut
* Perlu dilakukan analisis lebih lanjut terkait faktor-faktor lain yang juga berpengaruh terhadap kondisi bayi
* Dapat dilakukan uji coba dengan berbagai metode untuk menghasilkan hasil perangkingan yang lebih akurat


