# Regex-Tutorial

What is Regex or regular expressions?

Regular expressions are specially formatted text strings to find patterns in text. Commonly used for text processing and manipulation and validation of input. Regex is formed by a sequence of characters to create a search pattern, which can be applied to text search, validation of input and text replace operations.

## Summary

This tutorial will tackle and explain how to make a regex to validate an input to be an email.
To validate then input we will have the regex as shown below:       

               /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

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
Anchors are part of the regex that do not match any character that we intend to search or validate.  They are considered as indicator for a start and end and is represented by the ^ and $.

The ^ anchor indicates to match a string after the anchor.  This means applying ^r will match 'r' for a string of 'reg'.  ^reg will match 're' of the string 'reg' and that ^reg will match 'reg' of the whole string of 'reg'.

The $ anchor serves as a terminator or end of the regex search or validation.  This means x$ macthes 'x' for a string/input of 'ex'. In turn, e$ does not match for the same string but ex$ will match the whole string of 'ex'.

Therefore in our regex to validate that the input maches an email, we start of with a ^ as we want to test for characters after it.  We then have the $ at the end to indicate the 'end' of the expression.  

### Quantifiers

Quantifiers as what the terms suggested will be you requirement for the number of characters.  A quantifier or quantifiers may indicate a requirement for the minimum number of characters, exact number of characters to be matched and a specific minimum to maximum number of characters to be matched. The curly bracets {} serves as a container for the quantifiers

Quantifiers can choose wilcards to specify the number of characters.

-   '*' -- is a univeral wildcard that accepts any character and any number of inputs. A zero input is acceptable the the asterisk. '*' wildcard.
        -     *com basically matches basic.com, abbasiccom, abscom, acom or com but does not match bacis.cmm.
-   '+'  -- is a wildcard that validates or matches a patter for one or more times.
        -     +com as with *com will match 'basiccom', 'abbasiccom', 'abscom' but rejects 'com', as as least 1 character must be there before the .com string.
-   '?' -- is a wildcard that will accept a pattern for 

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
