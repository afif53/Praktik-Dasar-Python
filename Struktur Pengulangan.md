🚀 Praktik Dasar Python: Pemilihan, frozenset, dan PengulanganDokumen ini mencakup tiga topik dasar dalam pemrograman Python: Struktur Pemilihan (if), tipe data frozenset (set yang tidak dapat diubah), dan Struktur Pengulangan (for dan while).1. 🚦 Struktur Pemilihan (if, elif, else)Dalam Python, struktur pemilihan dibuat menggunakan perintah if. Klausa else harus ditulis sejajar dengan perintah if. Sebelum memulai blok baru, wajib menyertakan tanda titik dua atau colon (:). Indentasi menentukan blok kode. Untuk menangani banyak kondisi, digunakan klausa elif sebelum else.Contoh 1: Pemilihan SederhanaPython# Contoh:
str = 'Pemrograman Python'
versi = 3

if versi == 3:
    print(str + ' 3')
else:
    print(str)

# Output:
# Pemrograman Python 3
Contoh 2: Memeriksa Versi Python dengan sysPython# Contoh
import sys
versi = sys.version

if versi[1] == '3':
    print('Bahasa\t: Python 3')
    print('Versi Python\t: ' + versi[:5])
else:
    print('Versi tidak diketahui')

# Contoh Output:
# Bahasa	: Python 3
# Versi Python	: 3.11. 
Contoh 3: Kalkulator dengan if-elif-elsePython# Contoh kode Python
def main():
    x = float(input('Masukkan bilangan pertama\t:'))
    y = float(input('Masukkan bilangan kedua\t:'))
    op = input('Masukkan operator (+,-,*,/)\t: ')

    if op == '+':
        print('%.2f + %.2f = %.2f' % (x, y, x+y))
    elif op == '-':
        print('%.2f - %.2f = %.2f' % (x, y, x-y))
    elif op == '*':
        print('%.2f * %.2f = %.2f' % (x, y, x*y))
    elif op == '/':
        # Asumsi y != 0 untuk menghindari ZeroDivisionError
        print('%.2f / %.2f = %.2f' % (x, y, x/y))
    else:
        print('ERROR: Gunakan operator +,-,*,/')

if __name__ == '__main__':
    main()

# Contoh Input/Output:
# Masukkan bilangan pertama	:1034
# Masukkan bilangan kedua	:273
# Masukkan operator (+,-,*,/)	:*
# 1034.00 * 273.00 = 282282.00
2. 🧊 Tipe frozenset (Immutable Set)frozenset adalah tipe data himpunan yang tidak dapat diubah (immutable). Oleh karena itu, ia tidak memiliki metode mutator seperti add(), update(), remove(), atau clear(). Percobaan untuk menggunakan metode-metode ini akan menghasilkan AttributeError.Contoh Kesalahan (AttributeError)Percobaan MetodeKodeHasil Erroradd()python\nfs = frozenset([1, 2, 3])\nprint(fs)\nfs.add(4)AttributeError: 'frozenset' object has no attribute 'add'update()python\nfs = frozenset([1, 2, 3])\nprint(fs)\nfs.update([4, 5])AttributeError: 'frozenset' object has no attribute 'update'remove()python\nfs = frozenset([1, 2, 3])\nprint(fs)\nfs.remove(3)AttributeError: 'frozenset' object has no attribute 'remove'clear()python\nfs = frozenset([1, 2, 3])\nprint(fs)\nfs.clear()AttributeError: 'frozenset' object has no attribute 'clear'3. 🔄 Struktur Pengulangan (for dan while)Python menyediakan dua perintah untuk melakukan proses pengulangan: for dan while.3.1 Perintah forPerintah for digunakan untuk mengulang perintah berdasarkan indeks atau menelusuri elemen-elemen dalam sebuah koleksi (iterable). Untuk mengulang perintah berdasarkan indeks, gunakan fungsi range(), yang berfungsi untuk membuat objek dari kelas range berisi kumpulan nilai dalam rentang tertentu.A. Mengulang Karakter dalam StringPython# Contoh program
a = 'Python'
# menelusuri semua karakter dalam string:
for c in a:
    print(c, end='')
    
# Output:
# Python
B. Mengulang Elemen dalam ListPython# Contoh program
b = ['Python', 'Ruby', 'Perl', 'PHP']
# menelusuri semua karakter di dalam list:
for e in b:
    print(e)
    
# Output:
# Python
# Ruby
# Perl
# PHP
C. Mengulang Pasangan Kunci-Nilai dalam DictionaryPython# Contoh program
c = {'one':'satu', 'two':'dua', 'three':'tiga'}
# menelusuri semua elemen di dalam dictionary:
for key in c:
    print('Arti "%s" adalah "%s"' % (key, c[key]))

# Output:
# Arti "one" adalah "satu"
# Arti "two" adalah "dua"
# Arti "three" adalah "tiga"
D. Mengulang dengan range() (Satu Argumen)range(N) menghasilkan angka dari 0 hingga N-1.Python# Contoh
for i in range(6):
    print(i, end='')

# Output:
# 012345
E. Mengulang dengan range() (Tiga Argumen)range(start, stop, step) menghasilkan angka mulai dari start hingga sebelum stop, dengan interval step.Python# Contoh:
# range(10, 22, 2) artinya dari 10 sampai sebelum 22, langkah 2
for i in range(10, 22, 2):
    print("%d " % i, end='')

# Output:
# 10 12 14 16 18 20 
