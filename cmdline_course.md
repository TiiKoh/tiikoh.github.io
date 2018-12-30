---
layout: default
---

The course was mainly intended as a gentle introduction to command-line tools for linguists.
It was organised as an online course, with weekly assignments and a bigger final project.
The aim of the course was to cover the fundamentals of Unix-like command-line environments,
and especially those that are relevant to linguists.

According to the [course page](https://courses.helsinki.fi/en/kik-lg218/126710126),
after completing the course, students should be able to:

- operate in a Unix-like environment.
- use Unix command-line on a Windows or Mac OSX computer.
- use the Unix command-line.
- use regular expressions.
- processing corpora at a basic level.
- run programs from the command-line.
- install programs.
- write basic scripts.
- use version control tools.
- work on a remote server.
- create and host a webpage on GitHub Pages.
- stay calm and google when things go wrong.

I feel like the last point is especially important. As this was an online course,
the discussion forum on Moodle was an important part of the learning process.
Students had different operating systems and faced different problems,
so it was good to have a forum on which questions could be asked.
Not only teachers offered their assistance, but also other students.


## Week 1

The first week was basically an introduction. We started from the very beginning:
launching the terminal, getting familiar with some basic commands, and using text
editors to view and modify files. Commands used during the first week included
`mkdir`, `cp` and `mv`. For example, the command

```
$ mv myfile.txt myfiles
```

moves the file **myfile.txt** into the directory **myfiles**.

The first week was not too challenging, which was nice of course. My knowledge of
command-line environments at the start of the course was virtually non-existent,
having mostly only used Windows my whole life. However, most basic commands were
rather straightforward, and the whole environment feels pretty intuitive. However,
some simple commands were a bit difficult for me—for some reason, I never seemed
to remember which way around the source and target should go. If I type
`mv file1 file2`, which is the source and which is the target? I am slowly
starting to remember now.


## Week 2

During the second week of the course we learned about navigating the Unix file system.
We learned about users and permissions, processes, and working with a remote server.
This was a very interesting week in the sense that I felt like the topic should be very
familiar to me but I still somewhat struggled with it. Perhaps it is the terminology that
is confusing and unfamiliar: "administrator" is something that I recognise, but "superuser",
and "root user"? Similarly, I have an CSC account, and I have worked on the Taito-shell
environment—however, as it turns out, I do not understand much about remote servers.
So this was a very useful week for me, and I think I learned a lot.

We learned a very useful command, `chmod`, which is used to change access permissions.
For example, the command

```
$ chmod a+r file.txt
```

allows *read* permission to everyone, and

```
$ chmod a-x file.txt
```

denies *execute* permission to everyone.


## Week 3

The third week was about corpus processing. We learned about regular expressions and
text processing commands. In our assignments, we worked with texts from [Project Gutenberg](http://www.gutenberg.org/).
We mainly examined frequencies: for example, how many times a certain word form occurs in a given text. The difference between *word*, *word-form* and
*token* was important to remember. The `grep` and `egrep` commands were very useful here.
For example, the command

```
$ grep '[A-C]' file.txt
```

reads **file.txt** and prints out lines which contain capital letters from A to C.

Another useful command was ``tr``. For example, the command

```
$ cat file.txt | tr -cd '[:alnum:]'
```

removes all non-alphanumeric characters from **file.txt**.

This week was already a bit more challenging for me. I have seen and used regular
expressions a couple of times before, but they have always remained a bit of a mystery
to me. I still need a lot of practice.


## Week 4

The fourth week's topic was scripting and Unix configuration files. Being a Windows user,
I was not familiar with bash scripts and configuration files at all beforehand, so this
was quite a challenging week for me. However, it was also very interesting, and customising
my own bash prompt was something that I found genuinely enjoyable and fun. As I work on a
Windows system, I recall having some troubles with file permissions during this week, but
I think I managed to fix or bypass these problems somehow.

An example of a `for` loop in a bash script **loop.sh**:

```
/#!/bin/sh
for i in 1 2 3 4 5
do
  echo "Looping ... number $i"
done
```

## Week 5

This week was about installing and running programs. I have used **pip** before, but
everything else—like **apt** and **brew**—was new to me.


## Week 6

During the sixth week we learned about GitHub: how to set up a Git Repository, how the
branches work, what is version control, and so on. Unfortunately, I was very busy this
week and was not able to work on the assignments. However, I already had a GitHub account
set up because of an earlier course at the university, so luckily I had some experience
of Git.

https://xkcd.com/1597/
<img src="assets/images/git.png" alt="Image" hspace="20" width="30%" align="right"/>

## Week 7

The remainder of the course was dedicated to the final project, which is this webpage.
For this, we used a *static site generator* called Jekyll. As GitHub typically takes
a while to process the changes we have made, depending on the site traffic, we can use
Jekyll to quickly see how everything looks like while we are working. This way we do not
need to wait for the changes to appear on our actual GitHub page every time we wish to
see what the final result looks like. The command

```
$ bundle exec jekyll serve
```

is used to run Jekyll, which then builds a local site.

I have used Git before, but not on bash. Jekyll and the Ruby installation environment
were also completely unfamiliar to me. I had some trouble getting everything up and
running, but after some heavy googling ( :) ) I overcame my obstacles, and the rest
of the work went smoothly.
