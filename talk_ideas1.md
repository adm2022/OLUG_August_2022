%title: OLUG.org August 2nd, 2022
%author: Aaron Grothe & Matt Payne
%date: 2022-08-02

-> CLI for Comfort <-
=========
Slide 1

In the terminal, the command line interface, things are hard.
Until you are used to it.

-------------------------------------------------
Slide 2

I think there are a lot of great tricks that many 
folks don't know about (numbered but not really ordered):

1. arrows, CTRL-R, and history

-------------------------------------------------
Slide 3

IDEA DUMP: Pipes, redirection, xargs, job control, find, environment variables

awk, sed, history, egrep, git grep

https://swcarpentry.github.io/shell-novice/

-------------------------------------------------
Slide 4

1. export A=`pwd`  # then use $A as part of a destination
2. mkdir -p some/big/deep/{part1,part2}/paths/you/want/to/make
3. cd -
4. the deal with source script vs. ./script
5. tricks with redirecting and pipes
6. environment variables -- what's to know other than PATH?
7. I don't know what else at the moment
8. setting up starship prompt -- will this work if you're just sshing or putting into a box?

-------------------------------------------------
Slide 5

-> # The most BASH Matt ever writes <-

```
for f in `find . -type f | egrep -i 'something|otherthing'`
do 
   echo $f
   cp $f  ${HOME}/some/place/else
done
```


-------------------------------------------------
Slide 6

-> ## Use this not that <-

1. ss instead of ifconfig
1. ip instead of ifconfig

-------------------------------------------------
-> ## Fun things <-
Slide 7

1. https://cheat.sh/


-------------------------------------------------
-> ## Last words <-
Slide 8

[GitHub Repo for this talk](https://github.com/adm2022/OLUG_August_2022).

