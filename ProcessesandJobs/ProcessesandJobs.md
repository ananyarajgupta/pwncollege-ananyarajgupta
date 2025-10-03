# 1.	Listing Processes
To list the process currently running

## My solve

**Flag:** ` pwn.college{0Z5JlOJIVj_-FDWRxo4kU6NfnG2.QX4MDO0wSM1gjNzEzW}`
``` bash 
Connected!
hacker@processes~listing-processes:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.0  0.0   1056   640 ?        Ss   20:20   0:00 /sbin/docker-init -- /nix/var/nix/profiles/dojo-works
root           7  0.0  0.0 231708  2560 ?        S    20:20   0:00 /run/dojo/bin/sleep 6h
root         132  0.0  0.0   4132  2560 ?        S    20:20   0:00 /challenge/6124-run-4948
root         135  0.0  0.0   2744  1280 ?        S    20:20   0:00 sleep 6h
hacker       146  0.0  0.0  36972 21760 ?        Sl   20:20   0:00 /nix/store/g0q8n7xfjp7znj41hcgrq893a9m0i474-ttyd-1.7.
hacker       150  0.0  0.0 231940  4160 pts/0    Ss+  20:21   0:00 /run/dojo/bin/bash --login
hacker       160  0.1  0.0 231576  2880 pts/1    Ss   20:22   0:00 /nix/store/0nxvi9r5ymdlr2p24rjj9qzyms72zld1-bash-inte
hacker       166  0.0  0.0 231940  4160 pts/1    S    20:22   0:00 /run/dojo/bin/bash --login
hacker       175  0.0  0.0 233600  3840 pts/1    R+   20:22   0:00 ps aux
hacker@processes~listing-processes:~$ /challenge/6124-run-4948
Yahaha, you found me! Here is your flag:
pwn.college{0Z5JlOJIVj_-FDWRxo4kU6NfnG2.QX4MDO0wSM1gjNzEzW}
```

Ran ps aux to list current processes in the terminal, got the name of challenge, found flag by running it


## What I learned
ps -ef and ps aux are used to list processes.
-e means every process and -f means full format so combine them to get -ef

 

## References 
Video in pwn.college

# 2.	Killing Processes
To delete characters

## My solve
**Flag:** ` pwn.college{Q5VkxXOX0vGqKK2RIn57t_rW_1q.QXyQDO0wSM1gjNzEzW}`
``` bash 
root@ANANYASOMU:~# ssh -i key hacker@dojo.pwn.college
Connected!
hacker@processes~killing-processes:~$ ps -e | grep /challenge/dont_run
hacker@processes~killing-processes:~$ ps aux | grep /challenge/dont_run
hacker       136  0.0  0.0 231576  3520 ?        Ss   12:13   0:00 /challenge/dont_run
hacker       180  0.0  0.0 230524  2560 pts/1    R+   12:16   0:00 grep --color=auto /challenge/dont_run
hacker@processes~killing-processes:~$ kill 136
hacker@processes~killing-processes:~$ /challenge/run
Great job! Here is your payment:
pwn.college{Q5VkxXOX0vGqKK2RIn57t_rW_1q.QXyQDO0wSM1gjNzEzW}
```

Found PID using ps -e and then I used it to kill /challenge/don’t_run
Then ran /challenge/run

## What I learned
To use the kill command to stop processes

## References 
Video in pwn.college

# 3.	Interrupting Processes
To interrupt a program from running and make it cleanly exit

## My solve

**Flag:** ` pwn.college{Et-ejZcqDZ7j5i0sGrIuTCZr6Ef.QXzQDO0wSM1gjNzEzW}`
``` bash 
hacker@processes~interrupting-processes:~$ /challenge/run
I could give you the flag... but I won't, until this process exits. Remember,
you can force me to exit with Ctrl-C. Try it now!
^C
Good job! You have used Ctrl-C to interrupt this process! Here is your flag:
pwn.college{Et-ejZcqDZ7j5i0sGrIuTCZr6Ef.QXzQDO0wSM1gjNzEzW}
```
Ran /challenge/run , then used Ctrl C to interrupt it

## What I learned
Ctrl C is used to interrupt programs and stop them from running

## References 
Video in pwn.college

# 4.	Killing misbehaving Processes

## My solve
**Flag:** ` pwn.college{MNEt7lTGBfGZdkA_rAIvjr1Zy7q.0lNxEzNxwSM1gjNzEzW}`
``` bash 
```

## What I learned

## References 
Video in pwn.college

# 5.	Suspending Processes
To suspend a currently running program
## My solve

**Flag:**`pwn.college{A75QqaUzhBetOm37QWKNYuRCCjb.QX1QDO0wSM1gjNzEzW`

``` bash 
Connected!
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         161     129  0 12:46 pts/0    00:00:00 bash /challenge/run
root         163     161  0 12:46 pts/0    00:00:00 ps -f

I don't see a second me!

To pass this level, you need to suspend me and launch me again! You can
background me with Ctrl-Z or, if you're not ready to do that for whatever
reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~suspending-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running in
this terminal... Let's check!

UID          PID    PPID  C STIME TTY          TIME CMD
root         161     129  0 12:46 pts/0    00:00:00 bash /challenge/run
root         168     129  0 12:46 pts/0    00:00:00 bash /challenge/run
root         170     168  0 12:46 pts/0    00:00:00 ps -f

Yay, I found another version of me! Here is the flag:
pwn.college{A75QqaUzhBetOm37QWKNYuRCCjb.QX1QDO0wSM1gjNzEzW}
```
Used ctrl z to suspend run program, ran it again in the terminal to get the flag
## What I learned
Ctrl Z can be used to suspend a currently running program. It is less drastic than Ctrl C.


## References 
Video in pwn.college

# 5.	Resuming Processes
To resume the suspended programs

## My solve

**Flag:** ` pwn.college{8Lb5BbarVFAQZjLduIBmmf6hrRZ.QX2QDO0wSM1gjNzEzW}`
``` bash
Connected!
Connected!
hacker@processes~resuming-processes:~$ /challenge/run
Let's practice resuming processes! Suspend me with Ctrl-Z, then resume me with
the 'fg' command! Or just press Enter to quit me!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~resuming-processes:~$ fg
/challenge/run
I'm back! Here's your flag:
pwn.college{8Lb5BbarVFAQZjLduIBmmf6hrRZ.QX2QDO0wSM1gjNzEzW}
Don't forget to press Enter to quit me!

Goodbye!
```
Used Ctrl-Z to suspend the program , then resumed it using fg to get the flag

## What I learned
fg is a command used to resume the programs which were paused due to Ctrl-Z

## References 
Video in pwn.college

# 6.	Backgrounding Process
To run a program in the background

## My solve

**Flag:** ` pwn.college{wyLyoKelr6Ul_Pg7sotmYFdpkPU.QX3QDO0wSM1gjNzEzW}`
``` bash
hacker@processes~resuming-processes:~$
Connected!
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         162 S+   bash /challenge/run
root         164 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         162 S    bash /challenge/run
root         172 S    sleep 6h
root         173 S+   bash /challenge/run
root         175 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{wyLyoKelr6Ul_Pg7sotmYFdpkPU.QX3QDO0wSM1gjNzEzW}
```
Suspended the /challenge/run program , then ran bg command to run it background and then invoked /challenge/run again


## What I learned
bg command is used to run programs in background

## References 
Video in pwn.college

# 7.	Foregrounding Processes
to  foreground a background process just like we foreground a suspended process
##My Solve
**Flag:** ` pwn.college{MinEl_N8kxfVD2VmL7R9e7KAro6.QX4QDO0wSM1gjNzEzW}`
``` bash 
Connected!
hacker@processes~foregrounding-processes:~$ /challenge/run
To pass this level, you need to suspend me, resume the suspended process in the
background, and *then* foreground it without re-suspending it! You can
background me with Ctrl-Z (and resume me in the background with 'bg') or, if
you're not ready to do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~foregrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~foregrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out. After that, resume me into the foreground with 'fg';
I'll wait.

hacker@processes~foregrounding-processes:~$ fg
/challenge/run
YES! Great job! I'm now running in the foreground. Hit Enter for your flag!

pwn.college{MinEl_N8kxfVD2VmL7R9e7KAro6.QX4QDO0wSM1gjNzEzW}
```
Firstly , I suspended the program, resumed it in background and then foregrounded it

## What I learned
We can foreground a background program

## References 
Video in pwn.college


# 8.	Backgrounding Process
To run a program in the background

## My solve

**Flag:** ` pwn.college{wyLyoKelr6Ul_Pg7sotmYFdpkPU.QX3QDO0wSM1gjNzEzW}`
``` bash
hacker@processes~resuming-processes:~$
Connected!
hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         162 S+   bash /challenge/run
root         164 R+   ps -o user=UID,pid,stat,cmd

I don't see a second me!

To pass this level, you need to suspend me, resume the suspended process in the
background, and then launch a new version of me! You can background me with
Ctrl-Z (and resume me in the background with 'bg') or, if you're not ready to
do that for whatever reason, just hit Enter and I'll exit!
^Z
[1]+  Stopped                 /challenge/run
hacker@processes~backgrounding-processes:~$ bg
[1]+ /challenge/run &
hacker@processes~backgrounding-processes:~$


Yay, I'm now running the background! Because of that, this text will probably
overlap weirdly with the shell prompt. Don't panic; just hit Enter a few times
to scroll this text out.

hacker@processes~backgrounding-processes:~$ /challenge/run
I'll only give you the flag if there's already another copy of me running *and
not suspended* in this terminal... Let's check!

UID          PID STAT CMD
root         162 S    bash /challenge/run
root         172 S    sleep 6h
root         173 S+   bash /challenge/run
root         175 R+   ps -o user=UID,pid,stat,cmd

Yay, I found another version of me running in the background! Here is the flag:
pwn.college{wyLyoKelr6Ul_Pg7sotmYFdpkPU.QX3QDO0wSM1gjNzEzW}
```
Suspended the /challenge/run program , then ran bg command to run it background and then invoked /challenge/run again


## What I learned
bg command is used to run programs in background

## References 
Video in pwn.college

# 9.	Starting Backgrounding Processes
To start a process in background

## My solve

**Flag:** `pwn.college{ADC3tUCoKmnCWgjZWWaI7x764K7.QX5QDO0wSM1gjNzEzW}`
``` bash
hacker@processes~starting-backgrounded-processes:~$ /challenge/run &
[1] 161
hacker@processes~starting-backgrounded-processes:~$


Yay, you started me in the background! Because of that, this text will probably
overlap weirdly with the shell prompt, but you're used to that by now...

Anyways! Here is your flag!
pwn.college{ADC3tUCoKmnCWgjZWWaI7x764K7.QX5QDO0wSM1gjNzEzW}
```
Ran the /challenge/run with a & to run it in background


## What I learned
If I write ‘&’ in front of a command it starts running in background

## References 
Video in pwn.college
# 9.	Process Exit Codes
Processing exit codes of a command

## My solve

**Flag:** `pwn.college{ADC3tUCoKmnCWgjZWWaI7x764K7.QX5QDO0wSM1gjNzEzW}`
``` bash
Connected!
/challhacker@processes~process-exit-codes:~$ /challenge/get-code
Exiting with an error code!
hacker@processes~process-exit-codes:~$ echo $?
98
hacker@processes~process-exit-codes:~$ /challenge/submit-code 98
CORRECT! Here is your flag:
pwn.college{gdI2WcHHBvBQUjHsUJKBqePRagt.QX5YDO1wSM1gjNzEzW}
```
Ran the /challenge/get-code program which ended with error so got it exit code 98(which is a non-zero number), now provided this as an argument to /challenge/submit-code and got flag


## What I learned
If a command ran successfully, it returns 0, whereas if it did not, it will return a non-zero number 

## References 
Video in pwn.college



