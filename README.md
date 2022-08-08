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
Q.4)Given a year, determine whether it is a leap year. If it is a leap year, return the Boolean True, otherwise return False.
Note that the code stub provided reads from STDIN and passes arguments to the is_leap function. It is only necessary to complete the is_leap function.
Sol) def is_leap(year):
        if (year%4==0) and (year%400==0 or year%100!=0):
            leap = True
        else:
            leap = False
        return leap

    year = int(input())
    print(is_leap(year))
 Q.5)Without using any string methods, try to print the following:123...n
 Sol) n = int(input())
    # x=1
    # for i in range(2,n+1):
    #     x=str(x)+str(i)
    # print(x)
    for i in range(1,n+1):
        print(i,end='')
Q.6) Given an integer,n, perform the following conditional actions:
If n is odd, print Weird
If n is even and in the inclusive range of 2 to 5 , print Not Weird
If n is even and in the inclusive range of 6 to 20 , print Weird
If n is even and greater than 20 , print Not Weird
Sol)n = int(input().strip())
    if(n%2==1):
        print('Weird')
    elif(n%2==0 and 2<=n<=5):
        print('Not Weird')
    elif(n%2==0) and 6<=n<=20:
        print('Weird')
    elif(n%2==0) and n>20:
        print('Not Weird')    

