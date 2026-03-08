<script src="https://sagecell.sagemath.org/static/embedded_sagecell.js"></script>

<script>
sagecell.makeSagecell({
inputLocation: ".sage"
});
</script>
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

### Jika menggunakan sage cell

<div class="sage">
<script type="text/x-sage">
# Matriks augmented
A = matrix([
[1,1,1,1,1,15],
[2,1,1,1,1,16],
[1,2,1,1,1,17],
[1,1,2,1,1,18],
[1,1,1,2,1,19]
])
A
</script>
</div>

#### Langkah 1 — Menghilangkan elemen di bawah pivot pertama

Operasi:

Tujuan:

$$
\begin{aligned}
R_2 &= R_2 - 2R_1 \\
R_3 &= R_3 - R_1 \\
R_4 &= R_4 - R_1 \\
R_5 &= R_5 - R_1
\end{aligned}
$$

- Pivot pertama berada di kolom 1 baris 1 (nilai = 1).
- Semua angka di bawah pivot tersebut harus menjadi 0.

<div class="sage">
<script type="text/x-sage">
# Langkah 1
A.add_multiple_of_row(1,0,-2)
A.add_multiple_of_row(2,0,-1)
A.add_multiple_of_row(3,0,-1)
A.add_multiple_of_row(4,0,-1)
A
</script>
</div>

#### Langkah 2 — Membuat pivot kedua bernilai 1

Operasi:

$$
R_2 = -R_2
$$

Tujuan:

- Pivot pada baris kedua awalnya -1.
- Supaya standar eliminasi, pivot diubah menjadi 1.
<div class="sage">
<script type="text/x-sage">
# Langkah 2
A.rescale_row(1,-1)
A
</script>
</div>

#### Langkah 3 — Menghilangkan elemen di bawah pivot kedua

Operasi:

$$
R_3 = R_3 - R_2
$$

Tujuan:

- Menghilangkan angka di bawah pivot kedua.
- Sehingga kolom kedua menjadi:
<div class="sage">
<script type="text/x-sage">
# Langkah 3
A.add_multiple_of_row(2,1,-1)
A
</script>
</div>

#### Langkah 4 — Membuat pivot ketiga bernilai 1

Operasi:

$$
R_3 = -R_3
$$

Tujuan:

- Pivot ketiga awalnya -1.
- Diubah menjadi 1 agar sesuai standar eliminasi.

<div class="sage">
<script type="text/x-sage">
# Langkah 4
A.rescale_row(2,-1)
A
</script>
</div>

#### Langkah 5 — Menghilangkan elemen di bawah pivot ketiga

Operasi:

$$
R_4 = R_4 - R_3
$$

Tujuan:

- Membuat angka di bawah pivot ketiga menjadi 0.
- Kolom ketiga sekarang berbentuk:
<div class="sage">
<script type="text/x-sage">
# Langkah 5
A.add_multiple_of_row(3,2,-1)
A
</script>
</div>

#### Langkah 6 — Membuat pivot keempat bernilai 1

Operasi:

$$
R_4 = -R_4
$$

Tujuan:

- Pivot awalnya -1.
- Diubah menjadi 1.
<div class="sage">
<script type="text/x-sage">
# Langkah 6
A.rescale_row(3,-1)
A
</script>
</div>

#### Langkah 7 — Menghilangkan elemen di bawah pivot keempat

Operasi:

$$
R_5 = R_5 - R_4
$$

Tujuan:

- Membuat elemen di bawah pivot keempat menjadi 0.
<div class="sage">
<script type="text/x-sage">
# Langkah 7
A.add_multiple_of_row(4,3,-1)
A
</script>
</div>

#### Langkah 8 — Membuat pivot kelima bernilai 1

Operasi:

$$
R_5 = -R_5
$$

Tujuan:

- Pivot terakhir awalnya -1.
- Diubah menjadi 1.

Sekarang matriks sudah berbentuk segitiga atas:

$$
\begin{aligned}
1 + * + * + * + * \\
0 + 1 + * + * + * \\
0 + 0 + 1 + * + * \\
0 + 0 + 0 + 1 + * \\
0 + 0 + 0 + 0 + 1
\end{aligned}
$$

<div class="sage">
<script type="text/x-sage">
# Langkah 8
A.rescale_row(4,-1)
A
</script>
</div>