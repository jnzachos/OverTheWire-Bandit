# Bandit Level 5 → 6

```bash
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
```

We see that there are many directories. Can't go and check all of them. 

What we will do instead is use the command `find`.

We know that we are looking for a human-readable and not executable file with a size of 1033 bytes.

```bash
bandit5@bandit:~/inhere$ find . -type f -size 1033c
./maybehere07/.file2
```
Breakdown:
- `.` starting in this directory
- `-type f` file
- `size 1033c` 1033 bytes / characters

The output matches what we're looking for.

```bash
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
```
Note: There are other ways to find that file,but this is the easiest and most simple one.
