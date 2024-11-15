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
