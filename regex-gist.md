# Introduction

There are several useful functions on the Internet that go through a specific analytic process before moving forward. 
Examples include when creating a password; the password must be at least 8 characters, or when using the "Find/Replace" feature to find/replace a specific keyword/phrase in a very long article on the Internet. 
All of these processes use Regex to scan and analyze strings in order to make streamline the way strings are read and used.

## Summary

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

^: matches exact string and is case-sensitive
$: string ends with characters that precede it (can be exact or range)

### Quantifiers

 *: matches pattern 0-5 times
 +: "       "       >=1 "
 ?: "       "       0 or 1 "
 {}: { n }: matches exactly n times
    { n, }: "      at least n "
    { n, x}: " n to x "

### OR Operator

 |: if one expression in several grouping constructs is true, entire expression is true

### Character Classes

 .: matches any char except newline char (\newline)
 \d: " Arabic numeral digit; equivalent to [0-9]
 \w: " alphanumeric with basic Latin alphabet, including underscore (_); equivalent to [A-Za-z0-9_]
 \s: " single whitespace character, including tabs & line breaks

### Flags

 i: search is case-insensitive
 g: searches all matches
 m: multiline mode; affects behavior of '^' and '$' 
 s: "dotall" mode; allows dot '.' to match newline character '\n'
 u: enables full Unicode support, allowing greater coverage for many different characters
 y: "Sticky" mode; allowing search at a given position in the source string

### Grouping and Capturing

 grouping(()): if two or more subexpressions, all must exactly match; similar to AND operator in Javascript
 capturing: useful for capturing very specific data (dates, phone numbers, emails, etc.)

### Bracket Expressions

 []: range of characters to match
    -[a-z]: lowercase letter between a-z; uppercase letters must be searched with [a-zA-Z]
    -[0-9]: any number between 0-9
    -[_-]: contains underscore or hyphen

### Greedy and Lazy Match
 
 greedy: will match more characters than expected
 lazy:   will match fewer characters than expected

### Boundaries

 \b: word boundary; matches positions of a word char depending on boundary placement
 \B: Not-a-word-boundary; " "         " individual chars in a string, in that order
 Left- and Right-of-Word boundaries
    [[:<:]]: beginning-of-word; will find strings starting with word; cannot be placed at end
    [[:>:]]: end-of-word; will find strings ending with word; cannot be placed at beginning

### Back-references
 
 a way to match same text as previously matched by a capturing grouping
    Ex: finding duplicate words, palindromes, and replacing text 

### Look-ahead and Look-behind

 (?=chars): find pattern ahead of current position of string without comsuming chars in string
 (?!chars): find pattern if NOT followed by chars in string
 (?<=chars): find pattern behind position of chars in string
 (?<!chars): do not match a string if chars before it

## Author

 Daniel Chen: another Berkeley bootcamp student

 Github: https://github.com/Dragonung

