# TUGAS-DISTRIK-PERTEMUAN-7
1. Simulasi Tabel Kebenaran (Truth Table)
Program ini menghasilkan tabel kebenaran untuk operator logika dasar (and, or, not,
implies).
import itertools
# Definisi fungsi implikasi
def implies(p, q):
 return (not p) or q
# Header tabel
print(f"{'p':<5}{'q':<5}{'p and q':<10}{'p or q':<10}{'¬p':<5}{'p → q':<8}")
# Iterasi semua kombinasi p dan q (True/False)
for p, q in itertools.product([True, False], repeat=2):
 print(f"{p!s:<5}{q!s:<5}{(p and q)!s:<10}{(p or q)!s:<10}{(not p)!s:<5}{implies(p, q)!s:<8}")

BAGIIAN 2
2. Pembuktian Kontradiksi Sederhana (Logika Matematis)
Contoh pembuktian:
Jika n² ganjil, maka n juga ganjil.
Kita buktikan secara logika bahwa kebalikannya menghasilkan kontradiksi.
def is_odd(n):
 return n % 2 == 1
def proof_by_contradiction():
 for n in range(1, 10):
 if is_odd(n**2) and not is_odd(n):
 print(f"Kontradiksi ditemukan pada n={n}!")
 return False
 print("Tidak ada kontradiksi ditemukan → pernyataan benar (jika n² ganjil maka n
ganjil).")
 return True
proof_by_contradiction()
