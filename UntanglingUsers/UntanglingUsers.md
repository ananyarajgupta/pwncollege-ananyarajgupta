# 1.	Becoming root with su
To become root using su command

## My solve

**Flag:** ` pwn.college{kAuZ0c5cbGEvLImg_Ml1XYcIgB7.QXxcTN0wSM1gjNzEzW}`
``` bash 
root@users~becoming-root-with-su:/home/hacker#
Connected!
hacker@users~becoming-root-with-su:~$ su
Password:
root@users~becoming-root-with-su:/home/hacker# ls
COLLEGE  PWN  flag  instructions  myflag  not-the-fla  not-the-flag  not-the-glag  output  p  t  the-flag
root@users~becoming-root-with-su:/home/hacker# cat not-the-flag
pwn.college{MtXVaH8dAYpzzAXrQ_p7Y_k5uMj.QX1UDN1wSM1gjNzEzW}
```

Ran su command, entered password and then came into root and then cat not-the-flag


## What I learned
su is an ancient command which requires root password to grant access to root, this method is not used anymore

 

## References 
Video in pwn.college

# 2.	Other users with su
To access other users with su

## My solve
**Flag:**` pwn.college{EqQPJzN777T7Uudez2bfDOlUT6L.QX2UDN1wSM1gjNzEzW}`
``` bash 
Connected!
hacker@users~other-users-with-su:~$ su zardus
Password:
zardus@users~other-users-with-su:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{EqQPJzN777T7Uudez2bfDOlUT6L.QX2UDN1wSM1gjNzEzW}
```

Passed zardus as an argument to su, entered password and then became the user zardus, ran /challenge/run to get the flag

## What I learned
su can be used to access other users by passing their username as an argument to su and then entering password

## References 
Video in pwn.college

# 3.	Cracking passwords
To crack hashed passwords and become the user

## My solve

**Flag:** pwn.college{YeJJr1K0cJjXtxUyYZdteWf3bbf.QX3UDN1wSM1gjNzEzW}`
``` bash 
Connected!
hacker@users~cracking-passwords:~$ cat /challenge/shadow-leak
root:*:20182:0:99999:7:::
daemon:*:20182:0:99999:7:::
bin:*:20182:0:99999:7:::
sys:*:20182:0:99999:7:::
sync:*:20182:0:99999:7:::
games:*:20182:0:99999:7:::
man:*:20182:0:99999:7:::
lp:*:20182:0:99999:7:::
mail:*:20182:0:99999:7:::
news:*:20182:0:99999:7:::
uucp:*:20182:0:99999:7:::
proxy:*:20182:0:99999:7:::
www-data:*:20182:0:99999:7:::
backup:*:20182:0:99999:7:::
list:*:20182:0:99999:7:::
irc:*:20182:0:99999:7:::
gnats:*:20182:0:99999:7:::
nobody:*:20182:0:99999:7:::
_apt:*:20182:0:99999:7:::
systemd-timesync:*:20357:0:99999:7:::
systemd-network:*:20357:0:99999:7:::
systemd-resolve:*:20357:0:99999:7:::
mysql:!:20357:0:99999:7:::
messagebus:*:20357:0:99999:7:::
sshd:*:20357:0:99999:7:::
hacker::20357:0:99999:7:::
zardus:$6$iV/KeXKqc3CZymqn$3Fr3KrUySIE5OP89wFMzLGB92xHUiXL4GfOWMXmB2qwnR4M2oU1EWH5JRIkzSChA.ga85yzKe2wlSNk5eEu8O0:20364:0:99999:7:::
hacker@users~cracking-passwords:~$ echo '$6$iV/KeXKqc3CZymqn$3Fr3KrUySIE5OP89wFMzLGB92xHUiXL4GfOWMXmB2qwnR4M2oU1EWH5JRIkzSChA.ga85yzKe2wlSNk5eEu8O0' > leaked-file
hacker@users~cracking-passwords:~$ john leaked-file
Loaded 1 password hash (crypt, generic crypt(3) [?/64])
Press 'q' or Ctrl-C to abort, almost any other key for status
0g 0:00:00:08 1% 2/3 0g/s 286.2p/s 286.2c/s 286.2C/s chacha..jazmin
aardvark         (?)
1g 0:00:00:10 100% 2/3 0.09970g/s 287.1p/s 287.1c/s 287.1C/s Johnson..buzz
Use the "--show" option to display all of the cracked passwords reliably
Session completed
hacker@users~cracking-passwords:~$ su zardus
Password:
zardus@users~cracking-passwords:/home/hacker$ /challenge/run
Congratulations, you have become Zardus! Here is your flag:
pwn.college{YeJJr1K0cJjXtxUyYZdteWf3bbf.QX3UDN1wSM1gjNzEzW}
```
Cat the leaked file and got the hashed password file of zardus, stored it in a file and then gave it as an argument to john command which converted it into password, used su to get into zardus and then ran /challenge/run

## What I learned
Passwords used to be stored in /etc/passwd but since it is a global readable file, we store it in /etc/shadow
john command converts hashed passwords to original ones

## References 
Video in pwn.college

# 4.	Using sudo
Using sudo to find flag

## My solve
**Flag:** `pwn.college{kAuZ0c5cbGEvLImg_Ml1XYcIgB7.QXxcTN0wSM1gjNzEzW}`
``` bash 
hacker@users~using-sudo:~$ sudo grep hacker /etc/shadow
hacker::20357:0:99999:7:::
hacker@users~using-sudo:~$ sudo cat flag
pwn.college{kAuZ0c5cbGEvLImg_Ml1XYcIgB7.QXxcTN0wSM1gjNzEzW}
```

## What I learned
In recent time, people don’t used su, instead sudo is used which does not check for password but sudo policies which are defined under /etc/sudoers but grant access

## References 
Video in pwn.college
