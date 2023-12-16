# Offline Badge Script Tutorial

If you'd like to start doing your work offline in your local kwl clone but don't have the body of the most recent issue you can follow the following steps to write your own script to get the badge instructions.

## Getting Started

For later in the script you will need .jq to run the script correctly. The download can be found [here.](https://cameronnokes.com/blog/working-with-json-in-bash-using-jq/).

To get started with creating a script that gets offline badge instructions you need to create a file for the script to run:
```{toggle}
touch badgeinstructions.sh
```

Now you will need to open that file, and type the following on the first line:
```{toggle}
#!/bin/bash
```

Then on the 2nd line you will need to enter:
```{toggle}
outputfile="offline_badge_instructions-$(date "+%Y-%m-%d").md"
```

Then, you will need to write this on the next line:
```{toggle}
badgeissue=$(gh issue list --label review -L 1 --json number | jq -r '.[0].number')
```
Here we are getting the issue list, sorting by review, getting the most recent review issue, and getting the issue number with json.
Then we're going to pipe a jq -r '.[0].number' command to get the raw output of the gh command and we get the number of the issue for our variable.

*Note*: If you want to change the badge type you need to replace review with practice in the label part of the badgeissue command.


Next we're going to make a variable called badgeinstructions and assign the gh issue view command to it:
```{toggle}
badgeinstructions=$(gh issue view $badgeissue)
```

Next we're gonna echo a title for the top of the output file:
```{toggle}
echo "Most Recent Badge Instructions" >> $outputfile
```

Now we're gonna echo the badgeinstructions into the output file as well:
```{toggle}
echo "$badgeinstructions" >> $outputfile
```

Once we do this we should be all set to run the script:

```{toggle}
bash badgeinstructions.sh
```

Now we are all set!