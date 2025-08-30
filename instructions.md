# Cara Menggunakan Generator di Netlify & Blogger

Panduan ini membantu Anda meng-hosting file generator secara gratis dan menyematkannya di postingan Blogger.

---

## Langkah 1: Unggah ke GitHub

1. **Buat Akun GitHub**  
   Jika belum punya, daftar di [github.com](https://github.com).

2. **Buat Repositori Baru**

   - Klik ikon `+` di pojok kanan atas, lalu pilih **New repository**.
   - Beri nama repositori, misal: `blogger-generator`.
   - Pastikan repositori diatur ke **Public**.
   - Klik **Create repository**.

3. **Unggah File**
   - Di halaman repositori, klik **Add file** lalu **Upload files**.
   - Seret file `post_generator.html` ke area unggah.
   - Klik **Commit changes**.

---

## Langkah 2: Sebarkan ke Netlify

1. **Buat Akun Netlify**  
   Daftar di [netlify.com](https://netlify.com) menggunakan akun GitHub.

2. **Impor Proyek dari Git**

   - Di dashboard Netlify, klik **Add new site** > **Import an existing project**.
   - Pilih **GitHub** sebagai provider.
   - Cari dan pilih repositori yang baru dibuat (`blogger-generator`).

3. **Konfigurasi & Deploy**

   - Netlify akan otomatis mendeteksi pengaturan yang benar.
   - Klik tombol **Deploy site**.

4. **Dapatkan URL Anda**
   - Setelah deploy, Netlify akan memberikan URL acak (misal: `random-name-12345.netlify.app`).
   - Anda bisa mengubahnya di **Site settings** > **Change site name**.
   - Simpan URL ini.

---

## Langkah 3: Sematkan (Embed) di Blogger

1. Buka editor postingan/halaman di Blogger.
2. Beralih ke mode **Tampilan HTML** (`</>`).
3. Salin dan tempel kode di bawah ini ke dalam editor.

**PENTING:** Ganti `URL_NETLIFY_ANDA` dengan URL Netlify Anda dari langkah sebelumnya.

```html
<div
  style="position: relative; width: 100%; padding-top: 150%; overflow: hidden; border-radius: 12px; border: 1px solid #ddd;"
>
  <iframe
    src="URL_NETLIFY_ANDA"
    style="position: absolute; top: 0; left: 0; width: 100%; height: 100%; border: 0;"
    allowfullscreen=""
    loading="lazy"
  >
  </iframe>
</div>
```

Kode `<iframe>` di atas sudah responsif, sehingga tampil baik di desktop maupun mobile.

---
