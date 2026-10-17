# Data Visualisasi Dataset Titanic

Repository ini berisi latihan visualisasi data menggunakan Python di Google Colab. Notebook menggunakan dataset Titanic yang telah dibersihkan (`titanic_train_clean.csv`) untuk memeriksa ringkasan statistik dan memvisualisasikan distribusi variabel, fitur kategori, serta korelasi antarvariabel.

## Informasi Notebook

- **Nama notebook:** `2318120_DataVisualisasi.ipynb`
- **Platform:** Google Colab
- **Dataset:** `titanic_train_clean.csv`
- **Jumlah data:** 891 baris
- **Jumlah kolom:** 19 kolom

## Kolom Dataset

Beberapa kolom yang digunakan dalam visualisasi antara lain:

| Kolom | Keterangan berdasarkan nama kolom |
|---|---|
| `Survived` | Status keselamatan penumpang |
| `Pclass` | Kelas penumpang |
| `Sex` | Jenis kelamin yang telah dikodekan |
| `Age` | Usia penumpang |
| `SibSp` | Jumlah saudara/pasangan yang tercatat |
| `Parch` | Jumlah orang tua/anak yang tercatat |
| `Has_Cabin` | Indikator keberadaan informasi kabin |
| `FamilySize` | Ukuran keluarga hasil rekayasa fitur |
| `IsAlone` | Indikator bepergian sendirian |
| `Fare_Log` | Nilai tarif setelah transformasi log |
| `Embarked_Q`, `Embarked_S` | Kolom hasil encoding pelabuhan keberangkatan |
| `Title_*` | Kolom hasil one-hot encoding gelar penumpang |
| `Age_Group_*` | Kolom kategori usia hasil feature engineering |

## Tujuan

Latihan ini bertujuan untuk memahami karakteristik dataset melalui ringkasan statistik dan visualisasi, sehingga pola distribusi data serta hubungan antarvariabel dapat diamati dengan lebih mudah.

## Teknologi dan Library

Notebook menggunakan beberapa library Python berikut:

- **Pandas** untuk membaca dan mengelola data berbentuk DataFrame.
- **NumPy** untuk kebutuhan komputasi numerik.
- **Matplotlib** untuk membuat dan mengatur grafik.
- **Seaborn** untuk membuat visualisasi statistik.
- **Google Colab Drive** untuk mengakses file dataset yang disimpan di Google Drive.

## Cara Menjalankan Notebook

1. Buka [Google Colab](https://colab.research.google.com/).
2. Unggah file `2318120_DataVisualisasi.ipynb` atau buka notebook dari repository GitHub.
3. Siapkan file dataset `titanic_train_clean.csv`.
4. Jika menggunakan Google Drive, simpan dataset di lokasi yang sesuai dengan path pada notebook:
   `MyDrive/Colab Notebooks/titanic_train_clean.csv`
5. Jalankan setiap sel secara berurutan.

Jika dataset disimpan di lokasi lain, sesuaikan variabel `file_path` pada notebook dengan lokasi file yang sebenarnya.

## Tahapan Latihan

### 1. Persiapan Environment dan Import Library

Mengimpor library yang diperlukan dan mengatur tema visualisasi menggunakan Seaborn serta konfigurasi font Matplotlib.

### 2. Memeriksa Ringkasan Statistik Data

Membaca dataset `titanic_train_clean.csv`, menampilkan lima baris pertama, memeriksa tipe data dan kelengkapan kolom menggunakan `info()`, serta melihat ringkasan statistik numerik menggunakan `describe()`.

Dataset yang digunakan memiliki 891 baris dan 19 kolom. Berdasarkan pemeriksaan pada notebook, setiap kolom memiliki 891 nilai terisi.

### 3. Visualisasi Distribusi Variabel Numerik

Membuat dua visualisasi:
- Histogram dengan kurva KDE untuk melihat distribusi usia penumpang (`Age`) setelah imputasi.
- Kurva KDE untuk mengamati distribusi nilai tarif (`Fare_Log`) setelah transformasi log.

### 4. Visualisasi Fitur Kategori dan Feature Engineering

Membuat visualisasi untuk mengamati:
- Frekuensi gelar penumpang dari kolom hasil one-hot encoding, seperti `Title_Miss`, `Title_Mr`, `Title_Mrs`, dan `Title_Rare`.
- Distribusi ukuran keluarga melalui kolom `FamilySize`.
- Perbandingan penumpang yang bepergian sendirian dan tidak sendirian melalui kolom `IsAlone` (`0` = tidak sendirian, `1` = sendirian).

### 5. Visualisasi Matriks Korelasi

Membuat heatmap berdasarkan korelasi antarvariabel pada dataset. Nilai korelasi ditampilkan dalam format dua angka desimal dengan rentang warna dari -1 hingga 1 untuk membantu melihat arah dan kekuatan hubungan linear antarvariabel.

## Hasil yang Diharapkan

Setelah seluruh sel dijalankan, notebook menampilkan:
- Lima baris pertama dataset.
- Informasi struktur kolom dan ringkasan statistik.
- Histogram distribusi usia dan kurva KDE `Fare_Log`.
- Grafik frekuensi gelar, ukuran keluarga, dan status bepergian sendirian.
- Heatmap korelasi antarvariabel.
