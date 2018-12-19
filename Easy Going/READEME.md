# link
https://www.hackerearth.com/practice/algorithms/sorting/bubble-sort/practice-problems/algorithm/min-max-difference/


# difference between maximum sum and minimum sum of N-M elements of the given array.

# Input:
- First line contains an integer T denoting the number of testcases.
- First line of every testcase contains two integer N and M.
- Next line contains N space separated integers denoting the elements of array 

# Output:
- For every test case print your answer in new line

# SAMPLE INPUT
1
5 1
1 2 3 4 5

# SAMPLE OUTPUT
4


<pre>
<code>
t = int(input())
for i in range(t):
    n, m = input().split(' ')
    n = int(n)
    m = int(m)
    a = list(map(int, input().split()))
    a = sorted(a)
    print(sum(a[n-m:]) - sum(a[:m]))
</code>
</pre>