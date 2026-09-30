# Dataset — Indonesian Religious Corpus

## 1. Identitas Dataset

| Informasi     | Detail                                                               |
| ------------- | -------------------------------------------------------------------- |
| Nama Dataset  | Indonesian Religious Corpus                                          |
| Sumber        | Hugging Face                                                         |
| Repository    | `dansachs/indonesian-religious-corpus`                               |
| URL           | https://huggingface.co/datasets/dansachs/indonesian-religious-corpus |
| Format        | CSV                                                                  |
| File Raw      | `data.csv`                                                           |
| Bahasa        | Bahasa Indonesia                                                     |
| License       | MIT                                                                  |
| Jenis Data    | Data teks / korpus bahasa                                            |
| Unit Analisis | Unit kalimat (`Sentence_Unit`)                                       |

## 2. Deskripsi Dataset

**Indonesian Religious Corpus** merupakan dataset korpus teks berbahasa Indonesia yang berisi kumpulan unit kalimat dari berbagai sumber daring yang berkaitan dengan konten keagamaan.

Dataset menyediakan teks dalam bahasa Indonesia beserta sejumlah metadata, seperti label, denominasi, judul dokumen, sumber asli, lokasi, dan tanggal apabila informasi tersebut tersedia.

Dataset digunakan dalam proyek ini sebagai objek **Big Data Analytics** untuk mempelajari karakteristik, kualitas, distribusi, serta pola yang terdapat pada korpus teks berukuran besar.

Analisis difokuskan pada karakteristik dan kualitas data, bukan pada penilaian terhadap agama atau keyakinan tertentu.

## 3. Ukuran Dataset

Berdasarkan informasi pada repository sumber:

* **Ukuran:** sekitar 982 MB
* **Jumlah data:** sekitar 3 juta unit kalimat
* **Format:** CSV
* **Split:** `train`

Jumlah baris aktual akan diverifikasi kembali menggunakan **Polars** pada `01_data_profiling.ipynb`.

## 4. Unit Analisis

Unit analisis utama dalam dataset adalah **unit kalimat (sentence unit)**.

Setiap baris merepresentasikan satu unit teks atau kalimat yang berasal dari sumber daring.

Variabel teks utama:

```text
Sentence_Unit
```

## 5. Struktur Data

| Kolom           | Deskripsi                                |
| --------------- | ---------------------------------------- |
| `Label`         | Label atau kategori utama pada data      |
| `Denomination`  | Informasi denominasi/kategori keagamaan  |
| `Title`         | Judul dokumen atau halaman sumber        |
| `Sentence_Unit` | Unit kalimat yang menjadi objek analisis |
| `Original_Link` | Tautan sumber asli data                  |
| `Location`      | Informasi lokasi apabila tersedia        |
| `Date`          | Informasi tanggal apabila tersedia       |

> Struktur kolom aktual akan diverifikasi kembali pada tahap profiling.

## 6. Sumber Data

Dataset diperoleh dari:

**Indonesian Religious Corpus**

Repository: `dansachs/indonesian-religious-corpus`

URL: https://huggingface.co/datasets/dansachs/indonesian-religious-corpus

## 7. Penyimpanan Raw Data

Data mentah disimpan pada:

```text
data/
└── raw/
    └── data.csv
```

File `data.csv` merupakan **raw data** dan tidak dimodifikasi secara langsung.

Proses cleaning dan transformasi dilakukan pada data hasil pemrosesan yang disimpan secara terpisah.

## 8. Penggunaan Dataset

Dataset digunakan dalam tiga tahap utama:

### 8.1 Data Profiling

Dilakukan pemeriksaan terhadap:

* jumlah baris dan kolom;
* ukuran file;
* nama kolom;
* tipe data;
* missing values;
* duplicate records;
* statistik deskriptif;
* distribusi label;
* distribusi denominasi;
* karakteristik panjang teks;
* informasi tanggal;
* informasi lokasi.

### 8.2 Data Cleaning

Proses cleaning meliputi:

* pemeriksaan missing values;
* pemeriksaan data duplikat;
* standardisasi tipe data;
* standardisasi format data;
* pembersihan whitespace;
* pemeriksaan kualitas teks;
* pembuatan fitur turunan;
* validasi hasil cleaning.

Contoh fitur turunan:

```text
text_length
word_count
title_length
```

### 8.3 Exploratory Data Analysis

EDA dilakukan untuk menganalisis:

* distribusi label;
* distribusi denominasi;
* pola data berdasarkan waktu;
* distribusi lokasi;
* distribusi panjang kalimat;
* distribusi panjang judul;
* distribusi sumber data;
* perubahan jumlah data berdasarkan periode;
* karakteristik teks berdasarkan kategori.

Visualisasi dibuat menggunakan **Plotly/Altair**.

## 9. Teknologi yang Digunakan

| Teknologi        | Penggunaan                                                |
| ---------------- | --------------------------------------------------------- |
| Polars           | Membaca, membersihkan, mentransformasi, dan mengolah data |
| DuckDB           | Analytical query menggunakan SQL                          |
| Plotly / Altair  | Visualisasi interaktif                                    |
| Jupyter Notebook | Dokumentasi dan eksekusi analisis                         |
| Docker           | Reproduksibilitas lingkungan analisis                     |

## 10. Lisensi

Dataset mencantumkan **MIT License** pada repository sumber.

Penggunaan dataset dalam proyek ini ditujukan untuk keperluan pembelajaran dan analisis akademik.

Ketentuan penggunaan mengacu pada lisensi yang tercantum pada repository dataset sumber.

Sumber:

https://huggingface.co/datasets/dansachs/indonesian-religious-corpus

## 11. Alasan Pemilihan Dataset

Indonesian Religious Corpus dipilih karena memiliki ukuran data yang besar dan memenuhi kriteria ukuran dataset yang ditetapkan dalam tugas.

Dataset juga memiliki struktur data yang memungkinkan penerapan proses **Big Data Analytics** menggunakan:

* **Polars** untuk data processing;
* **DuckDB** untuk analytical query;
* **Plotly/Altair** untuk visualisasi;
* **Jupyter Notebook** untuk dokumentasi analisis.

Dataset digunakan untuk menghasilkan analisis mengenai karakteristik, kualitas, distribusi, dan pola data berdasarkan metadata serta karakteristik teks.

## 12. Ketentuan Raw Data

File raw:

```text
data/raw/data.csv
```

tidak dimodifikasi secara langsung.

Seluruh proses cleaning dan transformasi dilakukan pada hasil pemrosesan yang disimpan secara terpisah.

Karena ukuran dataset besar, file raw tidak disertakan dalam repository GitHub apabila melebihi batas penyimpanan repository.

## 13. Referensi

dansachs. **Indonesian Religious Corpus**. Hugging Face Datasets.

https://huggingface.co/datasets/dansachs/indonesian-religious-corpus
