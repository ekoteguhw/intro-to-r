# Chart and Graphic Plotting

## Coding Dasar

### Membaca file excel

Terdapat file excel petugas.xlsx dengan kolom `No, Nama, Pekerjaan, BertugasSebagai, NilaiPendalaman`

```r
# Package openxlsx
library(openxlsx)
# Membaca file petugas.xlsx
petugas <- read.xlsx("http://ekoteguh.my.id/petugas.xlsx", sheet="Sheet1")
# Tampilkan
petugas
# Tampilkan kolom usia
petugas$Pekerjaan
```

### Membuat Grafik sebaran Petugas

Terdapat file excel pns.xlsx dengan kolom `no, kementrian_lembaga, jumlah`

```r
# Package ggplot2
library(ggplot2)
# Package openxlsx
library(openxlsx)
# Membaca file pns.xlsx
pns <- read.xlsx("http://ekoteguh.my.id/pns.xlsx", sheet="Sheet1")
kl <- pns$kementrian_lembaga
jumlah <- pns$jumlah
# Tampilkan
gambar <- ggplot(pns, aes(x=kl, y=jumlah, fill=kl))
gambar <- gambar + geom_bar(width=1, stat="identity")
gambar
# Menambahkan judul grafik
gambar <- gambar + ggtitle("Jumlah PNS menurut Kementrian/Lembaga")
# Menambahkan caption pada sumbu x
gambar <- gambar + xlab("Kementrian/Lembaga")
# Menambahkan caption pada sumbu y
gambar <- gambar + ylab("Jumlah PNS")
# Edit Legenda
gambar <- gambar + guides(fill=guide_legend(title="Kementrian/Lembaga"))
# Menggambar grafik
gambar
```
