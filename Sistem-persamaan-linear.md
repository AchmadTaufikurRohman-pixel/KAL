# 1.2 Sistem Persamaan Linear

Mempelajari sistem persamaan merupakan bagian penting dalam matematika. 
Dalam bab ini kita membahas persamaan linear dan sistemnya secara cukup lengkap, 
karena materi ini menjadi dasar bagi aljabar linear. 

Dari pembahasan solusi sistem linear, nantinya akan muncul konsep-konsep 
seperti subruang, span (rentangan), dan kebebasan linear. 
Selain itu, kita juga akan menggunakan metode komputasi utama dalam aljabar linear, 
yaitu **eliminasi Gauss**.

---

## 1.2.1 Sistem Persamaan Linear

### Definisi 1.2.1 Persamaan Linear

Ekspresi linear dalam $n$ variabel $x_1, x_2, \ldots, x_n$ berbentuk

$$
a_1x_1 + a_2x_2 + \cdots + a_nx_n
$$

dengan $a_1, a_2, \ldots, a_n$ bilangan real tetap.

Sebuah persamaan linear adalah persamaan yang dapat disederhanakan 
(dengan penjumlahan dan pengurangan saja) ke bentuk baku:

$$
a_1x_1 + a_2x_2 + \cdots + a_nx_n = b
$$

Persamaan disebut:

- **Homogen** jika $b = 0$
- **Nonhomogen** jika $b \neq 0$
- **Nonlinear** jika tidak dapat ditulis dalam bentuk baku tersebut

Intinya, dalam persamaan linear tidak boleh ada pangkat, akar variabel, 
perkalian antar variabel, atau fungsi seperti $\sin x$ yang melibatkan variabel.

---

### Example 1.2.2

- Persamaan yang masih bisa disusun ulang ke bentuk baku tetap termasuk linear.
- Persamaan seperti $x^2 + y^2 = 1$ termasuk nonlinear karena mengandung pangkat dua.

---

### Definisi 1.2.3 Sistem Persamaan Linear

Sistem persamaan linear adalah kumpulan beberapa persamaan linear 
yang melibatkan variabel yang sama.

Bentuk umum sistem dengan $m$ persamaan dan $n$ variabel adalah:

$$
\begin{aligned}
a_{11}x_1 + \cdots + a_{1n}x_n &= b_1 \\
a_{21}x_1 + \cdots + a_{2n}x_n &= b_2 \\
\vdots \qquad\qquad & \vdots \\
a_{m1}x_1 + \cdots + a_{mn}x_n &= b_m
\end{aligned}
$$

Sistem disebut **homogen** jika semua $b_i = 0$.

---

### Remark 1.2.4 (Notasi Indeks)

Notasi $a_{ij}$ menggunakan dua indeks:

- Indeks $i$ menunjukkan baris (persamaan ke-$i$).
- Indeks $j$ menunjukkan kolom (variabel ke-$j$).
- Berlaku $1 \leq j \leq n$.

Memahami notasi ini penting karena akan sering digunakan dalam bentuk matriks.

---

### Definisi 1.2.5 Solusi Sistem Linear

Solusi persamaan linear adalah $n$-tuple $(s_1, \ldots, s_n)$ 
yang membuat persamaan benar setelah substitusi.

Solusi sistem persamaan linear adalah $n$-tuple yang memenuhi 
semua persamaan dalam sistem tersebut.

Himpunan solusi sistem linear hanya memiliki tiga kemungkinan:

1. Tidak ada solusi (sistem **tidak konsisten**)
2. Tepat satu solusi
3. Tak hingga banyak solusi

Secara geometris:
- Dua variabel → merepresentasikan garis di $\mathbb{R}^2$
- Tiga variabel → merepresentasikan bidang di $\mathbb{R}^3$

Ini membantu kita memahami solusi secara visual.

---

### Example 1.2.6

Suatu sistem sederhana bisa:

- Tidak memiliki solusi (misalnya dua garis sejajar berbeda)
- Memiliki satu solusi (dua garis berpotongan)
- Memiliki tak hingga solusi (dua persamaan yang sebenarnya sama)

---

## 1.2.1.1 Representasi Matriks dari Sistem Linear

### Definisi 1.2.7

Sistem persamaan linear dapat ditulis dalam bentuk matriks sebagai

$$
\mathcal{L}(A, \mathbf{b})
$$

dengan:

- $A$ = matriks koefisien
- $\mathbf{b}$ = vektor konstanta

Representasi ini mempermudah penulisan dan perhitungan sistem.

---

### Example 1.2.8

Dari suatu sistem, kita dapat membentuk:

- Matriks koefisien $A$
- Vektor konstanta $\mathbf{b}$

Sehingga sistem dinyatakan sebagai $\mathcal{L}(A, \mathbf{b})$.

---

### Definisi 1.2.9 Matriks Augmentasi

Matriks augmentasi diperoleh dengan menambahkan vektor konstanta 
sebagai kolom terakhir matriks koefisien:

$$
[A \mid \mathbf{b}]
$$

Matriks ini memuat seluruh informasi sistem dalam bentuk yang lebih ringkas.

Perlu diingat:
- Matriks augmentasi **bukan** sistem persamaan,
- tetapi selalu berkaitan langsung dengan sistem tersebut.

---

### Example 1.2.10

Sistem tiga persamaan tiga variabel dapat ditulis dalam bentuk matriks augmentasi:

$$
\left[
\begin{array}{ccc|c}
1 & -1 & 2 & 1 \\
2 & 1 & 1 & 8 \\
1 & 1 & 0 & 5
\end{array}
\right]
$$

Bentuk ini memudahkan kita menerapkan eliminasi Gauss 
untuk mencari solusi sistem secara sistematis.