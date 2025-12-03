🚀 Struktur Pengulangan
Python hanya menyediakan 2 perintah untuk melakukan proses pengulangan yaitu
"for" dan "while". Jika ingin menggunakan "for" untuk mengulang perintah
berdasarkan indeks, gunakan fungsi range( ). Selain itu, fungsi range( ) berguna
untuk membuat objek dari kelas range yang berisi kumpulan nilai dalam rentang
tertentu.

# Contoh program
a = 'Python'
# menelusuri semua karakter dalam string:
for c in a:
    print(c, end='')
    
output :Python

b = ['Python', 'Ruby', 'Perl', 'PHP']
# menelusuri semua karakter di dalam list:
for e in b:
    print(e)

output: Python
        Ruby
        Perl
        PHP

c = {'one':'satu', 'two':'dua', 'three':'tiga'}
# menelusuri semua elemen di dalam dictionary:
for key in c:
    print('Arti "%s" adalah "%s"' % (key, c[key]))

output :Arti "one" adalah "satu"
        Arti "two" adalah "dua"
        Arti "three" adalah "tiga"

for i in range(6):
    print(i, end='')

output : 012345

# range(10, 22, 2) artinya dari 10 sampai sebelum 22, langkah 2
for i in range(10, 22, 2):
    print("%d " % i, end='')

output :10 12 14 16 18 20 
