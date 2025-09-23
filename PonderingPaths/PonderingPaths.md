# 1.	The Root
The challenge asks to move from root directory.

## My solve

**Flag:** `pwn.college{00XuXsN2-9w3rOz18pDFQIO19R8.QX4cTO0wSM1gjNzEzW}`


From root directory, I came to pwn directory to get the flag.


## What I learned
I learned about absolute path.

## References 
Video in pwn.college

# 2.	Program and Absolute Paths
I went from root to another directory to run program.

## My solve
**Flag:** `pwn.college{AExW8e_pp9yPGOKpV5_YFATl8Ae.QX1QTN0wSM1gjNzEzW}`

Explored another layer, went from root(/) to challenge directory to run 


## What I learned
I learned to go across files using absolute path.

## References 
Video in pwn.college

# 3.	Position thy Self
Change my position in directory

## My solve

**Flag:** `pwn.college{4aR7_Npo0Iyaj3xfT5TM13W3bJz.QX2QTN0wSM1gjNzEzW}`

I ran /challenge/run but I was not in the correct directory. As the prompt instructed, I went in to the right directory and ran the program

## What I learned
I learned to handle cd

## References 
Video in pwn.college

# 4.	Position Elsewhere
Changing positions

## My solve

**Flag:** `pwn.college{4lDjVZCmdomp0PNp1BC4DHHMlFL.QX3QTN0wSM1gjNzEzW}`

Repeated the process, and came to another directory to run the same command.

## What I learned
Used cd in different context.

## References 
Video in pwn.college

# 5.	Position yet Elsewhere
Change my position in directory

## My solve

**Flag:** `pwn.college{Utt9aC7B6nDtW4GKizfFSls3u1l.QX4QTN0wSM1gjNzEzW}`

Repeated the process, invoked program in right directory.

## What I learned
Travelled across directories.

## References 
Video in pwn.college

# 6.	Implicit Relative Path, from /
Use relative path to invoke program

## My solve

**Flag:** `pwn.college{cnTa7MmovptDT_jgu2CltobZR8T.QX5QTN0wSM1gjNzEzW}`

Invoked program through relative path. I was in / and ran challenge.run from there

## What I learned
Learned about relative path

## References 
Video in pwn.college

# 7.	Explicit Relative Path, from /
Exploring . (which mean the same directory)

## My solve

**Flag:** `pwn.college{ohqpzSdgcsgAxTPNC4HrixRIhZA.QXwUTN0wSM1gjNzEzW}`

Used . to get path


## What I learned
Learned about relative explicit path

## References 
Video in pwn.college

# 8.	Implicit relative path
Using . to invoke program

## My solve

**Flag:** `pwn.college{coj122Gd_A7-eBK9gOPRpOsu0mw.QXxUTN0wSM1gjNzEzW}`

Invoked run program from ./run as /run did not work 

## What I learned
Learned that some programs cannot be explicitly executed as they can refer to utility files which can accidentally run to same name

## References 
Video in pwn.college

# 9.	Home Sweet Home
Exploring home directory

## My solve

**Flag:** `pwn.college{8KrmD_3NP_cX34o16rLcA6Ef4Xm.QXzMDO0wSM1gjNzEzW}`

Entered a path ~/p which starts with ~ (our home directory), command line wrote the file to p and read back it to me as flag

## What I learned
Learned to navigate to home directory and come to a file from there

## References 
Video in pwn.college

