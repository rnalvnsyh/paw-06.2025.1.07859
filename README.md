# Laporan Tugas Web Profile

- **Nama / NIM:** RENO ALVIANSYAH KHAREL / 06.2025.1.07859
- **Tema Terpilih:** Bento Grid (Soft Neutrals)
- **Alasan Memilih Tema:** Menginginkan tampilan modular yang rapi dengan kombinasi warna satu nada (*tone-on-tone*) yang tenang dan tidak terlalu mencolok
- **Hasil Validasi W3C Nu HTML Checker:** 0 Error- **Skor Lighthouse:** Accessibility (90+), SEO (90+)- **Deklarasi AI:** Menggunakan bantuan AI (Gemini) untuk penyusunan kerangka awal HTML5 semantik, struktur folder, dan panduan perintah Git


## 1. Tampilan Sebelum & Sesudah CSS
- **Sebelum (HTML Polos):** `![HTML Polos](profile/img/sebelum-css.png)`
- **Sesudah (Gaya Bento Grid):** `![Dengan CSS](profile/img/sesudah-css.png)`

---

## 2. Analisis Specificity CSS
1. **Kasus 1 (Elemen vs Class):**
   - Selector: `body` vs `.bento-card`
   - Nilai Specificity: `(0-0-1)` vs `(0-1-0)`
   - Pemenang: `.bento-card`
2. **Kasus 2 (Child Selector vs Attribute):**
   - Selector: `nav ul li a` vs `a[target="_blank"]`
   - Nilai Specificity: `(0-0-4)` vs `(0-1-1)`
   - Pemenang: `a[target="_blank"]`
3. **Kasus 3 (Pseudo-class vs Element):**
   - Selector: `a:hover` vs `a`
   - Nilai Specificity: `(0-1-1)` vs `(0-0-1)`
   - Pemenang: `a:hover`

---

## 3. Audit Kontras Warna (Standar AA)
- **Teks Utama (`#2C2A29`) di Latar Belakang (`#FBF9F5`):** Rasio Kontras ~13:1 (Lolos AA & AAA)
- **Kartu Bento (`#F2ECE4`) di Latar Belakang (`#FBF9F5`):** Perbedaan warna lembut untuk memisahkan area tanpa mengganggu keterbacaan.
- **Link (`#1A5F7A`) di Latar Kartu (`#F2ECE4`):** Rasio Kontras ~6.5:1 (Lolos AA)

---

## 4. Temuan DevTools & Solusi Bug
- **Bug:** Jarak spasi menu navigasi di `<header>` terlalu rapat dan menempel ke tepi atas layar.
- **Penyebab:** Belum ada aturan `margin-inline: auto` dan `padding` pada elemen `header`.
- **Solusi:** Menambahkan properti `max-width: 75ch`, `margin-inline: auto`, dan `padding: 1rem 1.5rem` di `style.css`.

---

## 5. Bukti Validasi
- **W3C Nu HTML Checker:** 0 Error
- **W3C Jigsaw CSS Validator:** 0 Error

---

## 6. Deklarasi Penggunaan AI
Menggunakan AI (Gemini) sebagai mitra diskusi untuk pembuatan reset dasar CSS, pemisahan struktur *selector*, serta panduan penulisan laporan `README.md`. Seluruh baris kode CSS diuji dan dipahami secara mandiri.