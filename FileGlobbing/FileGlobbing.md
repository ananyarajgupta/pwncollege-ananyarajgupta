# 1.	Matching with *
Using * to avoid writing full path

## My solve
**Flag:** ` pwn.college{cLqV-zdJosA78L2T4nUUPWeWN8G.QXxIDO0wSM1gjNzEzW}`
``` bash 
cd /ch*
hacker@globbing~matching-with-:/challenge$ /ch*/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{cLqV-zdJosA78L2T4nUUPWeWN8G.QXxIDO0wSM1gjNzEzW}
```

Used * to cd into Challenge and ran command to get flag

## What I learned
To use * which is wildcard to shorten path

## References 
Video in pwn.college

# 2.	Matching with ?
to read flag from /flag which is an absolute path

## My solve
**Flag:** ` pwn.college{8RsgVeCgn-4dZZ9pDGMBMdaxfdn.QXyIDO0wSM1gjNzEzW}}`
``` bash 
hacker@globbing~matching-with-:~$ cd /?ha??enge
hacker@globbing~matching-with-:/challenge$ /challenge/run
You ran me with the working directory of /challenge! Here is your flag:
pwn.college{8RsgVeCgn-4dZZ9pDGMBMdaxfdn.QXyIDO0wSM1gjNzEzW}
```


replaced c and l with ? to change directory
## What I learned
? is used to math single character wheread * takes multiple characters

## References 
Video in pwn.college

# 3.	Mathcing with []
using absolute path, find the flag

## My solve

**Flag:** ` pwn.college{4SmwnoG2pbubD4KbsZDTszLv49U.QXzIDO0wSM1gjNzEzW}`
``` bash 
hacker@globbing~matching-with-:~$ cd /challenge/files
hacker@globbing~matching-with-:/challenge/files$ /challenge/run file_[absh]
You got it! Here is your flag!
pwn.college{4SmwnoG2pbubD4KbsZDTszLv49U.QXzIDO0wSM1gjNzEzW}
```
Used [] to match with a, b, s , h

## What I learned
[] tries to match with potential characters
## References 
Video in pwn.college

# 4.	Matching paths with []
Use [] to match with paths
## My solve

**Flag:** ` pwn.college{g-fb1LMCkSZ2PsLxO4jjpBjBx7S.QX0IDO0wSM1gjNzEzW}`
``` bash 
hacker@globbing~matching-paths-with-:~$ /challenge/run /challenge/files/file_[absh]
You got it! Here is your flag!
pwn.college{g-fb1LMCkSZ2PsLxO4jjpBjBx7S.QX0IDO0wSM1gjNzEzW}
```

passed argument in challenge/run to paths of challenge/files



## What I learned
Using [] to access paths

## References 
Video in pwn.college

# 5.	Multiple Globs
Using two ** to find files that contain certain phrases or characters

## My solve

**Flag:** ` pwn.college{Qkbh2O6dSl8oawYnyd7iqORG_c-.0lM3kjNxwSM1gjNzEzW}`

``` bash 
hacker@globbing~multiple-globs:/challenge/files$ cd /challenge/files
hacker@globbing~multiple-globs:/challenge/files$ /challenge/run *p*
You got it! Here is your flag!
pwn.college{Qkbh2O6dSl8oawYnyd7iqORG_c-.0lM3kjNxwSM1gjNzEzW}
 ```

Ran a single argument to /challenge/run to find files that have ‘p’ in them

## What I learned
To use multiple globs

## References 
Video in pwn.college

# 6.	Mixing Globs
Using multiple globs to find files

## My solve

**Flag:** ` pwn.college{4XjXkmVifMIcf8j4jJlINkVQPzz.QX1IDO0wSM1gjNzEzW}`
``` bash
hacker@globbing~mixing-globs:/challenge/files$ /challenge/run [cep]*
You got it! Here is your flag!
pwn.college{4XjXkmVifMIcf8j4jJlINkVQPzz.QX1IDO0wSM1gjNzEzW}
```


Used multiple globs to match to the three given file names

## What I learned
Using multiple globs

## References 
Video in pwn.college

# 7.	Exclusionary Globbing
To invert gloabbing and exclude characters from matching

## My solve

**Flag:** ` pwn.college{UiK2Mb0jonK_mAL0b4UjpPicE9t.QX2IDO0wSM1gjNzEzW}`
``` bash
hacker@globbing~exclusionary-globbing:~$ cd /challenge/files
hacker@globbing~exclusionary-globbing:/challenge/files$ /challenge/run [^pwn]*
You got it! Here is your flag!
pwn.college{UiK2Mb0jonK_mAL0b4UjpPicE9t.QX2IDO0wSM1gjNzEzW}
```

Used ^ to exclude pwn from search

## What I learned
Using ^ or ! to exclude characters from search or matching

## References 
Video in pwn.college

# 8.	Tab Completion
to  use tab commands
##My Solve
**Flag:** ` pwn.college{kCw4vbuQ6-NedU0v4tlqvX-EF0w.0FN0EzNxwSM1gjNzEzW}`
``` bash 
hacker@globbing~tab-completion:~$ cat /challenge/pwncollege
pwn.college{kCw4vbuQ6-NedU0v4tlqvX-EF0w.0FN0EzNxwSM1gjNzEzW}
```
used tab to autocomplete filename

## What I learned
To use tab to autocomplete

## References 
Video in pwn.college

# 9.	Multiple Options for Tab Completion
Using tab when there are multiple options

## My solve

**Flag:** `pwn.college{MHBwyzWz0JWs3yVpo5NP51V8nCL.0lN0EzNxwSM1gjNzEzW}`
``` bash
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwn
pwn                    pwn-the-planet         pwncollege-flag        pwncollege-flyswatter
pwn-college            pwncollege-family      pwncollege-flamingo    pwncollege-hacking
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fl
pwncollege-flag        pwncollege-flamingo    pwncollege-flyswatter
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fla
pwncollege-flag      pwncollege-flamingo
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-fla
pwncollege-flag      pwncollege-flamingo
hacker@globbing~multiple-options-for-tab-completion:~$ cat /challenge/files/pwncollege-flag
pwn.college{MHBwyzWz0JWs3yVpo5NP51V8nCL.0lN0EzNxwSM1gjNzEzW}
```


At each stage, got multiple files when pressing tabs, finally arrived at flag

## What I learned
Tab can be used when there are multiple files with similar file names, it will give you multiple options, choose, type and proceed

## References 
Video in pwn.college

# 10.	Tab completion on commands
Using tab to auto-complete commands

## My solve

**Flag:** ` pwn.college{cFy73JI7T6HnnF1DaBVYr1uf2q3.0VN0EzNxwSM1gjNzEzW}`

``` bash 
hacker@globbing~tab-completion-on-commands:~$ pwn
pwn               pwncollege-21946  pwndbg            pwnstrip          pwntools-gdb
hacker@globbing~tab-completion-on-commands:~$ pwncollege-21946
Correct! Here is your flag:
pwn.college{cFy73JI7T6HnnF1DaBVYr1uf2q3.0VN0EzNxwSM1gjNzEzW}
```

Used tab to autocomplete pwncollege command

## What I learned
Tab can be used for commands but we should be careful as double-checking if the command is correct is important.


## References 
Video in pwn.college

