# 1.	Translating Characters
To translate characters

## My solve

**Flag:** ` pwn.college{QM8ps57XIsj7sg4KcPVG1QfIfkS.01MxEzNxwSM1gjNzEzW}`
``` bash 
Connected!
hacker@data~translating-characters:~$ /challenge/run | tr a-zA-Z A-Za-z
yOUR CASE-SWAPPED FLAG:
pwn.college{QM8ps57XIsj7sg4KcPVG1QfIfkS.01MxEzNxwSM1gjNzEzW}
```

Used tr to write A-Za-z to a-zA-Z which changed upper to lowercase and vice-versa


## What I learned
tr command is used to translate characters, first argument- character to be replaced, second argument – character to be replaced with
Use a-z to refer to all lower case characters, similar for upper case characters

## References 
Video in pwn.college

# 2.	Deleting Characters
To delete characters

## My solve
**Flag:** ` pwn.college{0lODwrh89eQOG_iQiQVS6xdSEfH.0FNxEzNxwSM1gjNzEzW}`
``` bash 
hacker@data~deleting-characters:~$ /challenge/run | tr -d %^
Your character-stuffed flag:
pwn.college{0lODwrh89eQOG_iQiQVS6xdSEfH.0FNxEzNxwSM1gjNzEzW}
```

Removed % and ^ from result

## What I learned
tr -d is used to delete characters
don’t use space between characters which you want to delete while passing them to tr

## References 
Video in pwn.college

# 3.	Deleting Newlines
To delete newlines from the program

## My solve

**Flag:** ` pwn.college{M05gLunCIFL9v2SCMKPYneLvWlE.0VNxEzNxwSM1gjNzEzW}`
``` bash 
Connected!
hacker@data~deleting-newlines:~$ /challenge/run | tr -d "\n"
Your line-split flag: pwn.college{M05gLunCIFL9v2SCMKPYneLvWlE.0VNxEzNxwSM1gjNzEzW}hacker@data~deleting-newlines:~$
```
Deleted \n occurrences from the flag

## What I learned
To delete \n occurrences put them in double quotes

## References 
Video in pwn.college

# 4.	Extracting the first lines with head
to extract specific number of lines with the head command

## My solve
**Flag:** ` pwn.college{MNEt7lTGBfGZdkA_rAIvjr1Zy7q.0lNxEzNxwSM1gjNzEzW}`
``` bash 
Connected!
hacker@data~extracting-the-first-lines-with-head:~$ /challenge/pwn | head -n 7 | /challenge/college
Congratulations, you piped the right codes!
pwn.college{MNEt7lTGBfGZdkA_rAIvjr1Zy7q.0lNxEzNxwSM1gjNzEzW}
```
Redirected the output of /challenge/pwn to head via pipe, then redirected the first 7 lines to /challenge/college

## What I learned
To use head (for first 10 lines) and head -n … for specific number of lines

## References 
Video in pwn.college

# 5.	Extracting Specific Sections of Text
To extract specific columns from the text
## My solve

**Flag:** ` pwn.college{sZ_bjSGYbzDqifr4DGQFkRmpu1O.01NxEzNxwSM1gjNzEzW} `

``` bash 
hacker@data~extracting-specific-sections-of-text:~$ /challenge/run | cut -d " " -f 2 | tr -d "\n"
pwn.college{sZ_bjSGYbzDqifr4DGQFkRmpu1O.01NxEzNxwSM1gjNzEzW}hacker@data~extracting-specific-sections-of-text:~$
```
Firstly extracted 2nd column of /challenge/run then dleted new lines to join characters
## What I learned
cut is the command to extract columns, -d is the coloumn delimiter (how columns are separated), -f tells me field number followed by me entering field number then the file


## References 
Video in pwn.college

# 6.	Sorting Data
To organize data

## My solve

**Flag:** ` pwn.college{s3Kkef4KN4qEjTs6ALfwSWYX04u.0FM0MDOxwSM1gjNzEzW}`
``` bash
Connected!
hacker@data~sorting-data:~$ sort /challenge/flags.txt
pvn.colkdgd{r2Kkdf3KN4pEjTs6ALfwSWYX03u.0EM0LDOxwSL0gjMzEzV}
pwn.colkege{s3Kkef4KN4pEjTs6ALfwSWYX04u.0FM0MDOxwSM1gjNzEzW}
pwn.college{s3Kkef4KN4qEjTs6ALfwSWYX04u.0FM0MDOxwSM1gjNzEzW}
pwn.college{s3Kkef4KN4qEjTs6ALfwSWYX04u.0FM0MDOxwSM1gjNzEzW}
hacker@data~sorting-data:~$
```
Sorted the output and last one is flag

## What I learned
Automatically sort command organizes data in ascending order alphabetically, this can be changes using 
-r: reverse order (Z to A)
-n: numeric sort (for numbers)
-u: unique lines only (remove duplicates)
-R: random order!

## References 
Video in pwn.college
