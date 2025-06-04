# Interpolasi Lagrange

## Kode Program

```python
# rumus Interpolasi Lagrange:
def LI(x, x_vs, y_vs):
    n = len(x_vs)
    result = 0

    for i in range(s):
        temp = y_vs[i]
        for j in range(s):
            if i != j:
                temp *= (x - x_vs[j]) / (x_vs[i] - x_vs[j])
        result += temp

    return result

# data:
x_vs = [6, 9, 12, 15]
y_vs = [234, 960, 2280, 4356]

# f(x) saat:
x = 11

# f(11):
f_x = LI(x, x_vs, y_vs)
print(f"f({x}) ≈ {f_x:.2f}")
```

## Penjelasan Kode

- Fungsi `LI` menerima parameter:
  - `x`: titik yang ingin dicari nilai fungsi interpolasi.
  - `x_vs`: daftar nilai x dari titik data.
  - `y_vs`: daftar nilai y dari titik data.

- Fungsi menghitung nilai interpolasi dengan rumus polinomial Lagrange:

  ![Rumus](./Rumus.png)

- `for i in range(n)`: mengiterasi tiap titik data untuk menghitung basis polinomial Lagrange.

- `for j in range(n)`: menghitung produk untuk `Li(x)` dengan mengalikan pecahan `(x - x_j) / (x_i - x_j)` untuk setiap `j ≠ i`.

- Variabel `result` menjumlahkan hasil tiap basis dikalikan nilai `y_i`.

## Anggota R08

- Nama Anggota 1  
- Nama Anggota 2  
- Nama Anggota 3  


