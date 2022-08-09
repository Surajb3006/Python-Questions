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

Q.7)Given the participants' score sheet for your University Sports Day, you are required to find the runner-up score. You are given n scores. Store them in a list and find the score of the runner-up.
Sol) n=int(input())
    arr = list(map(int, input().split()))
    arr.sort()
    a=max(arr)
    while max(arr)==a:
        arr.remove(a)
    print(arr[-1])
 
Q.8)Given the names and grades for each student in a class of N students, store them in a nested list and print the name(s) of any student(s) having the second lowest grade. 
Sol)    l = []
second_lowest_names = []
scores = set()

for _ in range(int(input())):
    name = input()
    score = float(input())
    l.append([name, score])
    scores.add(score) 
second_lowest = sorted(scores)[1]

for name, score in l:
    if score == second_lowest:
        second_lowest_names.append(name)

for name in sorted(second_lowest_names):
    print(name, end='\n')
    
 Q.9)The provided code stub will read in a dictionary containing key/value pairs of name:[marks] for a list of students. Print the average of the marks array for the student name provided, showing 2 places after the decimal.  
 Sol)n = int(input())
student_marks = {}
for _ in range(n):
    name, *line = input().split()
    scores = list(map(float, line))
    student_marks[name] = scores
query_name = input()
print("{0:.2f}".format(sum(student_marks.get(query_name))/len(student_marks.get(query_name))))
Q.10)If Give an integer N . Write a program to obtain the sum of the first and last digits of this number.
Sol)t = int(input())
 for tc in range(t) :
    n = int(input())
    res = n % 10
    while n >= 10 :
        n = n // 10
    res += n
    print(res)
    
Q11)The input begins with two positive integers n k (n, k<=107). The next n lines of input contain one positive integer ti, not greater than 109, each.
Write a single integer to output, denoting how many integers ti are divisible by k. 
Sol)(n, k) = map(int, input().split(' '))
ans = 0
for i in range(n):
	x = int(input())
	if x % k == 0:
		ans += 1
print(ans)	
Q12)Given an Integer N, write a program to reverse it.
Sol)t = int(input())
for i in range(t):
    reverse = 0
    num = int(input())
    while(num):
        remainder = num%10
        reverse =reverse*10+remainder
        num = int(num/10)
    print(reverse)
Q13)Write a program to check whether a triangle is valid or not, when the three angles of the triangle are the inputs. A triangle is valid if the sum of all the three angles is equal to 180 degrees.
Sol)n=int(input())
for i in range(n):
    x,a,b=map(int,input().split())
    y=x+a+b
    if (y==180):
        print('YES')
    else:
        print('NO')
Q14)Impressed by the power of this number, Kostya has begun to look for occurrences of four anywhere. He has a list of T integers, for each of them he wants to calculate the number of occurrences of the digit 4 in the decimal representation. He is too busy now, so please help him        
Sol)t = int(input())
for i in range(t):
    a=input()
    print(a.count('4'))
    # fours = 0
    # num = int(input())
    # while(num):
    #     if(num%10 == 4):
    #         fours +=1
    #     num = int(num/10)
    # print(fours)
    
Q15)Chef has to travel to another place. For this, he can avail any one of two cab services.
The first cab service charges XX rupees.
The second cab service charges YY rupees.
Chef wants to spend the minimum amount of money. Which cab service should Chef take?
Sol)n=int(input())
for i in range(n):
    a,b=map(int,input().split())
    if(a>b):
        print('SECOND')
    elif(a==b):
        print('ANY')
    else:
        print('FIRST')
