# link - https://www.hackerearth.com/practice/algorithms/string-algorithm/basics-of-string-manipulation/practice-problems/algorithm/dna-pride/

You are given a string that contains the nucleotide bases of DNA and RNA, you are needed to find the correct pair for all the bases and print the corresponding sequence obtained. In case the sequence contains a RNA base, print "Error RNA nucleobases found!" (without quotes)

# Input
- The first line of input contains T, the no of test cases. The next line of input contains N 
- the no of bases in each of the DNA sequence The line after that contains the DNA sequence.

- 3
- 2
- AG
- 4
- ATGC
- 6
- UGCACT

# output

For each test case output your answer on a new line.

- TC
- TACG
- Error RNA nucleobases found!


<pre>
<code>

t = int(input())
for i in range(t):
    n = input()
    w = list(map(str, input()))
    if 'U' in w:
        print('Error RNA nucleobases found!')
    else:
        for i in range(len(w)):
            if w[i] == 'A': w[i] = 'T'
            elif w[i] == 'G': w[i] = 'C'
            elif w[i] == 'T': w[i] = 'A'
            elif w[i] == 'C': w[i] = 'G'
        print("".join(w))
</code>
</pre>