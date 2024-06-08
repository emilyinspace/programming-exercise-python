# mini-grep
Out of the 3 choices, mini-grep was chosen. Two files `textfile1` and `textfile2` are included for testing purposes.
## Tests
1. To check that the regex pattern can't be invalid, we can run 

`python3 mini_grep -e "[" textfile1 textfile2`
which returns 
`ERROR: regex pattern [ is invalid!`

2. To check that the code is PEP8 compliant we can use pylint. 

`$ python3 -m pylint mini_grep`
 returns
```
--------------------------------------------------------------------
Your code has been rated at 10.00/10 (previous run: 10.00/10, +0.00)
```

3. To check that the regex matching inside files works, we can run `python3 mini_grep -e "Dylan" textfile1 textfile2`
which returns
```
2: Just say the word and I’ll get you a coffee cozy literally right now, Dylan.
4: Who is Dylan?
3: This line in textfile2 is about Dylan, since he wrote it.
```
4. To check that the quiet option works, we can add it to the command ran on step 3 like so:

`python3 mini_grep -q -e "Dylan" textfile1 textfile2`
which returns
```
Just say the word and I’ll get you a coffee cozy literally right now, Dylan.
Who is Dylan?
This line in textfile2 is about Dylan, since he wrote it.
```
5. We can test that the stdin line matching works by running: ```python3 mini_grep -e "^Dylan$"```
which returns
`Enter your text below`
and then we can enter these three lines
```
This is Dylan
Dylan
Dylan is not here
```
which gives us the output 
```

2: Dylan
```


