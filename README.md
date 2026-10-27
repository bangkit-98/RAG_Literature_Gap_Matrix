# Literature GAP Matrix dengan Pipeline RAG (v1.0 & v1.1)

**Nama:** Bangkit Dwi Prasetyo  
**NIM:** P36.2026.0052  
**Matakuliah:** Introduction to Generative AI  

## 📌 Ringkasan Proyek
Repositori ini berisi *source code* untuk mengotomatisasi ekstraksi 10 artikel ilmiah menjadi *Literature Gap Matrix* menggunakan *Retrieval-Augmented Generation* (RAG). Sistem dibangun menggunakan model `gpt-oss-120b` yang diakses secara gratis melalui **Groq API**, serta mengimplementasikan prinsip *Frugal Computing* (Perhitungan terperinci terkait penggunaan token input dan token output).

## 📂 Struktur Repositori
- `/v1.0/`: Kode utama yang digunakan dalam penyusunan laporan RTM 2 (*Naive RAG*). Diuji pada 10 jurnal.
- `/v1.1/`: **Prototipe Usulan Perbaikan (*Proof-of-Concept*)**. Kode ini mendemonstrasikan perbaikan pada aspek ekstraksi metadata (DOI/Judul) dan *Retrieval Window*.
- `/data/`: Hasil ekstraksi (Excel/CSV) dari versi v1.0.
- `papers.json`: Daftar DOI dan tautan 10 jurnal (File PDF tidak diunggah untuk menghindari pelanggaran hak cipta).

## 🚀 Catatan Pengembangan (*Future Work*)
Berdasarkan evaluasi *LLM-as-a-Judge* pada versi v1.0, ditemukan kelemahan pada ekstraksi **DOI** dan **Future Work** karena letaknya yang berada di luar jangkauan 5 *chunk* teratas. 

Sebagai wujud **Penelitian Lanjutan**, penulis menyiapkan draf prototipe `/v1.1/` dengan pendekatan:
1. **Rule-based Extraction:** Menggunakan *Regular Expression* (Regex) untuk mengekstrak DOI dan Judul langsung dari halaman 1.
2. **Peningkatan Jendela Retrieval:** Mengubah parameter `k` pada tahap *Retrieval*.
3. **Prompt Cerdas:** Penambahan instruksi khusus untuk menangani paper bertipe *Survey*.

*(Catatan: Kode v1.1 disiapkan sebagai demonstrasi kode perbaikan dan masih akan dikembangkan ke versi v1.2 pada penelitian selanjutnya).*

## ⚙️ Cara Menjalankan
1. Buka file `.ipynb` di folder `/v1.0/` atau `/v1.1/` menggunakan Google Colab.
2. Jalankan **Sesi 0** untuk *mount* Google Drive (opsional).
3. Jalankan Sesi 1 hingga Sesi 7 secara berurutan.
