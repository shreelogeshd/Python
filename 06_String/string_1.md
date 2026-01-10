### Question 1
### Vowel Check in String
Question:<br>
Given a string S, print 'yes' if it has a vowel in it else print 'no'.

Sample Input:<br>
codekata

Sample Output:<br>
yes

Solution:
```python
def checkvowels(a):
    vowels={'a', 'e', 'i', 'o', 'u', 'A', 'E', 'I', 'O', 'U'}
    return "yes" if any(c in vowels for c in a) else 'no'
a= input()
print(checkvowels(a))
```

### Question 2
### String Middle Element Modification
Question:<br>
Given a string S, print it after changing the middle element to * (if the length of the string is even, change the 2 middle elements to *).

Sample Input:<br>
hello

Sample Output:<br>
he*lo

Solution:
```python
s = input().strip()
n = len(s)

if n % 2 == 1:  
    mid = n // 2
    s = s[:mid] + '*' + s[mid+1:]
else: 
    mid1, mid2 = n//2 - 1, n//2
    s = s[:mid1] + '**' + s[mid2+1:]

print(s)
```

### Question 3
### String Length Without Functions
Question:<br>
Problem Statement:<br>
Given a string S, find its length(including the spaces)without using any pre-defined functions.

Sample Input:<br>
codekata

Sample Output:<br>
8

Solution:
```python
s = input()

count= 0
for _ in s:
     count += 1
     
print(count)
```

### Question 4
### Case-Sensitive String Equality
Question:<br>
Problem Statement:<br>
Given 2 strings S1 and s2, check whether they are case senitively equal without using any predefined function(case sensitive).If they are not same print 'no'

Sample Input:<br>
guvi guvi

Sample Output:<br>
yes

Solution:
```python
S1,s2 = input().split()
print('yes' if S1 == s2 else 'no')
```

### Question 5
### First Occurrence of Character
Question:<br>
Problem Statement:<br>
Given a string 'S' and a character 'K', find at what position the character 'K' occurs for the first time in 'S'.(Assume the index of string starts at 1).If the character is not found in 'S' then print -1

Input Description:<br>
Input Size : |s| <= 100000

Sample Input:<br>
codekata a

Sample Output:<br>
6

Solution:
```python
s,k = input().split()

pos = s.find(k)
print(-1 if pos == -1 else pos+1)
```

### Question 6
### Character Count in String
Question:<br>
Problem Statement:<br>
Given a string 'S' and a character 'K', find how many times 'K' got repeated in 'S'.If 'K' is not found in 'S' print -1

Input Description:<br>
The input consists of a string 'S' and a character 'K'. The size of string 'S' is at most 100000.

Output Description:<br>
The output is the count of character 'K' in string 'S'. If 'K' is not found, print -1.

Sample Input:<br>
codekata a

Sample Output:<br>
2

Solution:
```python
s,k = input().split()

count = s.count(k)
print(count if count > 0 else -1)
```

### Question 7
### Count String Occurrences
Question:<br>
Problem Statement:<br>
Given a sentence and string S, find how many times S occurs in the given sentence.If S is not found in the sentence print -1

Input Description:<br>
Input Size : |sentence| <= 1000000(complexity O(n)).

Output Description:<br>
The output is the number of times S occurs in the given sentence, or -1 if S is not found.

Sample Input:<br>
I enjoy doing codekata<br>
codekata

Sample Output:<br>
1

Solution:
```python
sentence = input().strip()
s = input().strip()

count = sentence.count(s)
print(count if count > 0 else -1)
```

### Question 8
### Common Characters in Strings
Question:<br>
Problem Statement:<br>
Given 2 strings,check whether they have any common characters.If found print 'yes' else print 'no'.

Input Description:<br>
Input Size : |s| <= 100000(O(n))

Sample Input:<br>
guvi guvigeeks

Sample Output:<br>
yes

Solution:
```python
s = input().split()
print('yes' if s[0] in s[1] else 'no')
```

### Question 9
### Remove Characters from String
Question:<br>
Problem Statement:<br>
Given a string two strings S1 and S2, remove characters from the S1 which are present in the S2.If S1 becomes empty then print -1

Input Description:<br>
Input Size : N <= 100000

Sample Input:<br>
GUVI GEEK

Sample Output:<br>
UVI

Solution:
```python
s1, s2 = input().split()
result = []

for ch in s1:
    if ch not in s2:
        result += ch
        
print(''.join(result) if result else -1)
```

### Question 10
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

### Question 11
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

### Question 12
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

### Question 13
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

### Question 14
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

### Question 15
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

### Question 16
### Anagram Count
Question:<br>
Problem Statement:<br>
Given a number N and an array of N strings, find the number of strings that are an anagram of 'kabali'.If there exists no anagram for the given string print '0'.

Input Description:<br>
The input consists of an integer N, representing the number of strings, followed by N strings.
Constraints: 1 <= N <= 1000

Output Description:<br>
The output is a single integer representing the count of strings that are an anagram of 'kabali', or '0' if no such anagram exists.

Sample Input:<br>
5<br>
kabali<br>
kaabli<br>
kababa<br>
kab<br>
kabail<br>

Sample Output:<br>
3

Solution:
```python
n = int(input())
words = [input().strip() for _ in range(n)]

target = sorted(words[0])
count = 0

for word in words:
    if sorted(word) == target:
        count += 1

print(0 if count == 1 else count)
```

### Question 17
### Encode String by Adding 3
Question:<br>
Problem Statement:<br>
Given a string S, print the encoded string by adding 3 to each character(a maps to d,b maps to e,c maps to f and so on).

Input Description:<br>
Input Size : 1 <= N <= 100000

Sample Input:<br>
RADAR

Sample Output:<br>
UDGDU

Solution:
```python
def encode_string(s):
    result = []
    for ch in s:
        if 'A' <= ch <= 'Z':
            result.append(chr((ord(ch) - ord('A') + 3) % 26 + ord('A')))
        elif 'a' <= ch <= 'z':
            result.append(chr((ord(ch) - ord('a') + 3) % 26 + ord('a')))
        else:
            result.append(ch)
    return "".join(result)

s = input().strip()
print(encode_string(s))
```

### Question 18
### String Numeric Validation
Question:<br>
Problem Statement:<br>
Given a string S.Validate if a given string is numeric.print 'yes' if it is a numeric otherwise print 'no'.

Sample Input:<br>
guvigeeks

Sample Output:<br>
no

Solution:
```python
s = input()
print('yes' if s.isdigit() else 'no')
```

### Question 19
### Remove Extra Spaces
Question:<br>
Problem Statement:<br>
Given a sentence S take out the extra spaces.If no extra space is present print the same as output.

Input Description:<br>
Input Size : |s| <= 100000(complexity O(n))

Sample Input:<br>
codekata challenge

Sample Output:<br>
codekata challenge

Solution:
```python
s = input()
print(" ".join(s.split()))
```

### Question 20
### String Case Conversion
Question:<br>
Problem Statement:<br>
Given a string S change upper case to lowercase and lowercase to uppercase.

Input Description:<br>
The input consists of a string S with size |s| <= 10000000 (complexity O(n)).

Sample Input:<br>
CodEkaTa

Sample Output:<br>
cODeKAtA

Solution:
```python
s = input().strip()
print(s.swapcase())
```