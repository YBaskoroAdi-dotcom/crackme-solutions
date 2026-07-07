# Reverse Engineering Task Solutions

Repositori ini berisi solusi dan dokumentasi untuk berbagai tantangan *Reverse Engineering* (CrackMe) yang dikerjakan sebagai bagian dari tugas mata kuliah.

## Status Pengerjaan

| Nama Tantangan | Kesulitan | Status | Keterangan |
| :--- | :--- | :--- | :--- |
| CrackMe-03 | 1.0 | ✅ Selesai | Analisis statis dan validasi input. |
| CrackMe-04 | 2.2 | ✅ Selesai | Analisis aritmatika dan pembuatan *keygen*. |
| CrackMe-05 | 5.0 | ✅ Selesai | Analisis *anti-disassembly* dan dekripsi *flag*. |

## Struktur Repositori
- `crackme-03/`: Dokumentasi dan solusi tantangan 03.
- `crackme-04/`: Analisis `Untitled3.exe`, *keygen*, dan *writeup*.
- `crackme-05/`: Analisis tantangan tingkat Hard (`mbb.exe`) dan dekripsi *flag*.

## Metodologi
Setiap tantangan diselesaikan menggunakan metode:
1. **Static Analysis**: Menggunakan Ghidra untuk memetakan alur kontrol dan algoritma validasi.
2. **Verification**: Melakukan pengujian langsung di lingkungan terisolasi untuk memastikan kebenaran hasil.
3. **Documentation**: Menyusun *writeup* teknis yang mencakup deskripsi algoritma dan pembuktian matematis.

---
*Dibuat untuk tugas mata kuliah Reverse Engineering - Semester 4.*