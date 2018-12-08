#You are given a matrix of characters. The matrix has N rows and M columns. Given a string s, you have to tell if it is possible to generate that string from given matrix.
<br />
#Rules for generating string from matrix are:

- You have to pick first character of string from row 1, second character from row 2 and so on. - The  character of string is to be picked from row 1, that is, you can traverse the rows in a cyclic manner (row 1 comes after row N).
- If an occurrence of a character is picked from a row, you cannot pick the same occurrence again from that row.

#Input Format

- First line consists of T, denoting the number of test cases.
- Each test case consists of:
- First line consists of two integers N and M, denoting the matrix dimensions.
- Following N lines consist of M characters each.
- Last line consists of a string s.

# Output Format
- For each test case, print "Yes" if string can be generated else print "No". Answer for each test case should come in a new line.

# input 
1
3 3
aba
xyz
bdr
axbaydb

#output
Yes

<br />

<pre>
<code>
t = int(input())
a = []
ctr = -1

    
for i in range(t):
    m, n = input().split()
    m, n = int(m), int(n)
    
    for i in range(m):
        temp = input()
        a_temp = [x for x in temp]
        a.append(a_temp)
    word = input()

    
    for i, w in enumerate(word):
        ctr = ctr + 1
        if w in a[ctr]:
            a[ctr].remove(w)
        else:
            print('No')
            ctr = -1
            a = []
            break
            

        if ctr >= (m-1):
            ctr = -1
        else:
            pass
        
        if(len(word) == (i+1)):
            print('Yes')
            ctr = -1
            a = []
            break
        else:
            pass
</code>
</pre>