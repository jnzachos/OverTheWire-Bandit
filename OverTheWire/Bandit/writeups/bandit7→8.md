# Bandit Level 7 → 8

```bash
bandit7@bandit:~$ ls
data.txt
```

The password is stored inside that `.txt` file, next to the word "millionth"

In order find it, we will use the command `grep`

```bash
bandit7@bandit:~$ grep "millionth" data.txt
millionth       ...
```
