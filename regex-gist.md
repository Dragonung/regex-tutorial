# Introduction

There are several useful functions on the Internet that go through a specific analytic process before moving forward. 
Examples include when creating a password; the password must be at least 8 characters, or when using the "Find/Replace" feature to find/replace a specific keyword/phrase in a very long article on the Internet. 
All of these processes use Regex to scan and analyze strings in order to make streamline the way strings are read and used.

## Summary

Under the TOC lists various terms that contain different methods on how to perform various regular expressions. <br/>

The code will act as an example of how regex is broken down in order for users to better understand how it analyzes certain strings.

## Table of Contents

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

 -^: matches exact string and is case-sensitive <br/>
 -$: string ends with characters that precede it (can be exact or range)

### Quantifiers

 -*: matches pattern 0-5 times <br/>
 -+: matches pattern >=1 time <br/>
 -?: matches pattern 0 or 1 time <br/>
 -{}: { n }: matches exactly n times <br/>
     { n, }: "      at least n " <br/>
     { n, x}: " n to x "

### OR Operator

 |: if one expression in several grouping constructs is true, entire expression is true

### Character Classes

 -.: matches any char except newline char (\newline) <br/>
 -\d: " Arabic numeral digit; equivalent to [0-9] <br/>
 -\w: " alphanumeric with basic Latin alphabet, including underscore (_); equivalent to [A-Za-z0-9_] <br/>
 -\s: " single whitespace character, including tabs & line breaks

### Flags

 -i: search is case-insensitive <br/>
 -g: searches all matches <br/>
 -m: multiline mode; affects behavior of '^' and '$' <br/>
 -s: "dotall" mode; allows dot '.' to match newline character '\n' <br/>
 -u: enables full Unicode support, allowing greater coverage for many different characters <br/>
 -y: "Sticky" mode; allowing search at a given position in the source string

### Grouping and Capturing

 -grouping(()): if two or more subexpressions, all must exactly match; similar to AND operator in Javascript <br/>
 -capturing: useful for capturing very specific data (dates, phone numbers, emails, etc.)

### Bracket Expressions

 -[]: range of characters to match <br/>
    -[a-z]: lowercase letter between a-z; uppercase letters must be searched with [a-zA-Z] <br/>
    -[0-9]: any number between 0-9 <br/>
    -[_-]: contains underscore or hyphen 

### Greedy and Lazy Match
 
 -greedy: will match more characters than expected <br/>
 -lazy:   will match fewer characters than expected

### Boundaries

 -\b: word boundary; matches positions of a word char depending on boundary placement <br/>
 -\B: Not-a-word-boundary; matches positions of individual chars in a string, in that order <br/>
 -Left- and Right-of-Word boundaries <br/>
    -[[:<:]]: beginning-of-word; will find strings starting with word; cannot be placed at end <br/>
    -[[:>:]]: end-of-word; will find strings ending with word; cannot be placed at beginning

### Back-references
 
 -a way to match same text as previously matched by a capturing grouping <br/>
    -Ex: finding duplicate words, palindromes, and replacing text 

### Look-ahead and Look-behind

 -(?=chars): find pattern ahead of current position of string without comsuming chars in string <br/>
 -(?!chars): find pattern if NOT followed by chars in string <br/>
 -(?<=chars): find pattern behind position of chars in string <br/>
 -(?<!chars): do not match a string if chars before it

## Author

 Daniel Chen: another Berkeley bootcamp student

 Github: https://github.com/Dragonung

