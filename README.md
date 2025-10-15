# Website Katalog Undangan Digital

Website katalog undangan digital statis yang dibuat dengan HTML, CSS (Tailwind), dan JavaScript murni. Siap untuk di-deploy ke GitHub Pages.

## 🚀 Fitur

- **Responsive Design**: Tampilan optimal di desktop, tablet, dan mobile
- **Filter Kategori**: Menyaring undangan berdasarkan kategori
- **Pencarian Real-time**: Mencari undangan berdasarkan nama
- **Lazy Loading**: Optimasi loading gambar untuk performa lebih baik
- **Animasi Halus**: Transisi dan hover effects yang menarik
- **Single File**: Semua kode dalam satu file HTML

## 📁 Struktur File

```
├── index.html          # File utama website
└── README.md          # Dokumentasi ini
```

## 🛠 Cara Mengubah Brand, Logo, Warna, dan Link

### 1. Mengubah Nama Brand dan Informasi

Buka file `index.html` dan cari bagian CSS variables di dalam `<style>`:

```css
:root {
    --brand-name: "iiwedding";                    // Ganti dengan nama brand Anda
    --brand-tagline: "Pusat Undangan Digital";    // Ganti dengan tagline Anda
    --brand-description: "Buat momen spesialmu lebih berkesan dengan undangan digital yang elegan"; // Ganti deskripsi
    --logo-url: "https://i.ibb.co.com/tMhCh0FJ/Logo-Warna-2x-Kompres.png"; // Ganti URL logo
    --whatsapp-link: "https://api.whatsapp.com/send?phone=6282138860484&text=Halo%20kak%20%F0%9F%A4%97%20Saya%20mau%20tanya%20tentang%20undangan%20digital%20iiwedding"; // Ganti link WhatsApp
    --instagram-link: "https://www.instagram.com/iiwedding_undangan_digital?igsh=MTZja2J5aTI3c3llbg=="; // Ganti link Instagram
    --bg-color: #e8fffb;                          // Ganti warna background
    --accent-color: #06d2b3;                      // Ganti warna aksen
    --text-color: #1f2937;                        // Ganti warna teks
}
```

### 2. Mengubah Warna

#### Warna Background Utama
```css
--bg-color: #e8fffb; /* Ganti dengan kode hex warna yang diinginkan */
```

#### Warna Aksen (Tombol, Link, Hover)
```css
--accent-color: #06d2b3; /* Ganti dengan kode hex warna yang diinginkan */
```

#### Warna Teks
```css
--text-color: #1f2937; /* Ganti dengan kode hex warna yang diinginkan */
```

### 3. Mengubah Logo

Ganti nilai `--logo-url` dengan URL logo baru Anda:

```css
--logo-url: "https://URL-LOGO-ANDA.jpg";
```

### 4. Mengubah Link WhatsApp

Format link WhatsApp:
```
https://api.whatsapp.com/send?phone=NOMOR_HP&text=PESAN_ANDA
```

Contoh:
```css
--whatsapp-link: "https://api.whatsapp.com/send?phone=628123456789&text=Halo%20saya%20mau%20tanya";
```

### 5. Mengubah Link Instagram

Ganti dengan URL Instagram profil Anda:
```css
--instagram-link: "https://www.instagram.com/NAMA_INSTAGRAM_ANDA";
```

### 6. Mengubah Data Produk

Data produk tersimpan dalam array JavaScript di bagian bawah file `index.html`. Cari bagian:

```javascript
const products = [
    { nama: "Nama Produk", kategori: "Kategori", preview: "URL_PREVIEW", gambar: "URL_GAMBAR", keterangan: "Fast" },
    // ... data produk lainnya
];
```

Untuk menambah produk baru:
```javascript
{ 
    nama: "Nama Produk Baru", 
    kategori: "Kategori Baru", 
    preview: "https://contoh.com/preview", 
    gambar: "https://contoh.com/gambar.jpg", 
    keterangan: "Fast" // Opsional, kosongkan jika tidak ada label "kilat"
}
```

## 🎨 Kustomisasi Tambahan

### Mengubah Teks pada Section

#### Hero Section
Cari bagian ini di HTML:
```html
<h1 class="text-4xl md:text-5xl font-bold mb-4 text-gray-800">iiwedding</h1>
<p class="text-2xl md:text-3xl mb-6 accent-text font-semibold">Pusat Undangan Digital</p>
<p class="text-lg md:text-xl text-gray-600 max-w-2xl mx-auto">Buat momen spesialmu lebih berkesan dengan undangan digital yang elegan</p>
```

#### Section Catatan
Cari bagian ini di HTML:
```html
<div class="bg-gradient-to-br from-accent to-teal-500 p-8 rounded-xl shadow-lg text-white text-center">
    <h3 class="text-xl font-bold mb-4">CATATAN</h3>
    <p class="text-sm leading-relaxed">
        Waktu pengerjaan 3-7 hari tergantung banyaknya antrian...
    </p>
</div>
```

### Mengubah Fitur

Fitur-fitur ditampilkan dalam grid. Untuk mengubahnya, cari bagian:

```html
<div class="feature-card bg-white p-6 rounded-lg shadow-md text-center">
    <i class="fas fa-NAMA-ICON text-3xl mb-3 accent-text"></i>
    <p class="text-sm font-medium">NAMA FITUR</p>
</div>
```

Icon menggunakan Font Awesome. Ganti `fa-NAMA-ICON` dengan icon yang diinginkan.

## 🌐 Deploy ke GitHub Pages

1. Upload file `index.html` ke repository GitHub Anda
2. Buka repository → Settings → Pages
3. Pilih "Deploy from a branch"
4. Pilih branch `main` dan folder `/root`
5. Klik "Save"
6. Website akan tersedia di `https://NAMA_USER.github.io/NAMA_REPO`

## 📱 Responsive Breakpoints

- **Mobile**: < 768px (1 kolom produk)
- **Tablet**: 768px - 1024px (2 kolom produk)
- **Desktop**: > 1024px (4 kolom produk)

## 🎯 Tips Tambahan

1. **Optimasi Gambar**: Gunakan gambar dengan ukuran yang tepat (sekitar 400x300px untuk thumbnail)
2. **SEO**: Tambahkan meta tags di `<head>` untuk optimasi mesin pencari
3. **Analytics**: Tambahkan Google Analytics atau tracking lainnya
4. **Custom Domain**: Untuk GitHub Pages, tambahkan file `CNAME` di root repository

## 🐞 Troubleshooting

### Gambar Tidak Muncul
- Pastikan URL gambar valid dan accessible
- Cek apakah gambar menggunakan HTTPS (wajib untuk keamanan)

### Link Tidak Berfungsi
- Pastikan URL lengkap dengan https://
- Cek apakah target link valid

### Warna Tidak Berubah
- Pastikan mengubah nilai di CSS variables (`:root`)
- Clear cache browser setelah perubahan

## 📞 Support

Jika mengalami kesulitan, silakan cek:
1. Console browser untuk error JavaScript
2. Validasi HTML menggunakan W3C Validator
3. Pastikan semua link dan URL valid

---

**Dibuat dengan ❤️ menggunakan HTML, Tailwind CSS, dan JavaScript murni**