### Question 1
### Print Factors of a Number
Question:<br>
Problem Statement:<br>
Given a number N, print its factors.

Input Description:<br>
Input Size : n<=1000

Sample Input:<br>
6

Sample Output:<br>
1 2 3 6

Solution:
```python
n = int(input().strip())

factors = [str(i) for i in range(1, n+1) if n % i == 0]

print(" ".join(factors))
```

### Question 2
### Arithmetic Series Sum
Question:<br>
Problem Statement:<br>
Given 3 numbers A,B,C find the sum of Arithmetic Series with a=A, d=B and n=C

Sample Input:<br>
1 1 2

Sample Output:<br>
3

Solution:
```python
def arithmetic_series_sum(a, d, n):
    return (n * (2 * a + (n - 1) * d)) // 2 

A, B, C = map(int, input().split())
print(arithmetic_series_sum(A, B, C))
```

### Question 3
### Find Minimum Among Ten Numbers
Question:<br>
Problem Statement:<br>
Find the minimum among 10 numbers.

Input Description:<br>
The input consists of 10 space-separated integers.

Output Description:<br>
The output is the minimum of the given 10 integers.

Sample Input:<br>
5 4 3 2 1 7 6 10 8 9

Sample Output:<br>
1

Solution:
```python
import math
a = input().split()

b= min(a)
print(b)
```

### Question 4
### Counting Digits of a Number
Question:<br>
Problem Statement:<br>
Count the number of digits of a given number N.Size of the integer ranges from 1<N<100000000

Sample Input:<br>
548

Sample Output:<br>
3

Solution:
```python
n = input()
print(len(n))
```

### Question 5
### Nearest Greater Multiple of 10
Question:<br>
Problem Statement:<br>
Given a number N, find the nearest greater multiple of 10.

Input Description:<br>
Input Size : N <= 10000

Sample Input:<br>
3

Sample Output:<br>
10

Solution:
```python
def nearest_greater_multiple_of_10(N):
    return ((N // 10) + 1) * 10

N = int(input().strip())
print(nearest_greater_multiple_of_10(N))
```

### Question 6
### Second Smallest Element
Question:<br>
Problem Statement:<br>
Given a number N followed by N elements, find the second smallest element.If it cannot be found then print -1

Input Description:<br>
Input Size : N <= 100000 (ie do it in O(log n) time complexity)

Sample Input:<br>
5
1 2 3 4 5

Sample Output:<br>
2

Solution:
```python
n = int(input())
arr = list(map(int,input().split()))
 
unique = sorted(set(arr))
 
if(len(unique) < 2):
    print(-1)
else:
    print(unique[1])
```

### Question 7
### Descending Elements Below N
Question:<br>
Problem Statement:<br>
Given a number N and an array of N elements, print all elements lesser than N in descending order. If no element found print -1.

Input Description:<br>
The input consists of a number N, and an array of N elements. N is between 1 and 10000 (inclusive).

Output Description:<br>
Print all elements from the array that are lesser than N, in descending order. If no such elements are found, print -1.

Sample Input:<br>
5<br>
2 14 15 14 3<br>

Sample Output:<br>
3 2

Solution:
```python
n = int(input())
arr = list(map(int, input().split()))

filtered = [x for x in arr if x < n]

if filtered:
    filtered.sort(reverse = True)
    print(' '.join(map(str, filtered)))
else:
    print(-1)
```

### Question 8
### Numbers Repeated K Times
Question:<br>
Problem Statement:<br>
Given 2 numbers N,K and an array of N elements, print the number(s) that has been repeated K times.Print them in ascending order if there are more than one number to be printed.If no element satisfies the pattern then print -1

Input Description:<br>
The input consists of two integers N and K, followed by an array of N elements. N and K are up to 100000.

Output Description:<br>
Print the numbers that have been repeated K times in ascending order. If no such element exists, print -1.

Sample Input:<br>
5 2<br>
1 2 4 1 2<br>

Sample Output:<br>
1 2

Solution:
```python
from collections import Counter

n, k = map(int, input().split())
arr = list(map(int, input().split()))

freq = Counter(arr)

result = sorted([num for num, count in freq.items() if count == k])
print(' '.join(map(str, result)) if result else -1)
```

### Question 9
### Factorial of a Number-2
Question:<br>
Problem Statement:<br>
Given a number N, find the factorial of N.

Input Description:<br>
The input consists of a single integer N, constrained by 1 <= N <= 25.

Output Description:<br>
The output is the calculated factorial of N.

Sample Input:<br>
5

Sample Output:<br>
120

Solution:
```python
n = int(input())
result = 1
for i in range(1, n+1):
    result *= i
print(result)
```

### Question 10
### Max of Consecutive Pairs
Question:<br>
Problem Statement:<br>
Given a number N followed by N elements for every 2 consecutive numbers print the maximum of the 2.

Input Description:<br>
The input consists of an integer N, followed by N elements. N is an integer such that N <= 100000, implying an O(n) time complexity solution is expected.

Output Description:<br>
The output is a space-separated sequence of the maximums of every two consecutive numbers from the input.

Sample Input:<br>
5<br>
1 1 3 0 5<br>

Sample Output:<br>
1 3 3 5

Solution:
```python
n = int(input())
arr = list(map(int, input().split()))

result = []
for i in range(n-1):
    result.append(max(arr[i] , arr[i + 1]))
    
print(*result)
```

### Question 11
### Rotated Array Rotation Count
Question:<br>
Problem Statement:<br>
Given an value 'M' follwed by array of M elements in which the elements would have been rotated for certain 'N' times from the intial array representation where all elements are arranged in ascending order.Print the 'N' or print -1 if there is no rotation made or cannot be determined.Note: 1<=N<=length of the given array.

Sample Input:<br>
5<br>
15 18 2 3 6 12

Sample Output:<br>
2

Solution:
```python
def find_rotation_count(arr):
    n = len(arr)
    
    # Find index of minimum element
    min_index = arr.index(min(arr))
    
    # If no rotation (min at 0 and array sorted), return -1
    if min_index == 0 and arr == sorted(arr):
        return -1
    
    # Otherwise return index of min element (rotation count)
    return min_index


# Driver
M = int(input().strip())
arr = list(map(int, input().split()))

print(find_rotation_count(arr))
```

### Question 12
### Max Difference in Array
Question:<br>
Problem Statement:<br>
Given an array, find the maximum difference between any two elements.

Input Description:<br>
Input Size : N <= 1000000(complexity O(n) or O(nlogn))

Sample Input:<br>
5<br>
1 2 3 4 5

Sample Output:<br>
4

Solution:
```python
def max_diff(arr):
    return max(arr) - min(arr)
    
n = int(input())
arr = list(map(int, input().split()))
print(max_diff(arr))
```

### Question 13
### Minimum Difference in Array
Question:<br>
Problem Statement:<br>
Given an array, find the absolute minimum difference between any two elements in the array.

Input Description:<br>
Input Size : N <= 1000000(complexity O(n) or O(nlogn))

Sample Input:<br>
5<br>
0 2 3 4 5

Sample Output:<br>
1

Solution:
```python
# Read input
n = int(input())
arr = list(map(int, input().split()))

# Sort the array
arr.sort()

# Initialize minimum difference with a large value
min_diff = float('inf')

# Compare adjacent elements
for i in range(1, n):
    diff = abs(arr[i] - arr[i - 1])
    if diff < min_diff:
        min_diff = diff

print(min_diff)
```

### Question 14
### Reverse a String-2
Question:<br>
Problem Statement:<br>
Given a string S, print the reverse of the string.

Input Description:<br>
Input Size : |s| <= 100000 (ie do it in O(n) or O(log n) time complexity)

Sample Input:<br>
codekata

Sample Output:<br>
atakedoc

Solution:
```python
s = input()
print(s[::-1])
```

### Question 15
### Reverse Words Except Ends
Question:<br>
Problem Statement:<br>
Given a string S consisting of a sentence, the task is to reverse every word of the sentence except the first and last character of the words.

Input Description:<br>
The input consists of a string S representing a sentence.

Output Description:<br>
The output is the modified string with every word reversed except its first and last characters.

Sample Input:<br>
guvi coding platform

Sample Output:<br>
gvui cnidog proftalm.

Solution:
```python
def rev_middle(sentence):
    words = sentence.split()
    result =[]
    
    for word in words:
        if len(word) <= 2:
            result.append(word)
        else:
            middle = word[1:-1][::-1]
            result.append(word[0] + middle + word[-1])
            
    return " ".join(result)
       
sentence= input()
print(rev_middle(sentence))
```

### Question 16
### Swap Odd Even String Characters
Question:<br>
Problem Statement:<br>
Given a string 'S' swap the even and odd characters starting from index 1(Assume the index starts from 0).

Input Description:<br>
Input Size : |s| <= 10000000(complexity O(n))

Sample Input:<br>
codekata

Sample Output:<br>
ocedakat

Solution:
```python
s = input()
s = list(s)

for i in range(0,len(s)-1, 2):
    s[i], s[i+1] = s[i+1], s[i]
    
print(''.join(s))
```

### Question 17
### CamelCase Conversion
Question:<br>
Problem Statement:<br>
Given a string/sentence print its corresponding camelcase convention.

Input Description:<br>
Input Size : |s| <= 1000000(complexity O(n))

Sample Input:<br>
guvi geeks

Sample Output:<br>
GuviGeeks

Solution:
```python
def camelcase(s):
    words = s.split()
    return "".join(word.capitalize() for word in words)

s = input()
print(camelcase(s))
```

### Question 18
### Sum of Squares of Digits
Question:<br>
Problem Statement:<br>
Given a number N, print the sum of the squares of its digits.

Input Description:<br>
The input consists of a number N, where 1 <= N <= 1000000000000000000.

Output Description:<br>
The output is the sum of the squares of the digits of N.

Sample Input:<br>
19

Sample Output:<br>
82

Solution:
```python
def sum_of_squares(n):
    return sum(int(digit) ** 2 for digit in str(n))

n = int(input())
print(sum_of_squares(n))
```

### Question 19
### Reverse String After Removing Vowels
Question:<br>
Problem Statement:<br>
Given a string S, print the reverse of the string after removing the vowels.If the resulting string is empty print '-1'.

Input Description:<br>
Input Size : 1 <= N <= 100000

Sample Input:<br>
codekata

Sample Output:<br>
tkdc

Solution:
```python
s = input()
vowels = "aeiou"
result =''

for ch in s:
    if ch not in vowels:
        result += ch

print(result[::-1] if result else -1)
```

### Question 20
### Max Repeated Character Count
Question:<br>
Problem Statement:<br>
Given a string S,count the maximum number of times a character repeated in the string.If no character is repeated print '0'.

Input Description:<br>
Input Size : 1 <= N <= 100000

Sample Input:<br>
codekata

Sample Output:<br>
2

Solution:
```python
from collections import Counter

def max_char_repeats(s):
    freq = Counter(s)
    max_freq = max(freq.values())
    return max_freq if max_freq > 1 else 0

s = input().strip()
print(max_char_repeats(s))
```