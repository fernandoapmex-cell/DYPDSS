
# Descripción

The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.
# Solución 

```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep "==="
========== the
========== password
E========== is
5========== FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey
```
# Notas
# Referencias
