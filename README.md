# practice-nodejs-1

Project latihan Node.js dasar mengenai penggunaan **CommonJS Modules** (export dan import/require).

## 📁 Struktur Direktori

```text
be-nodejs1-myskill/
├── app/
│   └── app.js                  # Entry point aplikasi utama
├── modules/
│   └── operasi_aritmetika.js   # Module berisi fungsi aritmetika & utilitas
└── README.md                   # Dokumentasi proyek
```

---

## 📝 Penjelasan Folder & File

### 1. `modules/`
Folder ini berisi modul-modul kustom yang diekspor untuk digunakan di bagian aplikasi lainnya.

* **`modules/operasi_aritmetika.js`**
  Modul yang mengekspor fungsi-fungsi pembantu (*helper functions*) menggunakan sintaks `exports`:
  * `printName(name)`: Mengembalikan string salam berisi nama (contoh: `"ini nama saya Rivaldo"`).
  * `sumNumber(a, b)`: Mengembalikan hasil penjumlahan dua angka `a + b`.

---

### 2. `app/`
Folder ini berisi kode utama aplikasi yang mengonsumsi modul yang ada di folder `modules`.

* **`app/app.js`**
  File utama (*entry point*) yang mendemonstrasikan cara melakukan `require` modul dari folder `modules` dan memanggil fungsi-fungsinya:
  1. Meng-import modul `../modules/operasi_aritmetika`.
  2. Memanggil `operasiAritmetika.printName("Rivaldo")` dan mencetak hasilnya ke konsol.
  3. Memanggil `operasiAritmetika.sumNumber(5, 3)` dan mencetak hasil penjumlahannya ke konsol.

---

## 🚀 Cara Menjalankan

Jalankan perintah berikut di terminal:

```bash
node app/app.js
```

**Output:**
```text
result :  ini nama saya Rivaldo
result sum :  8
```
