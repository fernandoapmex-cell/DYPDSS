# Descripción

The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
# Solución 

Abri el archivo y el resultado obtenido lo pase en rot13 decorder

Password: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4

```
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ ~~~~+
}{_~~~~+: command not found
bandit11@bandit:~$ }{_^C
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat da
cat: da: No such file or directory
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4
bandit11@bandit:~$
```
![[Pasted image 20260211224103.png]]
# Notas
- Se uso ROT13
# Referencias

- https://rot13.com