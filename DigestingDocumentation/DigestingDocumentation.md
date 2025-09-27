# 1. Learning from Documentation
To read documentation and find flag
**Flag:**` pwn.college{QLyRSdPSoqY9MIXqWJKOJSW_W1j.QX0ITO0wSM1gjNzEzW}`
``` bash
 /challenge/challenge --giveflag
Correct argument! Here is your flag:
pwn.college{QLyRSdPSoqY9MIXqWJKOJSW_W1j.QX0ITO0wSM1gjNzEzW}
```
How I solved: Read documentation, passed argument –giveflag to the program , got the flag
## What I learned
Read documentation, passed argument –giveflag to the program , got the flag

## References 
Video in pwn.college

# 2. Learning Complex Usage
What it asks: to pass an argument to /challenge/challenge and print flag
**Flag:** `pwn.college{YJLSrDNGrlbznwMkBkx-vqeiqfR.QX1ITO0wSM1gjNzEzW}`
 ``` bash 
 /challenge/challenge --printfile /flag
Correct argument! Here is the /flag file:
pwn.college{YJLSrDNGrlbznwMkBkx-vqeiqfR.QX1ITO0wSM1gjNzEzW}
```
Passed correct argument


## What I learned
I learned to pass an argument to the argument of a program

## References 
Video in pwn.college

# 4.	Reading Manuals
What it asks: To read manual, get flag

## My solve

**Flag:** `pwn.college{MpfSIQDqu2fJNC6FIxHI7AR4VQm.QX0EDO0wSM1gjNzEzW}`

``` bash 
man challenge
hacker@man~reading-manuals:~$ /challenge/challenge --pfqufx 267
Correct usage! Your flag: pwn.college{MpfSIQDqu2fJNC6FIxHI7AR4VQm.QX0EDO0wSM1gjNzEzW}
```

read the manual, found the argument for the program, passed it to run the program

## What I learned
to read manuals 

## References 
Video in pwn.college

# 5.	Searching Manuals
What it asks: to search in manuals


## My solve

**Flag:** `pwn.college{QmI_bpewv4KL5uP-FZj4njBFE9w.QX1EDO0wSM1gjNzEzW}`
```bash man challenge
hacker@man~searching-manuals:~$ /challenge/challenge --uh
Initializing...
Correct usage! Your flag: pwn.college{QmI_bpewv4KL5uP-FZj4njBFE9w.QX1EDO0wSM1gjNzEzW}
```


searched in manual for flag, found argument –-uh , passed it to program



## What I learned
to search manuals

## References 
Video in pwn.college

# 6.	Searching for Manuals
What it asks: to read man of man to find man of /challenge/challenge


## My solve

**Flag:** `pwn.college{E9EY5EIiPh4uh8OQZCAMGuOexUf.QX2EDO0wSM1gjNzEzW}`

``` bash man man
hacker@man~searching-for-manuals:~$ man /challenge/challenge
man: can't open /challenge/challenge: Permission denied
hacker@man~searching-for-manuals:~$ man --wildcard "*challenge*"
hacker@man~searching-for-manuals:~$ /challenge/challenge -ihuhue 954
Incorrect usage! Please read the hidden challenge man page!
hacker@man~searching-for-manuals:~$ man --wildcard "*challenge*"
hacker@man~searching-for-manuals:~$ /challenge/challenge --ihuhue 954
Correct usage! Your flag: pwn.college{E9EY5EIiPh4uh8OQZCAMGuOexUf.QX2EDO0wSM1gjNzEzW}
```

 found wildcard *challenge* , it gave me man that had challenge manual page 

## What I learned
to search for manuals

## References 
Video in pwn.college

# Helpful Programs
What it asks: to used --help


## My solve

**Flag:** `pwn.college{soDC4IyFsQx4oAWd1vTxdu_iw8l.QX3IDO0wSM1gjNzEzW}`
``` bash
/challenge/challenge --help
usage: a challenge to make you ask for help [-h] [--fortune] [-v] [-g GIVE_THE_FLAG] [-p]

optional arguments:
  -h, --help            show this help message and exit
  --fortune             read your fortune
  -v, --version         get the version number
  -g GIVE_THE_FLAG, --give-the-flag GIVE_THE_FLAG
                        get the flag, if given the correct value
  -p, --print-value     print the value that will cause the -g option to give you the flag
hacker@man~helpful-programs:~$ /challenge/challenge -v
I'm exactly the version I need to be!
hacker@man~helpful-programs:~$ /challenge/challenge -g -p
You passed -p as an argument to -g! Please read the usage
carefully: -g takes *its own* numerical argument.
hacker@man~helpful-programs:~$ /challenge/challenge -p
The secret value is: 441
hacker@man~helpful-programs:~$ /challenge/challenge -g 441
Correct usage! Your flag: pwn.college{soDC4IyFsQx4oAWd1vTxdu_iw8l.QX3IDO0wSM1gjNzEzW}

```


passed argument –help to challenge to find arguments of the program to find flag

## What I learned
learned to use help

## References 
Video in pwn.college

# 8.	Help for Builtins
to use help command for shell builtin command

## My solve

**Flag:** `pwn.college{YvHBpMvol4LUiPkpEoiOqmOnB26.QX0ETO0wSM1gjNzEzW}`
``` bash
``` help challenge
challenge: challenge [--fortune] [--version] [--secret SECRET]
    This builtin command will read you the flag, given the right arguments!

    Options:
      --fortune         display a fortune
      --version         display the version
      --secret VALUE    prints the flag, if VALUE is correct

    You must be sure to provide the right value to --secret. That value
    is "YvHBpMvo".
hacker@man~help-for-builtins:~$ challenge --secret YvHBpMvo
Correct! Here is your flag!
pwn.college{YvHBpMvol4LUiPkpEoiOqmOnB26.QX0ETO0wSM1gjNzEzW}
```

challenge is a shell builtin, wrote help challenge to get information and get flag


## What I learned
to get help for builtin commands

## References 
Video in pwn.college

