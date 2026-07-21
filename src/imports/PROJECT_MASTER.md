# SISTEM INFORMASI TERPADU HIV/AIDS SIDOARJO

## Version

Prototype v1.0

---

# Project Overview

Sistem Informasi Terpadu HIV/AIDS Sidoarjo merupakan platform digital berbasis yayasan yang bertujuan menjadi media kolaborasi antara masyarakat, Dinas Kesehatan, Dinas Pendidikan, Rumah Sakit, Klinik, Puskesmas, Psikolog, dan berbagai stakeholder lainnya.

Platform ini berfungsi sebagai:

- Pusat Informasi HIV/AIDS
- Media Edukasi
- Platform e-Pelayanan
- Dashboard Monitoring
- Collaboration Hub

---

# Stakeholder

- Yayasan (Super Admin)
- Dinas Kesehatan
- Dinas Pendidikan
- Rumah Sakit
- Klinik
- Puskesmas
- Psikolog
- Masyarakat

---

# System Architecture

                    SUPER ADMIN (YAYASAN)
                                   │
         ┌─────────────────────────┼─────────────────────────┐
         │                         │                         │
         ▼                         ▼                         ▼
 Dinas Pendidikan          Dinas Kesehatan           Dashboard Publik
      (Mitra)                   (Mitra)                (Masyarakat)
         │                         │                         │
         │                         │                         │
 ┌──────────────────┐     ┌──────────────────┐      ┌──────────────────┐
 │ Education Center │     │   e-Pelayanan    │      │ Public Information│
 └──────────────────┘     └──────────────────┘      └──────────────────┘
         │                         │                         │
         ├── Marketplace Edukasi   ├── Assessment           ├── Informasi Umum
         ├── CSE                   ├── Screening            ├── Artikel
         ├── Modul Guru            ├── Konseling            ├── Berita
         ├── Media Edukasi         ├── Rujukan              ├── FAQ
         └── Coming Soon           ├── Monitoring           ├── Statistik
                                   ├── Pelaporan Kasus      ├── GIS Map
                                   └── Dashboard Nakes      └── Cari Faskes

                    │
                    ▼

         COLLABORATION DATA CENTER

                    │

      ┌─────────────┼─────────────┐

      ▼             ▼             ▼

Education Data   Clinical Data   Public Analytics

---

# Module Status

## Public Information

Status : Active

Menu

- Beranda
- Informasi Umum
- Artikel
- Berita
- FAQ
- Statistik
- GIS Map
- Cari Fasilitas

---

## e-Pelayanan

Status : Prototype

Menu

- Assessment
- Screening
- Konseling
- Rujukan
- Monitoring
- Pelaporan Kasus
- Dashboard Tenaga Kesehatan

---

## Education Center

Status : Coming Soon

Konsep

Marketplace Edukasi Digital

Target

- Guru
- Sekolah
- Mahasiswa
- Orang Tua
- Komunitas

---

# Dashboard Publik

## Informasi Umum

- Apa itu HIV
- Apa itu AIDS
- Pencegahan
- Penularan
- Layanan Pemerintah

## Artikel

CRUD melalui Dashboard Admin

## Berita

CRUD melalui Dashboard Admin

## FAQ

CRUD melalui Dashboard Admin

## Statistik

- Total Kasus
- Kasus Baru
- ODHIV
- ARV
- VCT
- Grafik
- Realtime Counter

## GIS

Interactive Map

Klik Kecamatan

↓

Jumlah Kasus

↓

Grafik

↓

Rumah Sakit

↓

Puskesmas

↓

Klinik

↓

Trend

---

# Dashboard Admin

## Super Admin

- Dashboard
- Approval Center
- User Management
- Role Management
- Analytics
- Notification
- Master Data
- Settings

---

## Admin Public Information

- Artikel
- Berita
- FAQ
- Banner
- Slider
- Homepage
- Informasi Umum
- GIS
- Statistik

---

## Admin Dinas Kesehatan

- e-Pelayanan
- Assessment
- Monitoring
- Konseling
- Rujukan
- Pelaporan Kasus
- Dashboard Nakes
- GIS Data
- Statistik

---

## Admin Dinas Pendidikan

Coming Soon

---

# Approval Workflow

Admin

↓

Submit

↓

Pending

↓

Super Admin

↓

Approve

↓

Publish

---

# Future Development

- Education Marketplace
- Volunteer Center
- Community Support
- Mobile Apps
- AI Recommendation
- AI Chatbot
- SIHA Integration
- SATUSEHAT Integration
- Decision Support System
