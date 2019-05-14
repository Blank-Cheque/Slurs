# Slurs
This is where I keep my custom regexes that I wrote for automod on reddit. They detect possible variations of slurs such as nigger, faggot, kike, etc. 

For questions, suggestions, or bug reports, contact /u/Blank-Cheque on reddit. 

# Types

## Verbose

Allows for as many variations as possible, including nonlatin characters and amount of letters. E.g., nigger, niiiiggggeerr, and ṊṋṈṉN̈n̈ȈȉI̋i̋ȊȋỊịḬḭƗɨᶖᶃꬶＧｇěËëẼẽĖėrrrrr will all be captured. 

## Concise

Allows for variations in the form of nonlatin characters, but not amount of letters. E.g., nigger and ṋıꝙʠểr will be captured but niiiiggggeerr will not be. 

## Laconic

Allows for neither variations in the form of nonlatin characters nor amount of letters. E.g., out of nigger, ṋıꝙʠểr, and niiiiggggeerr, only nigger will be captured. 

# Usage

In each folder, the file \_quick-add contains a premade automod rule which can be immediately added to your subreddit. To add it, go to https://www.reddit.com/r/[subreddit]/wiki/config/automoderator and add the entirety of \_quick-add. 

Please note that each \_quick-add uses the version of nigger detection which also detects nigga. To not detect nigga, go to the file for nigger in that folder, copy the filter which does not detect nigga, and replace the first filter in \_quick-add with it. 

To add a specific filter or filters, go to https://www.reddit.com/r/[subreddit]/wiki/config/automoderator and add the following:

```
###Slur detector by Blank-Cheque github.com/Blank-Cheque/Slurs###
title+body (regex): 
  - '[filter 1]'
  - '[filter 2]'
  - '[etc]'
action: filter
action_reason: 'Contains disallowed word "{{match}}"'
```

I'm no lawyer, but I'd kindly ask that you leave the comment included for credit. 
