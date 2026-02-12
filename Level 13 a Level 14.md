
# Descripción
The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a that can be used to log into the next level. Look at the commands that logged you into previous bandit levels, and find out how to use the key for this level.

# Solución 

```
 ls
sshkey.private
bandit13@bandit:~$ ls
sshkey.private
bandit13@bandit:~$ cat sshkey.private

bandit13@bandit:~$ exit

EN WINDOWS : 

PS C:\Users\fhern\OneDrive\Escritorio> 
PS C:\Users\fhern\OneDrive\Escritorio>
PS C:\Users\fhern\OneDrive\Escritorio>
Se procesaron correctamente 1 archivos; error al procesar 0 archivos
PS C:\Users\fhern\OneDrive\Escritorio> icacls bandit14.key /grant:r "$($env:USERNAME):R"
archivo procesado: bandit14.key
Se procesaron correctamente 1 archivos; error al procesar 0 archivos
PS C:\Users\fhern\OneDrive\Escritorio> icacls bandit14.key
bandit14.key FHER-PC\fher:(R)

PS C:\Users\fhern\OneDrive\Escritorio> ssh -i bandit14.key bandit14@bandit.labs.overthewire.org -p 2220

bandit14@bandit:/etc/bandit_pass$ ls
bandit0  bandit10  bandit12  bandit14  bandit16  bandit18  bandit2   bandit21  bandit23  bandit25  bandit27  bandit29  bandit30  bandit32  bandit4  bandit6  bandit8
bandit1  bandit11  bandit13  bandit15  bandit17  bandit19  bandit20  bandit22  bandit24  bandit26  bandit28  bandit3   bandit31  bandit33  bandit5  bandit7  bandit9
bandit14@bandit:/etc/bandit_pass$ cd bandit14
-bash: cd: bandit14: Not a directory
bandit14@bandit:/etc/bandit_pass$ cat bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS


```

# Notas
# Referencias