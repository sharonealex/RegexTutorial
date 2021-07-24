# RegexTutorial


Regular expressions are a way to describe a search pattern in string data. They are powerful tools for inpecting and processing strings.

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
___

