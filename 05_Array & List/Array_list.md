### Question 1
### Number Existence Check
Question:<br>
Problem Statement:<br>
Given 2 numbers N and K followed by elements of N .Print 'yes' if K exists else print 'no'.

Input Description:<br>
The input consists of two integers, N and K, followed by N integers.

Output Description:<br>
The output is 'yes' if K is found among the N integers, otherwise 'no'.

Sample Input:<br>
4 2<br>
1 2 3 3<br>

Sample Output:<br>
yes<br>

Solution:
```python
a, b = map(int, input().split())
elements = list(map(int, input().split()))

if b in elements:
    print('yes')
else:
    print('no')
```

### Question 2
### Delete Last K Array Elements
Question:<br>
Problem Statement:<br>
Given 2 numbers N,K print the array after deleting the last K elements.

Input Description:<br>
N,K <= 100000

Output Description:<br>
The array after deleting the last K elements.

Sample Input:<br>
5 4<br>
1 2 3 4 5<br>

Sample Output:<br>
1

Solution:
```python
n,k = map(int, input().split())
arr = list(map(int, input().split()))

result = arr[:n-k]

if result:
    print(*result)
```

### Question 3
### Find K in an Array
Question:<br>
Problem Statement:<br>
Given 2 numbers N,K and an array of N integers, find if the element K exists in the array.

Input Description:<br>
Input Size : N <= 100000

Output Description:<br>
The output is 'yes' if the element K exists in the array, otherwise 'no'.

Sample Input:<br>
5 2<br>
1 2 3 4 5<br>

Sample Output:<br>
yes

Solution:
```python
import bisect
def finduniq(arr, k):
    index = bisect.bisect_left(arr, k)
    if index < len(arr) and arr[index] == k:
        return 'yes'
    return 'no'

n,k = map(int, input().split())
arr = list(map(int, input().split()))
arr.sort()
print(finduniq(arr, k))
```

### Question 4
### Mirror Image Arrays
Question:<br>
Problem Statement:<br>
Given 2 arrays print 'yes' if they are mirror images of each other,otherwise 'no'.

Input Description:<br>
Input Size : N <= 1000000

Sample Input:<br>
4<br>
1 2 3 4<br>
4 3 2 1<br>

Sample Output:<br>
yes

Solution:
```python
n = int(input())
arr1 = list(map(int,input().split()))
arr2 = list(map(int,input().split()))
print("yes" if arr1 == arr2[::-1] else "no")
```

### Question 5
### Index Difference of Min and Max
Question:<br>
Problem Statement:<br>
Given a number N and array of N integers, print the difference between the indices of smallest and largest number(if there are multiple occurances, consider the first occurance).

Input Description:<br>
Input Size : |N| <= 1000000

Sample Input:<br>
5<br>
3 5 4 4 7

Sample Output:<br>
4

Solution:
```python
n= int(input())
arr = list(map(int, input().split()))

min_index = arr.index(min(arr))
max_index= arr.index(max(arr))

print(abs(max_index - min_index))
```

### Question 6
### Reverse a List of Numbers
Question:<br>
Problem Statement:<br>
Given a number N followed by a list of N numbers. Write a program to reverse the list and print the list.

Input Description:<br>
1 <= N <= 10000

Output Description:<br>
The reversed list, with elements separated by '->'.

Sample Input:<br>
7<br>
1 2 3 4 5 6 7

Sample Output:<br>
7->6->5->4->3->2->1

Solution:
```python
n = int(input())
arr = list(map(str, input().split()))
result = arr[::-1]
print("->".join(result))
```

### Question 7
### Find Min and Max Indices
Question:<br>
Problem Statement:<br>
Given a number N followed by N numbers.Find the smallest number and largest number and print both the indices(1 based indexing).

Input Description:<br>
Input Size : N <= 100000

Sample Input:<br>
5<br>
1 2 3 4 5

Sample Output:<br>
1 5

Solution:
```python
n = int(input())
arr = list(map(int, input().split()))

# Initialize with first element
min_val = arr[0]
max_val = arr[0]
min_index = 1  # 1-based index
max_index = 1

# Traverse the array
for i in range(1, n):
    if arr[i] < min_val:
        min_val = arr[i]
        min_index = i + 1  # convert to 1-based index
    elif arr[i] > max_val:
        max_val = arr[i]
        max_index = i + 1

# Output
print(min_index, max_index)
```

### Question 8
### Merge and Sort Two Arrays-2
Question:<br>
Problem Statement:<br>
You are given with two arrays. Your task is to merge the array such that first array is in ascending order and second one in descending order.

Input Description:<br>
First line contains two integer ‘n’ and ‘m’. ‘n’ denotes length of array 1 and ‘m’ of array 2.Next line contains n space separated numbers and third line contains ‘m’ space separated numbers

Output Description:<br>
Print a single array in desired order

Sample Input:<br>
3 3<br>
23 15 16<br>
357 65 10<br>

Sample Output:<br>
15 16 23 357 65 10

Explanation:<br>
15 16 23 is ascending order and 357 65 10 in descending order

Hence the answer is<br>
15 16 23 357 65 10

Solution:
```python
def merge_arrays(arr1,arr2):
    arr1.sort()
    arr2.sort(reverse=True)
    return ' '.join(map(str, arr1 + arr2))

n,m = map(int,input().split())
arr1 = list(map(int, input().split()))
arr2 = list(map(int, input().split()))
print(merge_arrays(arr1,arr2))
```

### Question 9
### Beautiful Array Check
Question:<br>
Problem Statement:<br>
you are given with array of numbers.you have to find whether array is beautiful or not. A beautiful array is an array whose sum of all numbers is divisible by 2, 3 and 5

Input Description:<br>
You are given a number ‘n’ denoting the size of array.Next line contains n space separated numbers.

Output Description:<br>
Print 1 if array is beautiful and 0 if it is not

Explanation:<br>
Sum is 90 which is divisible by 2,3,5

Sample Input:<br>
5<br>
5 25 35 -5 30

Sample Output:<br>
1

Solution:
```python
def divby(a,b):
    data = sum(b)
    if data % 2 ==0 and data % 3 == 0 and data % 5 ==0:
        return 1
    else:
        return 0

a = int(input())
b= list(map(int, input().split()))
print(divby(a, b))
```

### Question 10
### Majestic Array Check
Question:<br>
Problem Statement:<br>
You are given given task is to print whether array is 'majestic' or not.A 'majsetic' array is an array whose sum of first three number is equal to last three number.

Input Description:<br>
You are given a number 'n',Next line contains 'n' space separated

Output Description:<br>
Print 1 if array is majestic and 0 if it is not

Sample Input:<br>
7<br>
1 2 3 4 6 0 0

Sample Output:<br>
1

Solution:
```python
def majestic(n,arr):
    if n < 6:
        return 0
    return 1 if sum(arr[:3]) == sum(arr[-3:]) else 0

n = int(input())
arr = list(map(int,input().split()))
print(majestic(n,arr))
```

### Question 11
### Least Frequent Number
Question:<br>
Problem Statement:<br>
Given a number N and array of N integers, find the number which occurs the least number of times.

Input Description:<br>
Input Size : |N| <= 1000000

Sample Input:<br>
5<br>
3 3 4 4 7

Sample Output:<br>
7

Solution:
```python
from collections import Counter

N = int(input())
arr = list(map(int, input().split()))

# Count frequency of each element
freq = Counter(arr)

# Find the element with the smallest frequency
least_num = min(freq, key=freq.get)

print(least_num)

```

### Question 12
### Find Repeated Numbers
Question:<br>
Problem Statement:<br>
Given a number N followed by N numbers. Out of these N numbers some of them are repeated. Write a program to find the number which is repeated and print the repeated numbers in sorted order. If no numbers are repeated print "unique".

Input Description:<br>
Input Size : 1 <= N <= 100000

Sample Input:<br>
7<br>
1 2 3 2 3 4 3

Sample Output:<br>
2 3

Solution:
```python
from collections import Counter

n = int(input())
arr = list(map(int,input().split()))

counter = Counter(arr)
repeated_numbers = sorted([num for num,count in counter.items() if count > 1])
if repeated_numbers:
    print(*repeated_numbers)
else:
    print('unique')
```

### Question 13
### Find the Missing Number
Question:<br>
Problem Statement:<br>
You are given a number n,ranging from 1 to n. Out of which one number is missing. Your task is to print that missing number.<br>
Input Description:<br>
You are given a number ‘n’.

Output Description:<br>
Print the missing number.

Sample Input:<br>
5<br>
1 3 5 2

Sample Output:<br>
4

Solution:
```python
def find_missing(n,numbers):
    excpected_sum = n * (n + 1) // 2
    actual_sum = sum(numbers)
    return excpected_sum - actual_sum
    
n = int(input())
numbers = map(int, input().split())
print(find_missing(n, numbers))
```

### Question 14
### Find the Twice Repeated Number
Question:<br>
Problem Statement:<br>
You are provided with an array in which all elements are repeated thrice except one which is repeated twice.Your task is to print that number.O(n) time and O(1) extra space

Input Description:<br>
First line contains a number denoting size of array ‘n’.Next line contains n space separated numbers

Output Description:<br>
Print the number which is repeated twice

Sample Input:<br>
5<br>
13 12 13 12 13

Sample Output:<br>
12

Solution:
```python
from collections import Counter
def twicerep(a,b):
    x = Counter(b)

    for num,value in x.items():
        if value == 2:
            return num
            break
        
a= int(input())
b= list(map(int,input().split()))
print(twicerep(a,b))
```