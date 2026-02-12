# Descripción

The password for the next level is stored in the file **data.txt**, which contains base64 encoded data

# Solución 

```
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIGR0UjE3M2ZaS2IwUlJzREZTR3NnMlJXbnBOVmozcVJyCg==

Luego aplique base64 decode y obtuve la clave:

dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr
```
# Notas
# Referencias