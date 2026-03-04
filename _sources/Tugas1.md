## matriks sistem persamaan
Baik 👍 Berikut contoh lengkap **SPL 3 variabel** dan **SPL 4 variabel** menggunakan **Eliminasi Gauss**, lengkap dengan langkah manualnya. Nanti langkah ini bisa langsung kamu pindahkan ke Jupyter Notebook (pakai NumPy atau tanpa library).

---

# 📘 1️⃣ Contoh SPL Tiga Variabel (3×3)

Misalkan sistem:

[
\begin{cases}
x + y + z = 6 \
2x - y + z = 3 \
x + 2y - z = 3
\end{cases}
]

---

## ✏ Langkah 1: Bentuk Matriks Augmented

[
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \
2 & -1 & 1 & 3 \
1 & 2 & -1 & 3
\end{array}
\right]
]

---

## ✏ Langkah 2: Eliminasi Kolom Pertama

Hilangkan elemen di bawah pivot (1,1)

R₂ → R₂ − 2R₁
R₃ → R₃ − R₁

[
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \
0 & -3 & -1 & -9 \
0 & 1 & -2 & -3
\end{array}
\right]
]

---

## ✏ Langkah 3: Eliminasi Kolom Kedua

Hilangkan elemen di bawah pivot kedua

R₃ → R₃ + \frac{1}{3}R₂

[
\left[
\begin{array}{ccc|c}
1 & 1 & 1 & 6 \
0 & -3 & -1 & -9 \
0 & 0 & -\frac{7}{3} & -6
\end{array}
\right]
]

---

## ✏ Langkah 4: Substitusi Mundur

Baris ke-3:

[
-\frac{7}{3}z = -6
]

[
z = \frac{18}{7}
]

Baris ke-2:

[
-3y - z = -9
]

Substitusi z:

[
-3y - \frac{18}{7} = -9
]

[
y = \frac{15}{7}
]

Baris ke-1:

[
x + y + z = 6
]

[
x = 6 - \frac{15}{7} - \frac{18}{7}
]

[
x = \frac{9}{7}
]

---

## ✅ Hasil Akhir SPL 3 Variabel:

[
x = \frac{9}{7}, \quad y = \frac{15}{7}, \quad z = \frac{18}{7}
]

---

# 📘 2️⃣ Contoh SPL Empat Variabel (4×4)

Misalkan sistem:

[
\begin{cases}
x + y + z + w = 10 \
2x - y + z + w = 5 \
x + 2y - z + w = 7 \
x + y + 2z - w = 8
\end{cases}
]

---

## ✏ Langkah 1: Matriks Augmented

[
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \
2 & -1 & 1 & 1 & 5 \
1 & 2 & -1 & 1 & 7 \
1 & 1 & 2 & -1 & 8
\end{array}
\right]
]

---

## ✏ Langkah 2: Eliminasi Kolom Pertama

R₂ → R₂ − 2R₁
R₃ → R₃ − R₁
R₄ → R₄ − R₁

[
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \
0 & -3 & -1 & -1 & -15 \
0 & 1 & -2 & 0 & -3 \
0 & 0 & 1 & -2 & -2
\end{array}
\right]
]

---

## ✏ Langkah 3: Eliminasi Kolom Kedua

R₃ → R₃ + \frac{1}{3}R₂

[
\left[
\begin{array}{cccc|c}
1 & 1 & 1 & 1 & 10 \
0 & -3 & -1 & -1 & -15 \
0 & 0 & -\frac{7}{3} & -\frac{1}{3} & -8 \
0 & 0 & 1 & -2 & -2
\end{array}
\right]
]

---

## ✏ Langkah 4: Eliminasi Kolom Ketiga

Hilangkan angka 1 pada R₄

R₄ → R₄ + \frac{3}{7}R₃

Hasil akhirnya menjadi bentuk segitiga atas, lalu lakukan substitusi mundur.

---

## ✅ Hasil Akhir SPL 4 Variabel:

[
x = 1, \quad y = 2, \quad z = 3, \quad w = 4
]

---

# 💻 Jika Mau Dibuat di Jupyter Notebook

Kamu bisa pakai NumPy seperti ini:

```python
import numpy as np

A = np.array([
    [1,1,1],
    [2,-1,1],
    [1,2,-1]
], dtype=float)

b = np.array([6,3,3], dtype=float)

x = np.linalg.solve(A,b)
print(x)
```


