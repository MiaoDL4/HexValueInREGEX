# Hex value Regex explained

A Regular Expression, normally shortened to Regex, is a string of characters that define a search. You can think if it as the find fuction on a web browser or word document but with extra filters.

## Summary

this is going to be a break down of what makes a Regex we are going to use the following example: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ this looks for hex values , and what below will explain how.

## Table of Contents

- [Anchors](#anchors)
- [Bracket Expressions](#bracket-expressions)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping Constructs](#grouping-constructs)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Regex for Hex value](#Regex-for-Hex-value)


## Regex Components

### Anchors
Anchors are what is used to mark the start and end of the string.

They are represented as "^" and "$" for the start and end, respectively.

A basic example: /^Hello$/ this will find any string that strictly matches "Hello", so the it will not find "hello" regex is case sensitive.

Looking back at at out original regex /^#?([a-f0-9]{6}|[a-f0-9]{3})$/ notice it has a start and end.

### Bracket Expressions
specifically the square brackets [], the define a range of characters that you would like to search.

A basic example woule be /^[a]$/, this will find every string with the letter a regardless length.

useful Bracket Expressions are [a-z] and [0-9], addtionally you can combine expression therefore [a-gn-o0-4] is vaild.

further explaining the hex value regex it contains [a-f0-9] which looks for letter a-f and numbers between 0-9.

### Quantifiers
there are 6 quanitifers

1 - "*" - Matches zero or more times
2 - "+" - Matches one or more times
3 - "?" - Matches zero or one time
4 - "{ n }" - Matches n number of times
5 - "{ n , }" - Matches at least n times
6 - "{ n , x }" - Matches from n to x times

bring it back to /^#?([a-f0-9]{6}|[a-f0-9]{3})$/, and pull a small section [a-f0-9]{6}, it has { n } quanifier so this will look for [a-f0-9] with a length of 6. 

### Character Classes
simalar to Bracket Expressions, character classes definee a set of characters

some common charater classes include:
"\d" for digits
"\s" for space symbols, tabs, newlines
"\w" for alphanumberic characters

additional caplizing the letter in the charater will create the inverse effect

### Grouping Constructs
these allow the creation expression that have multiply sections, these sections are commonly refered to as sub-expressions.

they are done with the uses of regular brackets ().

A basic example is /^(.+)@(.+)$/ this is a simple email check that looks for any character before and after the @.

### The OR Operator
this operator is defined by "|" the vertical bar symbol, and will find all results that meet the search conditions,

A basic example /^i like dogs|cats$/, this will find "i like dogs" and "i like cats"

### Flags
flag are special indicaters placed at the end of a regex.
common flags are 
g - for global search and i - for case insensitive search

an example of use /^Hello$/g

### Character Escapes
these are used when searching for character that are used by regex. think if you wanted to search for the Anchor characters, ^ or $, it would be seen as still being an anchor
using "(\)" will strip any special character of its use within the character escape. 

### Regex for Hex value
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

/ at the start and end is the warper
^ and & are the anchors define the start and end
"#" nothing speical just find thet # symbol
() Grouping Constructs is use to make the # start for whats inside
[a-f0-9] a Bracket Expressions that find anything from a to f and 0-9
{6} and {3} Quantifiers looks to match the condition above 6 or 3 times,
| an OR Operator 

## Author
My name is Don and I am currently studying coding Bootcamp. if you like to look at things ive done so far there is a github [https://github.com/MiaoDL4]( https://https://github.com/MiaoDL4)
