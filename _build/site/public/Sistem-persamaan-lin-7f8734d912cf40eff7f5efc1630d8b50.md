# Sistem Persamaan Linear 
#### 1.2 Sistem Persamaan Linear 
Menghitung dan mempelajari solusi persamaan, serta sistem persamaan, tanpa diragukan lagi memainkan peran penting dalam matematika; meskipun kami segera menambahkan bahwa ini bukan satu-satunya hal yang dilakukan para matematikawan! Dalam bab ini, kita akan mengembangkan teori yang pada dasarnya lengkap untuk persamaan matematis yang relatif sederhana: yaitu, persamaan linear. Hal ini akan menjadi pengantar tidak langsung bagi studi aljabar linear kita, karena di balik deskripsi parametrik solusi sistem linear tersirat konsep-konsep ruang vektor seperti subruang, rentangan (span), dan kebebasan linear. Lebih jauh lagi, kita akan bertemu dengan salah satu alat komputasi paling penting dalam aljabar linear: eliminasi Gauss. 
#### 1.2.1 Sistem Persamaan Linear
Definition 1.2.1. Persamaan Linear.  Sebuah ekspresi linear dalam $n$
peubah tak diketahui (atau variabel) $x1,x2,...,xn$ adalah ekspresi berbentuk.
$$
a1_x1 + a_2x_2 + ... + a_nx_x,
$$
dengan $a_1,a_2,...,a_n$ adalah bilangan real tetap.

Sebuah persamaan linear dalam peubah $x_1,x_2,...,x_n$
 adalah persamaan yang dapat disederhanakan—hanya menggunakan penjumlahan dan pengurangan—menjadi bentuk
$$
a_1x_1+a_2x_2+...+a_nx_n = b,
$$
yang kita sebut sebagai bentuk baku. Suatu persamaan dalam peubah $x_1,x_2,...,x_n$
 disebut nonlinear jika tidak dapat disederhanakan ke bentuk di atas hanya dengan penjumlahan dan pengurangan.

Diberikan suatu persamaan linear dalam bentuk baku (1.2.1), persamaan tersebut disebut *homogen* jika , $b=0$
 dan *nonhomogen* jika $b \neq 0$ .

#### Example 1.2.2. Persamaan Linear dan Nonlinear. 
1. Tinjau $( \sqrt{3x} + sin(5) = 2x - e^4 y)$. Ini adalah persamaan linear dalam peubah $( x, y, z )$. Bentuk bakunya adalah $( \sqrt{3x} + e^4 y - 2x = -\sin(5) )$. Karena ruas kanannya tak nol, persamaan ini bersifat nonhomogen.

2. Persamaan $( x^2 + y^2 = 1 )$ adalah persamaan nonlinear dalam peubah $( x )$ dan $( y )$.

#### Definisi 1.2.3. Sistem Persamaan Linear. 
Sebuah *sistem persamaan linear* (atau *sistem linear*) adalah himpunan persamaan linear.

Sebuah sistem linear disebut *homogen* jika seluruh persamaannya homogen.

Saat menampilkan sistem yang terdiri atas $m$ persamaan dalam $n$ peubah 
$x_1, x_2, \ldots, x_n$, biasanya kita menuliskan setiap persamaan dalam bentuk baku 
dan menyelaraskan suku-suku yang bersesuaian ke dalam kolom:

$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n &= b_1 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n &= b_2 \\
\vdots \qquad\qquad\qquad\qquad & \vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n &= b_m
\end{aligned}
$$

Sistem homogen biasanya ditulis sebagai:

$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n &= 0 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n &= 0 \\
\vdots \qquad\qquad\qquad\qquad & \vdots \\
_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n &= 0
\end{aligned}
$$

#### Remark 1.2.4.
Anda perlu segera membiasakan diri dengan notasi indeks ganda yang digunakan 
untuk menampilkan sistem linear. Berikut cara memahaminya:

- Indeks $i$ pada $a_{ij}$ dan $b_i$ menunjukkan baris ke-$i$ dalam sistem yang ditampilkan, atau secara ekuivalen, persamaan ke-$i$.
- Indeks $j$ pada $a_{ij}$ menunjukkan kolom ke-$j$ yang berkaitan dengan peubah ke-$j$, untuk $1 \leq j \leq n$.

#### Definisi 1.2.5. Solusi Sistem Linear.
Sebuah *solusi persamaan linear*

$$
a_1x_1 + a_2x_2 + \cdots + a_nx_n = b
$$

adalah sebuah $n$-tuple $(s_1, s_2, \ldots, s_n)$ bilangan real sedemikian sehingga 
substitusi $x_1 = s_1, x_2 = s_2, \ldots, x_n = s_n$ menjadikan persamaan tersebut benar. 
Dalam hal ini, kita katakan bahwa $(s_1, \ldots, s_n)$ *memecahkan persamaan tersebut*.

Sebuah  *solusi sistem persamaan linear*

$$
\begin{aligned}
a_{11}x_1 + a_{12}x_2 + \cdots + a_{1n}x_n &= b_1 \\
a_{21}x_1 + a_{22}x_2 + \cdots + a_{2n}x_n &= b_2 \\
\vdots \qquad\qquad\qquad\qquad & \vdots \\
a_{m1}x_1 + a_{m2}x_2 + \cdots + a_{mn}x_n &= b_m
\end{aligned}
$$

adalah sebuah $n$-tuple $(s_1, s_2, \ldots, s_n)$ yang merupakan solusi dari masing-masing 
$m$ persamaan dalam sistem tersebut. Kita katakan bahwa 
$(s_1, s_2, \ldots, s_n)$ *memecahkan sistem tersebut.*

Diberikan suatu sistem linear, kita berupaya mencari himpunan *seluruh* 
solusinya. Seperti yang akan segera kita lihat, himpunan solusi ini memiliki 
salah satu dari tiga bentuk kualitatif berikut:

- item Himpunan solusi kosong; artinya, tidak ada solusi. Dalam hal ini, 
sistem disebut *tidak konsisten*. Jika tidak demikian, sistem disebut *konsisten*
    
- item Himpunan solusi berisi tepat satu elemen; artinya, hanya ada satu solusi.
    
- item Himpunan solusi berisi tak hingga banyak elemen; artinya, terdapat tak hingga solusi.


#### Example 1.2.6. Solusi Sistem Elementer. 
Untuk tiap sistem berikut, tentukan himpunan solusinya.

\begin{enumerate}
    \item 
    \[
    \begin{aligned}
    x - y &= 0 \\
    x - y &= 1
    \end{aligned}
    \]

    \item 
    \[
    \begin{aligned}
    x - y &= 0 \\
    x + y &= 1
    \end{aligned}
    \]

    \item 
    \[
    \begin{aligned}
    x - y &= 1 \\
    2x - 2y &= 2
    \end{aligned}
    \]
\end{enumerate}

*Solution.*

Seperti yang mungkin Anda ingat, suatu persamaan linear (nontrivial) 
dalam dua peubah mendefinisikan sebuah garis di $\mathbb{R}^2$, dan 
persamaan linear dalam tiga peubah mendefinisikan sebuah bidang di 
$\mathbb{R}^3$. Pengamatan ini memungkinkan kita menggunakan intuisi 
geometris yang kuat dalam menganalisis sistem linear dengan dua atau 
tiga peubah. Karena garis dan bidang juga akan menjadi sumber contoh 
penting dalam kuliah ini, kita mengingat kembali beberapa gagasan 
dasarnya di bawah ini.