
# Descripción

The password for the next level can be retrieved by submitting the password of the current level to **port 30001 on localhost** using SSL/TLS encryption.

**Helpful note: Getting “DONE”, “RENEGOTIATING” or “KEYUPDATE”? Read the “CONNECTED COMMANDS” section in the manpage.**
# Solución 
password: kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```
bandit15@bandit:~$ openssl s_client -connect localhost:30001
.
.
.
.

read R BLOCK
-
Correct!
kSkvUpMQ7lBYyCM4GBPvCvT1BfWRy0Dx
```

# Notas
# Referencias