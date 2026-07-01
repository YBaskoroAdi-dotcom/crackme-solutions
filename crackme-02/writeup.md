"# Writeup Crackme 02

## Analisis
Target kali ini adalah aplikasi yang meminta *serial key*. Saya mengamati bahwa aplikasi melakukan perhitungan aritmatika sederhana pada *input* pengguna sebelum membandingkannya dengan *key* yang benar.

## Langkah Pengerjaan
1. Static Analysis: Melacak instruksi `ADD` dan `SUB` di `Ghidra` yang memproses *input* pengguna.
2. Debugging: Melakukan *breakpoint* pada alamat `0x401234` untuk melihat nilai yang dihasilkan setelah kalkulasi.
3. Solusi: Saya mendapatkan *serial key* yang valid melalui hasil perhitungan di *debugger*."
