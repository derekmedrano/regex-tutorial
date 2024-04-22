# Regex-Tutorial-Matching-Hex-Value

Hey there! This is a short tutorial on <strong>regular expressions</strong> (or regex/regexp for short). Regex is a tool used to find patterns in string values. 
There are several ways to use it but today we will be going over one specific application of regex: <b>Matching Hexadecimal color values.</b>

## Summary

The regex pattern `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` lets us validate both long and short forms of hex values/codes. Below we will break down each component to better understand how it works!

0## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

Anchors check to see if the regex matches at specific positions within the string. 
In this hex regex the `^` declares the start of the string and the `$` is the end.

<i>Example</i>: `^#dd0000` matches the hex value of `#dd0000` but <strong>not</strong> `#dd0000xyz`.

### Quantifiers

Quantifiers determine the number of times a character/group should be matched. With Hex values we use the
` { } ` format to specificy the amount of characters. `{3}` and `{9}` specify that there must be 3 and 9 hex characters.

<i>Example</i>: `#([a-f0-9]{7})` matches `#abcdefg` but <strong>not</strong> `#abcd`.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
