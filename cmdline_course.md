---
layout: default
---

The course was mainly intended as a gentle introduction to command-line tools for linguists.
It was organised as an online course, with weekly assignments and a final project.
The course aimed to cover the fundamentals of Unix-like command-line environments, and
especially those that are relevant to linguists.

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
editors to view and modify files. Commands used during the first week include
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


## Week 3

The third week was about corpus processing. We learned about regular expressions and
text processing commands. In our assignments, we worked with texts from [Project Gutenberg]
(http://www.gutenberg.org/). We mainly examined frequencies: for example, how many times a
certain word form occurs in a given text. The difference between *word*, *word-form* and
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

Text here.

## Week 5

Text here.

## Week 6

Text here.
