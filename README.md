# RegexTutorial


Regular expressions are a way to describe a search pattern in string data. They are powerful tools for processing strings. It is a pattern that is matched against a subject string from left to right. Regular expressions are used to replace text within a string, string extraction based on a pattern match, and so much more. The term "regular expression" is also known as "regex" or "regexp".

## Summary
___

Regex used - matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents
___

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Lookarounds](#4-lookarounds)
  - [Positive Lookahead](#41-positive-lookahead)
  - [Negative Lookahead](#42-negative-lookahead)
  - [Positive Lookbehind](#43-positive-lookbehind)
  - [Negative Lookbehind](#44-negative-lookbehind)
- [Flags](#flags)


## Regex Components
___

### Anchors
The characters `^` and `$` do not match any of the character of the regex string. They only represent the position before and after, or between characters. They can be used to "anchor" the regex match at a certain position. The ^ matches the position beforre the first character in the string, similarly the $ matches right after the last character in the string. 
### Quantifiers
Indicates the numbers of characters or expressions to match. In the instance of &nbsp; `{2,6}` &nbsp; will match any letters in between 2 to 6 characters long.<br>
`+` matches the previous token between one and unlimited times, as many times as possible, giving back as needed (greedy)
 
### Grouping Constructs
From the regex used, there are three groups being used. 
- First capturing group: `[a-z0-9_\.-]+)@` The "name" to match at any letters, numbers, underscore, dots and/or hyphens followed by an att symbol.
- Second Capturing group: `[\da-z\.-]+)\.` The "domain" to match any digits meta characters, letters, dot and/or hyphens as long as need be followed by a dot.
- Third Capturing group: `[a-z\.]{2,6}` The "domain suffix" which can be 2 to 6 alphabets long
### Bracket Expressions
Bracket expression indicate a set of characters inside the bracket to match any invidual character, for e.g. `[a-z]` will match any alphabets in lowercase.

### Character Classes
- With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. The character to be matched should be placed inside the square brackets, only the one character will be matched. <br>
Inside a character class, the dot &nbsp;`\.`&nbsp; loses its special meaning and matches a literal dot. The &nbsp; `\d`&nbsp; matches any digits equivalent to `[0-9]`

### Lookarounds
Lookbehinds and lookaheads (also called lookarounds) are specific types of
***non-capturing groups*** (used to match a pattern but without including it in the matching
list). Lookarounds are used when we a pattern must be
preceded or followed by another pattern. For example, imagine we want to get all
numbers that are preceded by the `$` character from the string
`$4.44 and $10.88`. We will use the following regular expression `(?<=\$)[0-9\.]*`
which means: get all the numbers which contain the `.` character and are preceded
by the `$` character. These are the lookarounds that are used in regular
expressions:

|Symbol|Description|
|:----:|----|
|?=|Positive Lookahead|
|?!|Negative Lookahead|
|?<=|Positive Lookbehind|
|?<!|Negative Lookbehind|

### Flags

Flags are also called modifiers because they modify the output of a regular
expression. These flags can be used in any order or combination, and are an
integral part of the RegExp.

|Flag|Description|
|:----:|----|
|i|Case insensitive: Match will be case-insensitive.|
|g|Global Search: Match all instances, not just the first.|
|m|Multiline: Anchor meta characters work on each line.|

