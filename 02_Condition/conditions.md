

### Question 1
### Odd or Even Sum
Question:<br>
Problem Statement:<br>
Given 2 numbers N and M add both the numbers and check whether the sum is odd or even.

Input Description:<br>
The input consists of two integers, N and M.

Output Description:<br>
The output is 'odd' if the sum of N and M is odd, and 'even' if the sum is even.

Sample Input:<br>
9 2

Sample Output:<br>
odd

Solution:
```python
n,m = map(int, input().split())
print("even" if((n + m) % 2 == 0) else "odd")
```

### Question 2
### Prime Number Check
Question:<br>
Problem Statement:<br>
Given a number N, check whether it is prime or not. Print 'yes' if it is prime else print 'no'.

Input Description:<br>
The input consists of a single integer N.

Output Description:<br>
The output is 'yes' if N is prime, otherwise 'no'.

Sample Input:<br>
123

Sample Output:<br>
no

Solution:
```python
import math

n = int(input().strip())

if n <= 1:
    print('no')
else:
    is_prime=True
    for i in range(2, int(math.sqrt(n)) +1):
        if n % i == 0:
            is_prime = False
            
    print('yes' if is_prime else 'no')
```

### Question 3
### Check Divisibility by 7
Question:<br>
Problem Statement:<br>
Given a number N, print yes if the number is a multiple of 7 else print no.

Input Description:<br>
The input consists of a single integer N.

Output Description:<br>
Print 'yes' if N is a multiple of 7, otherwise print 'no'.

Sample Input:<br>
49

Sample Output:<br>
yes

Solution:
```python
N = int(input())
print('yes' if N % 7 == 0 else 'no') 
```

### Question 4
### Palindrome Check
Question:<br>
Problem Statement:<br>
Given a string S, print 'yes' if it is a palindrome or 'no' if it is not a palindrome.

Sample Input:<br>
lappal

Sample Output:<br>
yes

Solution:
```python
s = input()
n = 0

# Calculate length without using len()
for _ in s:
    n += 1

is_palindrome = True
for i in range(n // 2):
    if s[i] != s[n - 1 - i]:
        is_palindrome = False
        break

if is_palindrome:
    print("yes")
else:
    print("no")
```

### Question 5
### Number Range Check
Question:<br>
Given 3 numbers N , L and R. Print 'yes' if N is between L and R else print 'no'.

Sample Input:<br>
3<br>
2 6

Sample Output:<br>
yes

Solution:
```python
a = input()
b = input().split(' ')

if b[0] < a and a < b[1]:
    print('yes')
else:
    print('no')
```

### Question 6
### Check if Number is Composite
Question:<br>
Problem Statement:<br>
Given a number N, print 'yes' if it is composite else print 'no'.

Sample Input:<br>
123

Sample Output:<br>
yes

Solution:
```python
n = int(input())

def is_composite(num):
    if num <= 3:
        return False
    for i in range(2,num):
        if num % i == 0:
            return True
    return False
   
print('yes' if is_composite(n) else 'no')
```

### Question 7
### Check Divisibility by 13
Question:<br>
Problem Statement:<br>
Given a number N, print 'yes' if it is a multiple of 13 else print 'no'.

Sample Input:<br>
26

Sample Output:<br>
yes

Solution:
```python
n = int(input())
print('yes' if n % 13 == 0  else 'no')
```

### Question 8
### Odd Digits in a Number
Question:<br>
Problem Statement:<br>
Given a number N, print the odd digits in the number(space seperated) or print -1 if there is no odd digit in the given number.

Input Description:<br>
The input consists of a single integer N, where N <= 100000.

Output Description:<br>
The output should be the odd digits of N, space-separated, or -1 if no odd digits are present.

Sample Input:<br>
2143

Sample Output:<br>
1 3

Solution:
```python
n = input().strip()
result = []

for i in n:
    if int(i) % 2 != 0:
        result += i
        
print(' '.join(result) if result else -1)
```

### Question 9
### Odd Even String Split
Question:<br>
Problem Statement:<br>
Given a string S, print 2 strings such that first string containing all characters in odd position(s) and other containing all characters in even position(s).

Sample Input:<br>
XCODE

Sample Output:<br>
XOE CD

Solution:
```python
s = input()
odd_char= ''
even_char = ''

for i in range(len(s)):
    if((i +1)% 2 == 1):
        odd_char += s[i]
    else:
        even_char += s[i]

print(odd_char,even_char)
```

### Question 10
### Reverse a Number
Question:<br>
Problem Statement:<br>
Given a number N, print its reverse.

Input Description:<br>
Input Size : n <= 1000

Sample Input:<br>
10

Sample Output:<br>
1

Solution:
```python
n = input()
print(n[::-1].lstrip('0'))
```

### Question 11
### Even Odd Difference
Question:<br>
Problem Statement:<br>
Given 2 numbers N,M. Find their difference and check whether it is even or odd.

Sample Input:<br>
5 5

Sample Output:<br>
even

Solution:
```python
n,m = map(int,input().split())
diff = abs(n - m)
print('even' if diff % 2 == 0 else 'odd')
```

### Question 12
### Sum of First K Natural Numbers
Question:<br>
Problem Statement:<br>
Write a program to print the sum of the first K natural numbers.

Input Description:<br>
Input Size : n <= 100000

Sample Input:<br>
3

Sample Output:<br>
6

Solution:
```python
k = int(input())

#use formula to find k natural numbers
sum_k = (k * (k + 1))// 2
print(sum_k)
```

### Question 13
### Prime Count in a Range
Question:<br>
Problem Statement:<br>
Given a range of 2 numbers (i.e) L and R count the number of prime numbers in the range (inclusive of L and R ).

Input Description:<br>
Input Size : L <= R <= 100000(complexity O(n) read about Sieve of Eratosthenes)

Sample Input:<br>
2 5

Sample Output:<br>
3

Solution:
```python
def is_prime(num):
    """Check if a number is prime."""
    if num < 2:
        return False
    for i in range(2, int(num ** 0.5) + 1):
        if num % i == 0:
            return False
    return True

n,m = map(int,input().split())
count = 0
for i in range(n,m + 1):
    if is_prime(i):
        count +=1

print(count)
```

### Question 14
### One Character Difference
Question:<br>
Problem Statement:<br>
Given 2 strings check whether they differ exacly by one character.If yes then print 'yes' otherwise print 'no'

Input Description:<br>
Input Size : |s| <= 100000(complexity O(nlogn) or O(n))

Sample Input:<br>
codekata codekate

Sample Output:<br>
yes

Solution:
```python
def differ_by_one(s1, s2):
    if len(s1) != len(s2):
        return "no"
    
    diff_count = 0
    for a, b in zip(s1, s2):
        if a != b:
            diff_count += 1
            if diff_count > 1:
                return "no"
    
    return "yes" if diff_count == 1 else "no"

# Driver
s1, s2 = input().split()
print(differ_by_one(s1, s2))
```

### Question 15
### Holiday Check
Question:<br>
Problem Statement:<br>
Given a day, print 'yes' if it is a holiday otherwise print'no'.Assume that weekend days are holidays

Sample Input:<br>
saturday<br>
monday

Sample Output:<br>
yes<br>
no

Solution:
```python
day = input().lower()
weekend = {"saturday", "sunday"}
print('yes' if day in weekend else 'no')
```

### Question 16
### Power of Two Check-2
Question:<br>
Problem Statement:<br>
Given a number N, check if it is a power of 2.

Input Description:<br>
The input consists of a number N, where 1 <= N <= 100000.

Output Description:<br>
Print 'yes' if N is a power of 2, otherwise print 'no'.

Sample Input:<br>
64

Sample Output:<br>
yes

Solution:
```python
N = int(input())

# Check if N is a power of 2
if N > 0 and (N & (N - 1)) == 0:
    print("yes")
else:
    print("no")
```

### Question 17
### Power of a Number
Question:<br>
Problem Statement:<br>
Given 2 numbers N and K.check if N is a power of K.Print 'yes' if it is a power of k otherwise print 'no'.

Sample Input:<br>
64 8

Sample Output:<br>
yes

Solution:
```python
n, k = map(int, input().split())

# Edge case: if k == 1
if k == 1:
    print("yes" if n == 1 else "no")
else:
    while n % k == 0:
        n = n // k

    if n == 1:
        print("yes")
    else:
        print("no")
```

### Question 18
### Divisibility Check of a Number
Question:<br>
Problem Statement:<br>
Given a number N, check if N is divisible by any number less than N (ie.,it leaves no remainder)except 1.

Input Description:<br>
Input Size : 1 <= N <= 100000

Sample Input:<br>
10

Sample Output:<br>
yes

Solution:
```python
N = int(input())
divisible = False

for i in range(2, N):
    if N % i == 0:
        divisible = True
        break

if divisible:
    print("yes")
else:
    print("no")
```

### Question 19
### Power of Two Check
Question:<br>
Problem Statement:<br>
Given a number N, check whether it is a power of 2.

Sample Input:<br>
2048

Sample Output:<br>
yes

Solution:
```python
N = int(input())

# Check if N is a power of 2
if N > 0 and (N & (N - 1)) == 0:
    print("yes")
else:
    print("no")
```

### Question 20
### Odd or Even Checker
Question:<br>
Problem Statement:<br>
You are provided with a number check whether its odd or even.
Print "Odd" or "Even" for the corresponding cases.
Note: In case of a decimal, Round off to nearest integer and then find the output. Incase the input is zero, print "Zero".

Input Description:<br>
A number is provided as the input.

Output Description:<br>
Find out whether the number is odd or even.
Print "Odd" or "Even" for the corresponding cases.
Note: In case of a decimal, Round off to nearest integer and then find the output. In case the input is zero, print "Zero".

Explanation:<br>
2%2 = 0.<br>
2 is an even number.<br>

Sample Input:<br>
2

Sample Output:<br>
Even

Solution:
```python
a = int(input())

if a == 0:
    print('Zero')
elif a % 2 == 0:
    print('Even')
else:
    print('Odd')
```