## *1. Kalkulator sederhana*

Program pertama yang akan dibuat adalah Program untuk menampilkan angka pertama dan kedua dan masukan operator dan mendapat hasil dari input

Berikut flowchartnya

<img width="391" alt="Screenshot flochart kalkulator  2" src="https://github.com/user-attachments/assets/573c3cb7-fd25-4ea9-bb0a-2145a1c53cca">


*Program akan meminta kita untuk memasukkan 3 angka untuk dibandingkan :*

<img width="727" alt="output 2" src="https://github.com/user-attachments/assets/a253a51f-19e6-418f-845c-92b8b9cd535c">

*Penjelasan Code*

*1.*

```
def kalkulator():
  """Fungsi ini membuat kalkulator sederhana"""

  # Meminta input dari pengguna
  angka1 = float(input("Masukkan angka pertama: "))
  angka2 = float(input("Masukkan angka kedua: "))
  operator = input("Masukkan operator (+, -, *, /): ")

  # Melakukan operasi berdasarkan operator yang dipilih
  if operator == '+':
    hasil = angka1 + angka2
  elif operator == '-':
    hasil = angka1 - angka2
  elif operator == '*':
    hasil = angka1 * angka2
  elif operator == '/':
    if angka2 == 0:
      print("Tidak dapat membagi dengan nol")
    else:
      hasil = angka1 / angka2
  else:
    print("Operator tidak valid")

  # Menampilkan hasil
  if 'hasil' in locals():
    print("Hasil:", hasil)

kalkulator()
```

"""Fungsi ini membuat kalkulator sederhana""" Ini adalah komentar multi-baris yang menjelaskan tujuan dari fungsi kalkulator(). Komentar sangat penting dalam pemrograman untuk meningkatkan keterbacaan kode.
angka1 = float(input("Masukkan angka pertama: ")) 
angka2 = float(input("Masukkan angka kedua: ")) 
operator = input("Masukkan operator   
(+,-,*,/): ") Pada bagian ini, program meminta pengguna untuk memasukkan dua angka dan operator aritmatika yang ingin digunakan. Fungsi float() digunakan untuk mengonversi input pengguna menjadi bilangan desimal (float) agar bisa dilakukan operasi matematika.
Percabangan (if-elif-else): Kode ini menggunakan struktur kontrol if-elif-else untuk memeriksa nilai operator yang dimasukkan oleh pengguna. 
Jika operator adalah '+', maka akan dilakukan penjumlahan.
Jika operator adalah '-', maka akan dilakukan pengurangan.
Jika operator adalah '*', maka akan dilakukan perkalian.
Jika operator adalah '/', maka akan dilakukan pembagian.
Jika operator tidak sesuai dengan yang telah ditentukan, maka akan muncul pesan kesalahan.
Pengecekan Pembagian dengan Nol: Terdapat pengecekan khusus untuk mencegah pembagian dengan nol. Jika pengguna mencoba membagi dengan nol, program akan menampilkan pesan kesalahan.
print("Hasil:", hasil) Setelah operasi selesai, hasil perhitungan akan ditampilkan di layar.
kalkulator() Baris terakhir dari kode menjalankan fungsi kalkulator() sehingga program akan mulai meminta input dari pengguna dan melakukan perhitungan.


## *2. Pemesanan Tiket Bioskop*

Program pertama yang akan dibuat adalah Program untuk menampilkan tipe tiket reguler dan Anda memiliki kartu member? (ya/tidak) dan memunculkan harga tiket yang harus di bayar

Berikut flowchartnya

![Screenshot flochart bioskop 1 ](https://github.com/user-attachments/assets/65f2ba77-821c-4428-b0a1-6676ba52f238)

*Program akan meminta kita untuk memasukkan 3 angka untuk dibandingkan :*

<img width="712" alt="output 1" src="https://github.com/user-attachments/assets/ac667063-2669-406c-9c81-1981b97d8139">

*Penjelasan Code*

*2.*

```
def hitung_harga_tiket():
  """Fungsi untuk menghitung harga tiket bioskop"""

  # Harga dasar tiket
  harga_reguler = 50000
  harga_vip = 100000
  diskon_member = 0.2

  # Meminta input dari pengguna
  tipe_tiket = input("Masukkan tipe tiket (reguler/vip): ").lower()
  status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").lower()

  # Menghitung harga tiket berdasarkan tipe tiket dan status member
  if tipe_tiket == "reguler":
    harga_awal = harga_reguler
  elif tipe_tiket == "vip":
    harga_awal = harga_vip
  else:
    print("Tipe tiket tidak valid.")
    return

  # Menghitung diskon jika pengguna adalah member
  diskon = harga_awal * diskon_member if status_member == "ya" else 0
  harga_akhir = harga_awal - diskon

  # Menampilkan hasil
  print("Harga tiket yang harus dibayar:", harga_akhir)

hitung_harga_tiket()
```


def hitung_harga_tiket(): Baris ini mendefinisikan sebuah fungsi bernama hitung_harga_tiket(). Fungsi ini akan berisi serangkaian instruksi untuk menghitung harga tiket.
harga_reguler = 50000
harga_vip = 100000
diskon_member = 0.2 Di sini, kita mendefinisikan harga dasar untuk tiket reguler, VIP, dan besarnya diskon yang diberikan kepada member (20%).
tipe_tiket = input("Masukkan tipe tiket (reguler/vip): ").lower() 
status_member = input("Apakah Anda memiliki kartu member? (ya/tidak): ").lower() Program meminta pengguna untuk memasukkan tipe tiket (reguler atau VIP) dan status keanggotaan (ya atau tidak). Fungsi .lower() digunakan untuk mengubah semua input menjadi huruf kecil agar lebih mudah dibandingkan.
if tipe_tiket == "reguler": 
elif tipe_tiket == "vip": 
else: Bagian ini melakukan pengecekan terhadap tipe tiket yang dimasukkan. Jika tipe tiket reguler, maka harga awal adalah harga reguler. Jika tipe tiket VIP, maka harga awal adalah harga VIP. Jika input tipe tiket tidak valid, maka akan dicetak pesan kesalahan dan fungsi akan berhenti.
diskon = harga_awal * diskon_member if status_member == "ya" else 0 Baris ini menghitung besarnya diskon. Jika pengguna adalah member (status_member adalah "ya"), maka diskon akan dihitung berdasarkan harga awal dan besarnya diskon member. Jika bukan member, maka diskonnya adalah 0.
harga_akhir = harga_awal - diskon Harga akhir tiket dihitung dengan mengurangi harga awal dengan besarnya diskon.
print("Harga tiket yang harus dibayar:", harga_akhir) Hasil perhitungan harga tiket akhir akan dicetak di layar.
hitung_harga_tiket() Baris terakhir ini memanggil fungsi hitung_harga_tiket() untuk menjalankan semua instruksi di dalamnya.
