### Question 1
### Bitwise AND of Array Elements
Question:<br>
Problem Statement:<br>
Given a number N and an array of N elements ,find the Bitwise AND of the array elements.

Input Description:<br>
The input consists of an integer N, representing the size of the array, followed by N array elements. N <= 100000.

Output Description:<br>
The output is the Bitwise AND of all elements in the array.

Sample Input:<br>
4<br>
4 3 2 1<br>

Sample Output:<br>
0

Solution:
```python
n = int(input())
arr = list(map(int, input().split()))
result = arr[0]

for i in range(1, n):
    result &= arr[i]
    
print(result)
```

### Question 2
### Bitwise OR of Array Elements
Question:<br>
Problem Statement:<br>
Given a number N and an array of N elements, find the Bitwise OR of the array elements.

Output Description:<br>
The output is the Bitwise OR of the array elements.

Sample Input:<br>
2<br>
2 4<br>

Sample Output:<br>
6

Solution:
```python
n = int(input())
arr = list(map(int, input().split()))

result = 0

for num in arr:
    result |= num
    
print(result)
```

### Question 3
### Max Bitwise OR of Segments
Question:<br>
Problem Statement:<br>
Given a number N and an array of N integers, find the maximum of Bitwise OR of all segments.

Sample Input:<br>
2<br>
2 4<br>

Sample Output:<br>
6

Solution:
```python
N = int(input())
arr = list(map(int, input().split()))

# Compute bitwise OR of all elements
result = 0
for num in arr:
    result |= num   

print(result)

```

### Question 4
### Bitwise NOT of a Number
Question:<br>
Problem Statement:<br>
Given a number N, print the Bitwise NOT of that number.

Sample Input:<br>
5

Sample Output:<br>
-6

Solution:
```python
N = int(input())

print(~N)
```

### Question 5
### Bitwise Right Shift
Question:<br>
Problem Statement:<br>
Given 2 numbers N and K print the number after performing bitwise right shift 'K' times(upto 2 decimal places).

Input Description:<br>
The input consists of two numbers, N and K, where 1 <= N, K <= 1000.

Output Description:<br>
The output is the number N after performing a bitwise right shift K times, rounded to 2 decimal places.

Sample Input:<br>
5 2

Sample Output:<br>
1

Solution:
```python
N, K = map(int, input().split())

# Perform bitwise right shift
result = N >> K

# Print with up to 2 decimal places
print(f"{result:.2f}".rstrip('0').rstrip('.') if '.' in f"{result:.2f}" else result)
```

### Question 6
### Count Set Bits in Binary
Question:<br>
Problem Statement:<br>
Given a number N, find the number of ones in its binary representation.

Sample Input:<br>
276

Sample Output:<br>
3

Solution:
```python
n = int(input())
binary = bin(n)
count = binary.count('1')
print(count)
```

### Question 7
### First 1's Position in Binary Product
Question:<br>
Problem Statement:<br>
Print the position of first 1 from left to right, in binary representation of product of 2 integers after the first one.

Sample Input:<br>
18 2

Sample Output:<br>
4

Solution:
```python
a,b = map(int,input().split())
p = a * b
binary_p = bin(p)[2:]
first = binary_p.find('1',1)
print(first + 1)
```