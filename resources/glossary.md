# Glossary

```{tip}
We will build a glossary as the semester goes on. When you encounter a term you do not
know, create an issue to ask for help, or contribute a PR after you find the
answer.
```

```{glossary}


add (new files in a repository)
  the step that stages/prepares files to be committed to a repository from a local branch


bitwise operator
  an operation that happens on a bit string (sequence of 1s and 0s). They are typically faster than operations on whole integers. 


bitwise operator
  an operation that happens on a bit string (sequence of 1s and 0s). They are typically faster than operations on whole integers. 



Compiled Code
  code that is put through a compiler to turn it into lower level assemlby language before it is executed. must be compiled and re-executed everytime you make a change.


directory
  a collection of files typically created for organizational purposes



floating point number
  the concept that the decimal can move within the number (ex. scientific notation; you move the decimal based on the exponent on the 10). can represent more numbers than a fixed point number.
  
fixed point number
  the concept that the decimal point does not move in the number (the example in the notes where if we split up a bit in the middle and one half was for the decimal and the other half was for the whole number. Cannot represent as many numbers as a floating point number.

.gitignore
  a file in a git repo that will not add the files that are included in this .gitignore file. Used to prevent files from being unnecessarily committed.

git
  a version control tool; it's a fully open source and always free tool, that can be hosted by anyone or used without a host, locally only.


git objects
  something (a file, directory) that is used in git; has a hash associated with it


GitHub
  a hosting service for git repositories


Git Plumbing commands
  low level git commands that allow the user to access the inner workings of git.


Git Workflow
  a recipe or recommendation for how to use Git to accomplish work in a consistent and productive manner


HEAD
  the branch that is currently being checked out (think of the current branch)


merge
  putting two branches together so that you can access files in another branch that are not available in yours



hash function
  the actual function that does the hashing of the input (a key, an object, etc.)


hashing
  putting an input through a function and getting a different output for every input (the output is called a hash; used in hash tables and when git hashes commits).


interpreted code
  code that is directly executed from a high level language. more expensive computationally because it cannot be optimized and therefore can be slower.
  

  
integreated development environment
  also known as an IDE, puts together all of the tools a developer would need to produce code (source code editor, debugger, ability to run code) into one application so that everything can be done in one place. can also have extra features such as showing your file tree and connecting to git and/or github.


Linker
  a program that links together the object files and libraries to output an executable file.
  

pull (changes from a repository)
  download changes from a remote repository and update the local repository with these changes.

push (changes to a repository)
  to put whatever you were working on from your local machine onto a remote copy of the repository in a version control system.


repository
  a project folder with tracking information in it in the form of a .git file


ROM (Read-Only Memory)
  Memory that only gets read by the CPU and is used for instructions


SHA 1
  the hashing function that git uses to hash its functions (found to have very serious collisions (two different inputs have same hashes), so a lot of software is switching to SHA 256)


shell
  a command line interface; allows for access to an operating system


ssh 
  allows computers to safely connect to networks (such as when we used an ssh key to clone our github repos)


templating
  templating is the idea of changing the input or output of a system. For instance, the Jupyter book, instead of outputting the markdown files as markdown files, displays them as HTML pages (with the contents of the markdown file).


terminal
  a program that makes shell visible for us and allows for interactions with it


tree objects
  type of git object in git that helps store multiple files with their hashes (similar to directories in a file system)

yml
    see YAML

[YAML](https://yaml.org/)  
    a file specification that stores key-value pairs. It is commonly used for configurations and settings. 

```
