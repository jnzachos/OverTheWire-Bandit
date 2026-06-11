# Bandit Level 2

```bash
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cat -

```

As we can see, there is a file named `-`. When we try to print it using `cat`, the terminal waits for an input instead of printing the file's content. Why is that?

`-` is a special symbol in the terminal. It means "read from standard input" and therefore, the terminal waits for an input from the user.

How can we overcome that? By simply doing:

```bash
bandit1@bandit:~$ cat ./-
...
```

This tells `cat` to look for an actual file in our current directory and print it, by giving it a path instead of just a symbol.

