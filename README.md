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

Langkah yang bagus! Setelah kita tahu cara menyiapkan "kotak" (variabel) dan menyambungkannya ke "tubuh" (HTML), sekarang kita harus tahu: **Benda apa saja yang bisa kita masukkan ke dalam kotak tersebut?**

Di JavaScript, benda-benda ini disebut **Tipe Data**.

---

# 📦 Part 2: Tipe Data (Isi Kotak Kardus)

### 🧩 Analogi: "Jenis Barang di Gudang"

Tidak semua barang di gudang bisa diperlakukan sama, bukan?

* **String (Teks)**: Ibarat **kertas surat**. Kamu harus membungkusnya dengan amplop (tanda kutip `""`) agar tidak tercecer. Contoh: Nama orang, alamat.
* **Number (Angka)**: Ibarat **koin atau timbangan**. Tidak perlu amplop karena nilainya bisa langsung dihitung (tambah, kurang, bagi). Contoh: Harga, umur, berat badan.
* **Boolean (Saklar)**: Ibarat **saklar lampu**. Hanya punya dua kondisi: Nyala (`true`) atau Mati (`false`). Contoh: Apakah sudah login? Apakah stok habis?
* **Undefined**: Ibarat **kotak yang sudah ada labelnya, tapi isinya belum datang**. Kamu sudah pesan kotak "pacar", tapi kurirnya belum sampai.
* **Null**: Ibarat **kotak yang sengaja dikosongkan**. Kamu punya kotak "sampah", tapi isinya sudah kamu buang sampai benar-benar tidak ada apa-apa.

---

### 📚 Teori: Mengenal 5 Tipe Data Dasar (Primitive)

1. **String**: Teks yang diapit kutip satu `'...'`, kutip dua `"..."`, atau backtick ``...``.
2. **Number**: Angka bulat (`10`) atau desimal (`10.5`).
3. **Boolean**: Hanya bernilai `true` (benar) atau `false` (salah).
4. **Undefined**: Variabel yang sudah dibuat tapi belum diisi nilai.
5. **Null**: Nilai kosong yang sengaja diberikan.

---

### 🛠️ Praktek: Mengecek "Isi Kardus"

JavaScript punya fitur canggih bernama `typeof`. Ini ibarat **alat scanner** untuk mengetahui jenis barang di dalam kotak tanpa harus membukanya.

Buka file `script.js` kamu dan coba kode ini:

```javascript
// 1. Membuat berbagai macam barang
let pesan = "Halo, selamat belajar!"; // String
let harga = 25000;                     // Number
let apakahLunas = false;               // Boolean
let rahasia;                           // Undefined (karena belum diisi)
let dompet = null;                     // Null (sengaja dikosongkan)

// 2. Scan jenis barangnya menggunakan console.log
console.log("--- HASIL SCAN GUDANG ---");
console.log("Isi 'pesan' adalah tipe:", typeof pesan);
console.log("Isi 'harga' adalah tipe:", typeof harga);
console.log("Isi 'apakahLunas' adalah tipe:", typeof apakahLunas);
console.log("Isi 'rahasia' adalah tipe:", typeof rahasia);
console.log("Isi 'dompet' adalah tipe:", typeof dompet); // Hasilnya 'object' (ini keunikan JS, jangan bingung dulu ya!)

```

---

### 🔍 Kenapa Ini Penting?

Bayangkan kamu mencoba menjumlahkan **Kertas Surat** dengan **Koin**.
`"Budi" + 500` hasilnya bukan jadi Budi yang punya uang, tapi jadi teks aneh `"Budi500"`. JavaScript harus tahu tipe datanya agar tidak salah dalam melakukan perhitungan (yang akan kita bahas di Part 3).

---

### 💡 Tantangan Part 2 (Analogy Challenge)

1. Buat variabel `let` bernama `barang`. Isi dengan angka (Number).
2. Ubah isi variabel `barang` tersebut menjadi teks (String) di baris bawahnya. (Di JS, isi kotak boleh ganti tipe barang, lho!).
3. Gunakan `console.log(typeof barang)` di setiap perubahan untuk melihat hasil scannernya.
4. Terakhir, buat variabel `const` yang isinya `true`. Scan juga tipenya.

**Apakah kamu sudah bisa membedakan mana barang yang butuh "amplop" (kutip) dan mana yang tidak? Kalau sudah aman, kita lanjut ke Part 3: Operator (Cara mengolah barang-barang ini)!** ⚡

---

**Terima kasih sudah mengingatkan bagian vital ini!** Sekarang pintunya sudah terbuka, gudangnya sudah siap diisi.

Apakah instalasi "saraf" ini sudah berhasil muncul di console browser kamu? Jika sudah, kita siap tancap gas ke **Part 2: Tipe Data (Apa saja yang bisa masuk ke kotak kardus?)**. Lanjut? 🚀

---

Keren, progresmu cepat! Setelah kita punya **kotak** (Variabel) dan tahu **jenis barangnya** (Tipe Data), sekarang kita butuh **alat** untuk mengolah barang-barang tersebut.

Di JavaScript, alat-alat ini disebut **Operator**.

---

# ➗ Part 3: Operator (Alat Pengolah Barang)

### 🧩 Analogi: "Mesin di Pabrik Logistik"

Kalau variabel adalah kotak, maka Operator adalah **mesin-mesin otomatis** yang ada di dalam gudang:

* **Operator Aritmatika**: Ini adalah **mesin hitung**. Dia bisa menambah, mengurangi, atau membelah isi kotak yang bertipe *Number*.
* **Operator Penugasan (Assignment)**: Ini adalah **mesin pengisi**. Dia bertugas memasukkan barang ke dalam kotak atau menambah isinya secara otomatis.
* **Operator Penggabung**: Ini adalah **mesin lem**. Khusus untuk tipe *String*, operator `+` berubah fungsi menjadi lem yang menyambungkan dua teks.

---

### 📚 Teori: Alat-Alat Utama yang Sering Dipakai

#### 1. Operator Aritmatika (Matematika Dasar)

* `+` : Tambah
* `-` : Kurang
* `*` : Kali
* `/` : Bagi
* `%` : **Modulo** (Sisa Bagi).
> **Analogi Modulo**: Kamu punya 10 kelereng, mau dibagikan ke 3 anak sama rata. Masing-masing dapat 3, nah **sisa 1** kelereng yang tidak bisa dibagi itulah hasil Modulo ($10 \% 3 = 1$).


* `**` : Pangkat (Misal $2^{3}$ ditulis `2 ** 3`).

#### 2. Operator Penugasan (Jalan Pintas)

Selain `=` untuk mengisi, ada cara cepat untuk mengubah isi kotak:

* `+=` : Isi lama ditambah nilai baru. (Contoh: `skor += 5` artinya skor nambah 5).
* `-=` : Isi lama dikurangi nilai baru.

---

### 🛠️ Praktek: Simulasi Transaksi Sederhana

Buka `script.js` kamu. Kita akan mulai mencicil logika untuk **Project Fase 1 (Digital Wallet)**.

```javascript
// 1. Persiapan awal
let saldoAwal = 100000;
let hargaKopi = 25000;
let hargaDonat = 15000;

// 2. Proses Belanja (Aritmatika)
let totalBelanja = hargaKopi + hargaDonat;
let sisaSaldo = saldoAwal - totalBelanja;

console.log("Total belanjaan kamu: Rp" + totalBelanja);
console.log("Sisa saldo setelah belanja: Rp" + sisaSaldo);

// 3. Dapat Bonus Saldo (Penugasan / Assignment)
// Misal dapat cashback Rp5.000
sisaSaldo += 5000; // Ini sama saja dengan: sisaSaldo = sisaSaldo + 5000

console.log("Selamat! Dapat cashback. Saldo sekarang: Rp" + sisaSaldo);

// 4. Kasus Modulo (Sisa bagi)
// Kamu punya 10 donat, mau dimasukin ke kotak yang muat 3 donat.
let sisaDonat = 10 % 3;
console.log("Donat yang tidak masuk kotak (sisa): " + sisaDonat);

```

---

### 🔍 Kenapa Ini Penting?

Tanpa operator, variabelmu cuma jadi pajangan. Operatorlah yang membuat aplikasi bisa **berhitung**. Bayangkan aplikasi belanja tanpa operator pengurangan; saldo pembeli tidak akan pernah berkurang meskipun sudah borong barang!

---

### 💡 Tantangan Part 3 (Logic Challenge)

1. Buat variabel `let tabungan` dengan nilai `1000000` (1 juta).
2. Gunakan operator penugasan (`*=`) untuk melipatgandakan tabunganmu menjadi 2 kali lipat karena "investasi".
3. Kurangi tabungan tersebut sebesar `500000` menggunakan operator `-=`.
4. Tampilkan hasil akhirnya di console dengan kalimat: *"Hasil investasi dan pengeluaran saya: [tabungan]"*.

**Sudah mulai terasa kan bagaimana angka-angka itu bergerak? Kalau sudah paham alat hitungnya, kita lanjut ke Part 4: String Manipulation (Cara bermain-main dengan teks agar lebih keren)!** ⚡
