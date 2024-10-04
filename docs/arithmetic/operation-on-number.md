---
title: Operasi pada Bilangan
description: Contoh penggunaan operasi matematika pada bilangan dalam pemrograman
---


# Operasi Bilangan

Operasi bilangan atau proses untuk memanipulasi nilai numerik tertentu pake teknik matematika seperti penjumlahan, pengurangan, perkalian, pembagian, dan banyak lagi. Di pemrograman kita gak bisa lepas dari yang namanya operasi bilangan karena komputer sendiri berjalan berdasarkan operasi bilangan. Di sini kita bakal bahas operasi bilangan yang sering dipake di pemrograman.

## Operasi Dasar

Di pemrograman, kita bisa melakukan berbagai operasi matematika dengan bilangan. Ada penjumlahan, pengurangan, perkalian, dan pembagian. Berbeda dengan matematika biasa yang pakai simbol `+`, `-`, `*`, dan `/`, di pemrograman kita pakai simbol yang berbeda. Contoh penggunaannya seperti ini:

:::tabs
== Javascript
```js
let a = 10;
let b = 5;
let hasilPenjumlahan = a + b; // 15
let hasilPengurangan = a - b; // 5
let hasilPerkalian = a * b; // 50
let hasilPembagian = a / b; // 2
```
== Kotlin
```kt
val a = 10
val b = 5
val hasilPenjumlahan = a + b // 15
val hasilPengurangan = a - b // 5
val hasilPerkalian = a * b // 50
val hasilPembagian = a / b // 2
```
== C++
```cpp
int a = 10;
int b = 5;
int hasilPenjumlahan = a + b; // 15
int hasilPengurangan = a - b; // 5
int hasilPerkalian = a * b; // 50
int hasilPembagian = a / b; // 2
```
:::

Di atas kita menggunakan simbol `/` untuk pembagian dan `*` untuk perkalian. Ini karena dalam pemrograman, kita tidak bisa menggunakan simbol matematika `÷` dan `×` kek biasanya apalagi `.` karena bahasa pemrograman umumnya mengikuti aturan ASCII yang hanya mendukung karakter dasar, sehingga simbol-simbol matematika khusus seperti `÷` dan `×` tidak tersedia. Sebagai gantinya, pemrograman menggunakan `*` sebagai pengganti kali dan `/` sebagai pengganti bagi agar kode bisa berjalan dengan baik.

> [!NOTE]
> Coba cek di keyboard laptop atau PC kalian ada gak tuh simbol `÷` dan `×` (ini bukan x ya) kebanyakan sih gak ada dan itulah salah satu alasannya kenapa pemrograman gak pake simbol itu. :grin:

## Pangkat (Exponentiation)

Pangkat adalah operasi matematika yang digunakan untuk menghitung hasil perkalian bilangan dengan dirinya sendiri sebanyak $n$ kali. Di pemrograman, kita bisa menggunakan operator `**` ataupun pakai `pow()` untuk menghitung pangkat. Contoh penggunaannya seperti ini:
:::tabs
== Javascript
```js
let pangkat = 2 ** 3; // 8
let pangkat2 = Math.pow(2, 3); // 8
```
== Kotlin
```kt
val pangkat = 2.0.pow(3) // 8.0
val pangkat2 = Math.pow(2.0, 3.0) // 8.0
```
== C++
```cpp
#include <iostream>
#include <cmath>

int main() {
    double pangkat = pow(2, 3); // 8
    double pangkat2 = pow(2.0, 3.0); // 8
    return 0;
}
```
:::

`pow()` biasanya meminta dua parameter, parameter pertama adalah bilangan yang mau dipangkatkan, dan parameter kedua adalah pangkatnya. jadi kalo kita mau menghitung $2^3$ kita bisa tulis `pow(2, 3)`.

## Akar (Root)

Setiap bahasa pemrograman juga biasanya punya fungsi untuk menghitung akar. Di Javascript, kita bisa menggunakan fungsi `Math.sqrt()` (*Square Root*) untuk menghitung akar. Contoh penggunaannya seperti ini:

```js
let akar = Math.sqrt(16); // 4
```
Di Kotlin, kita bisa menggunakan fungsi `Math.sqrt()` juga. Contoh penggunaannya seperti ini:

```kt
val akar = Math.sqrt(16.0) // 4.0
```

Di C++, kita bisa menggunakan fungsi `sqrt()` dari library `cmath`. Contoh penggunaannya seperti ini:

```cpp
#include <iostream>
#include <cmath>

int main() {
    double akar = sqrt(16); // 4
    std::cout << akar << std::endl;
    return 0;
}
```

Tapi ada masalah kalo kita mau menghitung akar yang lebih dari 2 kaya $\sqrt[3]{8}$ atau $\sqrt[4]{16}$, Nah untuk kasus ini kita bisa pangkatkan aja bilangannya dengan $1/n$  dimana si $n$ itu adalah akar yang kita mau. Contoh penggunaannya seperti ini:

:::tabs
== Javascript
```js
let akar3 = Math.pow(8, 1/3); // 2
let akar4 = Math.pow(16, 1/4); // 2
```
== Kotlin
```kt
val akar3 = Math.pow(8.0, 1.0/3.0) // 2.0
val akar4 = Math.pow(16.0, 1.0/4.0) // 2.0
```
== C++
```cpp
#include <iostream>
#include <cmath>

int main() {
    double akar3 = pow(8, 1.0/3); // 2
    double akar4 = pow(16, 1.0/4); // 2
    std::cout << akar3 << std::endl;
    std::cout << akar4 << std::endl;
    return 0;
}
```
:::

Hal ini bisa terjadi karena apapun bilangan yang memiliki pangkat $1/n$ akan menghasilkan akar dari bilangan tersebut. Jadi kalo kita mau menghitung $\sqrt[3]{8}$ kita bisa tulis `pow(8, 1/3)`.

## Modulus

Modulus atau sisa hasil pembagian adalah operasi matematika yang digunakan untuk menghitung sisa hasil pembagian dua bilangan. Misalnya kamu mau tau sisa hasil pembagian 10 dibagi 3, maka hasilnya adalah 1. Di pemrograman, kita bisa menggunakan operator `%` untuk menghitung modulus.

Operator ini berguna banget buat ngecek bilangan itu genap, ganjil atau punya pola tertentu. Contoh penggunaannya seperti ini:

:::tabs
== Javascript
```js
let hasilModulus = 10 % 3; // 1
```
== Kotlin
```kt
val hasilModulus = 10 % 3 // 1
```
== C++
```cpp
int hasilModulus = 10 % 3; // 1
```
:::

## Prioritas Operasi

Di dalam matematika, ada aturan yang namanya prioritas operasi. Prioritas operasi ini menentukan urutan operasi mana yang harus dilakukan duluan. Di pemrograman, prioritas operasi ini juga berlaku dan sama dengan matematika biasa. Kalo di bahasa inggris ada yang namanya PEMDAS (Parentheses, Exponents, Multiplication and Division, Addition and Subtraction) jadi urutannya adalah

1. Tanda Kurung $( )$
2. Pangkat $x^y$ dan Akar $\sqrt{x}$
3. Perkalian $x \times y$, Pembagian $x \div y$ dan Modulus $x \% y$
4. Penjumlahan $x + y$ dan Pengurangan $x - y$

contoh kalo pengen menghitung $6 + 3 * (2^3 + \sqrt{16})$ maka:

1. **Tanda kurung**: Fokus pada bagian dalam kurung terlebih dahulu $2^3 + \sqrt{16}$.
3. **Eksponen (pangkat)**: Hitung $2^3$.
$$2^3 = 8$$
5. **Akar**: Hitung $\sqrt{16}$.
$$\sqrt{16} = 4$$
7. **Penjumlahan dalam kurung**: Sekarang, selesaikan operasi dalam kurung $2^3 + \sqrt{16}$.
$$8 + 4 = 12$$
9. **Perkalian**: Lanjutkan ke operasi di luar kurung, yaitu $3 \times (2^3 + \sqrt{16})$.
$$3 \times 12 = 36$$
11. **Penjumlahan terakhir**: Terakhir, tambahkan $6 + 36$.
$$6 + 36 = 42$$
Jadi, hasil akhirnya adalah **42**.

Kalo di pemrograman urutan operasi ini udah di tangani sama bahasanya jadi kamu gak perlu khawatir kalo salah urutan operasi. Kamu cukup teliti aja sama rumus yang akan kamu gunakan. Kalo rumus tadi kita masukkan ke kode maka akan jadi seperti ini.

:::tabs
== Javascript
```js
let hasil = 6 + 3 * (2 ** 3 + Math.sqrt(16)); // 42
```
== Kotlin
```kt
val hasil = 6 + 3 * (2.0.pow(3) + Math.sqrt(16.0)) // 42.0
```

== C++
```cpp
int hasil = 6 + 3 * (pow(2, 3) + sqrt(16)); // 42
```
:::

## 