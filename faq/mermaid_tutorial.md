# Mermaid Overview

## What is Mermaid?

[Mermaid](https://mermaid.js.org/intro/) is a flowchart and diagram visualization tool based on JavaScript and uses Markdown syntax to create flowcharts that are extremely dynamic and high quality. [Mermaid](https://mermaid.js.org/intro/) is especially useful because you are able to display your beautiful flowcharts using backticks to create a code block. 

## Tutorial for Using Mermaid

Either on the [Mermaid](https://mermaid.live/) website or within the **GitHub** markdown file that you're making edits to you can make complex flowcharts seamlessly. 

### Using Code Blocks

A code block should look like the following:
````
```{mermaid}
blah blah blah
```
````

#### Example Mermaid Code Block

```{mermaid}
flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
```

In Mermaid there are different styles for boxes with either square or round edges and the option to give a description of each item in its pipe.

So the code above actually looks like this in it's code block:

````
```{mermaid}
flowchart TD
    A[Christmas] -->|Get money| B(Go shopping)
    B --> C{Let me think}
    C -->|One| D[Laptop]
    C -->|Two| E[iPhone]
    C -->|Three| F[fa:fa-car Car]
```
````

There's lots of cool and unique things that can be created using Mermaid and the best way to understand it better is to continue to practice. 
