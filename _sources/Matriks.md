### MATRIKS

#### 1. Pengertian Matriks
Matriks adalah susunan bilangan yang disusun dalam baris dan kolom serta dibatasi oleh tanda kurung atau kurung siku.

Secara umum matriks ditulis sebagai 

$$
A = \begin{bmatrix} a_{11} & a_{12} & a_{13} \\ a_{21} & a_{22} & a_{23} \end{bmatrix}
$$

Keterangan:
- $a_{ij}$ adalah elemen matriks
- $ i $ menunjukkan baris
- $ j $ menunjukkan kolom

Jika matriks memiliki $ m $ baris dan $n $ kolom, maka disebut matriks berordo 

$$ m \times n $$

---

**Contoh:**

$$ 
A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}
$$

Matriks tersebut memiliki 2 baris dan 3 kolom sehingga ordonya adalah $ 2 x 3 $.

---

### 2. Jenis-Jenis Matriks

#### 2.1 Matriks Baris
Matriks yang hanya memiliki 1 baris.

**Contoh:**  

$$
A = \begin{bmatrix} 2 & 4 & 8 & 8 \end{bmatrix}
$$

Ordo: $ 1 \times 4 $

#### 2.2 Matriks Kolom
Matriks yang hanya memiliki 1 kolom.

**Contoh:**

$$
B = \begin{bmatrix} 3 \\ 4 \\ 5 \end{bmatrix}
$$

**Ordo:** $ 3 \times 1 $

---

#### 2.3 Matriks Persegi
Matriks yang jumlah baris dan kolomnya sama.

**Contoh:**

$$
C = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}
$$

**Ordo:** $ 2 \times 2 $

---

#### 2.4 Matriks Nol
Matriks yang semua elemennya 0.

$$
O = \begin{bmatrix} 0 & 0 \\ 0 & 0 \end{bmatrix}
$$

---

#### 2.5 Matriks Identitas
Matriks persegi yang elemen diagonalnya 1 dan lainnya 0.

$$
I = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}
$$

### 3. Operasi pada Matriks

#### 3.1 Penjumlahan Matriks
Dua matriks dapat dijumlahkan jika memiliki ordo yang sama.

**Contoh:**

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}
$$

$$
B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}
$$

**Maka:**

$$
A + B = \begin{bmatrix} 1 + 5 & 2 + 6 \\ 3 + 7 & 4 + 8 \end{bmatrix} = \begin{bmatrix} 6 & 8 \\ 10 & 12 \end{bmatrix}
$$

---

#### 3.2 Pengurangan Matriks

$$
A - B = \begin{bmatrix} 1 - 5 & 2 - 6 \\ 3 - 7 & 4 - 8 \end{bmatrix} = \begin{bmatrix} -4 & -4 \\ -4 & -4 \end{bmatrix}
$$

---

#### 3.3 Perkalian Matriks dengan Skalar
Perkalian matriks dengan skalar dilakukan dengan mengalikan setiap elemen matriks dengan bilangan skalar tersebut.

**Contoh:**

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}
$$

Kalikan dengan 2:

$$
2A = \begin{bmatrix} 2 \times 1 & 2 \times 2 \\ 2 \times 3 & 2 \times 4 \end{bmatrix} = \begin{bmatrix} 2 & 4 \\ 6 & 8 \end{bmatrix}
$$

#### 3.4 Perkalian Dua Matriks

Perkalian matriks hanya bisa dilakukan jika jumlah **kolom matriks pertama sama dengan jumlah baris matriks kedua**.

**Syarat:** Kolom A = Baris B

**Contoh:**

$$
A = \begin{bmatrix} 1 & 2 \\ 3 & 4 \end{bmatrix}
$$

$$
B = \begin{bmatrix} 5 & 6 \\ 7 & 8 \end{bmatrix}
$$

**Maka:**

$$
AB = \begin{bmatrix} 
(1 \times 5 + 2 \times 7) & (1 \times 6 + 2 \times 8) \\
(3 \times 5 + 4 \times 7) & (3 \times 6 + 4 \times 8)
\end{bmatrix}
=
\begin{bmatrix} 
19 & 22 \\
43 & 50
\end{bmatrix}
$$

---

### 4. Transpose Matriks

Transpose matriks adalah menukar baris menjadi kolom dan kolom menjadi baris.

**Contoh:**

$$
A = \begin{bmatrix} 1 & 2 & 3 \\ 4 & 5 & 6 \end{bmatrix}
$$

**Maka:**

$$
A^T = \begin{bmatrix} 1 & 4 \\ 2 & 5 \\ 3 & 6 \end{bmatrix}
$$

### 5. Determinan Matriks

**Determinan hanya berlaku untuk matriks persegi**

**Contoh matriks:**

$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}
$$

**Determinan:**

$$
|A| = ad - bc
$$

**Contoh:**

$$
A = \begin{bmatrix} 2 & 3 \\ 1 & 4 \end{bmatrix}
$$

$$
|A| = (2 \times 4) - (3 \times 1)
$$

$$
= 8 - 3 = 5
$$

---

### 6. Invers Matriks

**Jika diberikan matriks:**

$$
A = \begin{bmatrix} a & b \\ c & d \end{bmatrix}
$$

**Maka inversnya adalah:**

$$
A^{-1} = \frac{1}{ad - bc} \begin{bmatrix} d & -b \\ -c & a \end{bmatrix}
$$

**Contoh:**

$$
A = \begin{bmatrix} 2 & 1 \\ 1 & 1 \end{bmatrix}
$$

**Determinan:**

$$
|A| = (2 \times 1) - (1 \times 1) = 2 - 1 = 1
$$

**Invers:**

$$
A^{-1} = \frac{1}{1} \begin{bmatrix} 1 & -1 \\ -1 & 2 \end{bmatrix} = \begin{bmatrix} 1 & -1 \\ -1 & 2 \end{bmatrix}
$$

### 7. Penerapan Matriks pada Sistem Persamaan Linear

Selesaikan sistem persamaan linear berikut:

$$ 
x + y = 8\\
2x + y = 7
$$
Sistem persamaan tersebut dapat ditulis dalam bentuk matriks sebagai:

$$
\begin{bmatrix}
1 & 1 \\
2 & 1
\end{bmatrix}
\begin{bmatrix}
x \\
y
\end{bmatrix}
=
\begin{bmatrix}
8 \\
7
\end{bmatrix}
$$ 

Dengan metode eliminasi diperoleh:

$x = -1$
$y = 9$