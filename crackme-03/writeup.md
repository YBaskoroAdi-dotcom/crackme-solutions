# Writeup Crackme 03: Analisis code.exe

## Tujuan Analisis
Tujuan dari tantangan ini adalah menemukan dua angka rahasia yang dibutuhkan untuk memicu pesan keberhasilan program.

## Proses Analisis
1. **Triage**: Memeriksa file menggunakan Ghidra untuk membedah *binary* PE.
2. **Static Analysis**: 
   - Ditemukan fungsi `main` yang menggunakan `scanf` untuk menerima input pengguna.
   - Analisis kode menunjukkan adanya dua tahap pengecekan:
     - Tahap 1: `if (local_c == 0x21)` 
     - Tahap 2: `if (local_10 == 0x66)`
3. **Logika**: 
   - Nilai `0x21` (heksadesimal) setara dengan **33** (desimal).
   - Nilai `0x66` (heksadesimal) setara dengan **102** (desimal).

## Hasil Eksekusi
Program berhasil memberikan pesan sukses "Congratulations, you have completed the challenge!" setelah input diberikan melalui *command prompt* sesuai dengan hasil konversi nilai heksadesimal tersebut.

## Kesimpulan
Analisis statis melalui Ghidra sangat efektif untuk menemukan logika perbandingan angka, dan eksekusi melalui *command prompt* mengonfirmasi validitas analisis tersebut.