# INCLUSA — Dokumentasi Proyek Website

> **Sistem Informasi Terpadu HIV/AIDS Sidoarjo**
> Prototype v1.0 · Frontend React + Tailwind CSS
>
> Dokumen ini merangkum **apa saja yang SUDAH ada** di website ini. Silakan dikoreksi /
> ditambahkan di bagian [Catatan & Rencana](#-catatan--rencana-diisi-oleh-anda).

---

## 1. Ringkasan

INCLUSA (*Inclusive Space*) adalah platform digital yayasan yang menjadi media kolaborasi
antara masyarakat, Dinas Kesehatan, Dinas Pendidikan, Rumah Sakit, Klinik, Puskesmas,
Psikolog, dan stakeholder lain untuk penanggulangan HIV/AIDS di Sidoarjo.

**Fungsi utama:** Pusat Informasi · Media Edukasi · e-Pelayanan · Dashboard Monitoring · Collaboration Hub.

---

## 2. Identitas Brand

| Aspek | Detail |
|---|---|
| Nama | **INCLUSA** (IN = coral, CLUS = teal, A = kuning) |
| Makna | *Inclusive Space* — ruang inklusif untuk belajar, tumbuh, dan saling mendukung tanpa stigma |
| Logo | Ilustrasi keluarga berpelukan dalam lingkaran (di-crop dari aset asli → `src/imports/inclusa-mark.png`) |
| Filosofi logo | Arc Atas = Perlindungan · Keluarga = Kebersamaan · Arc Bawah = Pelukan & Dukungan · Titik = Individu |

### Palet Warna (dari logo)
| Token | Hex | Pemakaian |
|---|---|---|
| `brand-blue` (primary) | `#1F9AA0` | Tombol utama, tautan, ikon |
| `brand-teal` | `#34BEC4` | Aksen, ring, highlight |
| `brand-blue-deep` | `#123A40` | Judul, footer, teks gelap |
| `brand-maize` | `#F7C948` | Aksen kuning, sorotan |
| `brand-coral` | `#F0654E` | Aksen hangat |
| `brand-red` | `#E4412F` | CTA mendesak (Tes HIV) |
| `brand-cream` | `#FFF8EE` | Latar section hangat |

- Font: **Poppins** (display/judul) + **Plus Jakarta Sans** (body).

---

## 3. Struktur Halaman (Sudah Jadi)

Routing memakai `react-router`. Semua halaman publik memakai layout dengan Navbar + Footer.

| Route | Halaman | Status | Isi Singkat |
|---|---|---|---|
| `/` | **Beranda** | ✅ Aktif | Hero, 4 pilar layanan, info dasar, preview kurikulum, statistik kolaborasi, artikel, testimoni, CTA |
| `/tentang` | **Tentang Kami** | ✅ Aktif | Makna nama, **filosofi logo**, Visi & Misi, Nilai Inti, mitra kolaborasi |
| `/informasi` | **Informasi Umum** | ✅ Aktif | Tab: Apa itu HIV, Apa itu AIDS, Pencegahan, Penularan, Layanan Pemerintah + Mitos vs Fakta + U=U |
| `/artikel` | **Artikel** | ✅ Aktif | Pencarian + filter kategori, artikel unggulan, grid artikel |
| `/berita` | **Berita** | ✅ Aktif | Berita utama + daftar berita, tag kategori |
| `/statistik` | **Statistik** | ✅ Aktif | KPI, grafik tren (area), distribusi populasi (pie), sebaran per kecamatan (bar) — pakai `recharts` |
| `/peta` | **Peta GIS** | ✅ Aktif | Peta kecamatan interaktif (klik → detail kasus/ODHIV/ARV/faskes + grafik) |
| `/faq` | **FAQ** | ✅ Aktif | Akordeon + filter kategori + CTA hotline |
| `/faskes` | **Cari Fasilitas** | ✅ Aktif | Pencarian & filter RS/Puskesmas/Klinik + kartu detail layanan |
| `/e-pelayanan` | **e-Pelayanan** | 🟡 Prototype | Skrining risiko mandiri (kuesioner bertahap + hasil), pilar layanan, CTA konseling |
| `/edukasi` | **Education Center** | 🟠 Coming Soon | Kurikulum per jenjang usia, tema besar, waitlist email |
| `/admin` | **Dashboard Admin** | 🟡 Prototype | Sidebar menu, KPI, grafik, Approval Center (setujui/tolak) |

---

## 4. Struktur File

```
src/app/
├── App.tsx                      # Router utama
├── data/
│   └── content.ts               # SEMUA data mock (artikel, berita, faq, faskes, statistik, dll)
└── components/
    ├── layout/
    │   ├── Layout.tsx           # Wrapper Navbar + Outlet + Footer
    │   ├── Navbar.tsx
    │   ├── Footer.tsx
    │   └── Logo.tsx             # Logo + Wordmark INCLUSA
    ├── ui-kit/
    │   └── Shared.tsx           # SectionHeading, StatCard, PageHero, Chip, Eyebrow
    ├── ui/                      # Komponen shadcn/ui (bawaan)
    ├── figma/ImageWithFallback.tsx
    └── pages/
        ├── Home.tsx
        ├── TentangKami.tsx
        ├── InformasiUmum.tsx
        ├── Artikel.tsx
        ├── Berita.tsx
        ├── Faq.tsx
        ├── Statistik.tsx
        ├── PetaGIS.tsx
        ├── CariFasilitas.tsx
        ├── EPelayanan.tsx
        ├── EducationCenter.tsx
        └── AdminDashboard.tsx

src/imports/
├── inclusa-mark.png            # Logo (latar transparan, hasil crop)
└── inclusa-logo-full.png       # Logo + wordmark
```

---

## 5. Data yang Tersedia (mock di `content.ts`)

- **Statistik**: heroStats, quickStats, trendData (2020–2026), populationData
- **12 Kecamatan**: kasus, ODHIV, ARV, jumlah faskes
- **6 Artikel** · **4 Berita** · **6 FAQ** · **8 Fasilitas Kesehatan**
- **5 Topik Informasi** · **5 Modul Kurikulum** · **3 Testimoni**
- **Filosofi logo** & **Nilai inti**

> ⚠️ Semua data masih **mock/dummy** (belum terhubung backend/Supabase).

---

## 6. Tech Stack (Saat Ini vs Rencana)

| Kategori | Terpasang di prototype ini | Rencana (dari TECH_STACK.md) |
|---|---|---|
| Frontend | React 18, Tailwind v4, react-router, recharts, lucide-react, motion | Next.js 15, React 19, TanStack Query, Leaflet, ECharts |
| Backend | — (mock data) | NestJS, Prisma, PostgreSQL + PostGIS, Redis |
| Auth | — | JWT + Refresh Token + RBAC |
| Storage | — | Cloudflare R2 / S3 |

---

## 7. Yang BELUM Ada / Masih Placeholder

- [ ] Backend & database nyata (semua data masih dummy)
- [ ] Autentikasi & login multi-role (Super Admin, Dinkes, Dinas Pendidikan, dll)
- [ ] Peta GIS berbasis Leaflet/peta asli (sekarang grid kecamatan)
- [ ] CRUD nyata untuk Artikel/Berita/FAQ dari dashboard
- [ ] Halaman detail artikel/berita (sekarang hanya kartu)
- [ ] Konseling online, rujukan, pelaporan kasus (baru konsep di e-Pelayanan)
- [ ] Education Center (masih Coming Soon)
- [ ] Notifikasi, User & Role Management (baru tampilan)
- [ ] Integrasi SIHA / SATUSEHAT, AI Chatbot (Future Development)

---

## 8. Catatan & Rencana (diisi oleh Anda)

> Silakan tulis di bawah ini bagian mana yang mau dikembangkan / diubah:

- [ ] ...
- [ ] ...
- [ ] ...

---

_Dokumen dibuat otomatis sebagai ringkasan status prototype. Perbarui sesuai kebutuhan._
