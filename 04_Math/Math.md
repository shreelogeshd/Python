### Question 1
### Next Greater Power of 2
Question:<br>
Given a number N, find its next immediate greater power of 2(i.e 2^1, 2^2, 2^3...).

Input Description:<br>
The input consists of a number N where N <= 1000.

Sample Input:<br>
4

Sample Output:<br>
8

Solution:
```python
import math

n = int(input())
power = 1
while power <= n:
    power *= 2
    
print(power)
```

### Question 2
### Perfect Square Product
Question:<br>
Problem Statement:<br>
Given 2 numbers N,M. Print 'yes' if their product is a perfect square else print 'no'.

Sample Input:<br>
5 5

Sample Output:<br>
yes

Solution:
```python
import math

n = input().split(" ")
product = int(n[0]) * int(n[1])

if (math.sqrt(product) ** 2 == product):
    print('yes')
else:
    print('no')
```

### Question 3
### Product of Digits
Question:<br>
Problem Statement:<br>
Given a number N, print the product of the digits.

Input Description:<br>
Input Size : N <= 100000000000

Sample Input:<br>
2143

Sample Output:<br>
24

Solution:
```python
n = input().strip()

product = 1
for i in n:
    product *= int(i)

print(product)
```

### Question 4
### Greatest Common Divisor-2
Question:<br>
Problem Statement:<br>
Given a number N and a number K, find the greatest number which divides both.

Input Description:<br>
N and K <= 100000

Sample Input:<br>
5 10

Sample Output:<br>
5

Solution:
```python
import math
n, k = map(int, input().split())
print(math.gcd(n, k))
```

### Question 5
### Smallest Divisible Number
Question:<br>
Problem Statement:<br>
Given a number N and an array of N integers, find the smallest number divisible by all the elements of the array.

Input Description:<br>
Input Size : N <= 100000

Output Description:<br>
The smallest number divisible by all the elements of the array.

Sample Input:<br>
5<br>
1 2 3 4 5<br>

Sample Output:<br>
60

Solution:
```python
import math

N = int(input())
arr = list(map(int, input().split()))

# Function to compute LCM of two numbers
def lcm(a, b):
    return a * b // math.gcd(a, b)

# Compute LCM of all array elements
result = arr[0]
for i in range(1, N):
    result = lcm(result, arr[i])

print(result)
```

### Question 6
### Factorial Ratio
Question:<br>
Problem Statement:<br>
Given 2 numbers a and B.Print the value of a!/b!.

Input Description:<br>
A,B <= 10000 and A-B <= 5

Output Description:<br>
The value of a!/b!.

Sample Input:<br>
4 2

Sample Output:<br>
12

Solution:
```python
a, b = map(int, input().split())

# Compute a! / b!
res = 1
for i in range(b + 1, a + 1):
    res *= i

print(res)
```

### Question 7
### Solve Linear Equation
Question:<br>
Problem Statement:<br>
Given the values of a,b and x in the equation ax + b = y. Find the value of y.

Input Description:<br>
The input consists of three space-separated integers a, b, and x.

Output Description:<br>
The output is a single integer representing the value of y.

Sample Input:<br>
3 5 2

Sample Output:<br>
11

Solution:
```python
a, b,x = map(int, input().split())
print((a * x) + b)
```

### Question 8
### Compute A^B
Question:<br>
Problem Statement:<br>
Given numbers A,B find A^B.

Input Description:<br>
Input Size : 1 <= A <= 5 <= B <= 50

Sample Input:<br>
3 4

Sample Output:<br>
81

Solution:
```python
a, b = map(int, input().split())
result = 1

for _ in range(b):
    result *= a
print(result)
```

### Question 9
### Triangle Area Calculation
Question:<br>
Problem Statement:<br>
Given base(B) and height(H) of a triangle find its area.

Input Description:<br>
The input consists of the base (B) and height (H) of a triangle. The input size N is up to 1000000.

Sample Input:<br>
2 4

Sample Output:<br>
4

Solution:
```python
B, H = map(int, input().split())

area = (B * H) / 2 
print(area)
```

### Question 10
### Rectangle Area Calculation
Question:<br>
Problem Statement:<br>
You are given A = Length of a rectangle & B = breadth of a rectangle. Find its area “C”. (A and B are natural numbers)

Input Description:<br>
The inputs are two natural numbers representing the length and the breadth of a rectangle.

Output Description:<br>
Find the area of the rectangle formed by the provided input. Round off the answer to the first decimal place if required.

Explanation:<br>
Area = LB = AB = 2*3 = 6

Sample Input:<br>
2<br>
3<br>

Sample Output:<br>
6

Solution:
```python
a = int(input())
b = int(input())
    
area = a * b
print(area)
```

### Question 11
### Kilometer to Meter and Centimeter
Question:<br>
Problem Statement:<br>
You are given a number A in Kilometers. Convert this into B: Meters and C: Centi-Metres.

Input Description:<br>
A number "A" representing some distance in kilometer is provided to you as the input.

Output Description:<br>
Convert and print this value in meters and centimeters.

Explanation:<br>
1 KM = 1000 M<br>
1M = 100 CM<br>
1KM = 1000*100 CM = 100000 CM<br>

Sample Input:<br>
2

Sample Output:<br>
2000200000

Solution:
```python
a = int(input())
b= (a * 1000)
c = (a * 100000)
print(b)
print(c)
```

### Question 12
### Equilateral Triangle Area
Question:<br>
Problem Statement:<br>
The area of an equilateral triangle is ¼(√3a²) where "a" represents a side of the triangle. You are provided with the side "a". Find the area of the equilateral triangle.

Input Description:<br>
The side of an equilateral triangle is provided as the input.

Output Description:<br>
Find the area of the equilateral triangle and print the answer up to 2 decimal places after rounding off.

Explanation:<br>
Area of Triangle = ½ × base × height

⇒ Area = ½ × a × ½(√3a)<br>
when a = 20<br>
Area = 173.21<br>

Sample Input:<br>
20

Sample Output:<br>
173.21

Solution:
```python
import math

a = float(input().strip())
area = (math.sqrt(3) / 4) * (a ** 2)
print(f"{area:.2f}")
```

### Question 13
### Largest of Three Numbers
Question:<br>
Problem Statement:<br>
You are given three numbers A, B & C. Print the largest amongst these three numbers.

Input Description:<br>
Three numbers are provided to you.

Output Description:<br>
Find and print the largest among the three

Sample Input:<br>
1<br>
2<br>
3

Sample Output:<br>
3

Solution:
```python
a = int(input())
b = int(input())
c = int(input())

if a > b and a > c:
    print(a)
elif b >a and b > c:
    print(b)
else:
    print(c)
```

### Question 14
### Square Root of Perfect Square
Question:<br>
Problem Statement:<br>
Given number n print the square root of the number n note n is a perfect square number

Input Description:<br>
You will given a number n 0<n<=100

Output Description:<br>
print the square root of the number n

Sample Input:<br>
16

Sample Output:<br>
4

Solution:
```python
import math
n = int(input())
print(int(math.sqrt(n)))
```

