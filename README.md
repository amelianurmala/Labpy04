# Labpy04

# LATIHAN
![Screenshot (99)](https://github.com/user-attachments/assets/d19394ae-ba21-40f2-9cd5-aacafef76f6d)

![Screenshot (100)](https://github.com/user-attachments/assets/3ab3c558-f545-4a19-9d7f-ad053855686b)


Berikut penjelasan hasil kode di atas:

1. **List A Didefinisikan:**
   ```python
   A = [15, 27, 35, 43, 50]
   ```
   List `A` berisi lima elemen awal: `[15, 27, 35, 43, 50]`.

2. **Akses Elemen List:**
   ```python
   print(A[2])  # Elemen ke-3
   print(A[1:4]) # Elemen ke-2 sampai ke-4
   print(A[-1])  # Elemen terakhir
   ```
   - `A[2]` mengembalikan elemen ke-3, yaitu `35`.
   - `A[1:4]` mengambil elemen dari ke-2 hingga ke-4 (tidak termasuk indeks ke-4), yaitu `[27, 35, 43]`.
   - `A[-1]` mengembalikan elemen terakhir, yaitu `50`.

3. **Ubah Elemen dalam List:**
   ```python
   A[3] = 100
   A[3:] = [200, 300]
   ```
   - `A[3] = 100`: Mengganti elemen ke-4 (indeks 3) menjadi `100`. List sekarang: `[15, 27, 35, 100, 50]`.
   - `A[3:] = [200, 300]`: Mengganti elemen mulai dari ke-4 hingga akhir menjadi `[200, 300]`. List sekarang: `[15, 27, 35, 200, 300]`.

4. **Tambahkan Elemen Baru ke List B:**
   ```python
   B = A[:2]
   B.append("Python")
   B.extend([400, 500, 600])
   ```
   - `B = A[:2]`: Membuat list `B` dari dua elemen pertama `A` (`[15, 27]`).
   - `B.append("Python")`: Menambahkan string `"Python"` ke `B`. List `B` sekarang: `[15, 27, 'Python']`.
   - `B.extend([400, 500, 600])`: Menambahkan tiga elemen baru ke `B`. List `B` sekarang: `[15, 27, 'Python', 400, 500, 600]`.

5. **Menggabungkan List A dan B:**
   ```python
   C = A + B
   ```
   - `C` adalah gabungan dari `A` dan `B`. List `C` sekarang: `[15, 27, 35, 200, 300, 15, 27, 'Python', 400, 500, 600]`.

6. **Cetak Hasil Akhir:**
   ```python
   print(A)  # [15, 27, 35, 200, 300]
   print(B)  # [15, 27, 'Python', 400, 500, 600]
   print(C)  # [15, 27, 35, 200, 300, 15, 27, 'Python', 400, 500, 600]
   ```
   - `A` adalah hasil modifikasi dari list awal.
   - `B` adalah list baru dengan elemen dari `A` yang telah ditambahkan elemen baru.
   - `C` adalah gabungan dari list `A` dan `B`.


# TUGAS PRATIKUM

BERIKUT ADALAH GAMBAR KODENYA
![Screenshot (105)](https://github.com/user-attachments/assets/31ac7d7d-d631-40c6-92cb-43909f5e3d17)

![Screenshot (106)](https://github.com/user-attachments/assets/e07fdaf8-0b57-4072-89f3-096f47ade42b)

BERIKUT ADALAH GAMBAR HASINYA (OUTPUT)
![Screenshot (103)](https://github.com/user-attachments/assets/2e7ac7d9-3fcc-4c3a-bb21-91f4828c673d)

![Screenshot (104)](https://github.com/user-attachments/assets/dcd749a5-c168-4013-a892-328897a74406)

BERIKUT INI PENELASANNYA

### Penjelasan Kode

1. **Membuat List `mahasiswa`:**
   ```python
   mahasiswa = []
   ```
   List `mahasiswa` ini akan digunakan untuk menyimpan data tiap mahasiswa dalam bentuk dictionary.

2. **Fungsi `hitung_nilai_akhir`:**
   ```python
   def hitung_nilai_akhir(tugas, uts, uas):
       return (tugas * 0.3) + (uts * 0.35) + (uas * 0.35)
   ```
   Fungsi ini menghitung nilai akhir berdasarkan bobot: nilai tugas 30%, nilai UTS 35%, dan nilai UAS 35%. Fungsi ini menerima tiga parameter (`tugas`, `uts`, dan `uas`) dan mengembalikan nilai akhir yang dihitung.

3. **Pengulangan Input Data Mahasiswa:**
   ```python
   while True:
       # Input data mahasiswa
       nama = input("Masukkan Nama: ")
       nim = input("Masukkan NIM: ")
       tugas = float(input("Nilai Tugas: "))
       uts = float(input("Nilai UTS: "))
       uas = float(input("Nilai UAS: "))
   ```
   - Dalam loop `while True`, pengguna diminta untuk memasukkan nama, NIM, nilai tugas, nilai UTS, dan nilai UAS dari mahasiswa. 
   - Nilai tugas, UTS, dan UAS diubah menjadi `float` karena mungkin mengandung desimal.

4. **Menghitung Nilai Akhir Mahasiswa:**
   ```python
   nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)
   ```
   Memanggil fungsi `hitung_nilai_akhir` untuk menghitung nilai akhir mahasiswa berdasarkan nilai tugas, UTS, dan UAS.

5. **Menyimpan Data Mahasiswa ke dalam Dictionary:**
   ```python
   data = {
       'nama': nama,
       'nim': nim,
       'tugas': tugas,
       'uts': uts,
       'uas': uas,
       'nilai_akhir': nilai_akhir
   }
   mahasiswa.append(data)
   ```
   - Data setiap mahasiswa disimpan dalam dictionary `data`, yang berisi nama, NIM, nilai tugas, UTS, UAS, dan nilai akhir.
   - Dictionary ini kemudian ditambahkan ke dalam list `mahasiswa` menggunakan `append()`.

6. **Memeriksa Apakah Ingin Menambah Data Lagi:**
   ```python
   lanjut = input("Tambah data (y/t)? ")
   if lanjut.lower() == 't':
       break
   ```
   Setelah data dimasukkan, pengguna ditanya apakah ingin menambah data lagi. Jika jawabannya adalah `t` (tidak), maka loop akan berhenti.

7. **Menampilkan Data Mahasiswa dalam Bentuk Tabel:**
   ```python
   print("\nDaftar Nilai Mahasiswa")
   print("="*80)
   print("{:<20} {:<15} {:<10} {:<10} {:<10} {:<10}".format(
       "Nama", "NIM", "Tugas", "UTS", "UAS", "Nilai Akhir"))
   print("-"*80)
   ```
   - Header tabel dicetak dengan format rapi menggunakan `str.format()`. `"{:<20}"` berarti teks akan diratakan ke kiri dalam kolom selebar 20 karakter, begitu juga untuk kolom lainnya.

8. **Mencetak Setiap Data Mahasiswa:**
   ```python
   for data in mahasiswa:
       print("{:<20} {:<15} {:<10} {:<10} {:<10} {:<10.2f}".format(
           data['nama'],
           data['nim'],
           data['tugas'],
           data['uts'],
           data['uas'],
           data['nilai_akhir']
       ))
   ```
   - Loop `for` digunakan untuk menampilkan data setiap mahasiswa yang disimpan dalam list `mahasiswa`.
   - `{:10.2f}` memastikan `nilai_akhir` ditampilkan dengan dua angka desimal.

9. **Penutup Tabel:**
   ```python
   print("="*80)
   ```
   Menampilkan garis penutup tabel agar tampak lebih rapi.

### Contoh Output
Misalkan data berikut dimasukkan:
```
Masukkan Nama: Amelia
Masukkan NIM: 312410199
Nilai Tugas: 80
Nilai UTS: 85
Nilai UAS: 90
Tambah data (y/t)? y
Masukkan Nama: Feby 
Masukkan NIM: 312410245
Nilai Tugas: 75
Nilai UTS: 80
Nilai UAS: 85
Tambah data (y/t)? t
```

Output:
```
Daftar Nilai Mahasiswa
================================================================================
Nama                 NIM             Tugas      UTS        UAS        Nilai Akhir
--------------------------------------------------------------------------------
Amelia                  12345           80.0       85.0       90.0       85.25     
Feby                    67890           75.0       80.0       85.0       80.50     
================================================================================
```

Output di atas menunjukkan data mahasiswa dalam bentuk tabel yang rapi, beserta nilai akhir yang dihitung sesuai dengan bobot masing-masing komponen.



