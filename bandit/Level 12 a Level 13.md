# Descripción

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

# Solución 
```
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ mktemp -d
/tmp/tmp.DbrGGVCyC4
bandit12@bandit:~$ ls
data.txt
bandit12@bandit:~$ cd /tmp/tmp.DbrGGVCyC4
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ cp ~/data.txt .
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ xxd -r data.txt data.bin
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data.bin  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data.bin
data.bin: gzip compressed data, was "data2.bin", last modified: Tue Oct 14 09:26:06 2025, max compression, from Unix, original size modulo 2^32 564
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ mv data.bin data.gz
gzip -d data.gz
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data
data: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ mv data data.bz2
bzip2 -d data.bz2
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data
data: gzip compressed data, was "data4.bin", last modified: Tue Oct 14 09:26:06 2025, max compression, from Unix, original size modulo 2^32 20480
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ mv data data.gz
gzip -d data.gz
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ tar -xf data
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data5.bin  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ cat data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data5.bin  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data
data: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data5.bin
data5.bin: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ tar -xf data5.bin
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data5.bin  data6.bin  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data6.bin
data6.bin: bzip2 compressed data, block size = 900k
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data5.bin  data6.bin  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ mv data6.bin data6.bz2
bzip2 -d bata6.bz2
bzip2: Can't open input file bata6.bz2: No such file or directory.
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ bzip2 -d data6.bz2
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data5.bin  data6  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data6
data6: POSIX tar archive (GNU)
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ tar -xf data6
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data5.bin  data6  data8.bin  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data8.bin
data8.bin: gzip compressed data, was "data9.bin", last modified: Tue Oct 14 09:26:06 2025, max compression, from Unix, original size modulo 2^32 49
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ mv data8.bin data8.gz
gzip -d data8.gz
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ ls
data  data5.bin  data6  data8  data.txt
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ file data8
data8: ASCII text
bandit12@bandit:/tmp/tmp.DbrGGVCyC4$ cat data8
The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
```

# Notas
# Referencias