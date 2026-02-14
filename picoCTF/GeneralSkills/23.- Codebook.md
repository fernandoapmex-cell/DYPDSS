# Descripción

Run the Python script `code.py` in the same directory as `codebook.txt`.

# Solución 


```
FhernandoAP-picoctf@webshell:~$ ls
code.py  codebook.txt
FhernandoAP-picoctf@webshell:~$ chmod -x code.py
FhernandoAP-picoctf@webshell:~$ ./code.py
-bash: ./code.py: Permission denied
FhernandoAP-picoctf@webshell:~$ chmod -+x code.py
FhernandoAP-picoctf@webshell:~$ ./code.py
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
./code.py: line 7: syntax error near unexpected token `('
./code.py: line 7: `def str_xor(secret, key):'
FhernandoAP-picoctf@webshell:~$ chmod +x code.py
FhernandoAP-picoctf@webshell:~$ ./code.py
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
import-im6.q16: unable to open X server `' @ error/import.c/ImportImageCommand/346.
./code.py: line 7: syntax error near unexpected token `('
./code.py: line 7: `def str_xor(secret, key):'
FhernandoAP-picoctf@webshell:~$ ls
code.py  codebook.txt
FhernandoAP-picoctf@webshell:~$ cat codebook.txt
azbycxdwevfugthsirjqkplomn
FhernandoAP-picoctf@webshell:~$ ls
code.py  codebook.txt
FhernandoAP-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_d9aa2df2}
```
# Notas
# Referencias