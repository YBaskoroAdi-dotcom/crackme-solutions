"# Writeup Crackme 01

## Analisis
Crackme ini memiliki proteksi sederhana berupa pengecekan *input password*. Saya menggunakan `Ghidra` untuk menemukan fungsi `check_password` yang membandingkan *input* pengguna dengan *string* statis di memori.

## Langkah Pengerjaan
1. Triage: Menggunakan `DIE` untuk memastikan *binary* tidak diproteksi.
2. Debugging: Menggunakan `x64dbg` untuk memantau register setelah instruksi `CMP`.
3. Solusi: Mengubah instruksi `JNE` menjadi `NOP` agar program selalu menganggap *password* benar."
