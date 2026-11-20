# Plan: Dashboard ULPS Kolej Komuniti Kelana Jaya

## Gambaran Keseluruhan

Membina sebuah **portal web** untuk Unit Latihan dan Pembangunan Staf (ULPS) Kolej Komuniti Kelana Jaya (KKKJ) yang berfungsi sebagai pusat maklumat latihan bagi semua warga KKKJ — pensyarah dan staf pentadbiran. Portal ini **bukan sistem pengurusan data penuh**, tetapi sebuah **laman web interaktif statik/semi-statik** yang memaparkan maklumat latihan, menyediakan akses kepada pautan penting, dan membolehkan warga KKKJ mengakses semua sumber berkaitan ULPS dari satu tempat.

### Skop
- Laman web responsif (desktop & mudah alih)
- Bahasa: Bahasa Melayu
- Stack: HTML + Tailwind CSS + JavaScript (tiada backend kompleks diperlukan)
- Data: Dibenamkan terus dalam HTML/JS berdasarkan fail-fail ULPS sedia ada
- Semua pautan Google Form dan Google Drive disepadukan

### Di Luar Skop
- Sistem login/autentikasi
- Pangkalan data dinamik
- Sistem pengurusan rekod automatik (ESIS mengendalikan ini)

---

## Sub-Tugas

---

### Sub-Tugas 1: Struktur Projek dan Halaman Utama (Homepage)

**Intent**
Mewujudkan asas projek web dan halaman utama dashboard yang memaparkan ringkasan ULPS KKKJ, pengumuman terkini, dan navigasi ke semua modul.

**Expected Outcomes**
- Folder projek tersusun dengan fail HTML, CSS (Tailwind via CDN), dan JS
- Halaman utama dengan header KKKJ, navigasi, hero section, dan kad ringkasan
- Responsif pada skrin desktop dan mudah alih
- Branding mengikut warna rasmi KPT/Kolej Komuniti (biru dan emas)

**Todo List**
- [ ] Cipta struktur folder: `index.html`, `css/style.css`, `js/main.js`, `assets/`
- [ ] Tambah Tailwind CSS via CDN dan font Google (Inter atau Poppins)
- [ ] Bina header dengan logo KKKJ, nama portal "ULPS KKKJ", dan nav bar
- [ ] Bina hero section dengan tagline dan butang CTA utama
- [ ] Bina 4 kad ringkasan: Takwim 2026, Program SIP, Muat Naik Sijil, Pautan Berguna
- [ ] Bina footer dengan maklumat PLPS: Salwa Binti Anuar, Kolej Komuniti Kelana Jaya

**Relevant Context**
- PLPS: Salwa Binti Anuar
- Disemak oleh: Mohd Zaki bin Abd Kadir (Timbalan Pengarah Akademik)
- Disahkan oleh: Sr Ts. Fazrul Idzam bin Zainal Abidin (Pengarah KKKJ)
- Prosedur rujukan: KKKJ-PK-PS-08

**Status:** [ ] pending

---

### Sub-Tugas 2: Halaman Takwim Program ULPS 2026

**Intent**
Memaparkan senarai 12 program latihan ULPS 2026 secara visual dan interaktif, dengan status setiap program berdasarkan tarikh semasa.

**Expected Outcomes**
- Jadual atau kad program yang memaparkan semua 12 aktiviti latihan 2026
- Setiap aktiviti menunjukkan: nombor, nama program, tarikh, dan status (Selesai / Akan Datang / Sedang Berlangsung)
- Status dikira secara automatik berdasarkan tarikh semasa (JavaScript)
- Boleh ditapis mengikut bulan atau status

**Todo List**
- [ ] Cipta `takwim.html` atau bahagian takwim dalam `index.html`
- [ ] Benamkan data 12 program ULPS 2026 sebagai array JavaScript
- [ ] Papar sebagai kad interaktif dengan warna status berbeza
- [ ] Tambah logik JavaScript untuk kira status automatik (lampau/akan datang)
- [ ] Tambah fungsi tapis mengikut bulan (Jan-Des)

**Data Program ULPS 2026 (dari Takwim ULPS 2026 b.docx)**
1. Taklimat Pengurusan KPI — 13 Januari 2026
2. Kursus Pemerkasaan Bahasa Melayu: Betulkan yang Biasa, Biasakan yang Betul — 16 Januari 2026
3. Bengkel LMS-CIDOS — 5 Februari 2026
4. Bengkel Penggunaan RMS-Repositori dan Turnitin — 6 Februari 2026
5. Bengkel Sangkutan Industri Pensyarah dan TVET Instruction Technology Update Melalui Kaedah Coaching dan Mentoring — 10 Februari 2026
6. Kursus Penggunaan Google NotebookLM — 11 Februari 2026
7. Kursus Kesihatan Mental: Self-Care Bukan Selfish — 19 Jun 2026
8. Ceramah Integriti: Telus, Tulus, Lulus — Navigasi Integriti Organisasi — 6 Julai 2026
9. Kursus Asas Keselamatan dan Kesihatan Pekerjaan — 21 Oktober 2026
10. Perkongsian Ilmu Penyelidikan/Inovasi/Amalan Baik — 18 November 2026
11. Kursus ToT Asas Pemesinan (Lathe Machine) — 11 November 2026
12. Kursus ToT Asas Pemeriksaan Kenderaan — 25 November 2026

**Status:** [ ] pending

---

### Sub-Tugas 3: Halaman Muat Naik Sijil dan Rekod Latihan

**Intent**
Menyediakan akses mudah kepada semua pautan Google Form untuk warga KKKJ menghantar sijil dan rekod latihan mereka kepada ULPS.

**Expected Outcomes**
- Seksyen dengan 3 kad pautan muat naik yang jelas dan mudah diakses
- Penerangan ringkas tujuan setiap pautan
- Pautan terus ke Google Form/Drive yang betul
- Boleh diakses dari halaman utama dan navigasi

**Todo List**
- [ ] Cipta seksyen "Kemaskini Rekod Latihan" dalam halaman
- [ ] Kad 1: Muat naik sijil kursus/bengkel/seminar (pautan form: https://forms.gle/J8XmPBFKNr3gSR5W8)
- [ ] Kad 2: Muat naik pentauliahan kelayakan/sijil profesional (pautan form: https://forms.gle/7q65zJoZaHJG4Ncg7)
- [ ] Kad 3: Muat naik nota kursus/bengkel yang dihadiri (pautan form Google Form nota kursus)
- [ ] Tambah arahan ringkas cara muat naik dan dokumen yang diperlukan
- [ ] Tambah pautan semak/muat turun Sijil Dalaman KUDAP 2026: https://bit.ly/4jMXOeR

**Relevant Context**
- Dari Ringkasan dan pautan.docx: 3 pautan Google Form utama untuk warga KKKJ
- Dasar: kakitangan perlu capai 40 jam latihan setahun (Prosedur KKKJ-PK-PS-08)
- KPI: bilangan hari berkursus 15 hari (dari Laporan KPI Bakat Sukuan 4.pdf)

**Status:** [ ] pending

---

### Sub-Tugas 4: Halaman Program SIP (Sangkutan Industri Pensyarah)

**Intent**
Memaparkan maklumat lengkap tentang Program Sangkutan Industri Pensyarah (SIP) khusus untuk KKKJ, termasuk syarat, prosedur, jenis sangkutan, dan pautan permohonan.

**Expected Outcomes**
- Halaman info SIP dengan 4 seksyen utama: Apa itu SIP, Syarat, Jenis Sangkutan, Cara Memohon
- Infografik atau timeline prosedur SIP (3 fasa: Sebelum, Semasa, Selepas)
- Pautan terus ke sistem ESIS untuk permohonan SIP
- Maklumat borang penilaian LTSPI dan markah lulus (50%)

**Todo List**
- [ ] Cipta `sip.html` atau seksyen SIP dalam halaman
- [ ] Bina accordion/tab untuk 4 seksyen info SIP
- [ ] Tambah timeline visual 3 fasa SIP: Sebelum / Semasa / Selepas
- [ ] Papar 3 jenis sangkutan: Block-released (28 hari), Day-released (20 hari), Hour-released (154 jam)
- [ ] Tambah syarat kelayakan peserta (5 syarat dari Panduan SIP)
- [ ] Tambah pautan permohonan ESIS: https://esis.gov.my/esis2/v3/latihan/sip/mainsip.jsp
- [ ] Tambah maklumat penilaian LTSPI: Laporan 60% + Pembentangan LISS 40%
- [ ] Papar maklumat Rakan Pengamal Industri (RPI) dan kriteria syarikat

**Relevant Context**
- Dari Panduan SIP.pdf (JPPKK 2021): prosedur lengkap, jenis sangkutan, syarat
- Dari Borang Penilaian SIP Industri.pdf: borang penilaian sedia ada
- Dari Template Laporan SIP KKKJ.docx: format laporan dalaman KKKJ
- Dari Maklumat Rakan Industri.docx: maklumat RPI yang diperlukan

**Status:** [ ] pending

---

### Sub-Tugas 5: Halaman Pautan Berguna dan Dokumen

**Intent**
Menyediakan satu tempat untuk semua pautan berguna, dokumen rujukan, dan sumber penting yang kerap diakses oleh warga KKKJ berkaitan latihan.

**Expected Outcomes**
- Seksyen pautan berkategori: Sistem (ESIS), Sijil, Borang, Panduan
- Pautan ke fail Google Drive untuk nota kursus dan sijil dalaman
- Fail boleh dimuat turun atau dibuka terus
- Maklumat prosedur latihan ringkas (dalaman vs luaran)

**Todo List**
- [ ] Cipta seksyen "Sumber & Pautan" dalam halaman
- [ ] Kategori 1 — Sistem: Pautan ke ESIS (esis.gov.my)
- [ ] Kategori 2 — Sijil Dalaman (KUDAP): https://bit.ly/4jMXOeR
- [ ] Kategori 3 — Borang: Borang penilaian keberkesanan latihan (Lampiran 1-3 dari prosedur)
- [ ] Kategori 4 — Panduan: Panduan SIP JPPKK 2021
- [ ] Kategori 5 — Nota Kursus: Pautan ke Google Drive nota kursus
- [ ] Tambah info ringkas prosedur latihan dalaman vs luaran (carta alir ringkas)

**Relevant Context**
- Dari Pautan Sijil Dalaman.docx: https://bit.ly/4jMXOeR
- Dari Pautan Sijil KUDAP 2026.xlsx: pautan sijil KUDAP
- Dari Pautan Nota Kursus.xlsx: pautan nota kursus
- Dari Prosedur Latihan dan Pembangunan Staf.pdf (KKKJ-PK-PS-08): prosedur lengkap

**Status:** [ ] pending

---

### Sub-Tugas 6: Halaman Maklumat ULPS dan Hubungi

**Intent**
Memaparkan maklumat rasmi tentang ULPS KKKJ, peranan unit ini, pegawai bertanggungjawab, dan cara menghubungi PLPS.

**Expected Outcomes**
- Halaman "Tentang ULPS" dengan misi, skop tanggungjawab, dan carta organisasi ringkas
- Maklumat pegawai: PLPS Salwa Binti Anuar dan struktur pengurusan
- Petunjuk KPI tahunan: 40 jam latihan per staf, bilangan hari berkursus
- Prosedur ringkas latihan dalaman dan luaran

**Todo List**
- [ ] Cipta seksyen "Tentang ULPS" dalam halaman
- [ ] Papar misi & objektif ULPS (dari Prosedur KKKJ-PK-PS-08)
- [ ] Kad carta organisasi: Pengarah > Timbalan Pengarah Akademik > PLPS
- [ ] Papar KPI tahunan: 40 jam latihan / staf / tahun
- [ ] Tambah definisi penting: ESIS, Latihan Dalaman, Latihan Luaran, SIP, PLPS, JPPKK
- [ ] Tambah maklumat hubungi: nama dan jawatan PLPS

**Relevant Context**
- Pengarah: Sr Ts. Fazrul Idzam bin Zainal Abidin
- Timbalan Pengarah Akademik: Mohd Zaki bin Abd Kadir
- PLPS: Salwa Binti Anuar
- KPI: Memastikan kakitangan KKKJ menghadiri latihan selama 40 jam setahun
- Skop: latihan dalaman, luaran, dan SIP

**Status:** [ ] pending

---

## Seni Bina Portal

```
ulps-kkkj/
├── index.html          (Halaman Utama - semua seksyen dalam satu halaman)
├── css/
│   └── style.css       (Custom styles tambahan)
├── js/
│   └── main.js         (Logik interaktif: status takwim, navigasi)
└── assets/
    └── logo-kkkj.png   (Logo KKKJ)
```

**Pendekatan:** Single Page Application (SPA) dengan navigasi smooth-scroll. Semua kandungan dalam satu `index.html` dengan seksyen-seksyen bernama. Ini memudahkan penyelenggaraan tanpa memerlukan server.

---

## Stack Teknologi

| Komponen | Teknologi |
|---------|-----------|
| HTML | HTML5 semantik |
| CSS | Tailwind CSS v3 (CDN) + custom CSS minimum |
| JavaScript | Vanilla JS (tiada framework) |
| Ikon | Heroicons atau Font Awesome (CDN) |
| Font | Google Fonts - Poppins |
| Hosting | Boleh host di GitHub Pages, Netlify, atau pelayan KKKJ |

---

## Nota Penting

- **Pautan Google Form/Drive** dibenamkan terus — warga KKKJ klik dan terus ke form ESIS/Google
- **Data takwim** dibenamkan sebagai JavaScript array — PLPS boleh kemaskini teks bila perlu
- **Tiada login diperlukan** — ini portal maklumat awam dalaman, bukan sistem pengurusan
- **Rekod sebenar** tetap diuruskan melalui sistem ESIS rasmi seperti prosedur sedia ada
