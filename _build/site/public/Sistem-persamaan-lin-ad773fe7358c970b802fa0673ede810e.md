# 1.2 Sistem Persamaan Linear

Mempelajari sistem persamaan merupakan bagian penting dalam matematika. 
Dalam bab ini dibahas teori dasar persamaan linear yang menjadi fondasi aljabar linear. 
Dari pembahasan solusi sistem linear, muncul konsep-konsep seperti subruang, span (rentangan), kebebasan linear, serta metode komputasi utama yaitu eliminasi Gauss.

---

## 1.2.1 Sistem Persamaan Linear

### Definisi 1.2.1 Persamaan Linear

Ekspresi linear dalam $n$ variabel $x_1, x_2, \ldots, x_n$ berbentuk

$$
a_1x_1 + a_2x_2 + \cdots + a_nx_n
$$

dengan $a_1, \ldots, a_n$ bilangan real.

Persamaan linear dapat disederhanakan ke bentuk baku

$$
a_1x_1 + a_2x_2 + \cdots + a_nx_n = b
$$

Persamaan disebut:
- **Homogen** jika $b = 0$
- **Nonhomogen** jika $b \neq 0$
- **Nonlinear** jika tidak dapat dituliskan dalam bentuk baku tersebut hanya dengan penjumlahan dan pengurangan

---

### Example 1.2.2

- Persamaan dengan akar, pangkat, atau fungsi trigonometri yang masih bisa disusun ulang ke bentuk baku tetap termasuk linear.
- Persamaan seperti $x^2 + y^2 = 1$ adalah nonlinear karena mengandung pangkat dua.

---

### Definisi 1.2.3 Sistem Persamaan Linear

Sistem persamaan linear adalah kumpulan beberapa persamaan linear.

Bentuk umum sistem dengan $m$ persamaan dan $n$ variabel:

$$
\begin{aligned}
a_{11}x_1 + \cdots + a_{1n}x_n &= b_1 \\
\vdots \qquad\qquad & \vdots \\
a_{m1}x_1 + \cdots + a_{mn}x_n &= b_m
\end{aligned}
$$

Sistem disebut **homogen** jika semua ruas kanannya nol.

---

### Remark 1.2.4 (Notasi Indeks)

- Indeks $i$ pada $a_{ij}$ dan $b_i$ menunjukkan baris (persamaan ke-$i$).
- Indeks $j$ pada $a_{ij}$ menunjukkan kolom yang berkaitan dengan variabel ke-$j$.
- Berlaku $1 \leq j \leq n$.

---

### Definisi 1.2.5 Solusi Sistem Linear

Solusi persamaan linear adalah $n$-tuple $(s_1, \ldots, s_n)$ yang membuat persamaan benar setelah substitusi.

Solusi sistem persamaan linear adalah $n$-tuple yang memenuhi seluruh persamaan dalam sistem.

Himpunan solusi hanya memiliki tiga kemungkinan:

1. Tidak ada solusi (sistem tidak konsisten)
2. Tepat satu solusi
3. Tak hingga banyak solusi

Secara geometris:
- Dua variabel → garis di $\mathbb{R}^2$
- Tiga variabel → bidang di $\mathbb{R}^3$

---

### Example 1.2.6

Beberapa sistem sederhana dapat:
- Tidak memiliki solusi (dua garis sejajar berbeda)
- Memiliki satu solusi (dua garis berpotongan)
- Memiliki tak hingga solusi (dua persamaan ekuivalen)

---

## 1.2.1.1 Representasi Matriks dari Sistem Linear

### Definisi 1.2.7

Sistem dapat ditulis dalam bentuk matriks sebagai

$$
\mathcal{L}(A, \mathbf{b})
$$

dengan:
- $A$ matriks koefisien
- $\mathbf{b}$ vektor konstanta

---

### Example 1.2.8

Sistem dapat direpresentasikan menjadi:
- Matriks koefisien $A$
- Vektor konstanta $\mathbf{b}$

Sehingga sistem dituliskan sebagai $\mathcal{L}(A, \mathbf{b})$.

---

### Definisi 1.2.9 Matriks Augmentasi

Matriks augmentasi diperoleh dengan menambahkan vektor konstanta sebagai kolom terakhir matriks koefisien:

$$
[A \mid \mathbf{b}]
$$

Matriks ini memuat seluruh informasi sistem, tetapi bukan sistem persamaan itu sendiri.

---

### Example 1.2.10

Sistem tiga persamaan tiga variabel dapat ditulis dalam bentuk matriks augmentasi:

$$
\left[
\begin{array}{ccc|c}
\cdot & \cdot & \cdot & \cdot \\
\cdot & \cdot & \cdot & \cdot \\
\cdot & \cdot & \cdot & \cdot
\end{array}
\right]
$$

Representasi ini memudahkan penggunaan eliminasi Gauss untuk mencari solusi.