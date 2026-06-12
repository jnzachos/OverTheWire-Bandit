# Bandit Level 8→9

We know that the password for the next level is stored in the file data.txt and is the only line of text that occurs only once.

```bash
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
...
```
Breakdown:
- `sort` sorts lines alphabetically
- `uniq -u` prints lines that appear exactly once
- `|` is called a pipe. It connects the output of a command to the input of the next

For more info on piping and redirection click [here](https://ryanstutorials.net/linuxtutorial/piping.php).
