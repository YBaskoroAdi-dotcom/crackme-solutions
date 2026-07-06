# Writeup Crackme-03: Analisis Logika Input `code.exe`

## Informasi Tantangan
* **Nama File**: `code.exe`
* **Tingkat Kesulitan**: 1.0 (Easy)
* **Arsitektur**: x86-64 (PE32)
* **Tujuan**: Membedah logika pengecekan *input* program dan menemukan nilai kunci yang benar.

## 1. Analisis Statis (Triage)
Pada tahap awal, file dieksekusi menggunakan *Static Analysis Tool* (Ghidra) untuk mengidentifikasi alur kerja program.
* **Metode**: Dekompilasi *binary* menjadi kode representatif bahasa C.
* **Temuan Awal**: Program menggunakan fungsi standar `printf` dan `scanf` untuk interaksi pengguna.

## 2. Bedah Logika (Ghidra Decompiler)
Hasil dekompilasi menunjukkan adanya dua tahap pengecekan input yang bersifat *hardcoded*:

## Proses dalam Ghidra   
![Analisis Ghidra](ghidra.png)

Berdasarkan kode di atas, ditemukan logika berikut:
1. **Input Pertama**: Harus bernilai `0x21` (heksadesimal) atau **33** (desimal).
2. **Input Kedua**: Harus bernilai `0x66` (heksadesimal) atau **102** (desimal).

## 3. Hasil Eksekusi (Dinamis)
Setelah mengetahui nilai yang diharapkan, dilakukan pengujian melalui *Command Prompt* untuk memverifikasi temuan:

## Hasil eksekusi melalui command prompt
![Hasil Eksekusi](result.png)

Program berhasil mengeluarkan pesan *"Congratulations, you have completed the challenge!"* setelah input **33** dan **102** dimasukkan secara berurutan.

## 4. Kesimpulan
Tantangan ini mengajarkan dasar-dasar *reverse engineering* di mana analis harus mampu melakukan konversi nilai antara heksadesimal ke desimal serta membaca alur logika program melalui dekompilator. Tantangan ini berhasil diselesaikan dengan metode analisis statis yang dikonfirmasi dengan pengujian dinamis.