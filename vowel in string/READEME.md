# find the number of vowels in string

# input
- number of test case
- stings

# output
- number of vowels

<pre>
<code>
t = int(input())
vowel = ['a', 'e', 'i', 'o', 'u']
for i in range(t):
    ctr = 0
    word = list(map(str, input()))
    for w in word:
        if w in vowel:
            ctr = ctr + 1
        else:
            pass
    print(ctr)

</code>
</pre>