# Descripción
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size
# Solución 
```
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cd /var/lib/dpkg/info/
bandit6@bandit:/var/lib/dpkg/info$ cat "bandit7.password"
Password: morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj
```
# Notas
# Referencias
