# PortfolioTracker - Dashboard Pelacak Portofolio Pribadi

Dashboard profesional untuk melacak dan mengelola portofolio investasi Anda dengan UI modern dan dark mode theme dengan aksen emerald green.

## Fitur Utama

- **Header Interaktif**: Menampilkan total nilai portofolio dan persentase perubahan harian
- **Sidebar Navigasi**: Menu navigasi untuk Dasbor, Aset, Riwayat, dan Pengaturan
- **Grafik Kinerja**: Visualisasi pertumbuhan portofolio dengan line chart interaktif
- **Tabel Aset**: Menampilkan detail aset (Nama, Kategori, Jumlah, Nilai, Laba/Rugi)
- **Tambah Aset**: Modal untuk menambahkan aset investasi baru
- **Dark Mode**: Theme gelap modern dengan aksen emerald green

## Teknologi yang Digunakan

- **Next.js 16** - React framework dengan App Router
- **TypeScript** - Type-safe development
- **Tailwind CSS v4** - Utility-first CSS framework
- **shadcn/ui** - Komponen UI yang dapat disesuaikan
- **Recharts** - Library untuk grafik dan visualisasi data
- **Lucide React** - Icon set modern

## Cara Install & Menjalankan

### Opsi 1: Menggunakan Shadcn CLI (Direkomendasikan)

```bash
npx shadcn@latest init portfolio-tracker
cd portfolio-tracker
npm install
npm run dev
```

### Opsi 2: Download ZIP

1. Klik tombol "..." di kanan atas project
2. Pilih "Download ZIP"
3. Extract file ZIP
4. Buka terminal di folder project
5. Jalankan perintah:

```bash
npm install
npm run dev
```

### Opsi 3: Deploy ke Vercel

1. Klik tombol "Publish" di kanan atas
2. Login ke akun Vercel Anda
3. Aplikasi akan otomatis di-deploy

## Struktur Folder

```
portfolio-tracker/
├── app/
│   ├── layout.tsx          # Root layout dengan metadata
│   ├── page.tsx            # Homepage
│   └── globals.css         # Global styles & theme
├── components/
│   ├── portfolio.tsx       # Main portfolio component
│   ├── portfolio-header.tsx    # Header dengan total value
│   ├── portfolio-sidebar.tsx   # Sidebar navigasi
│   ├── portfolio-chart.tsx     # Grafik kinerja
│   ├── assets-table.tsx        # Tabel daftar aset
│   └── add-asset-modal.tsx     # Modal tambah aset
└── components/ui/          # shadcn/ui components
```

## Customisasi

### Mengubah Warna Theme

Edit file `app/globals.css` untuk mengubah color tokens:

```css
:root {
  --primary: oklch(0.65 0.22 166);  /* Emerald green accent */
  --background: oklch(0.145 0 0);   /* Dark background */
  /* ... token lainnya ... */
}
```

### Menambah Data Aset

Edit file `components/assets-table.tsx` untuk menambahkan data aset:

```tsx
const assets = [
  {
    id: 1,
    name: "Bitcoin",
    category: "Cryptocurrency",
    amount: "2.5 BTC",
    value: 85000000,
    change: 15.2,
    isPositive: true,
  },
  // Tambahkan aset lainnya...
]
```

## Fitur Mendatang

- Integrasi dengan API real-time untuk harga aset
- Database untuk menyimpan data portofolio
- Autentikasi pengguna
- Export data ke PDF/Excel
- Notifikasi perubahan harga
- Responsive mobile view yang lebih baik

## Support

Jika Anda menemukan bug atau memiliki pertanyaan, silakan buat issue atau hubungi support.

## Lisensi

MIT License - Bebas digunakan untuk proyek pribadi dan komersial.
