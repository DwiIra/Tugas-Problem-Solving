# Tugas Metode Numerik
Dosen Pengampuh : Anggay Luri Pramana,M.Kom

# Problem Solving
Problem-solving menggunakan metode numerik melibatkan penggunaan teknik-teknik matematika dan komputasi untuk mendapatkan solusi numerik dari suatu masalah.<br>
Contoh metode numerik melibatkan solusi persamaan differensial, pencarian akar persamaan nonlinear, atau interpolasi data. <br>
Berbagai metode seperti Metode Euler, Metode Newton-Raphson, atau Metode Runge-Kutta sering digunakan tergantung pada sifat masalah yang dihadapi.<br>

# Soal
Given an array of integers, calculate the ratios of its elements that are positive, negative, and zero.<br>
Print the decimal value of each fraction on a new line with  places after the decimal.<br>
Note: This challenge introduces precision problems. The test cases are scaled to six decimal places, though answers with absolute error of up to  are acceptable.
Example
    arr = [1, 1, 0, -1, -1]

There are  n=5 elements, two positive, two negative and one zero. Their ratios are ,  2/5 = 0.400000, 2/5 = 0.400000  and 1/5 = 0.200000. Results are printed as:
    0.400000
    0.400000
    0.200000

Function Description
Complete the plusMinus function in the editor below.
plusMinus has the following parameter(s):
int arr[n]: an array of integers

Print
Print the ratios of positive, negative and zero values in the array. Each value should be printed on a separate line with 6 digits after the decimal. The function should not return a value.

Input Format
The first line contains an integer, , the size of the array.
The second line contains  space-separated integers that describe arr[n].

Constraints
    0 < n <= 100
    -100 <= arr[i] <= 100

Output Format
Print the following 3 lines, each to 6 decimals:
1. proportion of positive values
2. proportion of negative values
3. proportion of zeros

Sample Input
    STDIN           Function
    -----           --------
    6               arr[] size n = 6
    -4 3 -9 0 4 1   arr = [-4, 3, -9, 0, 4, 1]

Sample Output
    0.500000
    0.333333
    0.166667

Explanation
There are 3 positive numbers, 2 negative numbers, and 1 zero in the array.
The proportions of occurrence are positive: 3/6 = 0.500000, negative: 2/6 = 0.33333 and zeros: 1/6 = 0.166667.

