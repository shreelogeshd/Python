#  Input & Output Programs

This notebook contains Python programs focused on **Basic input and output operations**.
These problems helped me understand how Python handles user input, formatted output, printing values, and simple data transformations.

### Question 1
### Integer Input and Output
Question:<br>
Problem Statement:<br>
Write a code to get the input in the given format and print the output in the given format

Input Description:<br>
To take an integer value

Output Description:<br>
Print the integer value
Sample Input:<br>
2

Sample Output:<br>
2

Solution:
```python
userInput = input()
print(userInput)
```

### Question 2
### Integer List Input/Output
Question:<br>
Problem Statement:<br>
Write a code to get the input in the given format and print the output in the given format

Input Description:<br>
A single line contains integers separated by space

Output Description:<br>
Print the integer list of integers separated by space

Sample Input:<br>
2 3 4 5 6 7 8

Sample Output:<br>
2 3 4 5 6 7 8

Solution:
```python
a = input().split(" ")
print(" ".join(a))
```

### Question 3
### Echo Input Array
Question:<br>
Problem Statement:<br>
Write a code to get the input in the given format and print the output in the given format.

Input Description:<br>
First-line indicates two integers which are the size of array and 'K' value.
Second-line indicates an integer contains elements of an array.

Output Description:<br>
Print the taken input in the same format.

Sample Input:<br>
5 3<br>
1 2 3 4 5

Sample Output:<br>
5 3<br>
1 2 3 4 5

Solution:
```python
a = input().split(" ")
b = input().split(" ")

print(" ".join(a))
print(" ".join(b))
```

### Question 4
### Input-Output Formatting
Question:<br>
Problem Statement:<br>
Write a code to get the input in the given format and print the output in the given format

Input Description:<br>
First-line indicates two integers separated by space. Second-line indicates two integers separated by space. Third-line indicates two integers separated by space.

Output Description:<br>
Print the input in the same format.

Sample Input:<br>
2 4<br>
2 4<br>
2 4<br>

Sample Output:<br>
2 4<br>
2 4<br>
2 4<br>

Solution:
```python
a = input().split(" ")
b = input().split(" ")
c = input().split(" ")

print(" ".join(a))
print(" ".join(b))
print(" ".join(c))
```

### Question 4
### Input-Output Formatting-2
Question:<br>
Problem Statement:<br>
Write a code to get the input in the given format and print the output in the given format

Input Description:<br>
First-line indicates two integers separated by space. Second-line indicates three integers separated by space. Third-line indicates three integers separated by space

Output Description:<br>
Print the input in the same format.

Sample Input:<br>
2 5<br>
2 5 6<br>
2 4 5<br>

Sample Output:<br>
2 5<br>
2 5 6<br>
2 4 5<br>

Solution:
```python
a = input().split(" ")
b = input().split(" ")
c = input().split(" ")

print(" ".join(a))
print(" ".join(b))
print(" ".join(c))
```

### Question 5
### Read and Print Integers
Question:<br>
Problem Statement:<br>
Write a code to get the input in the given format and print the output in the given format

Input Description:<br>
Three integers are given in line by line.

Output Description:<br>
Print the integers in a single line separate by space.

Sample Input:<br>
2<br>
4<br>
5<br>

Sample Output:<br>
2 4 5

Solution:
```python
a = input()
b = input()
c = input()

print(a+ " " + b + " " + c)
```

### Question 6
### Print Input Five Times
Question:<br>
Problem Statement:<br>
Write a code to get the input and print it 5 times.

Input Description:<br>
A single line contains an integer N.

Output Description:<br>
Output contains 5 lines with each line having the value N.

Explanation:<br>
The value N has been written 5 times.

Sample Input:<br>
4

Sample Output:<br>
4<br>
4<br>
4<br>
4<br>
4<br>

Solution:
```python
n = int(input())
for i in range(5):
    print(n)
```

### Question 7
### Print Input Five Times
Question:<br>
Problem Statement:<br>
Write a code to get 2 integers A and N. Print the integer A, N times in separate line.

Input Description:<br>
First line contains an integer A.
Second line contains an Integer N.

Output Description:<br>
Print the integer A, N times in a separate line.

Explanation:<br>
The integer A(2) is printed N(3) times.

Sample Input:<br>
2 3

Sample Output:<br>
2<br>
2<br>
2<br>

Solution:
```python
a = input().split()
for i in range(int(a[1])):
    print(a[0])
```

### Question 8
### Print Numbers 1 to N
Question:<br>
Problem Statement:<br>
Write a code to get an integer N and print values from 1 till N in a separate line.

Input Description:<br>
A single line contains an integer N.

Output Description:<br>
Print the values from 1 to N in a separate line.

Sample Input:<br>
5

Sample Output:<br>
1<br>
2<br>
3<br>
4<br>
5<br>

Solution:
```python
n = int(input().strip())
for i in range(1, n + 1):
    print(i)
```

### Question 9
### Print Even Numbers up to N
Question:<br>
Problem Statement:<br>
Write a code to get an integer N and print the even values from 1 till N in a separate line.

Input Description:<br>
A single line contains an integer N.

Output Description:<br>
Print the even values from 1 to N in a separate line.

Explanation:<br>
The even values from 1 upto N is printed.

Sample Input:<br>
6

Sample Output:<br>
2<br>
4<br>
6<br>

Solution:
```python
a = int(input())
for i in range(2, a + 1, 2):
    print(i)
```

### Question 10
### Reverse Integer Sequence
Question:<br>
Problem Statement:<br>
Write a code to get an integer N and print the values from N to 1.

Input Description:<br>
A single line contains an integer N.

Output Description:<br>
Print the values from N to 1 in a separate line.

Explanation:<br>
The values from N upto 1 is printed.

Sample Input:<br>
10

Sample Output:<br>
10<br>
9<br>
8<br>
7<br>
6<br>
5<br>
4<br>
3<br>
2<br>
1<br>

Solution:
```python
a = int(input())
for i in range(a, 0, -1):
    print(i)
```

### Question 11
### Sum of Numbers up to N
Question:<br>
Problem Statement:<br>
Write a code to get an integer N and print the sum of values from 1 to N.

Input Description:<br>
A single line contains an integer N.

Output Description:<br>
Print the sum of values from 1 to N.

Explanation:<br>
The sum of values from 1-10 is 55.

Sample Input:<br>
10

Sample Output:<br>
55

Solution:
```python
a = int(input())
for i in range (a):
    a = a + i

print(a)
```

### Question 12
### Print Integer Digits
Question:<br>
Problem Statement:<br>
Write a code to get an integer N and print the digits of the integer.

Input Description:<br>
A single line contains an integer N.

Output Description:<br>
Print the digits of the integer in a single line separated by space,

Explanation:<br>
The digits are splitted and displayed.

Sample Input:<br>
348

Sample Output:<br>
3 4 8

Solution:
```python
a = input().strip()
print(" ".join(a))
```

### Question 13
### Sum of Integer Digits
Question:<br>
Problem Statement:<br>
Write a code get an integer number as input and print the sum of the digits.

Input Description:<br>
A single line containing an integer.

Output Description:<br>
Print the sum of the digits of the integer.

Explanation:<br>
1+2+4=7

Sample Input:<br>
124

Solution:
```python
a = map(int,input().strip())
n=0
for i in a:
    n += i
print(n)
```

### Question 14
### Find Quotient and Remainder
Question:<br>
Problem Statement:<br>
Given a two number n and m find the Quotient and remainder

Input Description:<br>
Given two number separated by a space

Output Description:<br>
Need to print Quotient and remainder separated by a space

Sample Input:<br>
6 3

Sample Output:<br>
2 0

Explanation:<br>
6/3= 2(Quotient ) 6%3= 0(remainder)

Solution:
```python
n,m = map(int,input().split())
a= n //m
b= n % m
print(str(a) + " " + str(b))
```