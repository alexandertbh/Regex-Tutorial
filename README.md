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

In our email validation Regex we can see that the regex starts with an "^" after the first "\" which starts the expression. This means that is will be checking at the beginning of the string for something.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

### Quantifiers

Quanitifiers match the number of times that an indicated element appear in the string and can be shown a number of different ways. The easiert to start is the "+" quanitifier that simply means one or more times. This means if you have "a+" and then pass the string "banana" it will highlight each of the corresponding "a"'s.

In our eamil validation expression we can see the "+" used two times to more one or more of the preceeding charations. This is done to in the first portion of the validation that is checking for the personal identifier of the email before the @ symbol and then again when checking for the domain name after the @ symbol later on.

`/^([a-z0-9_\.-]    +     )@([\da-z\.-]    +    )\.([a-z\.]{2,6})$/`

### Grouping Constructs

Grouping Constructs, as the name suggests, allows you to group a series of searches togther and include all of them at the same time. This is denoted using partasis with whatever is inside being what is included.

In our example the parenthases followed by the square brackets show that we are looking for anthing lowercase in the alphabet "a-z". This is followed by "0-9" meaning any numbers can be included as well. Finally it ends with "\.-" which means that symbols are included. Normally the "." by iteself would mean symbols are included but since it is in a group ir needs to be seperated with a "\" and followed by a "-" in order for it to work.

### Bracket Expressions

Brackets allow for the searching of ranges of of characters, numbers, or symbols. If you were to only do a parathese expression like (a-c) this would be essentially an OR statement for ever character show. Meaning "a" OR "-" OR "c". By braketing this same expression we turn this into a range to search through. Meaning "[a-c]" would equate to any character from "a" to "c" or in this case "a", "b", or "c".

This specifically used in our email validation regex in order to search for all the lowercase alphat letter by using "[a-z]" and then also for all of the numbers 0-9 by adding "[0-9]", and finally by including all of the symbols with the added "[\.-]".

### Character Classes

Character classes are buckets that letters, numbers, and symbols fall into that are enclosed within sqaure brackets. This allows you to search either ranges in total or specific sub sections of words. A good subsection example would be "b[aeo]nd". This means any string that starts with a "b" contains either an "a", "e", or "o", and ends with an "nd" would be selected. This would include the "band", "bend", or "bond".

This is used for selecting the alphabet, numberic, and symbol ranges as explained above.

### The OR Operator

This or opporator is a simply denoted as "|" and just means either or. So "(a|e)" would mean either "a" or "e" when doing a search. This is not particularly used in our regex example but is still good to know.

### Flags

Flags can be added at the end of regex expression in order to change how it conducts its seach. The most common use cases are "g" meaning global or able to search through multi lines or "i" which allow for the search to be case insesitive. This is not used in our example either.

### Character Escapes

Character escapes allow you to "escape" a specific search in order to add another search parameter. In our example when we want to find all of the symbols in the front half of our regex we would normally want to add a ".". However, since would be following seperate search it would take on a different meaning so we need to "escape" the search. This is done by adding "\" before whatever it is that you are wanting to search. By using this to escape the search and adding the ".-" after it we are able to search for all of possible symbols that could be added in the email.

## Author

Hi! I hope you enjoyed reading my brief article on regex expressions! My name is Alex Horning and I am a 2023 bootcamp grad from the UW FullStack Web Development Bootcamp. I was a Technical Recruiter that took a liking to all of the interesting things I saw my software Engineering Candidates doing and have wanted to learn more about coding and the art of creating things online in the digital age.

If you would like to learn more feel free to check out my gihub profile at: https://github.com/alexandertbh
