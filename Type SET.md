🧠 Tipe Data set (Himpunan) di Python
Tipe data set di Python adalah kumpulan item yang tidak berurutan (unordered) dan tidak memiliki duplikat (unindexed). Tipe ini sangat berguna untuk melakukan operasi himpunan matematis seperti gabungan, irisan, dan selisih.

1. Operasi Dasar Set (Mutator Methods)
Bagian ini menunjukkan metode-metode yang digunakan untuk membuat, menambah (add, update), dan menghapus (remove, clear) elemen dari sebuah set.

Python

import sys

def printElements(s, info):
    print(info)
    if len(s) == 0:
        print("Himpunan kosong\n")
        # sys.exit(1) # Baris ini dikomentari agar kode berjalan penuh
    for e in s:
        print(str(e) + ", ", end='')
    print("\n")

# Membuat himpunan
s = set([11, 22, 33, 44, 55])
printElements(s, "Elemen awal:")

# Menambah anggota/elemen baru menggunakan metode add()
s.add(66)
s.add(77)
printElements(s, "Setelah pemanggilan add():")

# Menambah anggota/elemen baru menggunakan metode update() (untuk menambahkan beberapa item)
s.update([88, 99])
printElements(s, "Setelah pemanggilan update():")

# Menghapus elemen dengan nilai 44
# Catatan: Gunakan .discard() jika elemen mungkin tidak ada dan Anda tidak ingin KeyError.
s.remove(44)
printElements(s, "Setelah pemanggilan remove():")

# Menghapus semua elemen
s.clear()
printElements(s, "Setelah pemanggilan clear():")
⚙️ Output Kode 1:
Karena set tidak berurutan, urutan elemen dalam output mungkin berbeda-beda.

Elemen awal:
33, 11, 44, 22, 55, 

Setelah pemanggilan add():
33, 66, 11, 44, 77, 22, 55, 

Setelah pemanggilan update():
33, 66, 99, 11, 44, 77, 22, 55, 88, 

Setelah pemanggilan remove():
33, 66, 99, 11, 77, 22, 55, 88, 

Setelah pemanggilan clear():
Himpunan kosong
2. Operasi Himpunan Matematis
Tipe set mendukung operator khusus yang memungkinkan kita melakukan operasi himpunan layaknya dalam matematika (Union, Intersection, Difference, Symmetric Difference).

Getty Images

Python

# Type set mendukung operasi-operasi himpunan seperti:

x = set([1, 2, 3])
y = set([3, 4])

# 1. Union (Gabungan)
# Operator: | (Menggabungkan semua elemen dari kedua set)
a = x | y 
print('Operasi union:')
print(a) 

# 2. Intersection (Irisan)
# Operator: & (Mencari elemen yang ada di kedua set)
b = x & y 
print('Operasi intersection:')
print(b) 

# 3. Difference (Selisih)
# Operator: - (Elemen di set pertama yang TIDAK ada di set kedua)
c = x - y 
print('Operasi difference:')
print(c) 

# 4. Symmetric Difference (Selisih Simetris)
# Operator: ^ (Elemen yang ada di salah satu set, tetapi TIDAK di keduanya)
d = x ^ y 
print('Operasi symmetric difference:')
print(d) 
🔢 Output Kode 2:
Operasi union:
{1, 2, 3, 4}
Operasi intersection:
{3}
Operasi difference:
{1, 2}
Operasi symmetric difference:
{1, 2, 4}
