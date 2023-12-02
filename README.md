# Tugas Metode Numerik
Dosen Pengampuh : Anggay Luri Pramana,M.Kom

# Problem Solving
Problem-solving menggunakan metode numerik melibatkan penggunaan teknik-teknik matematika dan komputasi untuk mendapatkan solusi numerik dari suatu masalah.<br>
Metode numerik pada dasarnya lebih sering digunakan untuk menyelesaikan permasalahan matematika yang melibatkan solusi numerik dari persamaan atau sistem persamaan matematis. <br>
Dalam kasus ini, yaitu problem-solving "plus minus", yang sebenarnya melibatkan perhitungan rasio dari sejumlah elemen dalam sebuah array, metode numerik mungkin terlalu canggung atau terlalu berlebihan.<br>
Contoh metode numerik melibatkan solusi persamaan differensial, pencarian akar persamaan nonlinear, atau interpolasi data. <br>
Berbagai metode seperti Metode Euler, Metode Newton-Raphson, atau Metode Runge-Kutta sering digunakan tergantung pada sifat masalah yang dihadapi.<br>

# Soal
Given an array of integers, calculate the ratios of its elements that are positive, negative, and zero.<br>
Print the decimal value of each fraction on a new line with  places after the decimal.<br>
Note: This challenge introduces precision problems. The test cases are scaled to six decimal places, though answers with absolute error of up to  are acceptable.<br>
**Example**

    arr = [1, 1, 0, -1, -1]

There are  n=5 elements, two positive, two negative and one zero. <br>
Their ratios are ,

    2/5 = 0.400000
    2/5 = 0.400000
    1/5 = 0.200000

Results are printed as:

    0.400000
    0.400000
    0.200000

**Function Description**<br>
Complete the plusMinus function in the editor below.<br>
plusMinus has the following parameter(s):

    int arr[n]: an array of integers

**Print**<br>
Print the ratios of positive, negative and zero values in the array. <br>
Each value should be printed on a separate line with 6 digits after the decimal. <br>
The function should not return a value.<br>

**Input Format**<br>
The first line contains an integer, n, the size of the array.<br>
The second line contains  space-separated integers that describe arr[n].<br>

**Constraints**

    0 < n <= 100
    -100 <= arr[i] <= 100

**Output Format** <br>
Print the following 3 lines, each to 6 decimals:<br>
1. proportion of positive values<br>
2. proportion of negative values<br>
3. proportion of zeros<br>

**Sample Input**

    STDIN           Function
    -----           --------
    6               arr[] size n = 6
    -4 3 -9 0 4 1   arr = [-4, 3, -9, 0, 4, 1]

**Sample Output**

    0.500000
    0.333333
    0.166667

**Explanation**<br>
There are 3 positive numbers, 2 negative numbers, and 1 zero in the array.<br>
The proportions of occurrence are :<br>
**Positive:**

    3/6 = 0.500000

**Negative:**

    2/6 = 0.33333 

**Zeros:**

    1/6 = 0.166667.

# Bahasa Python 3
Disini saya menggunakan bahasa Python 3 untuk mengenyelesaikan masalah tersebut.<br>
Berikut adalah masalah kodingan yang diberikan:
```python 
#!/bin/python3

import math
import os
import random
import re
import sys

#
# Complete the 'plusMinus' function below.
#
# The function accepts INTEGER_ARRAY arr as parameter.
#

def plusMinus(arr):
    # Write your code here

if __name__ == '__main__':
    n = int(input().strip())

    arr = list(map(int, input().rstrip().split()))

    plusMinus(arr)
```

# ANSWER & EXPLANATION
Seperti yang sudah saya jelaskan diatas bahwa saya menggunakan bahasa Python 3 untuk mengerjakan tugas berikut dan juga import yang saya gunakan dari pilihan diatas adalah import random. <br>
Berikut adalah jawaban kodingan saya:
```python 
def plusMinus(arr):
    positive_count = sum(1 for num in arr if num > 0)
    negative_count = sum(1 for num in arr if num < 0)
    zero_count = sum(1 for num in arr if num == 0)
    
    n = len(arr)
    
    positive_proportion = positive_count / n
    negative_proportion = negative_count / n
    zero_proportion = zero_count / n
    
    print("{:.6f}".format(positive_proportion))
    print("{:.6f}".format(negative_proportion))
    print("{:.6f}".format(zero_proportion))
```
Kode ini menghitung jumlah elemen positif, negatif, dan nol dalam array dan kemudian menghitung proporsinya, mencetak setiap proporsi dengan 6 tempat desimal.<br>

Sekarang kita coba untuk gabungkan maka akan menjadi seperti ini
```python 
#!/bin/python3
import math
import os
import random
import re
import sys

#
# Complete the 'plusMinus' function below.
#
# The function accepts INTEGER_ARRAY arr as parameter.
#

def plusMinus(arr):
    # Write your code here
    positive_count = sum(1 for num in arr if num > 0)
    negative_count = sum(1 for num in arr if num < 0)
    zero_count = sum(1 for num in arr if num == 0)
    
    n = len(arr)
    
    positive_proportion = positive_count / n
    negative_proportion = negative_count / n
    zero_proportion = zero_count / n
    
    print("{:.6f}".format(positive_proportion))
    print("{:.6f}".format(negative_proportion))
    print("{:.6f}".format(zero_proportion))
    
if __name__ == '__main__':
    n = int(input().strip())

    arr = list(map(int, input().rstrip().split()))
    
    plusMinus(arr)
```

# Input (stdin)
input yang akan di tes dalam web ini ada 2 yaitu:<br>
**Pertama**

    6
    -4 3 -9 0 4 1

**Ke-dua**

    8
    1 2 3 -1 -2 -3 0 0

# Output (stdout)
output yang diinginkan pada setiap input seperti berikut:<br>
**Pertama**

    0.500000
    0.333333

**Output**

    0.500000
    0.333333
    0.166667

**Ke-dua**

    0.375000
    0.375000

**Output**

    0.375000
    0.375000
    0.250000
