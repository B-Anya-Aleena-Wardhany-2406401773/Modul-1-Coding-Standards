 # Reflection

Anya Aleena Wardhany

2406401773

<details>
<summary><b>Exercise 1</b></summary>

## Prinsip Clean Code
1. Penamaan method sesuai tujuannya, seperti `editProductPage` untuk menampilkan form
2. Setiap fungsi hanya mengerjakan satu hal, seperti method `delete` yang berfokus pada penghapusan produk saja
3. Layout dan formatting yang rapih, seperti contohnya judul method berada pada indentasi yang sama
4. Tidak ada code yang hanya menjadi comment


## Prinsip Secure Coding
1. Validasi input data menggunakan `@ModelAttribute` 
2. Menerapkan secure redirect, seperti setelahh edit redirect ke pagge list

## Evaluasi
1. Penangan error saat data tidak ditemukan (findById)
2. Validasi keamanan ID di URL
</details>
<details>
<summary><b>Exercise 2</b></summary>

## About Unit Test
Setelah menulis unit test, saya merasa lebih percaya diri terhadap ketahanan kode saya. Unit test memastikan bahwa perubahan kecil di masa depan tidak akan merusak fitur yang sudah ada. Mengenai jumlahnya, menurut saya tidak ada jumlah pastinya, yang penting code coveragenya tinggi. Prinsip utamanya adalah setiap fungsi atau metode setidaknya harus memiliki satu test untuk skenario sukses (positive scenario) dan beberapa test untuk menangkap kemungkinan error atau input tidak valid (negative scenario). Walaupun begitu, code coverage tinggi bahkan 100% tidak menjamin program tidak ada bug, karena bisa saja ada skenario tak terduga. Bisa juga justru malah logika kode dari awal tidak sesuai dengan kebutuhan bisnis. Bug bisa juga muncul karena masalah integrasi.


## New Functional Test
Menurut saya, membuat kelas Java baru untuk functional test dengan menyalin prosedur setup dan variabel yang sama persis akan menurunkan kualitas kode karena menyebabkan code duplication. Hal ini melanggar prinsip Don't Repeat Yourself (DRY) dan membuat kode menjadi sulit dipelihara. Misalnya ada perubahan pada konfigurasi dasar atau URL, jadi harus diperbaiki di banyak tempat sekaligus. Masalah utamanya adalah redundansi pada bagian @BeforeEach dan inisialisasi kursor driver yang sebenarnya bisa disatukan. Untuk membuat kode lebih bersih, menurut saya bisa dilakukan dengan cara membuat sebuah base class yang menampung semua prosedur setup umum sehingga kelas test lainnya cukup melakukan inheritance. 

</details>