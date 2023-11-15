# Git Plubming Practice 

**read all instructions first and make sure you choose where to work accordingly**

## Setup and install for future classes

1. If you use Windows, install [putty](https://www.putty.org/)
2. make sure you know where you can run python programs and bash commands in the same terminal, test with [courseutils](https://github.com/introcompsys/courseutils)

## Get ready for checkout 

Create a branch linked to this issue and on that branch create `lab6.md` use the template below:

```
# Lab 6 

## Time traveling commit

<!-- include how you completed this task (commands or English)-->

## Test repo status Map

<!-- diagram -->

## Reflection

<!-- describe anything you had trouble with, or learned. Did the past two days of working with plumbing commands change how you understand the porcelain commands?  -->
```

## Time traveling commit

You goal is to use plumbing commands to make a second commit on the main branch of your `test` repo from yesterday that assigns the "test content" blob to file called `revisionist.txt` with the commit message "changing history". 

Consider the following: 
- How does a blob relate to a tree?
- What are **all** of the steps to make a commit?
- How is creating a second commit different from the first?  What do other commits have that our first commit does not?
- [`git commit-tree` docs](https://git-scm.com/docs/git-commit-tree)


## Test repo map

Use `git cat-file` over the objects to draw a graph diagram of your current status in your test directory using [mermaid](https://github.blog/2022-02-14-include-diagrams-markdown-files-mermaid/) syntax to diagram it. Name each node in your graph with 5-7 characters of the hash and the type. eg `0c913 commit`. Include your diagram in your `lab6.md` file. 

**hint:** I used mermaid for the diagrams in class and you have access to the source for the diagrams in the notes. 



## Lab checkout


Create a pull request with the following and discuss with a TA or instructor
```
- [ ] if windows, putty is installed or other means of ssh (must be local)
- [ ] can run python code (eg courseutils), gh,  and bash in the same terminal (codespace is okay)
```

