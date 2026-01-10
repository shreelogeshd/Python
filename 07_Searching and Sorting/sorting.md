### Question 1
### Find Position of Number in Array
Question:<br>
Problem Statement:<br>
Given a number N,K followed by array of N elements where the difference between any adjacent elements is 1. Find the position of the given number K.If K not found in the array print -1

Input Description:<br>
The input consists of two integers N and K, followed by an array of N elements where the difference between any adjacent elements is 1.

Output Description:<br>
The output is the position of the given number K. If K is not found in the array, print -1.

Sample Input:<br>
5 1<br>
3 2 1 2 3

Sample Output:<br>
3

Solution:
```python
n,k = map(int, input().split())
arr = list(map(int, input().split()))

if k in arr:
    print(arr.index(k) + 1)
else:
    print(-1)
```

### Question 2
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
1 2 4 1 2

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

### Question 3
### Remove Duplicates from Array
Question:<br>
Problem Statement:<br>
Given a number N and an array of N elements, print the array after removing duplicate elements.If no duplicate elements found print the same.

Sample Input:<br>
4<br>
2 4 4 2

Sample Output:<br>
2 4

Solution:
```python
N = int(input())
arr = list(map(int, input().split()))

unique = []
for num in arr:
    if num not in unique:
        unique.append(num)

print(*unique)
```

### Question 4
### Hybrid Sort of an Array
Question:<br>
Problem Statement:<br>
Given an array N, sort it in ascending order till it reaches kth elements and after that sort it in descending order.

Input Description:<br>
The input consists of two integers N and K on the first line, followed by N integers representing the array elements on the second line. N <= 100000.

Output Description:<br>
The output should be the modified array after applying the specified sorting logic.

Sample Input:<br>
5 2<br>
4 3 1 2 4

Sample Output:<br>
3 4 4 2 1

Solution:
```python
n,m = map(int,input().split())
arr = list(map(int,input().split()))

first = sorted(arr[:m])
second = sorted(arr[m:], reverse=True)
result = first + second
print(*result)
```

### Question 5
### Lexicographical Sorting of Strings
Question:<br>
Problem Statement:<br>
Ria is a 5 year old girl. Her mother wants to teach her how to sort words in the same order that they appear in a dictionary. She decides to write a program to sort a given set of strings based on their alphabetical order. Help Ria's mother to complete the program.

Input Description:<br>
A set of N strings

Output Description:<br>
Alphabetically sorted set of strings

Sample Input:<br>
3<br>
InfinityWar EndGame Avengers

Sample Output:<br>
Avengers EndGame InfinityWar

Solution:
```python
n = int(input())
words = input().split()

for i in range(n):
    for j in range(i + 1, n):
        if words[i] > words[j]:
            words[i], words[j] = words[j], words[i]

print(' '.join(words))
```