# regex-tutorial

# Title (replace with your title)

This is a tutorial that will walk you through Regular Expressions otherwise know as REGEX

## Summary

In this walk through you will learn about Regular expressions and how to use REGEX. Topics covered inclued "REGEX Components", "Anchors", "Quantifiers", "Grouping Constructs", Bracket Expressions, Character Classes, The OR Operator, Flags, and Character Escapes

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## REGEX Components

### Anchors
Anchors are characterized bt the "^" & "$" symbols expressed at the beginning and end of the of code shown shown below
/^([e+n0-9_\.+]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

The ^  signifies that the REGEX will match the beginning of the word (explanation below) that the "^" precedes. The "$" signifies  REGEX will match the ends of a string that the dollar sign follows.

example:

@AOl.com would not be matched by this REGEX because the @ sign at the beginning of the string is not included in the group that follows the caret.

Ronney@gmail.com would be matched because the string begins with characters that match the group.
### Quantifiers
Quantifiers in REGEX are "+" & "{}" 

example below:

/^([e+n0-9_\.+]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Quantifiers will match the amount of characters specified

The "+" quantifier matches 1 or more characters. The "*" quantifier matches >= 0  characters. The "?" matches 0 or 1 characters. The {n} quantifier will match n characters. The {x,y} quantifier will match an expression that is at least 1 characters, but no more than y characters.

The quantifier often follows a character class or bracket expression that defines what characters the REGEX will match, as in the example below:
[z-c0-9_\.+]-
In this example, [z-c0-9_\.+]-, a matching expression will be anywhere from 2 to 6 characters in length composed of characters as defined by the bracket expression that precedes the {} quantifier.

Within the braces defines what the REGEX will match, the quantifier indicates how manyto be matched
### Grouping Constructs
(_) are used for grouping in REGEX. In this particular REGEX, grouping is used to separate meta characters from literal characters. Grouping or capturing can be used to isolate partS of a string reference or to replace part of A string.

/^([e+n0-9_\.+]+)@([\bc-z\.-]+)\.([a-z\.]{2,6})$/
([e+n0-9_\.+]+) and ([\da-z\.-]+) and ([a-z\.]{2,6})
### Bracket Expressions
Bracket expressions defines what characters REGEX will match. An example of a bracket expression from the regex we have been examining is:

[e+n0-9_\.+]
### Character Classes
\d \w \s and .

\d         matches a single character that is a digit -> Try it!
\w         matches a word character (alphanumeric character plus underscore) -> Try it!
\s         matches a whitespace character (includes tabs and line breaks)

Use the . operator carefully since often class or negated character class (which we’ll cover next) are faster and more precise.
\d, \w and \s also present their negations with \D, \W and \S respectively.
For example, \D will perform the inverse match with respect to that obtained with \d.

\D         matches a single non-digit character

reference (https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)

### The OR Operator
a(b|c)     matches a string that has a followed by b or c (and captures b or c)
a[bc]      same as previous, but without capturing b or c
### Flags
A regex usually comes within this form /abc/, where the search pattern is delimited by two slash characters /. At the end we can specify a flag with these values (we can also combine them each other):
g (global) does not return after the first match, restarting the subsequent searches from the end of the previous match
m (multi-line) when enabled ^ and $ will match the start and end of a line, instead of the whole string
i (insensitive) makes the whole expression case-insensitive (for instance /aBc/i would match AbC)

reference (https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)

### Character Escapes
In order to be taken literally, you must escape the characters ^.[$()|*+?{\with a backslash \ as they have special meaning.
\$\d       matches a string that has a $ before one digit 

reference (https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
## Author
My Name is Brandon Williams I am a Student at NorthWestern Bootcamp studying o become a full-Stack web-developer
You can follow my journey and collab with me on my repos at https://github.com/brandonawilliams1
