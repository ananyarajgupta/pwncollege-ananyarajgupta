# 1.	cat: not the pet, but the command!
Using cat command

## My solve

**Flag:** `pwn.college{kAuZ0c5cbGEvLImg_Ml1XYcIgB7.QXxcTN0wSM1gjNzEzW}`
``` bash 
cat flag
pwn.college{kAuZ0c5cbGEvLImg_Ml1XYcIgB7.QXxcTN0wSM1gjNzEzW}
```

I navigated to the flag file in home directory using ~/flag and got flag


## What I learned
To use cat command to read out files
PS : cat can concatenate files

## References 
Video in pwn.college

# 2.	catting absolute paths
to read flag from /flag which is an absolute path

## My solve
**Flag:** `pwn.college{cwoxK5d53Ndo-iJDW0V3d7KSV9D.QX5ETO0wSM1gjNzEzW}`
``` bash 
cat /flag 
pwn.college{cwoxK5d53Ndo-iJDW0V3d7KSV9D.QX5ETO0wSM1gjNzEzW}
```


I tried home/hacker/flag which was wrong as /flag does not exist in home directory , it exists in the root directory as /flag


## What I learned
to cat using absolute path

## References 
Video in pwn.college

# 3.	more catting practice
using absolute path, find the flag

## My solve

**Flag:** `pwn.college{AX_eGjxQ87p4P3VF7cnUDHtctI_.QXwITO0wSM1gjNzEzW}`

``` bash 
cat /bin/X11/flag pwn.college{AX_eGjxQ87p4P3VF7cnUDHtctI_.QXwITO0wSM1gjNzEzW}
```
wrote /bin/X11/flag as the absolute path to get to the directory

## What I learned
to write absolute path without using cd, Even if I was in some other directory, I would be able to access the flag as /bin/X11/flag is an absolute path

## References 
Video in pwn.college

# 4.	grepping for a needle in haystack
to use grep to find flag

## My solve

**Flag:** `pwn.college{cvofwotRzzd5DlvzkZpXz3ptUEX.QX3EDO0wSM1gjNzEzW}`
``` bash 
grep pwn.college /challenge/data.txt
pwn.college{cvofwotRzzd5DlvzkZpXz3ptUEX.QX3EDO0wSM1gjNzEzW}
```

searched for pwn.college as flag starts with it and then wrote path to flag



## What I learned
Familiarsing with grep

## References 
Video in pwn.college

# 5.	comparing files
To find difference in two files and get the real flag which is the difference


## My solve

**Flag:** `pwn.college{U3geUbpXZjkoFbjPYzT_nsvgbRG.01MwMDOxwSM1gjNzEzW}`

``` bash 
diff /challenge/decoys_only.txt /challenge/decoys_and_real.txt
53a54
> pwn.college{U3geUbpXZjkoFbjPYzT_nsvgbRG.01MwMDOxwSM1gjNzEzW}
```


got 25a26 which would mean after 25th line in fake file, there is a 26th line which contains the real flag in 26th line on fake and real file

## What I learned
 2c2 – line 2 has changed <first file content,  >second file content, 1a2 after line of file 1, there is an added line 2 in file 2

## References 
Video in pwn.college

# 6.	listing files
se ls to see the file name and then find flag

## My solve

**Flag:** `pwn.college{cE6h_ry4f44COQfis6IBxlXX5ni.QX4IDO0wSM1gjNzEzW}`
``` bash
ls /challenge
6309-renamed-run-14222  DESCRIPTION.md
hacker@commands~listing-files:~$ cat /challenge/6309-renamed-run-14222
#!/opt/pwn.college/bash

echo "Yahaha, you found me! Here is your flag:"
cat /flag
hacker@commands~listing-files:~$ /challenge/6309-renamed-run-14222
Yahaha, you found me! Here is your flag:
pwn.college{cE6h_ry4f44COQfis6IBxlXX5ni.QX4IDO0wSM1gjNzEzW}
```


used ls to find the name of the file – and then came to the file to find flag

## What I learned
using ls to list files in a directory

## References 
Video in pwn.college

# 7.	touching files
To create two files in a directory tmp

## My solve

**Flag:** `pwn.college{sguE8ftsIkgylYmXBEyVIIREQqx.QXwMDO0wSM1gjNzEzW}`
``` bash
touch /tmp/pwn
hacker@commands~touching-files:~$ touch /tmp/college
hacker@commands~touching-files:~$ /challenge/run
Success! Here is your flag:
pwn.college{sguE8ftsIkgylYmXBEyVIIREQqx.QXwMDO0wSM1gjNzEzW}
```


using touch pwn and touch college, create two file touch and college, ran /challenge/run to get flag


## What I learned
touch commands creates a file

## References 
Video in pwn.college

# 8.	removing files
to  delete files
##My Solve
**Flag:** `pwn.college{MZWiR-x4WiaQn9IfVTkywR88Sze.QX2kDM1wSM1gjNzEzW}`
``` bash 
ls
delete_me  not-the-flag  p
hacker@commands~removing-files:~$ rm delete_me
hacker@commands~removing-files:~$ /challenge/check
Excellent removal. Here is your reward:
pwn.college{MZWiR-x4WiaQn9IfVTkywR88Sze.QX2kDM1wSM1gjNzEzW}
```
used rm command to delete delete_me and then challenge/check to check it


## What I learned
rm – used to delete files from directory

## References 
Video in pwn.college

# 9.	moving files
To move flag file to hack the planet


## My solve

**Flag:** `pwn.college{shg-RZKv_pkS5IW9i1vy0pPox5u.0VOxEzNxwSM1gjNzEzW}`
``` bash
mv /flag /tmp/hack-the-planet
Correct! Performing 'mv /flag /tmp/hack-the-planet'.
hacker@commands~moving-files:~$ /challenge/check
Congrats! You successfully moved the flag to /tmp/hack-the-planet! Here it is:
pwn.college{shg-RZKv_pkS5IW9i1vy0pPox5u.0VOxEzNxwSM1gjNzEzW}
```


wrote mv /flag /tmp/hack-the-planet and then checked to get flag

## What I learned
in the example given, writing  mv my-file your-file was sufficient because both are in the same current directory. However, in the case of question /flag originates from root /tmp/hack-the planet is intemp directory so specify the source properly

## References 
Video in pwn.college

# 10.	hidden files
Find flag in dot file


## My solve

**Flag:** `pwn.college{0iMNsCpgQvxFFpRk16DcYH4S_Kb.QXwUDO0wSM1gjNzEzW}`

``` bash 
ls /
bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ ls -a /
.   .dockerenv          bin   challenge  etc   lib    lib64   media  nix  proc  run   srv  tmp  var
..  .flag-683140429131  boot  dev        home  lib32  libx32  mnt    opt  root  sbin  sys  usr
hacker@commands~hidden-files:~$ /.flag-683140429131
bash: /.flag-683140429131: Permission denied
hacker@commands~hidden-files:~$ cat /.flag-683140429131
pwn.college{0iMNsCpgQvxFFpRk16DcYH4S_Kb.QXwUDO0wSM1gjNzEzW}
```


went into /, checked using ls -a , found flag file, viewed it using cat to find flag


## What I learned
files that start with . are hidden , we need to use ls -a to view them


## References 
Video in pwn.college

# 11.	An epic filesystem quest
What it asks: using, cat, ls, using cd, without using cd, ls -a, find flag, move around and search clues

## My solve

**Flag:** `pwn.college{kXJM9KKOlz_AdWbZVvpuPhwBfle.QX5IDO0wSM1gjNzEzW}`


used the commands learned to navigate around


## What I learned
if you can’t use cd to go to that directory and then file, view that file using absolute path and using cat

## References 
Video in pwn.college

# 12.	Making directories
To make a directory in a directory and add a new file to it

## My solve

**Flag:** `pwn.college{o5frfvgf8wuE9DdHtpV6gE_MHXW.QXxMDO0wSM1gjNzEzW}`
``` bash 
mkdir /tmp/pwn
hacker@commands~making-directories:~$ cd /tmp/pwn
hacker@commands~making-directories:/tmp/pwn$ touch college
hacker@commands~making-directories:/tmp/pwn$ /challenge/run
Success! Here is your flag:
pwn.college{o5frfvgf8wuE9DdHtpV6gE_MHXW.QXxMDO0wSM1gjNzEzW}
```


used mkdir to make directory then used touch to create a new file


## What I learned
using mkdir

## References 
Video in pwn.college

# 13. Finding Files
to find flag from a random directory

## My solve

**Flag:** `pwn.college{Mz_UftGizdJD54ombEaBX5qgAFF.QXyMDO0wSM1gjNzEzW}`
``` bash 
cat ./opt/busybox/busybox-1.33.2/include/config/debug/flag
pwn.college{Mz_UftGizdJD54ombEaBX5qgAFF.QXyMDO0wSM1gjNzEzW}hacker@commands~finding-files:/$
```


went to /, typed find -type f -name flag (specifically searched for file called flag of type file)


## What I learned
find flag is incorrect, it searches for directory name flag, to search for file named flag use find -name flag

## References 
Video in pwn.college

# 14.	Linking Files
To find /flag through symbolic link


## My solve

**Flag:** `pwn.college{Uw6shoel3J-g3YA9MvPMShKGI9K.QX5ETN1wSM1gjNzEzW}`
``` bash
rm /home/hacker/not-the-flag
hacker@commands~linking-files:~$ ln -s /flag /home/hacker/not-the-flag
How I solved: delete /home/hacker/not-the-flag , linked /flag to it and then ran /challenge/catflag
/challenge/catflag
About to read out the /home/hacker/not-the-flag file!
pwn.college{Uw6shoel3J-g3YA9MvPMShKGI9K.QX5ETN1wSM1gjNzEzW}
```



## What I learned
to make a link, delete the file at that path first

## References 
Video in pwn.college

