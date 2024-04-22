# Regex-Tutorial-Matching-Hex-Value

Hey there! This is a short tutorial on <strong>regular expressions</strong> (or regex/regexp for short). Regex is a tool used to find patterns in string values. 
There are several ways to use it but today we will be going over one specific application of regex: <b>Matching Hexadecimal color values.</b>

## Summary

The regex pattern `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` lets us validate both long and short forms of hex values/codes. Below we will break down each component to better understand how it works! 
My goal here is readability and easy understanding.

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

<i>Example</i>: `#([a-f0-9]{5})` matches `#abcde` but <strong>not</strong> `#abc`.

### OR Operator

The OR operator `|` lets us look for alternative matches and specifically it enables to match both full (`#rrggbb`) and short (`#rgb`) hex formats.

<i>Example</i>: `#([a-f0-9]{6}|[a-f0-9]{3})` matches both `#aabbcc` and `#123`.

### Character Classes

Character classes `[a-f0-9]` define a set of characters to match. With hex regex,
we can use this class to cover all <strong>valid</strong> hexadecimal characters (a-f and 0-9).

<i>Example</i>: `#[a-f0-9]{6}` matches any full hex color value such as `#abc000` or `#aa1234`.

### Flags

Flags are generally not needed for Hex Matching but some examples are `a` which is used for global
matching or `i` which is used for case-insensitivive matching.

<i>Possible Example</i>: `/#[a-f0-9]{6}/i` matches both `#dd1111` and `#DD1111.`
Again, flags won't be super important for hex codes, as they are almost always written in lowercase form.


### Grouping and Capturing

We use parentheses to group and capture subexpressions. With hex regex we can group the pattern for the short 
<strong>and</strong> long hexadecimal formats.

<i>Example</i>: `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/` captures the full or short hex value!

### Bracket Expressions

Bracket expressions are used in regex to declare character sets to match.
This is where the `[a-f0-9]`, repeated above often, comes into play. This is how we can ensure
that the values used are valid for hexadecimal use. 

<i>Example</i>: `#[abcdef0-9]{6}` matches any full hex color value like `#123456`, `#aaaaaa`, `#ff0945`, etc.

### Greedy and Lazy Match

Greedy quantifiers are used to match as much as possible. We add a `?` at the end to make it lazy. 

These kinds of quanitifiers can be explained in much more depth, but they aren't really needed when dealing with <br>
Hexadecimal codes so we'll move on, but further explanation can we found with these sources.

[Mastering Quantifiers](https://www.rexegg.com/regex-quantifiers.html) <br>
[What Do Greedy and Lazy mean in the context of regular expressions?](https://stackoverflow.com/questions/2301285/what-do-lazy-and-greedy-mean-in-the-context-of-regular-expressions)

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

This regex tutorial was written by Derek Medrano. Additional work can be found on here: https://github.com/derekmedrano
