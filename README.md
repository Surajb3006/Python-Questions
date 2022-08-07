# Python-Questions
Q.1)The provided code stub reads two integers from STDIN, a and b. Add code to print three lines where:

The first line contains the sum of the two numbers.
The second line contains the difference of the two numbers (first - second).
The third line contains the product of the two numbers.
Sol) a = int(input())
    b = int(input())
    A=a+b
    B=a-b
    C=a*b
    print(A,B,C,sep='\n')
    
Q.2)The provided code stub reads two integers, a and b, from STDIN.

Add logic to print two lines. The first line should contain the result of integer division, a // b. The second line should contain the result of float division, a/b .

No rounding or formatting is necessary.  
Sol)a = int(input())
    b = int(input())
    A=a//b
    B=a/b
    print(A,B,sep='\n')
Q.3) The provided code stub reads and integer,n, from STDIN. For all non-negative integers i<n, print i^2
Sol) n = int(input())
    for i in range(n):
        print(i**2)
