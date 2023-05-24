# Regex Tutorial

## Summary

Regex or regular expression is a way to conditionaly select and match characters, numbers, and symbols in a prescribed way. It is an incredibly powerful and robust tool that is most commonly used for extracting substrings, searching, relpacing, and rearranging things, and data extraction.

In this Tuturial I will be going over the use use of [Anchors](#anchors), [Quantifiers], [Grouping Constructs](#grouping-constructs)(#quantifiers), [Bracket Expressions](#bracket-expressions), [Character Classes](#character-classes), [The OR Operator](#the-or-operator), [Flags](#flags), and [Character Escapes](#character-escapes).

I will also summarize the matching an email regex: Matching an Email: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Briefly summarize the regex you will be describing and what you will explain. Include a code snippet of the regex. Replace this text with your summary

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

Regex anchors are used to not match specific values in the expression but rather other elements such as positioning.

For example ths use of the "^" symbol followed by a value checks to see if that value matches the value of the element at the beginning of the string or line. For example ^b will return true for the string "basketball" as the "b" is that the beginning of the string. However, it will not match if you pass in the string "volleyball" since the begining of the string starts with a "v" even though there is a "b" in the string.

Other examples of achors are the following:

- $: Checks for the end of the string or line
- \A: Checks only for the beginning of the string
- \Z: Checks only for the end of the string

### Quantifiers



### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
