# PROJECTUAS
## Link video : https://youtu.be/MgF4l7rhTI0?si=jQ2teI04VSZd6_eJ

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

### Program input barang

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
### Penjelasan kode program tambah barang

- def tanya():: Mendefinisikan fungsi bernama tanya().
- print("\n-------------------------------"): Menampilkan garis pemisah untuk memisahkan output dari bagian sebelumnya dengan pertanyaan yang akan diajukan kepada pengguna.
- tanya = input("Ingin tambah menu lainnya? [y/t] : "): Mengambil input dari pengguna berupa 'y' atau 't', yang menunjukkan apakah mereka ingin menambahkan menu lainnya atau tidak.
- print("-------------------------------"): Menampilkan garis pemisah setelah pengguna memberikan jawaban.
- if tanya == "y":: Melakukan pengecekan apakah jawaban pengguna adalah 'y' (yes).
Jika benar, maka memanggil fungsi daftar_barang(). Ini berarti pengguna ingin menambahkan menu lainnya, dan daftar menu akan ditampilkan kembali. Jika tidak, maka melanjutkan ke langkah berikutnya.
- elif tanya == "t":: Melakukan pengecekan apakah jawaban pengguna adalah 't' (tidak). Jika benar, maka memanggil fungsi akhir(). Ini berarti pengguna telah selesai memilih menu, dan program akan melanjutkan ke tahap selanjutnya (mungkin menampilkan total belanja dan proses pembayaran). Jika tidak, maka lanjut ke langkah berikutnya.
- else:: Menangani kondisi di mana jawaban pengguna tidak valid (bukan 'y' atau 't'). Menampilkan pesan bahwa pilihan yang dimasukkan pengguna salah.

### Program harga diskon dan struk pembelian
```Python
def akhir():
    for harga in total:
        print("SubTotal         : ", sum(total))
        diskon = 0
        a = sum(total)
        if a > 500000:
            diskon = a * 8/100
        elif a > 300000:
            diskon = a * 5/100
        elif a > 200000:
            diskon = a * 3/100
        elif a > 100000:
            diskon = a * 1/100
        else:
            diskon = 0
        print("Potongan Harga   : ", diskon)
        totalakhir = a - diskon
        print("Total            : ", totalakhir)
        print("-------------------------------")
        bayar = int(input("Bayar            :  "))
        kembalian = bayar - totalakhir
        print("Kembalian        : ", kembalian)
        print("-------------------------------")
        print("          Terima Kasih         ")
        print("-------------------------------")
daftar_barang()
print("Terima kasih sudah belanja ")
```

### Penjelasan Program harga diskon dan struk pembelian

- def akhir():: Mendefinisikan fungsi akhir() yang digunakan untuk menghitung subtotal, diskon, total akhir, serta melakukan proses pembayaran dan menghitung kembalian.
- for harga in total:: Menggunakan perulangan for untuk mengakses setiap elemen dalam daftar total. Ini diasumsikan bahwa total adalah daftar yang menyimpan total harga dari setiap item yang dibeli oleh pengguna.
- print("SubTotal : ", sum(total)): Menampilkan subtotal, yaitu jumlah dari semua elemen dalam daftar total.
- diskon = 0: Menginisialisasi variabel diskon dengan nilai awal 0.
- a = sum(total): Menyimpan nilai subtotal dalam variabel a untuk digunakan dalam perhitungan diskon dan total akhir.
- f a > 500000: ... elif a > 300000: ... elif a > 200000: ... elif a > 100000: ... else:: Menghitung diskon berdasarkan nilai subtotal a. Jika nilai subtotal lebih besar dari suatu batas tertentu, maka diberikan diskon sesuai dengan kondisi yang sesuai.
- totalakhir = a - diskon: Menghitung total akhir setelah memperhitungkan diskon.
- print("Potongan Harga : ", diskon): Menampilkan jumlah diskon yang diberikan.
- print("Total : ", totalakhir): Menampilkan total akhir setelah diskon.
- kembalian = bayar - totalakhir: Menghitung kembalian dengan mengurangkan total akhir dari jumlah uang yang dibayarkan.
- daftar_barang(): Memanggil fungsi daftar_barang(), yang mungkin berisi logika untuk menampilkan daftar barang dan menghitung total pembelian.
- print("Terima kasih sudah belanja "): Menampilkan pesan terima kasih setelah seluruh proses pembelian selesai.

### Cara Penggunaan

1. Pilih opsi sesuai dengan barang yang akan di pilih
2. Ikuti petunjuk yang muncul untuk setiap opsi, dan program akan merespons sesuai.
3. Program akan terus berjalan hingga pengguna memilih untuk tidak menambahkan barang.
