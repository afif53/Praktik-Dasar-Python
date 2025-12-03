# Praktik-Dasar-Python
Modul 5 TYPE SET, STRUKTUR PEMILIHAN DAN PENGULANGAN

# >>>>>>>> KODE TYPE SET 1.
import sys

def printElements(s, info):
    print(info)
    if len(s) == 0:
        print("Himpunan kosong\n")
        # sys.exit(1) # Menghilangkan sys.exit(1) agar kode dapat dieksekusi sampai selesai
    for e in s:
        print(str(e) + ", ", end='')
    print("\n")

# membuat himpunan
s = set([11, 22, 33, 44, 55])
printElements(s, "Elemen awal:")

# menambah anggota/elemen baru
# menggunakan metode add()
s.add(66)
s.add(77)
printElements(s, "Setelah pemanggilan add():")

# menambah anggota/elemen baru
# menggunakan metode update()
s.update([88, 99])
printElements(s, "Setelah pemanggilan update():")

# menghapus elemen dengan nilai 44
# Catatan: Jika elemen tidak ada, .remove() akan memicu KeyError. 
# Gunakan .discard() jika Anda tidak ingin error.
s.remove(44)
printElements(s, "Setelah pemanggilan remove():")

# menghapus semua elemen
s.clear()
printElements(s, "Setelah pemanggilan clear():")

### OUTPUT CELL ###
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

# >>>>>>>>>> KODE TYPE SET 2.
# Type set mendukung operasi-operasi himpunan seperti:

x = set([1, 2, 3])
y = set([3, 4])

# 1. Union (Gabungan)
# Operator: |
a = x | y 
print('Operasi union:')
print(a) 

# 2. Intersection (Irisan)
# Operator: &
b = x & y 
print('Operasi intersection:')
print(b) 

# 3. Difference (Selisih)
# Operator: -
# x - y: Elemen di x yang TIDAK ada di y
c = x - y 
print('Operasi difference:')
print(c) 

# 4. Symmetric Difference (Selisih Simetris)
# Operator: ^ 
# Elemen yang ada di x atau y, tapi TIDAK di keduanya (eksklusif)
d = x ^ y 
print('Operasi symmetric difference:')
print(d) 

### OUTPUT CELL ###
Operasi union:
{1, 2, 3, 4}
Operasi intersection:
{3}
Operasi difference:
{1, 2}
Operasi symmetric difference:
{1, 2, 4}
