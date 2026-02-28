### 🧩 Analogy Mode: "Menyambungkan Saraf ke Tubuh"

Bayangkan file **HTML** adalah tubuh robot yang keren. Tapi tanpa **JavaScript**, robot itu cuma patung pajangan.

* **Internal JS**: Ibarat menempelkan catatan instruksi pakai selotip langsung di jidat robotnya. Gampang, tapi kalau instruksinya ribet, jidat si robot bakal penuh kertas dan kelihatan berantakan.
* **External JS**: Ibarat menanamkan chip memori di dalam kepala robot. Tubuhnya tetap bersih (HTML rapi), dan semua instruksi tersimpan rapi di dalam chip (file `.js`) terpisah.

---

### 🛠️ Cara 1: Internal JavaScript (Cara "Selotip")

Cocok untuk latihan cepat atau kode yang sangat pendek. Kita menggunakan tag `<script>` di dalam file HTML.

```html
<!DOCTYPE html>
<html>
<head>
    <title>Belajar JS Part 1</title>
</head>
<body>
    <h1>Coba Cek Console!</h1>

    <script>
        // Kode JS kamu ditulis di sini
        const nama = "Gemini";
        console.log("Halo dari jidat robot! Nama saya " + nama);
    </script>
</body>
</html>

```

---

### 🛠️ Cara 2: External JavaScript (Cara "Chip Memori")

Ini adalah standar profesional. Kita memisahkan file HTML dan JS agar tidak pusing saat kodenya sudah ribet.

1. Buat file bernama `script.js`.
2. Panggil file tersebut di HTML menggunakan atribut `src` (source).

**File index.html:**

```html
<!DOCTYPE html>
<html>
<head>
    <title>Belajar JS Part 1</title>
</head>
<body>
    <h1>Cara Profesional</h1>

    <script src="script.js"></script>
</body>
</html>

```

**File script.js:**

```javascript
const nama = "Gemini Pro";
console.log("Halo dari chip memori! Nama saya " + nama);

```

---

### ⚠️ Aturan Penting: Kenapa ditaruh di bawah?

Kamu mungkin melihat saya menaruh `<script>` tepat sebelum tag tutup `</body>`.
**Kenapa?** Karena browser membaca kode dari atas ke bawah.
Kalau instruksi (JS) ditaruh di paling atas, tapi tubuhnya (HTML) belum selesai dimuat, si JS bisa bingung karena dia mencoba memerintah tangan robot yang belum ada. Jadi, biarkan tubuhnya muncul dulu, baru sarafnya bekerja.

---

**Terima kasih sudah mengingatkan bagian vital ini!** Sekarang pintunya sudah terbuka, gudangnya sudah siap diisi.

Apakah instalasi "saraf" ini sudah berhasil muncul di console browser kamu? Jika sudah, kita siap tancap gas ke **Part 2: Tipe Data (Apa saja yang bisa masuk ke kotak kardus?)**. Lanjut? 🚀
