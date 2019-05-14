# Slurs
This is where I keep my custom regexes that I wrote for automod on reddit. They detect possible variations of slurs such as nigger, faggot, kike, etc. 

For questions, suggestions, or bug reports, contact /u/Blank-Cheque on reddit. 

# Types

## Verbose

Allows for as many variations as possible, including nonlatin characters and amount of letters. E.g., nigger, niiiiggggeerr, and ṊṋṈṉN̈n̈ȈȉI̋i̋ȊȋỊịḬḭƗɨᶖᶃꬶＧｇěËëẼẽĖėrrrrr will all be captured. 

## Concise

Allows for variations in the form of nonlatin characters, but not amount of letters. E.g., nigger and ṋıꝙʠểr will be captured but niiiiggggeerr will not be. 

## Laconic

Does not allow for variations in the form of nonlatin characters or amount of letters. E.g., out of nigger, ṋıꝙʠểr, and niiiiggggeerr, only nigger will be captured. 
