# Scripts and Server Practice


Today you will practice with what we learned this week either using a github action or the remote server. Then you will share your work with a partner. 

Plan ahead and do the opposite task of the person you would like to work with.  

If you **really** do not want to work with anyone, you can do both tasks. 

## Write a script

Choose one of the following things to practice 

### Make a github action 

add a github action to your KWL repo (work directly on main to be able to test it) that posts a progress report issue using `courseutils` once a week on Fridays. 

tip: make it run on workflow dispatch to test and then swap the trigger. 

resources: 
- [schedule trigger](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule)
- [courseutils](https://github.com/introcompsys/courseutils)
- the actions in your KWL repo

### write a small script and submit it as a batch job

write a small script that calculates how many times `Act5C` occurs in the file `dmel-all-r6.19.gtf` on seawulf and submit it for scheduling using [sbatch](https://web.uri.edu/hpc-research-computing/using-seawulf/#sbatch)



## Explain your script

Explain how your script works and what you learned working on it to a classmate who did the other task. 

https://carpentries-incubator.github.io/hpc-intro/13-scheduler/index.html

Help your partner get your script running on their own. use a [github gist](https://docs.github.com/en/get-started/writing-on-github/editing-and-sharing-content-with-gists/creating-gists) to share your code. 

## Lab checkout 

To checkout, make `lab8.md` on a branch linked to this that includes your gist and your partner's gist and check out with a TA. 
