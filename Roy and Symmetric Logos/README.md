# Your task is to output YES if the logo is symmetric else output NO.

# Input:
- First line contains T - number of test cases.
- T test cases follow.
- First line of each test case contains the N - size of matrix.
- Next N lines contains binary strings of length N.

# Output:
- Print YES or NO in a new line for each test case

# SAMPLE INPUT
5
2
11
11
4
0101
0110
0110
0101
4
1001
0000
0000
1001
5
01110
01010
10001
01010
01110
5
00100
01010
10001
01010
01110

# SAMPLE OUTPUT
YES
NO
YES
YES
NO


<br>
<hr>
<br>
<pre>
<code>
n = int(input())

def chec(t, size):
    c=0
    l = len(t[0])
    
    for i in range(size):
        if t[i] == t[(size-1)-i]:
            for e in range(l):
                if t[i][e] == t[i][(l-1)-e]:
                    c = 1
                else:
                    c = 0
                    return 'NO'
                
        else:
            c = 0
            return 'NO'
            
    if c == 1:
        return 'YES'
        

for i in range(n):
    c = 0
    size = int(input())
    t = [list(map(int, input())) for i in range(size)]
    print(chec(t, size))
</code>
</pre>