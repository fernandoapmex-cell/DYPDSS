# Descripción
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
# Solución 
```
ls
cd inhere
ls
find . -type f -size 1033c ! -executable
cd maybehere07
ls -a
cat .file2
Password:HWasnPhtq9AVKe0dmk45nxy20cvUa6EG
```
# Notas
# Referencias
