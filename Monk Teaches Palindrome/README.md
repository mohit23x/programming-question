# link
https://www.hackerearth.com/practice/algorithms/string-algorithm/basics-of-string-manipulation/practice-problems/algorithm/monk-teaches-palindrome/

# - check palindrome
A palindrome is a sequence of characters which reads the same backward or forward." 

# input
- The first line consists of T, denoting the number of test cases.
- Next follow T lines, each line consisting of a string of lowercase English alphabets.

# Output:
- For each string , you need to find whether it is palindrome or not.
- If it is not a palindrome, print NO.
- If it is a palindrome, print YES followed by a space; then print EVEN it is an even else print ODD.
- Output for each string should be in a separate line.

# sample input
3
abc
abba
aba

# sample output
NO
YES EVEN
YES ODD

<pre>
<code>

t = int(input())
for i in range(t):
    word = list(map(str, input()))
    word_len = len(word)
    array_len = word_len-1
    check = 'EVEN' if word_len%2 == 0 else 'ODD'

    for j in range(word_len):
        if word[j] != word[array_len-j]:
            print('NO')
            break
        else:
            if j == array_len:
                print('YES', check)

</code>
</pre>