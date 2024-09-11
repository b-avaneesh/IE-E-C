'''Q1: Write a program to determine if the sum of two numbers is divisible by 7 (using if-else) and divisible by 5 (using a ternary operator).

Q2: Write a program to calculate the factorial of a given number using a for loop.

Q3: Write a program that:
Uses a function to determine if a given string is a palindrome.
In the main function, swaps the case of all letters in the original string (e.g., Input: aBC, Output: Abc).

Q4: Write a program to:
Find the transpose of a given matrix.
Calculate the sum of the elements in each column of the original matrix.'''

#Q1:
n1=int(input('Enter number 1: '))
n2=int(input('Enter number 2: '))

sum=n1+n2
if sum%7==0:
    print('Divisible by 7')
else:
    print('Not divisble by 7')

print('Divisble by 5') if (sum%5==0) else print('Not divisble by 5')

#Q2:
n=int(input('Enter the number: '))
fact=1
for i in range(1,n+1):
    fact=fact*i
print('Factorial of',n,'is: ',fact)


#Q3:
string=input("Enter a string: ")
rev=''
string_n=''
for i in string:
    
    if i>='A' and i<='Z':
        string_n= string_n + i.lower()
    if i>='a' and i<='z':
        string_n= string_n + i.upper()
print(string_n)

for j in range(0,len(string),-1):
    rev=rev+j



if rev==string:
    print('It is a pallindrome')
else:
    print('Not a pallindrome')

#Q4
matA=[[1,2,3],[4,5,6],[7,8,9]]

for i in range(0,3):
    sum=0
    for j in range(0,3):
        sum=sum+matA[j][i]
    print('Sum of column',i+1,'is ',sum)

for i in range(0,3):
    for j in range(0,3):
        if j>i:
            temp=matA[i][j]
            #print(matA[j][i])
            matA[i][j]=matA[j][i]
            matA[j][i]=temp
print('\nTranspose of Matrix is\n') 
print(matA)




