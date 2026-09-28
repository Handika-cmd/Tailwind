#Typography
# Typography

<p align="center">
  <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSl-i2V9tzMZ1iPpHV3CjFPQfQmdi4fGpYtSPrRIF5rU8-PzecjSibLy3UL&s=10" alt="Tailwind CSS" width="380">
</p>

<p align="center">
  <strong>Memahami cara mengatur tampilan teks menggunakan utility class Tailwind CSS.</strong>
</p>

---

## Materi

Hari ini saya belajar tentang typography di Tailwind CSS:

* Font Size
* Font Weight
* Text Alignment
* Line Height
* Letter Spacing
* Text Decoration
* Text Transform
* Kombinasi utility typography
* Membuat typography hierarchy
* Cheatsheet typography

---

# 1. Apa Itu Typography?

Typography adalah cara mengatur bagaimana teks ditampilkan pada sebuah halaman.

Typography tidak hanya berkaitan dengan ukuran font.

Beberapa hal yang termasuk di dalamnya:

```text
Typography
│
├── Font Size
├── Font Weight
├── Text Alignment
├── Line Height
├── Letter Spacing
├── Text Decoration
└── Text Transform
```

Contohnya:

```text
Judul
→ besar
→ tebal

Deskripsi
→ lebih kecil
→ normal
→ line-height lebih lega

Button
→ sedang
→ tebal
→ uppercase
```

Dengan Tailwind, semua pengaturan tersebut dapat dilakukan menggunakan utility class.

---

# 2. Font Size

Font size digunakan untuk mengatur ukuran teks.

Tailwind menggunakan prefix:

```text
text-*
```

Contoh:

```html
<p class="text-sm">Small Text</p>

<p class="text-base">Base Text</p>

<p class="text-lg">Large Text</p>

<p class="text-xl">Extra Large Text</p>
```

---

## Ukuran Font

Cheatsheet:

| Class       | Ukuran Default |
| ----------- | -------------: |
| `text-xs`   |        0.75rem |
| `text-sm`   |       0.875rem |
| `text-base` |           1rem |
| `text-lg`   |       1.125rem |
| `text-xl`   |        1.25rem |
| `text-2xl`  |         1.5rem |
| `text-3xl`  |       1.875rem |
| `text-4xl`  |        2.25rem |
| `text-5xl`  |           3rem |
| `text-6xl`  |        3.75rem |
| `text-7xl`  |         4.5rem |
| `text-8xl`  |           6rem |
| `text-9xl`  |           8rem |

Contoh:

```html
<h1 class="text-4xl">
  Belajar Tailwind CSS
</h1>
```

Artinya heading menggunakan ukuran `text-4xl`.

---

# 3. Font Weight

Font weight mengatur tingkat ketebalan teks.

Prefix yang digunakan:

```text
font-*
```

Contoh:

```html
<p class="font-normal">
  Normal
</p>

<p class="font-medium">
  Medium
</p>

<p class="font-semibold">
  Semibold
</p>

<p class="font-bold">
  Bold
</p>
```

---

## Font Weight Cheatsheet

| Class             | Weight |
| ----------------- | -----: |
| `font-thin`       |    100 |
| `font-extralight` |    200 |
| `font-light`      |    300 |
| `font-normal`     |    400 |
| `font-medium`     |    500 |
| `font-semibold`   |    600 |
| `font-bold`       |    700 |
| `font-extrabold`  |    800 |
| `font-black`      |    900 |

Contoh:

```html
<h1 class="text-3xl font-bold">
  Belajar Tailwind
</h1>
```

Di sini terdapat dua utility:

```text
text-3xl
→ ukuran teks

font-bold
→ ketebalan teks
```

---

# 4. Text Alignment

Text alignment digunakan untuk mengatur posisi teks secara horizontal.

Prefix:

```text
text-*
```

Untuk alignment:

```html
<p class="text-left">
  Teks kiri
</p>

<p class="text-center">
  Teks tengah
</p>

<p class="text-right">
  Teks kanan
</p>

<p class="text-justify">
  Teks rata kiri dan kanan
</p>
```

---

## Alignment Cheatsheet

| Class          | Fungsi              |
| -------------- | ------------------- |
| `text-left`    | Rata kiri           |
| `text-center`  | Rata tengah         |
| `text-right`   | Rata kanan          |
| `text-justify` | Rata kiri-kanan     |
| `text-start`   | Mengikuti arah teks |
| `text-end`     | Mengikuti arah teks |

Contoh card:

```html
<div class="text-center">
  <h2 class="text-2xl font-bold">
    Handika Saputra
  </h2>

  <p>
    Calon Full Stack Developer
  </p>
</div>
```

---

# 5. Line Height

Line height mengatur jarak vertikal antar baris teks.

Tailwind menggunakan:

```text
leading-*
```

Contoh:

```html
<p class="leading-none">
  Teks dengan line height sangat rapat.
</p>
```

```html
<p class="leading-normal">
  Teks dengan line height normal.
</p>
```

```html
<p class="leading-loose">
  Teks dengan line height lebih longgar.
</p>
```

---

## Line Height Cheatsheet

| Class             | Fungsi        |
| ----------------- | ------------- |
| `leading-none`    | sangat rapat  |
| `leading-tight`   | rapat         |
| `leading-snug`    | sedikit rapat |
| `leading-normal`  | normal        |
| `leading-relaxed` | lebih lega    |
| `leading-loose`   | sangat lega   |

Ada juga nilai numerik:

```html
<p class="leading-4">Text</p>
<p class="leading-5">Text</p>
<p class="leading-6">Text</p>
<p class="leading-7">Text</p>
<p class="leading-8">Text</p>
```

---

```html
<p class="leading-relaxed">
  Lorem ipsum dolor sit amet, consectetur adipisicing elit,
  sed do eiusmod tempor incididunt ut labore et dolore magna
  aliqua.
</p>
```

Teks menjadi lebih nyaman dibaca.

Untuk paragraf panjang, `leading-relaxed` sering berguna sebagai titik awal, lalu disesuaikan berdasarkan desain.

---

# 6. Letter Spacing

Letter spacing mengatur jarak antar karakter.

Tailwind menggunakan prefix:

```text
tracking-*
```

Contoh:

```html
<p class="tracking-tight">
  Tight Text
</p>

<p class="tracking-normal">
  Normal Text
</p>

<p class="tracking-wide">
  Wide Text
</p>
```

---

## Letter Spacing Cheatsheet

| Class              | Fungsi           |
| ------------------ | ---------------- |
| `tracking-tighter` | sangat rapat     |
| `tracking-tight`   | rapat            |
| `tracking-normal`  | normal           |
| `tracking-wide`    | lebih lebar      |
| `tracking-wider`   | lebih lebar lagi |
| `tracking-widest`  | paling lebar     |

Contoh:

```html
<h2 class="uppercase tracking-widest">
  Portfolio
</h2>
```

Ini sering digunakan untuk label kecil atau heading bergaya editorial.

---

# 7. Text Decoration

Text decoration digunakan untuk memberikan dekorasi pada teks.

Contohnya:

```text
underline
line-through
overline
```

Tailwind menyediakan:

```html
<p class="underline">
  Underline
</p>

<p class="line-through">
  Coret
</p>

<p class="overline">
  Overline
</p>
```

---

## Menghapus Decoration

Gunakan:

```html
<a class="no-underline">
  Link
</a>
```

---

## Decoration Cheatsheet

| Class          | Fungsi              |
| -------------- | ------------------- |
| `underline`    | garis bawah         |
| `overline`     | garis atas          |
| `line-through` | garis tengah        |
| `no-underline` | menghapus underline |

---

# 8. Text Transform

Text transform digunakan untuk mengubah bentuk huruf.

Tailwind menyediakan:

```html
<p class="uppercase">
  hello world
</p>
```

Hasil:

```text
HELLO WORLD
```

---

### Lowercase

```html
<p class="lowercase">
  HELLO WORLD
</p>
```

Hasil:

```text
hello world
```

---

### Capitalize

```html
<p class="capitalize">
  hello world
</p>
```

Hasil:

```text
Hello World
```

---

### Normal Case

```html
<p class="normal-case">
  Hello World
</p>
```

---

## Transform Cheatsheet

| Class         | Hasil                   |
| ------------- | ----------------------- |
| `uppercase`   | HURUF BESAR             |
| `lowercase`   | huruf kecil             |
| `capitalize`  | Huruf Awal Besar        |
| `normal-case` | mengikuti bentuk normal |

---

# 9. Menggabungkan Typography

Kekuatan Tailwind mulai terasa ketika beberapa utility digabungkan.

Contoh:

```html
<h1 class="text-4xl font-bold text-center leading-tight">
  Belajar Tailwind CSS
</h1>
```

Kita dapat membacanya:

```text
text-4xl
→ ukuran

font-bold
→ ketebalan

text-center
→ posisi

leading-tight
→ jarak antar baris
```

Contoh yang lebih lengkap:

```html
<h2 class="text-2xl font-semibold text-center uppercase tracking-wide">
  About Me
</h2>
```

Artinya:

```text
text-2xl
→ ukuran besar

font-semibold
→ cukup tebal

text-center
→ rata tengah

uppercase
→ huruf kapital

tracking-wide
→ jarak antar huruf lebih lebar
```

---

# 10. Typography Hierarchy

Website biasanya memiliki tingkatan teks.

Contoh:

```text
H1
↓
Judul utama

H2
↓
Judul section

H3
↓
Subsection

Paragraph
↓
Informasi

Small Text
↓
Keterangan tambahan
```

Contoh menggunakan Tailwind:

```html
<h1 class="text-4xl font-bold">
  Personal Portfolio
</h1>

<h2 class="text-2xl font-semibold">
  About Me
</h2>

<h3 class="text-xl font-medium">
  My Skills
</h3>

<p class="text-base leading-relaxed">
  Saya sedang mempelajari web development
  dan membangun fondasi full stack development.
</p>

<span class="text-sm">
  Last updated: September 2026
</span>
```

---

# 11. Contoh Typography pada Website

Misalnya membuat bagian hero:

```html
<section class="text-center">

  <p class="text-sm uppercase tracking-widest">
    Welcome to my portfolio
  </p>

  <h1 class="mt-3 text-4xl font-bold leading-tight">
    Handika Saputra
  </h1>

  <p class="mt-4 text-lg leading-relaxed">
    Calon Full Stack Developer yang sedang membangun
    fondasi web development dari HTML, CSS, JavaScript,
    Tailwind CSS, PHP, dan database.
  </p>

  <a
    href="#project"
    class="mt-6 inline-block underline"
  >
    Lihat Project
  </a>

</section>
```

Di sini hampir semua materi Day 4 digunakan.

---

# 12. Typography Cheat Sheet

Bagian ini bisa digunakan sebagai referensi cepat ketika lupa utility class.

## Font Size

```text
text-xs
text-sm
text-base
text-lg
text-xl
text-2xl
text-3xl
text-4xl
text-5xl
text-6xl
text-7xl
text-8xl
text-9xl
```

## Font Weight

```text
font-thin
font-extralight
font-light
font-normal
font-medium
font-semibold
font-bold
font-extrabold
font-black
```

## Text Alignment

```text
text-left
text-center
text-right
text-justify
text-start
text-end
```

## Line Height

```text
leading-none
leading-tight
leading-snug
leading-normal
leading-relaxed
leading-loose
```

## Letter Spacing

```text
tracking-tighter
tracking-tight
tracking-normal
tracking-wide
tracking-wider
tracking-widest
```

## Text Decoration

```text
underline
overline
line-through
no-underline
```

## Text Transform

```text
uppercase
lowercase
capitalize
normal-case
```

---

# 13. Cheat Sheet Lengkap

| Kebutuhan         | Prefix / Utility | Contoh            |
| ----------------- | ---------------- | ----------------- |
| Font size         | `text-*`         | `text-2xl`        |
| Font weight       | `font-*`         | `font-bold`       |
| Text alignment    | `text-*`         | `text-center`     |
| Line height       | `leading-*`      | `leading-relaxed` |
| Letter spacing    | `tracking-*`     | `tracking-wide`   |
| Underline         | `underline`      | `underline`       |
| Overline          | `overline`       | `overline`        |
| Coret             | `line-through`   | `line-through`    |
| Hapus decoration  | `no-underline`   | `no-underline`    |
| Huruf besar       | `uppercase`      | `uppercase`       |
| Huruf kecil       | `lowercase`      | `lowercase`       |
| Awal kata kapital | `capitalize`     | `capitalize`      |
| Normal            | `normal-case`    | `normal-case`     |

---

# 14. Cheat Sheet Visual

```text
UKURAN
text-sm
text-base
text-lg
text-xl
text-2xl
text-3xl
text-4xl


KETEBALAN
font-light
font-normal
font-medium
font-semibold
font-bold
font-extrabold


POSISI
text-left
text-center
text-right
text-justify


JARAK BARIS
leading-tight
leading-normal
leading-relaxed
leading-loose


JARAK HURUF
tracking-tight
tracking-normal
tracking-wide
tracking-wider
tracking-widest


DEKORASI
underline
overline
line-through
no-underline


TRANSFORMASI
uppercase
lowercase
capitalize
normal-case
```

---

# 15. Praktik Mandiri

Buat sebuah halaman sederhana dengan struktur:

```text
Portfolio
│
├── Badge / Label
│
├── Heading
│
├── Description
│
├── Button
│
└── Small Information
```

Gunakan minimal:

```text
text-*
font-*
text-center
leading-*
tracking-*
uppercase
underline
```

Jangan melihat contoh sebelumnya ketika mulai mengetik.

Tujuannya untuk menguji apakah saya sudah mulai mengingat pola utility class.

---

# 16. Challenge — Profile Introduction

Buat sebuah profile introduction menggunakan data sendiri.

Contoh hasil:

```text
WELCOME TO MY PROFILE

Handika Saputra

Calon Full Stack Developer

Saya sedang mempelajari web development
dan membangun kemampuan dari frontend
hingga backend.

[ Explore My Journey ]
```

Minimal gunakan:

```text
text-*
font-*
leading-*
tracking-*
uppercase
text-center
```
---

# 17. Mini Project — Typography Showcase

Membuat satu halaman yang menampilkan seluruh materi typography.

Contoh struktur:

```html
<main>

  <h1>Typography Showcase</h1>

  <section>
    <h2>Font Size</h2>
    <p class="text-sm">Small</p>
    <p class="text-base">Base</p>
    <p class="text-xl">Large</p>
    <p class="text-4xl">Extra Large</p>
  </section>

  <section>
    <h2>Font Weight</h2>
    <p class="font-light">Light</p>
    <p class="font-normal">Normal</p>
    <p class="font-bold">Bold</p>
    <p class="font-black">Black</p>
  </section>

  <section>
    <h2>Alignment</h2>
    <p class="text-left">Left</p>
    <p class="text-center">Center</p>
    <p class="text-right">Right</p>
  </section>

</main>
```

---

# 18. Kesalahan yang Perlu Dihindari

### Jangan menganggap `text-*` hanya untuk ukuran

Ada beberapa utility yang sama-sama menggunakan prefix `text-`.

Contoh:

```text
text-2xl
→ font size

text-center
→ alignment
```

Jadi konteks utility perlu diperhatikan.

---

### Jangan menggunakan font weight berlebihan

Tidak semua teks harus:

```text
font-bold
```

Biasanya hierarchy lebih mudah dibaca jika terdapat perbedaan antara:

```text
font-normal
font-medium
font-semibold
font-bold
```

---

### Jangan mengabaikan line height

Ukuran font yang bagus belum tentu menghasilkan teks yang nyaman dibaca.

Contoh:

```html
<p class="text-lg leading-relaxed">
  ...
</p>
```

kombinasi tersebut dapat lebih nyaman untuk paragraf yang cukup panjang dibandingkan hanya:

```html
<p class="text-lg">
  ...
</p>
```

---


# 19. Ringkasan Hari Ini

```text
text-*       → ukuran teks
font-*       → ketebalan teks
text-center  → alignment
leading-*    → line height
tracking-*   → letter spacing
underline    → underline
overline     → overline
line-through → coret
uppercase    → huruf besar
lowercase    → huruf kecil
capitalize   → kapital pada awal kata
```

---

<p align="center">
  <strong>04-Typography</strong>
</p>

<p align="center">
  Learn the utility. Understand the design. Build it yourself.
</p>
