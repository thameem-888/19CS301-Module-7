# 19CS301-Module-7
EX: 7.1   Recursion 

### AIM: 

To write a Python program to find N^P using recursion (without using the ** operator).

### ALGORITHM:
Step1: Start.

Step 2: Define a recursive function power(base, exponent).

Step3: If exponent is 0, return 1 (base case).

Step 4: Otherwise, return base * power(base, exponent - 1).

Step 5: Read base and exponent as input.

Step 6:Call the recursive function and print the result.

Step 7:Stop.

### PROGRAM:
```
a=int(input())
b=int(input())
def power(a,b):
	if b==0:
		return 1
	elif a==0:
		return 0
	elif b==1:
		return a
	else:
		return a*power(a,b-1)
print(a,"Power",b,":",power(a,b))
```
### OUTPUT:
![image](https://github.com/user-attachments/assets/229c7eb3-e15b-44ae-9c92-85ab71194560)


### RESULT: 

The program successfully calculates N^P using recursion and displays the correct result without using the ** operator.

EXP.No: 7.b Types of Recursion

### AIM: 

To write a Python program to find your name in a sorted list of shortlisted students using tree recursion (binary search). If found, print the position (1-based), otherwise print 0.


###ALGORITHM:
Step 1: Start

Step 2: Read the number of student names and input them into a list.

Step 3: Sort the list of names alphabetically.

Step 4: Define a recursive function binary_search_recursive(list, left, right, target).

Step 5: In the function, if left > right, return 0 (not found).

Step 6: Find the middle index. 
        
Step 7: Call the recursive function and display the result.

Step 8: Stop

### PROGRAM:
```
def binary_search(l, low, high, elem):
    if high >= low:
        mid = (high + low)//2
        if l[mid] == elem:
            return mid
        elif l[mid] > elem:
            return binary_search(l,low, mid-1,elem)
        else:
            return binary_search(l,mid + 1,high,elem)
    else:
        return -1

    
    
l = [ ]
n=int(input())
for i in range(n):
    x=input()
    l.append(x)
name = input()
l.sort()
print("The sorted list is")
print(l)
print(binary_search(l,0,len(l)-1,name)+1)
```
###OUTPUT:


![image](https://github.com/user-attachments/assets/08c02aa5-9c08-4242-a86e-6a3687241b60)

###RESULT: 

The program successfully finds the position of a given name using tree recursion (binary search). It returns the 1-based index if found, otherwise it returns 0.

EX: 7.3 Taylor Series

### AIM: 

To write a Python program to evaluate sinh(x) for n terms using recursion.

### ALGORITHM:

Step 1: Start

Step 2: Read the values of x and n (number of terms)

Step 3: Define a recursive function to calculate factorial

Step 4: Define a recursive function to calculate sinh(x) using the formula:
        sinh(x) = x + x^3/3! + x^5/5! + ... up to n terms

Step 5: Use recursion to sum the terms

Step 6: Display the result

Step 7: Stop

### PROGRAM:


```from abc import ABC
def fact(i):
    if i==1 or i==0:
        return 1
    else:
        return i*fact(i-1)
def sinh(x,n):
    if n==0:
        return  x
    else:
        return(((pow(x,(2*n+1)))/(fact(2*n+1))) + sinh(x,n-1))
x=int(input())
n=int(input())
print(sinh(x,n))
```
### OUTPUT:

![image](https://github.com/user-attachments/assets/31949ea9-5669-4e83-bb5e-fa4dc7de7aff)


### RESULT: 

The program successfully evaluates sinh(x) using recursion and displays the result up to n terms using the Taylor series expansion.


EXP.No: 7.4   Advance Recursion Problems


### AIM:

To write a Python program to check whether a string is a palindrome using recursion.

###ALGORITHM: 

Step 1: Start

Step 2: Read the input string

Step 3: Define a recursive function to check palindrome:

Step 4: Call the recursive function with input string

Step 5: Print "String is a palindrome" if True, else print "String is not a palindrome"

Step 6: Stop

###PROGRAM:
```
def is_palindrome(word):
    if len(word) <= 1:
        return True
    else:
        return word[0] == word[-1] and is_palindrome(word[1:-1])
str=input() 
if(is_palindrome(str)):
    print("String is a palindrome")
else:
    print("String is not a palindrome")
```
### OUTPUT:
 
![image](https://github.com/user-attachments/assets/2ae1b7c9-354a-4a0a-aac0-35d075f2b4b6)

 

### RESULT: 

The program correctly checks whether the input string is a palindrome using recursion and prints the appropriate message.

EXP.No: 7.5   ASSESSMENT EXAM -VII -SEB


### AIM:

To write a Python program to calculate the sum of factorials from 1! to n! using recursion.

###ALGORITHM: 

Step 1: Start

Step 2: Read input n

Step 3: Define a recursive function factorial(n):

Step 4: Define a recursive function sum_factorials(n):

Step 5: Call sum_factorials(n) and print the result

Step 6: Stop


###PROGRAM:
```
def func(n):
    if n==0:
        return 1
    else:
        return n*func(n-1)
n=int(input())
sum=0
for i in range(1,n+1):
    sum+=func(i)
print(sum)

```
### OUTPUT:
 
![image](https://github.com/user-attachments/assets/7c8a3baa-9242-4a55-ab5a-44d29845aa8a)

 

### RESULT: 

The program successfully calculates the sum of factorials from 1 to n using recursion.





