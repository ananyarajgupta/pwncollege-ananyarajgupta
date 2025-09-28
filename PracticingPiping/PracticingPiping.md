# 1.	Redirecting Output
Redirecting output to another file

## My solve

**Flag:** ` pwn.college{UsgpHD09s6qaIXr4E-rK2upPu3-.QX0YTN0wSM1gjNzEzW}`
``` bash 
hacker@piping~redirecting-output:~$ echo PWN > COLLEGE
Correct! You successfully redirected 'PWN' to the file 'COLLEGE'! Here is your
flag:
pwn.college{UsgpHD09s6qaIXr4E-rK2upPu3-.QX0YTN0wSM1gjNzEzW}
```

Used > to redirect file


## What I learned
Using > to redirect output

## References 
Video in pwn.college

# 2.	Redirecting more output
to redirect output of /challenge/run program

## My solve
**Flag:** ` pwn.college{wc14c9bb0TsEqmv6suN3p1QI2gB.QX1YTN0wSM1gjNzEzW}`
``` bash 
Connected!
hacker@piping~redirecting-more-output:~$ /challenge/run > myflag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-more-output:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{wc14c9bb0TsEqmv6suN3p1QI2gB.QX1YTN0wSM1gjNzEzW}
```


Shifted the flag to myflag file and then cat that file

## What I learned
to redirect output of different commands

## References 
Video in pwn.college

# 3.	Appending Output
Using >> to append my output

## My solve

**Flag:** ` pwn.college{gIEhzQuBXSjRT_rKGvVt2W8FqzL.QX3ATO0wSM1gjNzEzW}`
``` bash 
hacker@piping~appending-output:~$ /challenge/run >> ~/the-flag
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /home/hacker/the-flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] Good luck!

[TEST] You should have redirected my stdout to a file called /home/hacker/the-flag. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
I will write the flag in two parts to the file /home/hacker/the-flag! I'll do
the first write directly to the file, and the second write, I'll do to stdout
(if it's pointing at the file). If you redirect the output in append mode, the
second write will append to (rather than overwrite) the first write, and you'll
get the whole flag!
hacker@piping~appending-output:~$ cat ~/the-flag
 |
\|/ This is the first half:
 v
pwn.college{gIEhzQuBXSjRT_rKGvVt2W8FqzL.QX3ATO0wSM1gjNzEzW}
                              ^
     that is the second half /|\
                              |

If you only see the second half above, you redirected in *truncate* mode (>)
rather than *append* mode (>>), and so the write of the second half to stdout
overwrote the initial write of the first half directly to the file. Try append
mode!
```
~/the-flag had first half of file and /challenge/run had second half, appened to get the final result

## What I learned
To append output

## References 
Video in pwn.college

# 4.	Redirecting Errors
to redirect errors and outputs

## My solve
**Flag:** ` pwn.college{kPUAczVYEbhyzJme8OIG4PNUWiD.QX3YTN0wSM1gjNzEzW}`
``` bash 
hacker@piping~redirecting-errors:~$ /challenge/run > myflag 2> instructions
hacker@piping~redirecting-errors:~$ cat instructions
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : myflag
[INFO] - the challenge will check that error output is redirected to a specific file path : instructions
[INFO] - the challenge will output a reward file if all the tests pass : /flag

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /flag file.

[TEST] You should have redirected my stdout to a file called myflag. Checking...

[PASS] The file at the other end of my stdout looks okay!

[TEST] You should have redirected my stderr to instructions. Checking...

[PASS] The file at the other end of my stderr looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~redirecting-errors:~$ cat myflag

[FLAG] Here is your flag:
[FLAG] pwn.college{kPUAczVYEbhyzJme8OIG4PNUWiD.QX3YTN0wSM1gjNzEzW}
```

Redirected output and error to different files

## What I learned
To redirect outputs and errors produces using > and 2> respectively

## References 
Video in pwn.college

# 5.	Redirecting Input
To redirect input to different files

## My solve

**Flag:** ` pwn.college{U4AcGrr289j1vSaBu0DRm7OUEbA.QXwcTN0wSM1gjNzEzW}`

``` bash 
hacker@piping~redirecting-input:~$ echo COLLEGE > PWN
hacker@piping~redirecting-input:~$ /challenge/run < PWN
Reading from standard input...
Correct! You have redirected the PWN file into my standard input, and I read
the value 'COLLEGE' out of it!
Here is your flag:
pwn.college{U4AcGrr289j1vSaBu0DRm7OUEbA.QXwcTN0wSM1gjNzEzW}
```

Redirected output to PWN file and then redirected input to PWN

## What I learned
Redirecting input to different files

## References 
Video in pwn.college

# 6.	Grepping Stored Results
Used redirecting and grep

## My solve

**Flag:** ` pwn.college{8wDwfD3JXa-A64VXH-XyYT4Lv57.QX4EDO0wSM1gjNzEzW}`
``` bash
Connected!
hacker@piping~grepping-stored-results:~$ /challenge/run > /tmp/data.txt
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge will check that output is redirected to a specific file path : /tmp/data.txt
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to a file called /tmp/data.txt. Checking...

[HINT] File descriptors are inherited from the parent, unless the FD_CLOEXEC is set by the parent on the file descriptor.
[HINT] For security reasons, some programs, such as python, do this by default in certain cases. Be careful if you are
[HINT] creating and trying to pass in FDs in python.

[PASS] The file at the other end of my stdout looks okay!
[PASS] Success! You have satisfied all execution requirements.
hacker@piping~grepping-stored-results:~$ grep "pwn.college" /tmp/data.txt
pwn.college{8wDwfD3JXa-A64VXH-XyYT4Lv57.QX4EDO0wSM1gjNzEzW}
```
Redirected output of the program and then grep the flag

## What I learned
To redirect output and grep required flag

## References 
Video in pwn.college

# 7.	Grepping Live Output
Using |

Used | to redirect output and grep “pwn.college” , then cat that flag

## My solve

**Flag:** ` pwn.college{4u-jdlimNSRaW5tXq2qO5Zpkl59.QX5EDO0wSM1gjNzEzW}`
``` bash
Connected!
hacker@piping~grepping-live-output:~$ /challenge/run | grep "pwn.college"
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stdout : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stdout to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stdout!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{4u-jdlimNSRaW5tXq2qO5Zpkl59.QX5EDO0wSM1gjNzEzW}
```



## What I learned
To use pipe command

## References 
Video in pwn.college

# 8.	Grepping Errors
to  grep errors
##My Solve
**Flag:** ` pwn.college{g_t-rhfdcBQRFNzldv8e2C9ZOp0.QX1ATO0wSM1gjNzEzW}`
``` bash 
Connected!
hacker@piping~grepping-errors:~$ /challenge/run 2>& 1 | grep "pwn.college"
[INFO] WELCOME! This challenge makes the following asks of you:
[INFO] - the challenge checks for a specific process at the other end of stderr : grep
[INFO] - the challenge will output a reward file if all the tests pass : /challenge/.data.txt

[HYPE] ONWARDS TO GREATNESS!

[INFO] This challenge will perform a bunch of checks.
[INFO] If you pass these checks, you will receive the /challenge/.data.txt file.

[TEST] You should have redirected my stderr to another process. Checking...
[TEST] Performing checks on that process!

[INFO] The process' executable is /nix/store/8b4vn1iyn6kqiisjvlmv67d1c0p3j6wj-gnugrep-3.11/bin/grep.
[INFO] This might be different than expected because of symbolic links (for example, from /usr/bin/python to /usr/bin/python3 to /usr/bin/python3.8).
[INFO] To pass the checks, the executable must be grep.

[PASS] You have passed the checks on the process on the other end of my stderr!
[PASS] Success! You have satisfied all execution requirements.
pwn.college{g_t-rhfdcBQRFNzldv8e2C9ZOp0.QX1ATO0wSM1gjNzEzW}
```
Firstly I redirect the stderror to stdout then use pipe and then grep to get flag from error

## What I learned
To grep through stderror

## References 
Video in pwn.college

# 9.	Filtering with grep v
To use grep v to exclude lines containing that word

## My solve

**Flag:** ` pwn.college{U-fUdxbaXXXbyFtdINfVEpx_IyG.0FOxEzNxwSM1gjNzEzW}`
``` bash
Connected!
hacker@piping~filtering-with-grep-v:~$ /challenge/run | grep -v DECOY
pwn.college{U-fUdxbaXXXbyFtdINfVEpx_IyG.0FOxEzNxwSM1gjNzEzW}
```


Excluded decoy lines and got the line with flag

## What I learned
To use grep -v to exclude lines

## References 
Video in pwn.college

# 10.	Duplicating piped data with tee
Using tee

## My solve

**Flag:** ` pwn.college{s41Ievbs9wx6zVM7yvmzmhtFLQ2.QXxITO0wSM1gjNzEzW}`
``` bash 
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn | tee output | /challenge/college
Processing...
WARNING: you are overwriting file output with tee's output...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ cat output
Usage: /challenge/pwn --secret [SECRET_ARG]

SECRET_ARG should be "s41Ievbs"
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret [s41Ievbs] | /challenge/college
Processing...
The input to 'college' does not contain the correct secret code! This code
should be provided by the 'pwn' command. HINT: use 'tee' to intercept the
output of 'pwn' and figure out what the code needs to be.
hacker@piping~duplicating-piped-data-with-tee:~$ /challenge/pwn --secret s41Ievbs | /challenge/college
Processing...
Correct! Passing secret value to /challenge/college...
Great job! Here is your flag:
pwn.college{s41Ievbs9wx6zVM7yvmzmhtFLQ2.QXxITO0wSM1gjNzEzW}
```
Used tee to find what pwn wanted, it wanted an argument, passed it and redirected content to command and then got flag

## What I learned
To use tee to look at the flow of commands

## References 
Video in pwn.college

# 11.	Process substitution for Input
Using <(command) 

## My solve

**Flag:** ` pwn.college{oTFXPHX17z_lonGgnwKguOhJ3dh.0lNwMDOxwSM1gjNzEzW}`
```bash
Connected!
hacker@piping~process-substitution-for-input:~$ diff </challenge/print_decoys </challenge/print_decoys_and_flag
diff: missing operand after 'diff'
diff: Try 'diff --help' for more information.
hacker@piping~process-substitution-for-input:~$ diff <(/challenge/print_decoys) <(/challenge/print_decoys_and_flag)
60a61
> pwn.college{oTFXPHX17z_lonGgnwKguOhJ3dh.0lNwMDOxwSM1gjNzEzW}
```

Used <(command) to find difference between two files’ output


## What I learned
<(command) creates a piped file which is not a real file and stores the ouput of the command there, this file can be used to run commands on

## References 
Video in pwn.college

# 12.	Writing to Multiple Programs
Using tee to duplicate the output as input to other programs

## My solve

**Flag:** ` pwn.college{4bGIryfWWR9xbEHRIJkwNKF9WdB.QXwgDN1wSM1gjNzEzW}`
``` bash 
Connected!
hacker@piping~writing-to-multiple-programs:~$ /challenge/hack | tee >(/challenge/the) >(/challenge/planet)
This secret data must directly and simultaneously make it to /challenge/the and
/challenge/planet. Don't try to copy-paste it; it changes too fast.
11403327491753419400
Congratulations, you have duplicated data into the input of two programs! Here
is your flag:
pwn.college{4bGIryfWWR9xbEHRIJkwNKF9WdB.QXwgDN1wSM1gjNzEzW}
```

Piped the output of /challenge/hack to tee, then gave that as input to /challenge/the and /challenge/planet


## What I learned
Using process substitution for writing commands

## References 
Video in pwn.college

# 13. Split piping stderr and stdout
To redirect stderr and stdout to two different files

## My solve

**Flag:** ` pwn.college{s6d-E7t3p7oKQZWrkkE_WDxJKT1.QXxQDM2wSM1gjNzEzW}`
``` bash 
hacker@piping~split-piping-stderr-and-stdout:~$ /challenge/hack 2>&1 | /challenge/the | /challenge/hack | /challenge/planet
You must redirect my standard error into '/challenge/the'!
Congratulations, you have learned a redirection technique that even experts
struggle with! Here is your flag:
pwn.college{s6d-E7t3p7oKQZWrkkE_WDxJKT1.QXxQDM2wSM1gjNzEzW}
```

Firstly piped stderr of /challenge/hack to /challenge/the , then stdout to /challenge/planet

## What I learned
To split piping of stdout and stderr

## References 
Video in pwn.college

# 14.	Named Pipes
To name my pipes


## My solve

**Flag:** ` pwn.college{UfCPnaeGbYfibK0sW2SP8VjstA8.01MzMDOxwSM1gjNzEzW}`
``` bash
hacker@piping~named-pipes:~$ mkfifo /tmp/flag_fifo
hacker@piping~named-pipes:~$ /challenge/run > /tmp/flag_fifo
You're successfully redirecting /challenge/run to a FIFO at /tmp/flag_fifo!
Bash will now try to open the FIFO for writing, to pass it as the stdout of
/challenge/run. Recall that operations on FIFOs will *block* until both the
read side and the write side is open, so /challenge/run will not actually be
launched until you start reading from the FIFO!
hacker@piping~named-pipes:~$ cat /tmp/flag_fifo 
You've correctly redirected /challenge/run's stdout to a FIFO at 
/tmp/flag_fifo! Here is your flag:
pwn.college{UfCPnaeGbYfibK0sW2SP8VjstA8.01MzMDOxwSM1gjNzEzW}
```
Redirected output to pipe flag file, then cat that file using two terminals

## What I learned
FIFO (First byte in First Byte Out)
Command used to name pipes - mkfifo

## References 
Video in pwn.college

