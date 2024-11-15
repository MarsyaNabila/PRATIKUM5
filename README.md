# TUGAS PRATIKUM 5
# NAMA: MARSYA NABILA PUTRI
# KELAS: TI.24.A.4
# MATKUL: BAHASA PEMROGRAMAN
# Input dan output dari Pratikum 5

## masukan
![inputprak5](https://github.com/user-attachments/assets/b8f95592-bf25-4c66-8a32-ef9b3c652f49)

## keluaran 
![WhatsApp Image 2024-11-15 at 09 02 29_91c8b3fc](https://github.com/user-attachments/assets/ca025e4d-0680-4dbe-87a5-2714ca062c68)

## flowchart
![flowchart](https://github.com/user-attachments/assets/a5b2fd16-c6b0-4bf3-8299-8fb5edb0188a)
## 1. Fungsi
## `hitung_nilai_akhir(tugas, uts, uas):`

```python
def hitung_nilai_akhir(tugas, uts, uas):
    return (tugas * 0.30) + (uts * 0.35) + (uas * 0.35)
````


- Fungsi ini menerima 3 parameter:
  nilai tugas, UTS, dan UAS
- Menghitung nilai akhir dengan bobot:
  - Tugas: 30% (0.30)
  - UTS: 35% (0.35)
  - UAS: 35% (0.35)
- Mengembalikan hasil perhitungan nilai akhir

## 2. Fungsi
## `tampilkan_daftar(daftar_mahasiswa):`

```python
def tampilkan_daftar(daftar_mahasiswa):
    print("=" * 70)  # Membuat garis pembatas
    print("| No |     Nama      |    NIM    | Tugas | UTS | UAS | Akhir |")
    print("=" * 70)  # Membuat garis pembatas
````

- Menerima parameter berupa list yang berisi data mahasiswa
- Membuat tampilan tabel dengan header
- Menggunakan perulangan untuk menampilkan setiap data mahasiswa
- Format output menggunakan string formatting untuk merapikan tampilan
- enumerate(daftar_mahasiswa, 1) digunakan untuk membuat penomoran mulai dari 1

## 3. Fungsi `main()`
```python
def main():
    daftar_mahasiswa = []  # Inisialisasi list kosong
````
- Fungsi utama program
- Membuat list kosong untuk menyimpan data mahasiswa

## 4.Input Data dan Validasi
```python
while True:
    print("\nMasukkan data mahasiswa")
    nama = input("Nama : ")
    nim = input("NIM : ")
    
    while True:
        try:
            tugas = float(input("Nilai Tugas : "))
            if 0 <= tugas <= 100:
                break
            print("Nilai harus antara 0-100!")
        except ValueError:
            print("Masukkan nilai yang valid!")
````

- Menggunakan nested while loop untuk input dan validasi
- Try-except untuk menangani input nilai yang tidak valid
- Validasi rentang nilai (0-100)
- Proses yang sama dilakukan untuk nilai UTS dan UAS

## 5. Menyimpan Data:
```python
# Hitung nilai akhir
nilai_akhir = hitung_nilai_akhir(tugas, uts, uas)

# Tambahkan ke daftar
mahasiswa = {
    'nama': nama,
    'nim': nim,
    'tugas': tugas,
    'uts': uts,
    'uas': uas,
    'nilai_akhir': nilai_akhir
}
daftar_mahasiswa.append(mahasiswa)
````

- Memanggil fungsi hitung_nilai_akhir
- Membuat dictionary untuk menyimpan data satu mahasiswa
- Menambahkan dictionary ke dalam list daftar_mahasiswa

## 6. Konfirmasi Tambahan Data:
```python
tambah = input("\nTambah data (y/t)? ")
if tambah.lower() != 'y':
    break
````

- Meminta konfirmasi untuk menambah data lagi
- Jika input bukan 'y', keluar dari loop

## 7. Menampilkan Hasil:
```pythom
print("\nDaftar Nilai Mahasiswa:")
tampilkan_daftar(daftar_mahasiswa)
````

- Memanggil fungsi tampilkan_daftar untuk menampilkan semua data

## 8. Entry Point Program:
```pyton
if __name__ == "__main__":
    main()
````

- Memastikan fungsi main() hanya dijalankan jika file dijalankan langsung
- Tidak akan dijalankan jika file di-import sebagai modul

Fitur-fitur Program:

  1. Dapat menambahkan data mahasiswa secara dinamis
  2. Validasi input untuk nilai (harus numerik dan 0-100)
  3. Perhitungan nilai akhir otomatis dengan bobot yang ditentukan
  4. Tampilan output dalam bentuk tabel yang rapi
  5. Penanganan error untuk input yang tidak valid
  6. Konfirmasi untuk menambah data baru

Program ini dibuat untuk memudahkan pengelolaan data nilai mahasiswa dengan interface yang user-friendly dan penanganan error yang baik.









