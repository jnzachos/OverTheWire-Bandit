# Bandit Level 2 → 3

```bash
bandit2@bandit:~$ ls
--spaces in this filename--
```

We notice that this file has spaces in its name. How can we print it using `cat`?

First we will have to use what we learned from the previous challenge, since it starts with `--`.

So our command so far looks like `cat ./`

But what can we do about the spaces?

There are 2 solutions to this problem:
- Cancel out the `spaces` with `\`
- Put the filename inside `" "`

```bash
bandit2@bandit:~$ cat ./--spaces\ in\ this\ filename--
...
bandit2@bandit:~$ cat ./"--spaces in this filename--"
...
```

We can see both of them work.

It is also worth mentioning that typing `cat ./--` and pressing `TAB` will auto-fill it for us.
