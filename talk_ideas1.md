%title: OLUG.org August 2nd, 2022
%author: Aaron Grothe & Matt Payne
%date: 2022-08-02

-> CLI is Hard <-
=========

## In the terminal, the command line interface, things are hard.
1. Don't know your location (`pwd` == print working directory)
2. `cd new_location` == goes to new_location
   1. Absolute paths start with `/`
   1. Relative paths do not start with `/`
   1. `.` is the current directory and `..` is the parent directory
3. `cd -` == goes to the previous location

## Things are hard, until you are used to it.

-------------------------------------------------
-> CLI for Comfort <-
=========

I think there are a lot of great tricks that many folks don't know about

1. you can not use your mouse
1. arrows, CTRL-R, and history
1. Result code: `echo $?` (0 is good, not zero is bad)

-------------------------------------------------
-> CLI power tools <-
=========
1. redirection
2. pipes
3. find
4. grep, egrep, git grep
5. xargs
6. for loops
7. job controls
8. environment variables
   1. source script.sh  # notes about fork & exec
9. sed & awk


-------------------------------------------------
-> CLI power tools: Redirection <-
=========
redirection

-------------------------------------------------
-> CLI power tools: Pipes <-
=========
Pipes, 

-------------------------------------------------
-> CLI power tools: find <-
=========
find

-------------------------------------------------
-> CLI power tools: environment grep etc <-
=========
egrep, git grep

-------------------------------------------------
-> CLI power tools: xargs <-
=========
xargs - When you hit the limit of the # of command line parameters... 

-------------------------------------------------
-> CLI poser tools: for loop <-
=========
When you want to build up what you're doing
1. Confirm what you're getting
2. Then put the action into the loop

-> # The most BASH Matt ever writes <-

```
for f in `find . -type f | egrep -i 'something|otherthing'`
do 
   echo $f
   cp $f  ${HOME}/some/place/else
done
```

-------------------------------------------------
-> CLI power tools: job control <-
=========
job control do things in the background and then bring it into the foreground



-------------------------------------------------
-> CLI power tools: environment variables <-
=========
environment variables

-------------------------------------------------
-> CLI power tools: environment sed & awk <-
=========
awk, sed, 


-------------------------------------------------

-> Slide: References <-
=========
https://swcarpentry.github.io/shell-novice/

-------------------------------------------------
-> CLI power tools <-
=========

1. export A=`pwd`  # then use $A as part of a destination
2. mkdir -p some/big/deep/{part1,part2}/paths/you/want/to/make
3. cd -
4. the deal with source script vs. ./script
5. tricks with redirecting and pipes
6. environment variables -- what's to know other than PATH?
7. I don't know what else at the moment
8. setting up starship prompt -- will this work if you're just sshing or putting into a box?


-------------------------------------------------
-> ## Timing a bash function <-
=========

Time is little used function.

#!/bin/bash

time ( sleep 1; sleep 1; sleep 1 )

real    0m3.036s
user    0m0.006s
sys     0m0.000s

-------------------------------------------------
-> ## Use this not that <-
=========

1. tldr instead of man
1. ip instead of ifconfig

-------------------------------------------------

-> ## tldr instead of man <-
=========

tldr is the modern replacement for man

Each piece of documentation is pretty short

Make sure to do do "tldr -u" to download the latest version of the pages

E.g. tldr vim; tldr wget

-------------------------------------------------
-> ## Fun things <-
=========

1. https://cheat.sh/
1. bash insulter


-------------------------------------------------
-> ## Future things <-
=========

GNU Coreutils being rewritten in Rust

https://github.com/uutils/coreutils

Why is it the Future?

Moving away from classic languages like C. Interesting to see how long it will take to reach feature parity with the classic Coreutils.


-------------------------------------------------
-> ## Last words <-
=========

[GitHub Repo for this talk](https://github.com/adm2022/OLUG_August_2022).

