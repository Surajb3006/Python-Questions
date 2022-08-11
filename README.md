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
Q16)There is a hidden word S and a guess word T, both of length 55.

Chef defines a string M to determine the correctness of the guess word. For the ith index:
If the guess at the ith index is correct, the ithcharacter of M is G.
If the guess at the ith index is wrong, the ith character of M isB.
Given the hidden word SS and guess T, determine string M.	
Sol)n=int(input())
for i in range(n):
    x=input()
    y=input()
    for j in range(len(x)):
        if (x[j]==y[j]):
            print('G',end='')
        else:
            print('B',end='')
    print()
 Q17)For each input output "wins" if the number is a palindrome and "loses" if not, in a new line.
 Sol)n=int(input())
for i in range(n):
    x=int(input())                                
    y=x
    a=0
    while (x>0):
        a=(a*10 + (x%10))
        x=x//10
    if (a==y):
        print('wins')
    else:
        print('loses')
	
OR t = int(input())
for i in range(t):
    a = input()
    k = a[::-1]
    if a == k:
        print("wins")
    else:
        print("loses")
	
Q18)Chef recorded a video explaining his favorite recipe. However, the size of the video is too large to upload on the internet. He wants to compress the video so that it has the minimum size possible.

Chef's video has N frames initially. The value of the ith frame is Ai Chef can do the following type of operation any number of times:
Choose an index i(1≤i≤N) such that the value of the ith frame is equal to the value of either of its neighbors and remove the ith frame.Find the minimum number of frames Chef can achieve.
Sol)T=int(input())
for i in range(T):
    n=int(input())
    count=0
    A=list(map(int,input().split()))
    l=len(A)
    for i in range(n-1):
        p=A[i]
        r=A[i+1]
        if p==r:
            count=count+1  
        else:
            continue
    print(l-count)
    
 Q19)Given a positive integer N, MoEngage wants you to determine if it is possible to rearrange the digits of N (in decimal representation) and obtain a multiple of 5.For example, when N=108, we can rearrange its digits to construct 180=36*5 which is a multiple of 5.
 Sol)for i in range(int(input())):
    x=int(input())
    y=input()
    if "0" in y or "5" in y:
        print("YES")
    else:
        print("NO")
Q20)You are given a string and your task is to swap cases. In other words, convert all lowercase letters to uppercase letters and vice versa.
Sol)def swap_case(s):
    return s.swapcase()#change upper to lower case and lower to upper case
if __name__ == '__main__':
    s = raw_input()
    result = swap_case(s)
    print result
