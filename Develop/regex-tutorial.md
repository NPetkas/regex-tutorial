# Regex-Tutorial

Regular expressions, or regex for short, are a series of special characters that define a search pattern. They can feel like their own language at times, but in fact they are universal and can be used within all programming languages.

## Summary

In this tutorial, we're going to explore the following regex expression:

* Matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

This expression is used to validate the email. To understand the components of the expression, reference the quick walk through guide for more details.



## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)


## Regex Components


### Anchors

Anchors belong to the family of regex tokens that don't match any characters, but that assert something about the string or the matching process.

- The `^` anchor signifies a string that begins with the characters that follow it

- The `$` anchor signifies a string that ends with the characters that precede it.


### Quantifiers

Quantifiers set the limits of the string that your regex matches (or an individual section of the string). They frequently include the minimum and maximum number of characters that your regex is looking for.

- `+` indicates that the previous character must occur at least one or more times. In the given expression, it matches a to z, `0-9`, special characters `'.','_','-'` and must have at least one time.

- `{n,m}` indicates occurrences of the preceding element between n and m. The regex has `{2,6}` which allows a match from 2 to 6 characters for set `[a-z\.]`.


### Grouping Constructs
 
Grouping Constructs are multiple parts of a string to determine what different sections fulfill different requirements.

- Groups are `([a-z0-9_\.-]+)`, `([\da-z\.-]+)` and `([a-z\.]{2,6})` where the first group captures the username for the email which must contain at least one characters from a to z, number from 0 to 9, special characters like`'-', '.' , '_'`.

- The second and third group captures the domain name that comes after `@`, that should match character from a - z, number from 0-9, and characters like `'_', '.', '-'`. The third group captures the top level domain name. In this expression it captures `'.com'`.


### Bracket Expressions

Bracket Expressions are sets of square brackets `([])` to represents a range of characters that we want to match. They are also known as a positive character group, because they outline the characters we want to include

- We have `[a-z0-9_\.-]`, this matches characters between `a-z, 0-9, '-', '.', '_'`. Next one is `[\da-z\.-]` which matches number from 0-9, characters from a-z, character like `'.', '-'`. And the last one is `[a-z\.]` which matches characters between a-z and character `'.'`.


### Character Classes

Character classes define a set of characters, any one of which can occur in an input string to fulfill a match.

- `\d` in the expression matches a single digit characters from 0-9. In the example expression the username must have at least one number.


### The OR Operator

| OR operator matches a string that is matched by either.

 - the ERE `a((bc)|d)` matches the string `abc` and the string `ad`. This operator doesn't exist in the expression.


### Flags

Flags are an optional parameter that modifies its behavior of searching. They are placed at the end of a regex, after the second slash, and they define additional functionality or limits for the regex.

- `g`—Global search: the regex should be tested against all possible matches in a string.

- `i`—Case-insensitive search: case should be ignored while attempting a match in a string.

- `m`—Multi-line search: a multi-line input string should be treated as multiple lines.


### Character Escapes

Character Escapes, also known as escape sequences, are sequences of characters that represent a single character within a string literal. They are used to represent characters that are difficult or impossible to type directly, such as control characters, non-printable characters, or characters with special meanings in certain contexts.

- `\n`: Represents a newline character.
- `\t`: Represents a tab character.
- `\r`: Represents a carriage return character.
- `**"`: Represents a double quote character.
- `'`: Represents a single quote character.
- `\`: Represents a backslash character.


## Author

For any questions or information:

Github Gist: [https://gist.github.com/NPetkas](https://gist.github.com/NPetkas)

Github Profile: [https://github.com/NPetkas](https://github.com/NPetkas)

Email: [nicopetkas@gmail.com](nicopetkas@gmail.com)