🚀 Struktur Pengulangan
Python hanya menyediakan 2 perintah untuk melakukan proses pengulangan yaitu
"for" dan "while". Jika ingin menggunakan "for" untuk mengulang perintah
berdasarkan indeks, gunakan fungsi range( ). Selain itu, fungsi range( ) berguna
untuk membuat objek dari kelas range yang berisi kumpulan nilai dalam rentang
tertentu.

str = 'Pemrograman Python'
versi = 3

if versi == 3:
    print(str + ' 3')
else:
    print(str)

# Output:
Pemrograman Python 3

Contoh 2: Memeriksa Versi Python dengan sysPython
import sys
versi = sys.version

if versi[:1] == '3':
    print('Bahasa\t\t: Python '3')
    print('Versi Python\t: ' + versi[:5])

# Output: 
Bahasa	: Python 3
Versi Python	: 3.11. 

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

# Output:
Masukkan bilangan pertama	:1034
Masukkan bilangan kedua	:273
Masukkan operator (+,-,*,/)	:*
1034.00 * 273.00 = 282282.00

