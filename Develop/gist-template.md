# Title Regex-Tutorial

AS a web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines

## Summary

In this tutorial we'll be looking at how the following Regex is used to match an email address:
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Continue reading to learn what each section of this code does. 

## Table of Contents

- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Boundaries](#boundaries)
- [Author](#author)

## Regex Components

var emailRegex = /\b([a-z])([\w\.]+)([^\W_]+)@([\da-z\.-]+)\.([a-z\.]{1,3})\b/g;

### Quantifiers

"+" Matches the pattern one or more times
For example the following code: ([\w\.]+) => [\w\.] Matches any word character equal to \w = [a-zA-Z0-9_] or \. matches the character "." one or more times.

"{}" Sets either an exact amount, min and max, or more than one copies of the sequence.
For example the following code: ([a-z\.]{1,3}) matches the previous ([a-z\.]) between 1 and 3 times, as many times as possible.

### OR Operator

"[]" Matches a character that is contained within the brackets.
For example the following code: [a-z] Matches the range of lower case letters from "a" to "z". 

"[^...]" Matches a character that is not contained within the brakets.
For example the following code: [^\W_] Matches any character that is not present in the list. \W Matches any non-word character ([^a-zA-Z0-9_]) and _ matches the character "_".

### Character Classes

"\d" Matches a single character that is a digit.

"\w" Matches a word character, i.e. [a-zA-Z0-9_].

### Flags

A flag is an optional parameter to a regex that modifies its behavior of searching.

"g" (global) Allows for the search to continue after the first match, making the expression search for all occurrences.


### Grouping and Capturing
"()" Captures everything enclosed within the parenthesis. This is a way to treat multiple characters as a single unit.

### Boundaries
"\b" is an anchor that matches at a position which is called a “word boundary”. This match is zero-length.

## Author

Courtney Thibodeau Full-Stack Coding MSU Student

GitHub: https://github.com/cthibodeau09
