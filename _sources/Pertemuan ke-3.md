# SISTEM PERSAMAAN LINEAR 5 VARIABEL
## Sistem Persamaan Linear 5 Variabel

Misalkan sistem berikut:

$$
\begin{aligned}
x_1 + x_2 + x_3 + x_4 + x_5 &= 15 \\
2x_1 + x_2 + x_3 + x_4 + x_5 &= 16 \\
x_1 + 2x_2 + x_3 + x_4 + x_5 &= 17 \\
x_1 + x_2 + 2x_3 + x_4 + x_5 &= 18 \\
x_1 + x_2 + x_3 + 2x_4 + x_5 &= 19
\end{aligned}
$$

Bentuk matriks augmented:

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
2 & 1 & 1 & 1 & 1 & 16 \\
1 & 2 & 1 & 1 & 1 & 17 \\
1 & 1 & 2 & 1 & 1 & 18 \\
1 & 1 & 1 & 2 & 1 & 19
\end{array}
\right]
$$

### Langkah 1

Hilangkan elemen di bawah pivot pertama.

$$
\begin{aligned}
R_2 &= R_2 - 2R_1 \\
R_3 &= R_3 - R_1 \\
R_4 &= R_4 - R_1 \\
R_5 &= R_5 - R_1
\end{aligned}
$$

Hasil:

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & -1 & -1 & -1 & -1 & -14 \\
0 & 1 & 0 & 0 & 0 & 2 \\
0 & 0 & 1 & 0 & 0 & 3 \\
0 & 0 & 0 & 1 & 0 & 4
\end{array}
\right]
$$

### Langkah 2

Ubah pivot kedua menjadi 1

$$
R_2 = -R_2
$$

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & 1 & 1 & 1 & 14 \\
0 & 1 & 0 & 0 & 0 & 2 \\
0 & 0 & 1 & 0 & 0 & 3 \\
0 & 0 & 0 & 1 & 0 & 4
\end{array}
\right]
$$


### Langkah 3

Hilangkan elemen di bawah pivot kedua

$$
R_3 = R_3 - R_2
$$

Hasil:

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & 1 & 1 & 1 & 14 \\
0 & 0 & -1 & -1 & -1 & -12 \\
0 & 0 & 1 & 0 & 0 & 3 \\
0 & 0 & 0 & 1 & 0 & 4
\end{array}
\right]
$$


### Langkah 4

Ubah pivot ketiga menjadi 1

$$
R_3 = -R_3
$$

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & 1 & 1 & 1 & 14 \\
0 & 0 & 1 & 1 & 1 & 12 \\
0 & 0 & 1 & 0 & 0 & 3 \\
0 & 0 & 0 & 1 & 0 & 4
\end{array}
\right]
$$


### Langkah 5

Hilangkan elemen di bawah pivot ketiga

$$
R_4 = R_4 - R_3
$$

Hasil:

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & 1 & 1 & 1 & 14 \\
0 & 0 & 1 & 1 & 1 & 12 \\
0 & 0 & 0 & -1 & -1 & -9 \\
0 & 0 & 0 & 1 & 0 & 4
\end{array}
\right]
$$


### Langkah 6

Ubah pivot keempat menjadi 1

$$
R_4 = -R_4
$$

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & 1 & 1 & 1 & 14 \\
0 & 0 & 1 & 1 & 1 & 12 \\
0 & 0 & 0 & 1 & 1 & 9 \\
0 & 0 & 0 & 1 & 0 & 4
\end{array}
\right]
$$


### Langkah 7

Hilangkan elemen di bawah pivot keempat

$$
R_5 = R_5 - R_4
$$

Hasil:

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & 1 & 1 & 1 & 14 \\
0 & 0 & 1 & 1 & 1 & 12 \\
0 & 0 & 0 & 1 & 1 & 9 \\
0 & 0 & 0 & 0 & -1 & -5
\end{array}
\right]
$$

### Langkah 8: 
Mengubah Pivot Kelima Menjadi 1

Kita kalikan baris kelima dengan negatif satu:
$
\left[
R_5 = -R_5
\right]
$
Sehingga diperoleh matriks:

$$
\left[
\begin{array}{ccccc|c}
1 & 1 & 1 & 1 & 1 & 15 \\
0 & 1 & 1 & 1 & 1 & 14 \\
0 & 0 & 1 & 1 & 1 & 12 \\
0 & 0 & 0 & 1 & 1 & 9  \\
0 & 0 & 0 & 0 & 1 & 5  \\
\end{array}
\right]
$$

Sekarang pivot kelima (baris 5, kolom 5) sudah bernilai 1.