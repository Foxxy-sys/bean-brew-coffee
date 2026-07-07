# Bean & Brew Coffee — Company Profile Website

Website company profile premium untuk coffee shop. Dibangun dengan HTML, CSS, dan vanilla JS — tanpa framework, ringan, cepat.

## Struktur Folder

```
coffee-shop/
│
├── index.html              → halaman utama, semua section ada di sini
├── assets/
│   ├── css/
│   │   ├── style.css       → base styles, layout, komponen (navbar, hero, dst)
│   │   └── responsive.css  → media queries saja, di-load setelah style.css
│   ├── js/
│   │   └── script.js       → AOS init, navbar scroll state, mobile menu toggle
│   ├── images/             → taruh semua foto di sini (lihat catatan di bawah)
│   └── icons/               → favicon, icon custom (kalau ada)
└── README.md
```

## Cara pakai / development

1. Buka `index.html` langsung di browser, atau pakai Live Server (VS Code extension) supaya reload otomatis.
2. Semua warna & font diatur lewat CSS variable di `assets/css/style.css` bagian `:root` — ubah di situ kalau mau ganti tone.
3. Section baru cukup ditambahkan sebagai `<section>` baru di `index.html`, lalu style-nya masuk ke `style.css`. Kalau butuh override khusus mobile/tablet, taruh di `responsive.css`.

## Status Progress (Sprint)

| Sprint | Section | Status |
|---|---|---|
| 1 | Navbar | ✅ Selesai |
| 1 | Hero | ✅ Selesai |
| 2 | Featured Coffee | ⏳ Belum |
| 2 | Why Choose Us | ⏳ Belum |
| 3 | Menu | ⏳ Belum |
| 3 | Gallery | ⏳ Belum |
| 3 | Testimonials | ⏳ Belum |
| 4 | FAQ | ⏳ Belum |
| 4 | CTA | ⏳ Belum |
| 4 | Footer | ⏳ Belum |
| 4 | SEO, Responsive polish, Deploy | ⏳ Belum |

## Catatan Penting

- **Nomor WhatsApp** masih placeholder (`6281234567890`) di dua tempat (tombol "Contact" di navbar & "Order Now" di hero). Ganti ke nomor asli sebelum deploy — cari & replace string `6281234567890` di `index.html`.
- **Foto hero** saat ini masih hotlink langsung dari Unsplash (`images.unsplash.com/...`) supaya bisa langsung dilihat tanpa setup tambahan. Untuk production, sebaiknya:
  1. Download foto aslinya dari Unsplash (link difoto: photo oleh Behnam Norouzi).
  2. Simpan sebagai `assets/images/hero-coffee.jpg` (kompres dulu, misal pakai [Squoosh](https://squoosh.app) atau [TinyPNG](https://tinypng.com), target di bawah 200KB).
  3. Ganti `src` gambar di `index.html` dari URL Unsplash ke `assets/images/hero-coffee.jpg`.
  4. Ini bikin loading lebih cepat & tidak bergantung ke server Unsplash (penting untuk skor Lighthouse & kestabilan jangka panjang).
- Semua asset dari CDN eksternal (Google Fonts, AOS) tetap dipertahankan lewat `<link>`/`<script>` tag — tidak perlu didownload manual, browser yang handle caching-nya.

## Checklist kualitas (target akhir project)

- [ ] Responsive penuh (mobile, tablet, desktop)
- [ ] Lighthouse score ≥ 90 di semua kategori
- [ ] SEO dasar (meta description, alt text semua gambar, struktur heading benar)
- [ ] Accessible (focus state kelihatan, kontras warna cukup, aria-label di tombol icon)
- [ ] Loading cepat (gambar di-compress, lazy-load gambar non-hero)