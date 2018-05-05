# Vector, List dan Data Frame

## Coding Dasar

### Vector

Vector hanya dapat menyimpan satu jenis data (numeric saja atau character saja)

```r
# Vektor numeric 3 angka
c(1, 2, 3)
# Assign ke dalam suatu variabel
angka <- c(1, 2, 3)
# Tampilkan
angka
# Vektor numeric dengan urutan angka yang pasti
c(1:10)
# Assign ke dalam suatu variabel
angka2 <- c(1:10)
# Tampilkan
angka2
# Vektor dengan karakter
pegawai <- c("Eko", "Teguh", "Widodo")
# Tampilkan
pegawai
```

### Vector Index dan Accessor

```r
# Vektor dengan isian 10-20
angka <- c(10:20)
# Tampilkan isian pada posisi ke-5
angka[5]
# Tampilkan isian pada posisi ke-8
angka[[8]]
# Tampilkan isian pada posisi 5-8
angka[5:8]
```

### Named Vector

```r
# Buat identitas_pegawai
identitas_pegawai <- c(nama="Teguh", alamat="Bandar Lampung", no_hp="08xx12345678")
# Tampilkan identitas_pegawai
identitas_pegawai
# Tampilkan nama dari identitas_pegawai
identitas_pegawai["nama"]
```

### List

List dapat menyimpan lebih dari satu jenis data

```r
# Buat variabel pegawai
pegawai <- list("Teguh", 29, 174.99)
# Tampilkan
pegawai
# Buat variabel identias_pegawai
identitas_pegawai <- list(nama="Teguh", usia=29, tinggi=174.99)
# Tampilkan
identitas_pegawai
```

Tampilan dari output `pegawai` agak berbeda dengan vector, dimana tiap output terdapat dua tampilan accessor (kurung siku tunggal dan ganda). Sedangkan untuk output `identitas_pegawai` juga terdapat tampilan yang berbeda dengan vector, yaitu tampilan pertama terdapat tanda `$` disertai key, tampilan kedua terdapat accessor disertai value.

### List Index

Caranya sama persis seperti vector.

```r
# Buat variabel pegawai
pegawai <- list("Teguh", 29, 174.99)
# Tampilkan index kedua []
pegawai[2]
# Tampilkan index kedua [[]]
pegawai[[2]]
# Tampilkan index kedua sd ketiga
pegawai[2:3]
```

### Data Frame

Data frame adalah jenis struktur data yang dirancang untuk representasi table, yang terdiri dari banyak kolom dengan tiap kolom berisi list ataupun vector dengan jumlah data yang sama. Untuk membuat data frame kita bisa gunakan function `data.frame`.

```r
# Buat vector nama_petugas
nama_petugas <- c("Eko", "Teguh", "Widodo")
# Buat vector bertugas_sebagai
bertugas_sebagai <- c("PML", "PCL", "PCL")
# Buat data frame petugas dari dua vector di atas
petugas <- data.frame(nama_petugas, bertugas_sebagai)
# Tampilkan
petugas
# Buat vector baru nilai_pendalaman
nilai_pendalaman <- c(90, 85, 80)
# Tambahkan ke dalam data frame di atas
petugas <- data.frame(nama_petugas, bertugas_sebagai, nilai_pendalaman)
# Tampilkan
petugas
```

### Cara Akses Data Frame

Gunakan accessor dengan tanda `$` diikuti nama kolom.

```r
# Buat vector nama_petugas
nama_petugas <- c("Eko", "Teguh", "Widodo")
# Buat vector bertugas_sebagai
bertugas_sebagai <- c("PML", "PCL", "PCL")
# Buat data frame petugas dari dua vector di atas
petugas <- data.frame(nama_petugas, bertugas_sebagai)
# Tampilkan
petugas
# Buat vector baru nilai_pendalaman
nilai_pendalaman <- c(90, 85, 80)
# Tambahkan ke dalam data frame di atas
petugas <- data.frame(nama_petugas, bertugas_sebagai, nilai_pendalaman)
# Tampilkan
petugas
# Akses kolom nilai_pendalaman
petugas$nilai_pendalaman
```
