# Spacing & Sizing

<p align="center">
  <img src="https://media.geeksforgeeks.org/wp-content/uploads/20210211221949/Screenshot20210211221930-660x448.png" alt="Tailwind CSS" width="280">
</p>

<p align="center">
  <strong>Belajar mengatur jarak, ukuran, dan ruang pada elemen menggunakan Tailwind CSS.</strong>
</p>

---
<p align="center"> <img src="https://static.vecteezy.com/system/resources/previews/067/565/433/non_2x/tailwind-css-logo-rounded-free-png.png" alt="PHP" width="120"> </p>

## Target Belajar

Hari ini fokus pada bagaimana mengatur **ruang dan ukuran elemen** menggunakan utility class Tailwind CSS.

Target yang ingin saya pahami:

* memahami `padding`
* memahami `margin`
* memahami `space-*`
* memahami `width` dan `height`
* memahami perbedaan `p-*`, `m-*`, `w-*`, `h-*`
* membuat card sederhana

---

## Kenapa Spacing & Sizing Penting?

Website yang terlihat rapi bukan hanya tentang warna dan font.

Jarak antar elemen juga sangat menentukan bagaimana sebuah halaman terasa.

Misalnya:

```text
Tanpa spacing:

┌─────────────────────┐
│Nama                 │
│Deskripsi            │
│Button               │
└─────────────────────┘
```

dibandingkan dengan:

```text
Dengan spacing:

┌─────────────────────┐
│                     │
│  Nama               │
│                     │
│  Deskripsi          │
│                     │
│  [ Button ]         │
│                     │
└─────────────────────┘
```

Tailwind menyediakan utility class untuk mengatur spacing tanpa harus membuat banyak CSS sendiri.

---

# 1. Padding

`padding` adalah ruang **di dalam sebuah elemen**.

Secara sederhana:

```text
┌─────────────────────────────┐
│        padding              │
│   ┌─────────────────────┐   │
│   │      content        │   │
│   └─────────────────────┘   │
│        padding              │
└─────────────────────────────┘
```

Di Tailwind, padding menggunakan prefix:

```text
p-
```

Contoh:

```html
<div class="p-4">
  Hello Tailwind
</div>
```

Artinya elemen memiliki padding pada semua sisi.

---

## Arah Padding

Tailwind juga menyediakan pengaturan berdasarkan arah.

| Class  | Keterangan     |
| ------ | -------------- |
| `p-4`  | semua sisi     |
| `px-4` | kiri dan kanan |
| `py-4` | atas dan bawah |
| `pt-4` | atas           |
| `pr-4` | kanan          |
| `pb-4` | bawah          |
| `pl-4` | kiri           |

Contoh:

```html
<div class="px-6 py-4">
  Card Content
</div>
```

Artinya:

```text
px-6 → kiri + kanan
py-4 → atas + bawah
```

---

# 2. Margin

Kalau `padding` memberikan ruang **di dalam elemen**, maka `margin` memberikan ruang **di luar elemen**.

```text
          margin
    ↓               ↓

  ┌─────────────────────┐
  │       padding       │
  │   ┌─────────────┐   │
  │   │   content   │   │
  │   └─────────────┘   │
  └─────────────────────┘
```

Tailwind menggunakan prefix:

```text
m-
```

Contoh:

```html
<div class="m-4">
  Hello
</div>
```

---

## Arah Margin

| Class  | Keterangan     |
| ------ | -------------- |
| `m-4`  | semua sisi     |
| `mx-4` | kiri dan kanan |
| `my-4` | atas dan bawah |
| `mt-4` | atas           |
| `mr-4` | kanan          |
| `mb-4` | bawah          |
| `ml-4` | kiri           |

Contoh:

```html
<div class="mb-4">
  <h2>Judul</h2>
</div>
```

`mb-4` berarti memberikan margin bagian bawah.

---

# 3. Padding vs Margin

Ini salah satu bagian yang penting untuk dipahami.

| Padding                             | Margin                                  |
| ----------------------------------- | --------------------------------------- |
| Ruang di dalam elemen               | Ruang di luar elemen                    |
| Membuat content menjauh dari border | Membuat elemen menjauh dari elemen lain |
| `p-*`                               | `m-*`                                   |
| `px-*`, `py-*`                      | `mx-*`, `my-*`                          |

Cara sederhana mengingatnya:

```text
PADDING
Content ←→ bagian dalam

MARGIN
Element ←→ element lain
```

Contoh:

```html
<div class="p-6 mb-4">
  <h2>Card</h2>
</div>
```

Di sini:

```text
p-6  → memberi ruang di dalam card
mb-4 → memberi jarak setelah card
```

---

# 4. Space

Tailwind juga memiliki utility `space-*`.

`space-*` digunakan untuk memberikan jarak **antar child element**.

Contoh:

```html
<div class="space-y-4">
  <p>Nama</p>
  <p>Email</p>
  <p>Program Studi</p>
</div>
```

`space-y-4` memberikan jarak vertikal antar elemen tersebut.

Visualisasinya:

```text
Nama

    ↓ space-y-4

Email

    ↓ space-y-4

Program Studi
```

---

## `space-x-*`

Untuk arah horizontal:

```html
<div class="flex space-x-4">
  <button>Login</button>
  <button>Register</button>
</div>
```

Artinya memberikan jarak horizontal antar child.

```text
[ Login ]    [ Register ]
           ↑
        space-x-4
```

---

# 5. Width

Untuk mengatur lebar elemen digunakan:

```text
w-*
```

Contoh:

```html
<div class="w-64">
  Content
</div>
```

Beberapa contoh:

```html
<div class="w-32"></div>
<div class="w-48"></div>
<div class="w-64"></div>
<div class="w-full"></div>
```

`w-full` berarti menggunakan seluruh lebar parent yang tersedia.

---

## Width dengan Persentase

Tailwind juga menyediakan ukuran berbasis persentase.

Contoh:

```html
<div class="w-1/2">
  50%
</div>
```

```html
<div class="w-1/3">
  33.33%
</div>
```

```html
<div class="w-2/3">
  66.67%
</div>
```

---

# 6. Height

Untuk mengatur tinggi elemen digunakan:

```text
h-*
```

Contoh:

```html
<div class="h-32">
  Content
</div>
```

Contoh lainnya:

```html
<div class="h-24"></div>
<div class="h-32"></div>
<div class="h-48"></div>
<div class="h-64"></div>
```

Untuk memenuhi tinggi parent:

```html
<div class="h-full"></div>
```

---

# 7. Memahami `p-*`, `m-*`, `w-*`, dan `h-*`

Ini bagian yang perlu mulai dibiasakan ketika membaca class Tailwind.

| Prefix | Fungsi  | Contoh |
| ------ | ------- | ------ |
| `p-*`  | Padding | `p-4`  |
| `m-*`  | Margin  | `m-4`  |
| `w-*`  | Width   | `w-64` |
| `h-*`  | Height  | `h-32` |

Contoh:

```html
<div class="w-64 h-32 p-4 m-4">
  Hello
</div>
```

Cara membacanya:

```text
w-64 → lebar
h-32 → tinggi
p-4  → ruang bagian dalam
m-4  → jarak bagian luar
```

---

# 8. Studi Kasus — Membuat Card

Sekarang beberapa konsep digabungkan.

```html
<div class="w-80 p-6 m-4 bg-white rounded-xl shadow">
  <h2 class="text-xl font-bold">
    Belajar Tailwind
  </h2>

  <p class="mt-2">
    Hari ini belajar spacing dan sizing.
  </p>

  <button class="mt-4 px-4 py-2 bg-black text-white rounded-lg">
    Mulai Belajar
  </button>
</div>
```

Beberapa class yang digunakan:

```text
w-80
→ menentukan lebar card

p-6
→ memberi ruang di dalam card

m-4
→ memberi jarak di luar card

mt-2
→ memberi jarak antara heading dan paragraph

mt-4
→ memberi jarak antara paragraph dan button

px-4
→ padding horizontal button

py-2
→ padding vertical button
```

---

# 9. Visualisasi Card

Struktur sederhananya:

```text
                margin
        ↓                    ↓

      ┌──────────────────────────┐
      │          padding         │
      │                          │
      │   Belajar Tailwind       │
      │                          │
      │   Hari ini belajar...    │
      │                          │
      │   [     Mulai Belajar ]  │
      │                          │
      └──────────────────────────┘
```

Dengan kata lain:

```text
m-* → jarak card dengan lingkungan sekitar

p-* → jarak isi card dengan batas card

w-* → lebar card

h-* → tinggi card
```

---

# 10. Contoh Card yang Lebih Lengkap

```html
<!DOCTYPE html>
<html lang="id">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Day 2 - Spacing & Sizing</title>
  <script src="https://cdn.tailwindcss.com"></script>
</head>

<body class="bg-gray-100">

  <main class="min-h-screen flex items-center justify-center">

    <div class="w-80 p-6 bg-white rounded-2xl shadow-lg">

      <div class="space-y-3">

        <h1 class="text-2xl font-bold">
          Belajar Tailwind
        </h1>

        <p class="text-gray-600">
          Hari ini saya belajar spacing dan sizing
          menggunakan utility class Tailwind CSS.
        </p>

        <button class="w-full px-4 py-2 bg-black text-white rounded-lg">
          Mulai Belajar
        </button>

      </div>

    </div>

  </main>

</body>
</html>
```

Pada contoh ini beberapa konsep bekerja bersama:

```text
w-80
→ ukuran card

p-6
→ ruang bagian dalam card

space-y-3
→ jarak antar content

w-full
→ button memenuhi lebar card

px-4 py-2
→ padding button
```

---

# 11. Challenge

Setelah memahami contoh sebelumnya, coba buat card sendiri tanpa langsung menyalin kode di atas.

### Challenge — Profile Card

Buat sebuah card yang berisi:

```text
┌─────────────────────────┐
│                         │
│        FOTO             │
│                         │
│     Handika Saputra     │
│                         │
│   PAI Student           │
│   Learning Full Stack   │
│                         │
│    [ Lihat Profile ]    │
│                         │
└─────────────────────────┘
```

Gunakan minimal:

```text
w-*
p-*
m-*
space-*
```

dan tambahkan:

```text
rounded-*
shadow-*
bg-*
text-*
```

agar tampilannya lebih menarik.

---

# 12. Eksperimen

Setelah card berhasil, coba ubah:

```html
w-80
```

menjadi:

```html
w-64
```

Kemudian:

```html
p-6
```

menjadi:

```html
p-3
```

Kemudian:

```html
space-y-3
```

menjadi:

```html
space-y-6
```

Perhatikan perubahan visualnya.

Tujuannya bukan menghafal angka utility class, tetapi mulai memahami:

> "Kalau nilai spacing diperbesar, apa yang berubah pada layout?"

---

# 13. Kesalahan yang Perlu Diperhatikan

### Padding bukan margin

Jangan sampai tertukar:

```text
p-4 → ruang di dalam

m-4 → ruang di luar
```

### `space-*` bekerja pada hubungan antar child

Contoh:

```html
<div class="space-y-4">
  <p>One</p>
  <p>Two</p>
  <p>Three</p>
</div>
```

`space-y-4` mengatur jarak antar child tersebut.

### Jangan menggunakan terlalu banyak spacing

Spacing memang membuat layout lebih lega, tetapi terlalu banyak spacing juga dapat membuat halaman terasa kosong.

Jadi gunakan spacing berdasarkan kebutuhan layout.

---

# 14. Yang Saya Pahami

Setelah mempelajari materi ini, saya mulai memahami bahwa spacing bukan hanya sekadar memberi angka pada CSS.

Saya perlu melihat hubungan antar elemen.

Contohnya:

```text
Card
 │
 ├── padding
 │     └── ruang antara content dan card
 │
 ├── margin
 │     └── ruang antara card dan elemen lain
 │
 ├── width
 │     └── lebar card
 │
 └── height
       └── tinggi card
```

---

# 15. Hal yang Masih Membingungkan

Bagian ini saya isi berdasarkan pengalaman belajar sendiri.

Contoh:

```text
- Masih perlu latihan membedakan margin dan padding.
- Masih perlu membiasakan diri membaca utility class.
- Masih perlu memahami kapan menggunakan space-* dibanding margin.
- Masih perlu latihan membuat ukuran responsive.
```

Bagian ini boleh berubah setelah pemahaman bertambah.

---

# 16. Struktur File

```text
02_Spacing & Sizing/
│
├── index.html
└── README.md
```

---

# 19. Ringkasan Hari Ini

```text
p-*  → padding
m-*  → margin
space-* → jarak antar child
w-*  → width
h-*  → height
```

Cara mengingatnya:

```text
p = padding
m = margin
w = width
h = height
```

---
<p align="center"> <img src="https://static.vecteezy.com/system/resources/previews/067/565/433/non_2x/tailwind-css-logo-rounded-free-png.png" alt="PHP" width="120"> </p>

<p align="center">
  <strong>completed — Spacing & Sizing</strong>
</p>

<p align="center">
  Learning Tailwind CSS by building, experimenting, and documenting.
</p>
