# Regex Tutorial

As a web development student, I wanted to create a tutroial that would explain a particular regex by breaking down its components and exploring the search patterns involved.

## Summary

A regular expression, or regex for short, is a sequence of characters specifies search pattern in text. They consist of many components, many of which I break down below. The regex I chose to focus on is an email address template, which included anchors, quantifiers, character classes, grouping, and bracket expressions. The email address consists of three main sections broken up by an @ symbol and a period. Further explanation of the regex can be found by scrolling down or clicking the below links.

Matching an email
```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Anchors
```/^```([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})```$/```

The highlighted portion of the above Regex expression contain "anchors." These components signify the beginning (^) and the end ($) of a regular expression. 

Please note: The entire expression is wrapped in slashes (/) so that the regular expression is NOT read literally.


### Quantifiers
/^([a-z0-9_\.-]```+```)@([\da-z\.-]```+```)\.([a-z\.]```{2,6}```)$/

Quantifiers set the limits of the string that a regular expression matches. Quantifier characters include : ```+ ? {}```.
In the email example, ```{2,6}``` is the portion that counts as a qualifier. The match is hoping for a minimum of 2 characters and a maximum of 6 characters to end the email address. In other words, they look for the minimum and maximum character length within a string.
E.g. .com, .edu, .eu

The example email regex also includes ```+```. The plus sign quanitifier in a regular expression indicates that the preceding item(s) can repeat multiple times.


### Character Classes
/^([```a-z0-9_\.-```]+)@([```\da-z\.-```]+)\.([```a-z\.```]{2,6})$/

Character classes are very important regex components that tell us what kind of characters to expect. The easiest way to explain them is by breaking down the highlighted portions above.

```a-z``` is used to match any alphabetic character from A-Z
```0-9``` is used to match any number from 0-9 
```\d``` is effectively the same as ```0-9```, meaning it will match any digit 
```_``` means that an underscore _ character can be used
```\.``` indicates that a period . can be used (note: including the backslash\ "escapes" the period so it can just match a period rather than a period's special regex meaning)
```-``` means that a dash - character can be used

In other words, the first and second highlighted portions of the email can include any letter from A-Z, any number from 0-9, and any of the following characters: _.-
The third highlighted portion can include any letter from A-Z and a period. 

Important: the ```@``` is a character that must be included in the email address, as is the ```.``` that follows a backsplash between two groups. 

/^([a-z0-9_\.-]+)```@```([\da-z\.-]+)```\.```([a-z\.]{2,6})$/

### Grouping and Capturing
/^```([a-z0-9_\.-]+)```@```([\da-z\.-]+)```\.```([a-z\.]{2,6})```$/

The example above highlights the groups within the email regular expression. Simply put, parentheses are used to enclose blocks of the expression so that the block of the expression is "captured." This way, the pattern can be broken up into three distinctive parts (in our email example) and be separated by characters like ```@``` and ```.```.


### Bracket Expressions
/^(```[a-z0-9_\.-]```+)@(```[\da-z\.-]```+)\.(```[a-z\.]```{2,6})$/

Brackets are used to enclose a list of characters. A bracket expression matches a range of characters in a list, in our case.


## Author

Katarina Mihaylovich

Katarina Mihaylovich is a Los Angeles-based coding student at UCLA Extension. 
https://github.com/katarinamihaylovich


