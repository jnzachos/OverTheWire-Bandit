# Bandit Level 9 → 10

We know that the password for the next level is stored in the file `data.txt` in one of the few human-readable strings, preceded by several ‘=’ characters.
```bash
bandit9@bandit:~$ strings data.txt | grep "="
 ========== the
I\=Ow
V?L=
%3=VZ
========== password
={M\
========== is
=Dvq
=n/N
========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
zX]%=
]\{=
bandit9@bandit:~$ strings data.txt | grep "="
 ========== the
I\=Ow
V?L=
%3=VZ
========== password
={M\
========== is
=Dvq
=n/N
========== ...
zX]%=
]\{=
```

Breakdown:
- `strings`  looks through a file and prints any readable text it finds
- `|` pipe, gives the output as input to the next command
- `grep` searches through text and prints only the lines that match a pattern you give it

Basically we find the human-readable text using `strings`, then give it as input to `grep` to search for '=' and `grep` then prints all the lines that have it in them. One of these lineshas the password.
