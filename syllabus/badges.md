---
jupytext:
  text_representation:
    extension: .md
    format_name: myst
    format_version: 0.13
    jupytext_version: 1.10.3
kernelspec:
  display_name: Python 3
  language: python
  name: python3
---

# Badge Visualizations 

This page includes more visual versions of the information on the badge page.  You should read both, but this one is often more helpful, because some of the processes take a lot of words to explain and make more sense with a diagram for a lot of people. 

## Prepare work and Experience Badges Process

This is for a single example with specific dates, but it is similar for all future dates

The columns (and purple boxes) correspond to branches in your KWL repo and the yellow boxes are the things that you have to do. The "critical" box is what you have to wait for us on. The arrows represent PRs (or a local merge for the first one)


```{mermaid}
sequenceDiagram
    participant P as prepare Feb 21
    participant E as experience Feb 23
    participant M as main 
    note over P: complete prepare work<br/> between feb 21 and 23
    note over E: run experience badge workflow <br/> at the end of class feb 23
    P ->> E: local merge or PR you that <br/> does not need approval
    note over E: fill in experience reflection 
    critical Badge review by instructor or TA
        E ->> M: Experience badge PR
    option if edits requested
        note over E: make requested edits
    option when approved 
        note over M: merge badge PR
    end
```

In the end the commit sequence for this will look like the following:

```{mermaid}
gitGraph
   commit
   commit
   checkout main
   branch prepare-2023-02-21
   checkout prepare-2023-02-21
   commit id: "gitunderstanding.md"
   branch experience-2023-02-23
   checkout experience-2023-02-23
   commit id: "initexp"
   merge prepare-2023-02-21
   commit id: "fillinexp"
   commit id: "revisions" tag:"approved"
   checkout main
   merge experience-2023-02-23
```

Where the "approved" tag represents and approving reivew on the PR. 


## Review and Practice Badge 


Legend:
```{mermaid}
flowchart TD
    badgestatus[[Badge Status]]
    passive[/ something that has to occur<br/> not done by student /]      
    student[Something for you to do]

    style badgestatus fill:#2cf

    decisionnode{Decision/if}
      sta[action a]
      stb[action b]
      decisionnode --> |condition a|sta
      decisionnode --> |condition b|stb
    subgraph phase[Phase]
      st[step in phase]
    end
```

This is the general process for review and practice badges 

```{mermaid}
flowchart TD
%%    subgraph work[Steps to complete]
    subgraph posting[Dr Brown will post the Badge]
      direction TB
      write[/Dr Brown finalizes tasks after class/]
      post[/Dr. Brown pushes to github/]
      link[/notes are posted  with badge steps/]
      posted[[Posted: on badge date]]
      write -->post
      post -->link
      post --o posted
    end
    subgraph planning[Plan the badge]
      direction TB
      create[/Dr Brown runs your workflow/]
      decide{Do you need this badge?}
      close[close the issue]
      branch[create branch]
      planned[[Planned: on badge date]]
      create -->decide
      decide -->|no| close
      decide -->|yes| branch
    create --o planned
    end
    subgraph work[Work on the badge]
      direction TB
      start[do one task]
      commit[commit work to the branch]
      moretasks[complete the other tasks]
      ccommit[commit them to the branch]
      reqreview[request a review]
      started[[Started <br/> due within one week <br/> of posted date]]
      completed[[Completed <br/>due  within two weeks <br/> of posted date]]
      wait[/wait for feedback/]
      start --> commit
      commit -->moretasks
      commit --o started
      moretasks -->ccommit
      ccommit -->reqreview
      reqreview --> wait
      reqreview --o completed
    end
    subgraph review[Revise your completed badges]
      direction TB
      prreview[Read review feedback]
      approvedq{what type of review}
      merge[Merge the PR]
      edit[complete requested edits]
      earned[[Earned <br/> due by final grading]]
      discuss[reply to comments]
      prreview -->approvedq
      approvedq -->|changes requested|edit
      edit -->|last date to edit: May 1| prreview
      approvedq -->|comment|discuss
      discuss -->prreview
      approvedq -->|approved|merge
      merge --o earned
    end

    posting ==> planning
    planning ==> work
    work ==> review

%% styling 
style earned fill:#2cf
style completed fill:#2cf
style started fill:#2cf
style posted fill:#2cf
style planned fill:#2cf
```


## Explore Badges


```{mermaid}
flowchart TD
    subgraph proposal[Propose the Topic and Product]
      issue[create an issue]
      proposed[[Proposed]]
      reqproposalreview[Assign it to Dr. Brown]
      waitp[/wait for feedback/]
      proceedcheck{Did Dr. Brown apply a proceed label?}
      branch[start a branch]
      progress[[In Progress ]]
      iterate[reply to comments and revise]
      issue --> reqproposalreview
      reqproposalreview --> waitp
      reqproposalreview --> proposed
      waitp --> proceedcheck
      proceedcheck -->|no| iterate
      proceedcheck -->|yes| branch
      branch --> progress
      iterate -->waitp
    end
    subgraph work[Work on the badge]
      direction TB
      moretasks[complete the work]
      ccommit[commit work to the branch]
      reqreview[request a review]
      wait[/wait for feedback/]
      complete[[Complete]]
      moretasks -->ccommit
      ccommit -->reqreview
      reqreview --o complete
      reqreview --> wait
    end
    subgraph review[Revise your work]
      direction TB
      prreview[Read review feedback]
      approvedq{what type of review}
      revision[[In revision]]
      merge[Merge the PR]
      edit[complete requested edits]
      earned[[Earned <br/> due by final grading]]
      prreview -->approvedq
      approvedq -->|changes requested|edit
      edit --> prreview
      edit --o revision
      approvedq -->|approved| merge
      merge --o earned
    end

    proposal ==> work
    work ==> review

%% styling 
style proposed fill:#2cf
style progress fill:#2cf
style complete fill:#2cf
style revision fill:#2cf
style earned fill:#2cf

```



## Build Badges 


```{mermaid}
flowchart TD
    subgraph proposal[Propose the Topic and Product]
      issue[create an issue]
      proposed[[Proposed]]
      reqproposalreview[Assign it ]
      waitp[/wait for feedback/]
      proceedcheck{Did Dr. Brown apply a proceed label?}
      branch[start a branch]
      progress[[In Progress ]]
      iterate[reply to comments and revise]
      issue --> reqproposalreview
      reqproposalreview --> waitp
      reqproposalreview --> proposed
      waitp --> proceedcheck
      proceedcheck -->|no| iterate
      proceedcheck -->|yes| branch
      branch --> progress
      iterate -->waitp
    end
    subgraph work[Work on the badge]
      direction TB
      commit[commit work to the branch]
      moretasks[complete the work]
      draftpr[Open a draft PR and <br/> request a review]
      ccommit[incorporate feedback]
      reqreview[request a review]
      wait[/wait for feedback/]
      complete[[Complete]]
      commit -->moretasks
      commit -->draftpr
      draftpr -->ccommit
      moretasks -->reqreview
      ccommit -->reqreview
      reqreview --> complete
      reqreview --> wait
    end
    subgraph review[Revise your work]
      direction TB
      prreview[Read review feedback]
      approvedq{what type of review}
      revision[[In revision]]
      merge[Merge the PR]
      edit[complete requested edits]
      earned[[Earned <br/> due by final grading]]
      prreview -->approvedq
      approvedq -->|changes requested|edit
      edit --> prreview
      edit -->revision
      approvedq -->|approved| merge
      merge --o earned
    end

    proposal ==> work
    work ==> review

%% styling 
style proposed fill:#2cf
style progress fill:#2cf
style complete fill:#2cf
style revision fill:#2cf
style earned fill:#2cf

```
