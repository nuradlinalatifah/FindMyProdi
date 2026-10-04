# FindMyProdi

FindMyProdi adalah aplikasi sederhana yang membantu pengguna mencari rekomendasi program studi berdasarkan kata kunci yang dimasukkan.

Project ini dibuat menggunakan Streamlit dan menerapkan beberapa konsep pencarian, yaitu Binary Search Tree (BST), Binary Search, dan Regular Expression (Regex).

## Fitur

* Mencari program studi berdasarkan kata kunci.
* Menampilkan hasil pencarian dari Binary Search dan Regex.
* Menampilkan detail program studi.
* Menampilkan gambaran Binary Search Tree.
* Menampilkan penjelasan algoritma yang digunakan.
* Membandingkan waktu pencarian Binary Search dan Regex.

## Struktur Project

```text
FindMyProdi/
│
├── app.py
├── engine.py
├── data_keywords.py
├── data_details.py
└── README.md
```

### Penjelasan File

**app.py**
Berisi tampilan utama aplikasi menggunakan Streamlit, mulai dari halaman awal, input kata kunci, hasil pencarian, detail prodi, sampai halaman penjelasan sistem.

**engine.py**
Berisi proses pencarian dan struktur data yang digunakan. Di dalamnya terdapat Binary Search Tree, Binary Search, Regex Search, dan fungsi utama `search_prodi()`.

**data_keywords.py**
Berisi data kata kunci yang sudah dihubungkan dengan program studi.

**data_details.py**
Berisi informasi lebih lengkap mengenai program studi yang ditampilkan pada halaman detail.

**README.md**
Berisi penjelasan mengenai project dan cara menjalankannya.

## Teknologi yang Digunakan

* Python
* Streamlit
* Matplotlib
* Regular Expression (`re`)

## Cara Menjalankan

Pastikan Python sudah terinstall. Setelah itu install library yang diperlukan:

```bash
pip install streamlit matplotlib
```

Kemudian jalankan aplikasi dengan:

```bash
streamlit run app.py
```

Aplikasi akan terbuka melalui browser.

## Cara Kerja Sistem

Pengguna memasukkan kata kunci yang berkaitan dengan minat atau bidang yang ingin dicari.

Contohnya:

```text
python
```

Sistem kemudian melakukan pencarian menggunakan dua metode:

1. **Binary Search**
2. **Regex Search**

Hasil dari pencarian kemudian digunakan untuk menampilkan rekomendasi program studi beserta detailnya.

## Algoritma yang Digunakan

### 1. Binary Search Tree

Data kata kunci dimasukkan ke dalam Binary Search Tree atau BST. Setelah itu, data diambil kembali menggunakan traversal inorder sehingga menghasilkan data yang terurut.

Data terurut tersebut digunakan sebagai dasar untuk melakukan Binary Search.

### 2. Binary Search

Binary Search digunakan untuk mencari kata kunci yang sama persis.

Cara kerjanya adalah dengan mengambil elemen tengah dari data yang sudah terurut. Jika kata kunci yang dicari lebih kecil, pencarian dilanjutkan ke bagian kiri. Jika lebih besar, pencarian dilanjutkan ke bagian kanan.

Metode ini memiliki kompleksitas rata-rata `O(log n)` karena setiap pencarian dapat mengurangi sekitar setengah bagian data yang perlu diperiksa.

### 3. Regex

Regex digunakan untuk mencari kata yang memiliki kecocokan sebagian dengan input pengguna.

Contohnya, pengguna tidak harus memasukkan kata secara lengkap. Jika data memiliki kata `digital`, input seperti `dig` masih dapat ditemukan oleh Regex.

Regex juga digunakan secara case-insensitive sehingga perbedaan huruf besar dan kecil tidak menjadi masalah.

## Perbandingan Pencarian

| Metode        | Cara Mencari                                   | Kelebihan                               |
| ------------- | ---------------------------------------------- | --------------------------------------- |
| Binary Search | Mencari kata kunci yang sama pada data terurut | Cepat untuk exact match                 |
| Regex         | Mencari pola atau bagian kata                  | Lebih fleksibel untuk pencarian parsial |

Kedua metode digunakan bersama karena memiliki fungsi yang berbeda. Binary Search digunakan untuk pencarian yang lebih spesifik, sedangkan Regex membantu menemukan hasil ketika input pengguna hanya berupa sebagian kata.

## Halaman pada Aplikasi

Aplikasi terdiri dari beberapa bagian:

* **Halaman Awal** — halaman pembuka FindMyProdi.
* **Input** — tempat pengguna memasukkan kata kunci.
* **Hasil** — menampilkan hasil pencarian program studi.
* **Detail Prodi** — menampilkan informasi lebih lengkap tentang prodi yang dipilih.
* **BST** — menampilkan struktur atau proses yang berkaitan dengan Binary Search Tree.
* **Algoritma** — menjelaskan algoritma yang digunakan dalam sistem.
* **Penutup** — halaman akhir aplikasi.
* **Deskripsi Sistem** — menjelaskan cara kerja sistem dan metode pencarian.

## Contoh Pencarian

Jika pengguna memasukkan:

```text
python
```

sistem dapat menemukan beberapa program studi yang memiliki kata kunci tersebut, seperti:

* Teknik Informatika
* Sains Data
* Kecerdasan Artifisial

Hasil yang ditampilkan kemudian dapat dipilih untuk melihat detail program studi.

## Tujuan Project

Project ini dibuat sebagai penerapan materi struktur data dan algoritma, khususnya penggunaan Binary Search Tree dan metode pencarian dalam sebuah aplikasi sederhana.

## Anggota Kelompok

* Najla (041)
* Alin (068)
* Moza (185)

## Catatan

FindMyProdi merupakan project pembelajaran yang dibuat untuk keperluan perkuliahan.
