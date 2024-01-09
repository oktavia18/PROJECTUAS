# PROJECTUAS
## Link video https://youtu.be/MgF4l7rhTI0?si=jQ2teI04VSZd6_eJ

### Tugas Project UAS 
Buat program sederhana kasir di sebuah kantin, dengan kondisi berikut:

- List opsi pilihan makanan/minuman dan aksi, bisa menggunakan format dectionary
- program harus meminta input pilihanmakanan dari pengguna
- program harus menghitung total harga makanan yang dipesan.
- program harus menampilkan struk pembelian.

## Penjelasan Program

### Membuat dictionary dan Menambahkan daftar barang
```Python
def daftar_barang():
    print("| No |  Makanan/Minuman   | Harga |")
    print("-------------------------------")
    print("| 1  | Tempe Mendoan      | 1000  |")
    print("| 2  | Pangsit Kuah       | 5000  |")
    print("| 3  | Gyoza              | 1000  |")
    print("| 4  | Matcha Milk Ice    | 5000  |")
    print("| 5  | Teh Manis          | 3000  |")

    print("-------------------------------")
    kode = int(input("Masukkan angka makanan  : "))
    if kode == 1:
        jumlah1 = int(input("Masukkan jumlah makanan : "))
        total1 = 1000 * jumlah1
        total.append(total1)
        tanya()
    elif kode == 2:
        jumlah2 = int(input("Masukkan jumlah makanan : "))
        total2 = 5000 * jumlah2
        total.append(total2)
        tanya()
    elif kode == 3:
        jumlah3 = int(input("Masukkan jumlah makanan : "))
        total3 = 1000 * jumlah3 
        total.append(total3)
        tanya()
    elif kode == 4:
        jumlah4 = int(input("Masukkan jumlah makanan : "))
        total4 = 5000 * jumlah4
        total.append(total4)
        tanya()
    elif kode == 5:
        jumlah5 = int(input("Masukkan jumlah makanan : "))
        total5 = 3000 * jumlah5   
        total.append(total5)
        tanya()
    return
```
`if c.lower` Berfungsi seperti `or` input bisa berjalan jika memasukan T/t<br>

### Penjelasan program input barang

- def daftar_barang():: Ini adalah definisi dari fungsi daftar_barang. Fungsi ini digunakan untuk menampilkan daftar makanan/minuman dan meminta input dari pengguna.
- print("| No | Makanan/Minuman | Harga |"): Menampilkan header tabel untuk daftar makanan/minuman beserta harga.
- print("-------------------------------"): Menampilkan garis pemisah untuk memisahkan header dengan isi tabel.
- kode = int(input("Masukkan angka makanan : ")): Mengambil input dari pengguna berupa nomor makanan/minuman yang dipilih.
- if kode == 1: ... elif kode == 2: ... elif kode == 3: ...: Menjalankan blok kode sesuai dengan nomor makanan/minuman yang dimasukkan pengguna. Setiap blok meminta input jumlah makanan/minuman dan menghitung total harga berdasarkan harga per item.
- total.append(total1): Menambahkan total harga makanan/minuman ke dalam daftar total. Sebaiknya pastikan bahwa total telah didefinisikan sebelumnya di program.
- tanya(): Memanggil fungsi tanya() setelah menghitung total untuk melanjutkan eksekusi program ke bagian selanjutnya
- return: Mengakhiri eksekusi fungsi daftar_barang.

### program Tambahan barang
```Python
def tanya():
    print("\n-------------------------------")
    tanya = input("Ingin tambah menu lainnya? [y/t] : ")
    print("-------------------------------")
    if tanya == "y":
        daftar_barang()
    elif tanya == "t":
        akhir()
    else:
        print("Pilihan yang anda masukan salah!")
```
### penjelasan kode program tambah barang

