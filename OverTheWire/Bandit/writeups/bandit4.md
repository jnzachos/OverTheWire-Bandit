# Bandit Level 4

```bash
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls

```

We find the `inhere` directory and enter it using `cd`, but when we run `ls` again, nothing appears. What is going on?!

The answer is simple. The files inside this directory are hidden. All we have to do is run `ls -a` (list all). This will show all the files in the directory, including the hidden ones.

Note: Most people tend to use `ls -la` which also lists them as shown below:

```bash
bandit3@bandit:~/inhere$ ls -la
total 12
drwxr-xr-x 2 root    root    4096 Apr  3 15:18 .
drwxr-xr-x 3 root    root    4096 Apr  3 15:18 ..
-rw-r----- 1 bandit4 bandit3   33 Apr  3 15:18 ...Hiding-From-You
```

`ls -a` difference:

```bash
bandit3@bandit:~/inhere$ ls -a
.  ..  ...Hiding-From-You
```

```bash
bandit3@bandit:~/inhere$ cat ...Hiding-From-You
...
```
