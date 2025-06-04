# Interpolasi Lagrange

## Kode Program

```python
def LI(x, x_vs, y_vs):
    n = len(x_vs)
    result = 0

    for i in range(n):
        temp = y_vs[i]
        for j in range(n):
            if i != j:
                temp *= (x - x_vs[j]) / (x_vs[i] - x_vs[j])
        result += temp

    return result

# Data titik
x_vs = [6, 9, 12, 15]
y_vs = [234, 960, 2280, 4356]

# Titik yang ingin dicari f(x)
x = 11

# Menghitung f(11)
f_x = LI(x, x_vs, y_vs)
print(f"f({x}) ≈ {f_x:.2f}")

## Penjelasan Kode

- Fungsi `LI` menerima parameter:
  - `x`: titik yang ingin dicari nilai fungsi interpolasi.
  - `x_vs`: daftar nilai x dari titik data.
  - `y_vs`: daftar nilai y dari titik data.

- Fungsi menghitung nilai interpolasi dengan rumus polinomial Lagrange:

  \[
  L_i(x) = \prod_{\substack{j=0 \\ j \neq i}}^{n-1} \frac{x - x_j}{x_i - x_j}
  \]

  \[
  f(x) = \sum_{i=0}^{n-1} y_i \cdot L_i(x)
  \]

- `for i in range(n)`: mengiterasi tiap titik data untuk menghitung basis polinomial Lagrange.

- `for j in range(n)`: menghitung produk untuk \(L_i(x)\) dengan mengalikan pecahan \(\frac{x - x_j}{x_i - x_j}\) untuk setiap \(j \neq i\).

- Variabel `result` menjumlahkan hasil tiap basis dikalikan nilai \(y_i\).

## Anggota R08

- Nama Anggota 1  
- Nama Anggota 2  
- Nama Anggota 3  


