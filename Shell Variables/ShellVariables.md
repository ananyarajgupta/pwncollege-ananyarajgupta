# 1.	Printing Variables
To print variables in shell

## My solve

**Flag:** ` pwn.college{kJ14bYG-_5Cm_2pFf0GVrGEhOFZ.QX3UTN0wSM1gjNzEzW}`
``` bash 
hacker@variables~printing-variables:~$ echo $FLAG
pwn.college{kJ14bYG-_5Cm_2pFf0GVrGEhOFZ.QX3UTN0wSM1gjNzEzW}
```

Used echo with $ to print variable


## What I learned
To print variables

## References 
Video in pwn.college

# 2.	Setting Variables
To give values to variables

## My solve
**Flag:** ` pwn.college{kI5Dbi1jHUXni5vOqwkKwTb8dUP.QX5UTN0wSM1gjNzEzW}`
``` bash 
hacker@variables~setting-variables:~$ PWN=COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{kI5Dbi1jHUXni5vOqwkKwTb8dUP.QX5UTN0wSM1gjNzEzW}
```

Gave the value to VAR and got the flag

## What I learned
to give value to variables, do it without spaces , otherwise command line will think it’s a command

## References 
Video in pwn.college

# 3.	Multiword Variables
To set multiword variables

## My solve

**Flag:** ` pwn.college{crBWvktFWq6q3wth8z_xyYNVLqA.QXwYTN0wSM1gjNzEzW}`
``` bash 
Connected!
hacker@variables~multi-word-variables:~$ PWN="COLLEGE YEAH"
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{crBWvktFWq6q3wth8z_xyYNVLqA.QXwYTN0wSM1gjNzEzW}
```
Put the value as it is multiword under quotes

## What I learned
To set a multi-word token as the value to varable use dounble quotes, other wise command line will think when it encounters a space that things written after space are command 

## References 
Video in pwn.college

# 4.	Exporting Variables
to export variables to other commands

## My solve
**Flag:** ` pwn.college{gDFXmcCvGbZP8RGCqAPCXrAcgD0.QXyYTN0wSM1gjNzEzW}`
``` bash 
Connected!
hacker@variables~exporting-variables:~$ PWN=COLLEGE
You've set the PWN variable to the proper value!
hacker@variables~exporting-variables:~$ COLLEGE=PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ export PWN
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /chhalenge/run
bash: /chhalenge/run: No such file or directory
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
hacker@variables~exporting-variables:~$ /challenge/run
CORRECT!
You have exported PWN=COLLEGE and set, but not exported, COLLEGE=PWN. Great
job! Here is your flag:
pwn.college{gDFXmcCvGbZP8RGCqAPCXrAcgD0.QXyYTN0wSM1gjNzEzW}
You've set the PWN variable to the proper value!
You've set the COLLEGE variable to the proper value!
```

Exported PWN variable and not command variable and got the value

## What I learned
Variables are local to shell process, they need to be exported to other commands to use them there

## References 
Video in pwn.college

# 5.	Printing Exported Varaible
To print exported variables

## My solve

**Flag:** ` pwn.college{cdULJXop2wt7y3nOAmj5PEerjLX.QX4UTN0wSM1gjNzEzW}`

``` bash 
Connected!
hacker@variables~printing-exported-variables:~$ env
SHELL=/run/dojo/bin/bash
HOSTNAME=variables~printing-exported-variables
PWD=/home/hacker
MANPATH=/run/dojo/share/man:
DOJO_AUTH_TOKEN=366666141f5cd26eabe6eba402eaf2e03a1ee52b29516d4462f2daec0e04dafc
HOME=/home/hacker
LANG=C.UTF-8
FLAG=pwn.college{cdULJXop2wt7y3nOAmj5PEerjLX.QX4UTN0wSM1gjNzEzW}
TERMINFO=/run/dojo/share/terminfo
TERM=xterm-256color
SHLVL=2
LC_CTYPE=C.UTF-8
SSL_CERT_FILE=/run/dojo/etc/ssl/certs/ca-bundle.crt
PATH=/run/challenge/bin:/run/dojo/bin:/root/.cargo/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
DEBIAN_FRONTEND=noninteractive
_=/run/dojo/bin/env
```

Ran env command to see exported variables, flag was one of them
## What I learned
env command prints out all the exported variables

## References 
Video in pwn.college

# 6.	Storing Command Output
To store the output of a command in variable

## My solve

**Flag:** ` pwn.college{IWJ81Mik96JVLOpQfSsQqIsbjME.QX1cDN1wSM1gjNzEzW}`
``` bash
Connected!
hacker@variables~storing-command-output:~$ PWN=$(/challenge/run)
Congratulations! You have read the flag into the PWN variable. Now print it out
and submit it!
hacker@variables~storing-command-output:~$ echo PWN
PWN
hacker@variables~storing-command-output:~$ echo $PWN
pwn.college{IWJ81Mik96JVLOpQfSsQqIsbjME.QX1cDN1wSM1gjNzEzW}
```
Stored the output of command in PWN and then printed variable pwn

## What I learned
To store output of a command in a varaible and print it using variable 

## References 
Video in pwn.college

# 7.	Reading Input
To read input from user

## My solve

**Flag:** ` pwn.college{UyP4vXM-WR9FAmxd6a2ReM2Dk2A.QX4cTN0wSM1gjNzEzW}`
``` bash
hacker@variables~reading-input:~$ read -p "INPUT: " PWN
INPUT: COLLEGE
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{UyP4vXM-WR9FAmxd6a2ReM2Dk2A.QX4cTN0wSM1gjNzEzW}
```
Read COLLEGE into the variable PWN


## What I learned
To read values into variables 

## References 
Video in pwn.college

# 8.	Reading Files
to  read files and assign them as input to be read
##My Solve
**Flag:** ` pwn.college{UgbhVQQKhihabkB3cE7tAMjaoNy.QXwIDO0wSM1gjNzEzW}`
``` bash 
Connected!
hacker@variables~reading-files:~$ read PWN < /challenge/read_me
You've set the PWN variable properly! As promised, here is the flag:
pwn.college{UgbhVQQKhihabkB3cE7tAMjaoNy.QXwIDO0wSM1gjNzEzW}
```
Firstly , I redirecrected the content of read me file as input to read command which read it into PWN variable 

## What I learned
To read files and use them in variables

## References 
Video in pwn.college

