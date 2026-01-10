### Question 1
### Decimal to Binary Conversion
Question:<br>
Problem Statement:<br>
Given a number N in decimal convert it into binary value.

Input Description:<br>
Input Size : N <= 100000

Sample Input:<br>
5

Sample Output:<br>
101

Solution:
```python
N = int(input())

# Convert decimal to binary (remove '0b' prefix)
binary_value = bin(N)[2:]

print(binary_value)

```

### Question 2
### Binary to Decimal Conversion
Question:<br>
Problem Statement:<br>
Given a number N in binary format convert it to decimal number.

Sample Input:<br>
101

Sample Output:<br>
5

Solution:
```python
N = input()

# Convert binary to decimal
decimal_value = int(N, 2)

print(decimal_value)
```

### Question 3
### Binary to Octal Conversion
Question:<br>
Problem Statement:<br>
Given a binary number convert it into octal format.

Sample Input:<br>
1100100

Sample Output:<br>
144

Solution:
```python
binary = input().strip()
decimal = int(binary, 2)
octal = oct(decimal)[2:]
print(octal)
```

### Question 4
### Binary to Hexadecimal Conversion
Question:<br>
Problem Statement:<br>
Given a binary number convert it to hexadecimal.

Sample Input:<br>
1100100

Sample Output:<br>
64

Solution:
```python
binary= input()
hexa = hex(int(binary, 2))[2:].upper()
print(hexa)
```

### Question 5
### Date to Month Name Conversion
Question:<br>
Problem Statement:<br>
Given a date(DD-MM-YYYY),print the month in words.

Sample Input:<br>
01-01-2018

Sample Output:<br>
January

Solution:
```python
date_str = input().strip()

day, month, year = date_str.split('-')
months = [
    "January", "February", "March", "April", "May", "June",
    "July", "August", "September", "October", "November", "December"
]

month_name = months[int(month) - 1]
print(month_name)
```

### Question 6
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

### Question 7
### Celsius to Fahrenheit Conversion
Question:<br>
Problem Statement:<br>
You are given with a number A i.e. the temperature in Celcius. Write a program to convert this into Fahrenheit. Note: In case of decimal values, round-off to two decimal places.

Input Description:<br>
A number is provided in Celcius as the input of the program.

Output Description:<br>
The output shall be the temperature converted into Fahrenheit corresponding to the input value print up to two decimal places and round off if required.

Explanation:<br>
(X°C × 9/5) + 32 = 32°Fhere X is the input

Sample Input:<br>
12

Sample Output:<br>
53.60

Solution:
```python
celsius = int(input())

fahrenheit = float((9/5) * celsius + 32)
print(round(fahrenheit, 2))
```