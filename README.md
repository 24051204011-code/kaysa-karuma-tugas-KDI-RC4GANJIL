# kaysa-karuma-tugas-KDI-RC4GANJIL
Implementasi Algoritma Enkripsi RC4 (Rivest Cipher 4)
kaysa karuma amalia
24051204011
TIA
# deskripsi
Implementasi algoritma enkripsi RC4 (Rivest Cipher 4) dari scratch menggunakan Python 3, tanpa menggunakan library enkripsi eksternal. Program mendemonstrasikan seluruh proses algoritma RC4 secara step-by-step, mulai dari Key Scheduling Algorithm (KSA), proses enkripsi, hingga dekripsi.
# Struktur
├── rc4_demo.py   # Source code utama
└── README.md     # Dokumentasi ini

# syarat
Pastikan Python 3 sudah terinstall di sistem kamu,Tidak diperlukan instalasi library tambahan. Program hanya menggunakan modul time yang sudah bawaan Python.
# cara menjalankan1. Clone repositori ini:

git clone https://github.com/[USERNAME]/[NAMA-REPO].git
cd [NAMA-REPO]

2.jalankan program:

python demo_RC4.py

3.contoh output
<img width="1187" height="867" alt="Screenshot 2026-03-05 073559" src="https://github.com/user-attachments/assets/2bef20f5-f544-494e-a3cd-bd0048a587fa" />
<img width="1150" height="849" alt="Screenshot 2026-03-05 073613" src="https://github.com/user-attachments/assets/ee27b634-8774-4d48-b337-bd32e8c2a5a8" />

# algoritma
1. Input Data
Pada tahap ini program menerima:
Plaintext : Data2026
Key : TI_Unesa24
Kemudian setiap karakter diubah menjadi kode ASCII.
Sehingga:

Plaintext ASCII

[68, 97, 116, 97, 50, 48, 50, 54]

Key ASCII

[84, 73, 95, 85, 110, 101, 115, 97, 50, 52]

# Key Scheduling Algorithm (KSA)

Buat array S berisi angka 0–255

Buat array K dari key (diulang sampai panjang 256)

Lakukan proses pertukaran nilai (swap)

Rumusnya:

j = (j + S[i] + K[i]) mod 256
swap(S[i], S[j])

Hasil tahap ini adalah array S yang sudah teracak.
# Pseudo Random Generation Algorithm (PRGA)

i = (i + 1) mod 256

j = (j + S[i]) mod 256

swap(S[i], S[j])

t = (S[i] + S[j]) mod 256

Keystream:

[104, 223, 211, 175, 119, 122, 69, 39]

# Proses Enkripsi
<img width="296" height="362" alt="Screenshot 2026-03-05 022119" src="https://github.com/user-attachments/assets/c18fdc91-ee73-46cf-82f1-518e3ce23b45" />

ciphertax

8D57FB776AF73993
# Proses Dekripsi

Salah satu kelebihan RC4 adalah proses dekripsi menggunakan operasi yang sama.

Rumus:

Plaintext = Ciphertext XOR Keystream
