### Question 1
### Space Removal from String
Question:<br>
Problem Statement:<br>
Given a string/sentence remove all the spaces and print the result.

Input Description:<br>
Input Size : |s| <= 1000000(complexity O(n))

Sample Input:<br>
guvi geeks

Sample Output:<br>
guvigeeks

Solution:
```python
s = input()
print(s.replace(" ", ""))
```

### Question 2
### String Difference Check
Question:<br>
Problem Statement:<br>
Given 2 strings and a number K, check whether they differ exactly by K characters.

Input Description:<br>
Input Size : |s| <= 100000(complexity O(nlogn) or O(n))

Sample Input:<br>
codekata codeguvi 4

Sample Output:<br>
yes

Solution:
```python
s1, s2, k = input().split()
k = int(k)

if len(s1) != len(s2):
    print("no")
else:
    diff_count = sum(1 for i in range(len(s1)) if s1[i] != s2[i])
    if diff_count == k:
        print("yes")
    else:
        print("no")
```

### Question 3
### Print 1st and 3rd Character
Question:<br>
Problem Statement:<br>
Given a string S, print the 1st and 3rd character of the string (chracter index starts from 1).

Input Description:<br>
Input Size : 1 <= N <= 100000

Sample Input:<br>
codekata

Sample Output:<br>
cd

Solution:
```python
s = input()
print(s[0] + s[2])
```

### Question 4
### Substring Check-2
Question:<br>
Problem Statement:<br>
Given 2 strings.check if the second string is a substring of the first string.Print 'yes' if there exists a valid substring otherwise print 'no'.

Input Description:<br>
The input consists of two strings. The size of the strings (N) is between 1 and 100000 (inclusive).

Output Description:<br>
Print 'yes' if the second string is a substring of the first string, otherwise print 'no'.

Sample Input:<br>
codekata code

Sample Output:<br>
yes

Solution:
```python
s1, s2 = input().split()

if s2 in s1:
    print("yes")
else:
    print("no")
```

### Question 5
### Word Position in String
Question:<br>
Problem Statement:<br>
Given 2 strings S and X print the word position of X in S.(word count starts from 1).If the given word doesn't exists in S print '-1'.

Input Description:<br>
The input consists of 2 strings S and X. The size of S and X are between 1 and 1000 characters (1 <= |s|, |x| <= 1000).

Output Description:<br>
The output is the word position of X in S (starting from 1), or -1 if X is not found.

Sample Input:<br>
codekata coding challenge<br>
coding

Sample Output:
2

Solution:
```python
S = input()
X = input()
words = S.split()

# Check if X exists and print its position (1-based index)
if X in words:
    print(words.index(X) + 1)
else:
    print(-1)
```

### Question 6
### Reverse String with Separator
Question:<br>
Problem Statement:<br>
Given a input string S, reverse the given string by appending each character of the string with '-'.

Input Description:<br>
Input Size : |S| <= 100000

Sample Input:<br>
codekata

Sample Output:<br>
a-t-a-k-e-d-o-c

Solution:
```python
S = input()
result = '-'.join(S[::-1])
print(result)
```

### Question 7
### Lexicographically Smallest String
Question:<br>
Problem Statement:<br>
Given a number N and an array of N strings, find the lexicographically smallest string.

Input Description:<br>
The input consists of an integer N, representing the number of strings, followed by N strings. N is less than or equal to 1000.

Output Description:<br>
The output is the lexicographically smallest string among the given N strings.

Sample Input:<br>
3<br>
code<br>
learn<br>
practice<br>

Sample Output:<br>
code

Solution:
```python
N = int(input())
strings = [input().strip() for _ in range(N)]

smallest = min(strings)
print(smallest)
```

### Question 8
### String Deletion
Question:<br>
Problem Statement:<br>
Given 2 strings S,X. Print the string after deleting X.If X not found print the same string.

Input Description:<br>
Input Size : 1 <= |s|, |x| <= 1000

Sample Input:<br>
Happy Birthday<br>
Happy

Sample Output:<br>
Birthday

Solution:
```python
S = input().strip()
X = input().strip()

if X in S:
    print(S.replace(X, " ", 1).strip())
else:
    print(S)
```

### Question 9
### Vowel Check in Strings
Question:<br>
Problem Statement:<br>
Given a number N and an array of N strings,Print yes, if all strings have atleast one vowel in them otherwise print no.

Input Description:<br>
The input consists of an integer N (where N <= 1000), followed by N strings.

Output Description:<br>
The output is "yes" if all N strings contain at least one vowel, and "no" otherwise.

Sample Input:<br>
5<br>
code<br>
overload<br>
vishal<br>
sundar<br>
anish<br>

Sample Output:<br>
yes

Solution:
```python
n = int(input())
arr = [input().strip() for _ in range(n)]
vowels = "aeiouAEIOU"

def has_vowel(s):
    return any(char in vowels for char in s)

if all(has_vowel(s) for s in arr):
    print("yes")
else:
    print("no")
```

### Question 10
### Swap Words Around 'and'
Question:<br>
Problem Statement:<br>
Given a sentence interchange the between the word 'and'.

Input Description:<br>
The input consists of a single string S, representing the sentence, with a maximum length of 1,000,000 characters.

Sample Input:<br>
jack and jill went up and down to get water

Sample Output:<br>
jill and jack went down and up to get water

Solution:
```python
def swap_and_words(sentence):
    words= sentence.split()
    n = len(words)
    i =0

    while i < n:
        if words[i] == "and" and i > 0 and i < n - 1:
            words[i - 1], words[i + 1] = words[i+1],words[i-1]
        i +=1
    return " ".join(words)

sentence = input().strip()
print(swap_and_words(sentence))
```

### Question 11
### Capitalize Repeated Letters
Question:<br>
Problem Statement:<br>
Roman Reigns want to identify the repeated letters in two given strings and capitalize it.Help him to achieve it.

Sample Input:<br>
computer program

Sample Output:<br>
cOMPuteR PROgRaM

Solution:
```python
def capitalize_repeated_chars(sentence):
    words = sentence.split()
    combined= ''.join(words)

    repeated_chars ={ch for ch in combined if combined.count(ch) >  1}

    result= [''.join(ch.upper() if ch in repeated_chars else ch for ch in word)for word in words]
    return " ".join(result)
sentence = input()
print(capitalize_repeated_chars(sentence))
```

### Question 12
### String Contains Substrings
Question:<br>
Problem Statement:<br>
Given a string S, print 'yes' if the strings 'GUVI' and 'GEEK' is present case-sensitively in the string else print 'no'.

Input Description:<br>
The input consists of a string S. The size of the string S is between 1 and 100 characters (inclusive).

Output Description:<br>
Print 'yes' if both 'GUVI' and 'GEEK' are present case-sensitively in the string S, otherwise print 'no'.

Sample Input:<br>
Vishal_Sundar prepared this question

Sample Output:<br>
no

Solution:
```python
s = input()

print('yes' if 'GUVI' in s and 'GEEK' in s else 'no')
```

### Question 13
### Unique Characters in String
Question:<br>
Problem Statement:<br>
Given a string S, retain the character(s) once irrespective of number of times it occurs in the given string.

Input Description:<br>
Input Size : |S| <= 100000

Sample Input:<br>
aabbaa

Sample Output:<br>
ab

Solution:
```python
s = input()
result = ""

for char in s:
    if char not in result:
        result += char
        
print(result)
```

### Question 14
### Vowel then Consonant
Question:<br>
Problem Statement:<br>
Given a string S ,print the vowels first and then consonants in the same order as they have occurred in the string.

Input Description:<br>
Input Size : N <= 10000

Sample Input:<br>
GuVI

Sample Output:<br>
uIGV

Solution:
```python
name = input().strip()
vowels = "aeiouAEIOU"
vowels =[char for char in name if char in vowels]
normal = [char for char in name if char not in vowels]
print("".join(vowels+normal))
```

### Question 15
### Reverse String Case
Question:<br>
Problem Statement:<br>
Given a string S of length N, reverse the case of each letter.

Input Description:<br>
Input Size : N <= 100

Sample Input:<br>
HeLlo

Sample Output:<br>
hElLO

Solution:
```python
s = input()

result = ''.join(ch.lower() if ch.isupper() else ch.upper() for ch in s)
print(result)
```

### Question 16
### Reverse Word Order
Question:<br>
Problem Statement:<br>
Given a string S consisting of 2 words reverse the order of two words .

Input Description:<br>
The input consists of a string S with a maximum size of 10,000,000 characters.

Sample Input:<br>
hello world

Sample Output:<br>
world hello

Solution:
```python
n = input().split()
print(n[1] +' '+ n[0])
```

### Question 17
### Mirror String Pairs
Question:<br>
Problem Statement:<br>
Given an array of pairs of strings, find if there are mirror pairs. (s1, s2) & (s3, s4) are mirror pairs, if s1 = s4 and s2 = s3. The first string in each pair is distinct.

Input Description:<br>
The first line contains the number string pairs N.
Then N string pairs follow.

Output Description:<br>
Print YES, if a mirror pair exists, print NO otherwise.

Sample Input:<br>
3<br>
raja kili<br>
pan quil<br>
kili raja<br>

Sample Output:
YES

Solution:
```python
n = int(input())
pairs = []

for _ in range(n):
    a,b = input().split()
    pairs.append((a,b))

pair_set = set(pairs)

found = False
for a,b in pair_set:
    if (b,a) in pair_set:
        found = True
        break
    
print("YES" if found else "NO")
```

### Question 18
### String Length Without Spaces-2
Question:<br>
Problem Statement:<br>
Given a string find the length of the string without space

Input Description:<br>
Given a string

Output Description:<br>
Print length in number

Explanation:<br>
‘guvi geek’ is the given string, need to remove space from the string (‘guvigeek’),now print length of that string

Sample Input:<br>
guvi geek

Sample Output:<br>
8

Solution:
```python
n = input()
print(len(n.replace(' ','')))
```

### Question 19
### Extract Vowels from String
Question:<br>
Problem Statement:<br>
Given a string print the vowels in the string

Input Description:<br>
Given a string

Output Description:<br>
Print the String

Sample Input:<br>
guvi geek

Sample Output:<br>
ui ee

Solution:
```python
input_string = input()
vowels = "aeiouAEIOU"
vowel_string = ' '.join([''.join([char for char in word if char in vowels]) for word in input_string.split()])
print(vowel_string)
```

### Question 20
### Reverse a String-5
Question:<br>
Problem Statement:<br>
Given a string reverse the string

Input Description:<br>
Given a string

Output Description:<br>
Print string into reverse

Explanation:<br>
‘guvi geek’ is the given string, print the word from last as ‘geek guvi’

Sample Input:<br>
guvi geek

Sample Output:<br>
geek guvi

Solution:
```python
n = input()
print(' '.join(reversed(n.split())))
```

### Question 21
### String Uppercase Vowels
Question:<br>
Problem Statement:<br>
Given a string convert string into upper case where their vowel character

Input Description:<br>
Given a string

Output Description:<br>
Print string into upper case

Explanation:<br>
‘guvi geek’ is the given string, convert all vowels into uppercase and print it as ‘gUvI gEEk’

Sample Input:<br>
guvi geek

Sample Output:<br>
gUvI gEEk

Solution:
```python
def upper_vowels(n):
    vowels ="aeiou"
    result =""

    for char in n:
        if char.lower() in vowels:
            result = result + char.upper()
        else:
            result += char
    return result

n = input()
print(upper_vowels(n))
```

### Question 22
### Find Duplicate Characters-2
Question:<br>
Problem Statement:<br>
Given a string print the duplicate in the string if their no duplicate print -1

Input Description:<br>
Given a string

Output Description:<br>
Print duplicate of the string or -1

Explanation:<br>
The letters which are repeated in the given string(Guvi Geek) is G and e. So, Ge is printed as output

Sample Input:<br>
Guvi Geek

Sample Output:<br>
Ge

Solution:
```python
from collections import Counter
n = input().strip()
char_count = Counter(n)
elements = [char for char in n if char_count[char] > 1]
unique_duplicates = "".join(sorted(set(elements), key = elements.index))
print(unique_duplicates)
```

