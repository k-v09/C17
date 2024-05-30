# Understanding the Email Matching Regex

Regular expressions (regex) are tools for pattern matching and data validation. In this tutorial, I'll break down a regex that validates email addresses to understand how each part works. By the end, you'll have a clear understanding of how this ensures that user input is a properly formatted email address.

## Summary

The regex to be described is used for matching email addresses:

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

I will explain each component of this regex, which ensures that an email address is valid by checking the structure before and after the "@" symbol and the domain at the end.

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

Anchors are used to assert the position in a string. In our regex:
- `^` asserts the position at the start of the string.
- `$` asserts the position at the end of the string.

### Quantifiers

Quantifiers specify how many times a character or group can occur.
- `+` means one or more times. For example, in our regex `[a-z0-9_\.-]+` matches one or more lowercase letters, digits, underscores, dots, or hyphens.

### Grouping Constructs

Grouping constructs are used to create sub-expressions within a regex.
- `()` denotes a capturing group. So `([a-z0-9_\.-]+)` in our expression captures the username part of the email.

### Bracket Expressions

Bracket expressions match any one of the enclosed characters.
- `[a-z0-9_\.-]` matches any lowercase letter, digit, underscore, dot, or hyphen.

### Character Classes

Character classes match a set of characters.
- `\d` matches any digit.

### The OR Operator

The OR operator matches one of several patterns.
- `|` is not utilized in this particular regex but is common in others.

### Flags

Flags are used to modify the behavior of the regex.
- No flags are used, but common flags include `i` for case-insensitive matching.

### Character Escapes

Character escapes are used to match special characters. In our regex:
- `\.` matches a literal dot.

## Author

This tutorial was written by Noah Sehman. You can find more of my work on my [GitHub profile](https://github.com/k-v09).
