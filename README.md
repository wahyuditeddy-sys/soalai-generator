# 📚 SoalAI Generator

**Generator soal ujian otomatis berbasis AI untuk guru Indonesia**

Buat soal ujian lengkap (PG + Essay + Kunci Jawaban) langsung dari file kisi-kisi — dalam hitungan menit, siap cetak dalam format `.docx`.

🌐 **Live Demo:** [wahyuditeddy-sys.github.io/soalai-generator](https://wahyuditeddy-sys.github.io/soalai-generator)

---

## ✨ Fitur

| Fitur | Keterangan |
|-------|-----------|
| 📄 **Multi-format input** | Baca kisi-kisi dari PDF, DOCX, TXT, atau gambar |
| 🤖 **AI-powered** | Powered by Claude (Anthropic) — kualitas soal setara guru berpengalaman |
| 📝 **3 dokumen output** | Soal PG, Soal Essay, dan Kunci Jawaban guru — terpisah |
| 🎨 **Layout profesional** | Times New Roman, 2 kolom, margin A4, header sekolah |
| 🔑 **Kunci berwarna** | Tabel kunci jawaban dengan highlight warna A/B/C/D |
| 🏫 **Multi-sekolah** | Simpan daftar sekolah, flag konteks Islami |
| 💾 **Download langsung** | File `.docx` langsung didownload di browser, tanpa server |
| 🔒 **100% privat** | API Key hanya tersimpan di browser Anda, tidak dikirim ke server lain |

---

## 🚀 Cara Pakai

### Langsung di browser (tanpa install apapun)

1. **Buka** → [wahyuditeddy-sys.github.io/soalai-generator](https://wahyuditeddy-sys.github.io/soalai-generator)
2. **Klik ⚙️ Pengaturan API** → masukkan Anthropic API Key Anda
3. **Isi form** → sekolah, mata pelajaran, kelas, jenis ujian
4. **Upload kisi-kisi** → PDF, DOCX, TXT, atau gambar
5. **Klik 🚀 Generate** → tunggu proses AI
6. **Download** → Soal PG + Soal Essay + Kunci Jawaban `.docx`

### Jalankan lokal

```bash
# Clone repository
git clone https://github.com/wahyuditeddy-sys/soalai-generator.git
cd soalai-generator

# Buka langsung di browser
start index.html        # Windows
open index.html         # Mac
xdg-open index.html     # Linux
```

> Tidak perlu `npm install` atau server — murni HTML + JavaScript.

---

## 🔑 Mendapatkan API Key

1. Daftar / login ke [console.anthropic.com](https://console.anthropic.com)
2. Buka menu **API Keys** → **Create Key**
3. Copy key yang dihasilkan (`sk-ant-...`)
4. Paste di menu **⚙️ Pengaturan API** pada aplikasi

---

## 📁 Format Input yang Didukung

| Format | Keterangan |
|--------|-----------|
| `.pdf` | PDF kisi-kisi (teks atau scan) |
| `.docx` | Microsoft Word |
| `.txt` | Plain text |
| `.jpg` / `.png` / `.webp` | Foto/scan kisi-kisi |

---

## 📄 Output yang Dihasilkan

```
📝 soal_[mapel]_[kelas]_[id].docx    ← Lembar soal PG (2 kolom, header sekolah)
✏️ essay_[mapel]_[kelas]_[id].docx   ← Lembar soal Essay (garis jawaban)
🔑 kunci_[mapel]_[kelas]_[id].docx   ← Kunci + pembahasan + rubrik (RAHASIA GURU)
```

---

## 🏫 Sekolah yang Didukung

- **Umum** — semua jenjang (SD, SMP, SMA, SMK)
- **Islam / Muhammadiyah** — nama tokoh Islami (Ahmad, Fatimah, dll.) dan konteks keislaman diaktifkan otomatis

---

## ⚙️ Model AI yang Tersedia

| Model | Kecepatan | Kualitas | Rekomendasi |
|-------|-----------|----------|-------------|
| Claude Sonnet 4.6 | ⚡⚡⚡ | ⭐⭐⭐⭐ | ✅ Default |
| Claude Opus 4.7 | ⚡ | ⭐⭐⭐⭐⭐ | Soal sangat kompleks |
| Claude Haiku 4.5 | ⚡⚡⚡⚡ | ⭐⭐⭐ | Budget hemat |

---

## 🛠️ Teknologi

- **UI** — HTML5 + CSS3 + Vanilla JavaScript (zero framework)
- **AI** — [Anthropic Claude API](https://docs.anthropic.com)
- **DOCX** — [docx.js](https://docx.js.org) v8.5.0 (browser UMD)
- **PDF/DOCX reader** — [mammoth.js](https://github.com/mwilliamson/mammoth.js) v1.7.0
- **Hosting** — GitHub Pages

---

## 📋 Jenis Ujian yang Didukung

`UH` · `STS` · `PTS` · `UTS` · `PAS` · `UAS` · `Try-Out` · `Lainnya`

---

## 🔒 Keamanan & Privasi

- API Key **tersimpan di `localStorage` browser Anda**, tidak dikirim ke server manapun
- Seluruh proses berjalan di browser — file kisi-kisi tidak diupload ke server
- Hanya request ke `api.anthropic.com` yang dikirim (konten kisi-kisi untuk dianalisis AI)

---

## 📸 Screenshot

> *Generator soal PG, Essay, dan kunci jawaban dalam satu tampilan*

---

## 🤝 Kontribusi

Pull request dan issue sangat diterima! Beberapa ide pengembangan:

- [ ] Simpan sesi generate ke IndexedDB (history lokal)
- [ ] Export ke PDF langsung
- [ ] Dukungan format kisi-kisi Kemdikbud standar
- [ ] Multi-bahasa (Bahasa Indonesia + English)
- [ ] Preview soal sebelum download

---

## 📄 Lisensi

MIT License — bebas digunakan dan dimodifikasi untuk keperluan pendidikan.

---

*Dibuat dengan ❤️ untuk guru-guru Indonesia*
