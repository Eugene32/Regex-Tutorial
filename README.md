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

Quantifiers as what the terms suggested will be you requirement for the number of characters.  A quantifier or quantifiers may indicate a requirement for the minimum number of characters, exact number of characters to be matched and a specific minimum to maximum number of characters to be matched. The curly bracets { } serves as a container for the quantifiers

Quantifiers can choose wilcards to specify the number of characters.

-   ' * ' -- is a univeral wildcard that matches zero or more occurence.
        -   A regex of 29* will completely match an input of ' 2 ' as well as ' 299 '
-   ' + '  -- is a wildcard that validates or matches a patter for one or more times.
        -   A regex of 29+ will completely NOT match an input of ' 2 ' but will match ' 29 ' and ' 299 '
-   ' ? ' -- is a wildcard that will accept a pattern for one or no character.
        -   A regex of 29? willmatch an input of ' 2 ' and ' 29 ' but will NOT match ' 299 ' 

Using the curly brackets, { } as a limiter provides a better way of limit or dictating the match requirement.

-   { i } - sets the match to be an exact number of times.
        -   { 4 } means that it will only match if there are 4 characters in the input or string.
-   { i , }   - setting the minimum number of characters as a match.
        -   { 8 } means that it will only match if the input has at least 8 characters.
-   { i, n }  - the pattern must be a minimum character as i and a maximum of n characters.
        -   { 4 , 7 } means that a match will only happen when the evaluated string will have at least 4 characters and a maximum of seven characters.  Anything beyond the scope will not result to a match.
    
In our email regex, we have the { 2 , 6 } quantifier that sets the condition of the match to be a minimum of 2 characters to a maximum of 6 characters. This will cater for the email's domain that ends with a '.au', '.net', '.com' or '.museum'.


### Grouping Constructs

Grouping constructs allows evaluation of the regex as a group or segments instead of the entire entry.  A group is identfited by a pair of open and close parenthesis, ( ).

          /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
          
The email regex has three groups which represents the part of the email namely: username, `([a-z0-9_\.-]+)`, email server `([\da-z\.-]+)` and the domain, `([a-z\.]{2,6})`.  For an email address of fake@fakemail.com, the user name is 'fake', 'fakemail' is the server and the domain is '.com'.


### Bracket Expressions

Is a part of the regex represented by square brackets ([ ]).  The bracket translate as to look for a match regardless of length and location contained in it. 

Our email regex has `[a-z0-9_\.-\d]' dissecting the expresion means we will validate for:
- `[ a-z ]`  --> The string can contain all lowercase characters between a to z. Uppercase characters will not be considered as a match.  However, this not a problem as it is a protocol to convert all email address inputs to lowercase,thus there is no need to include A-Z requirement.
- `[ 0-9 ]` --> The string can contain numerical value from 0 - 9.
- `[ _\.-]` --> The string can include an underscore, ( _ ) , a period ( . ) and a hyphen ( - ).




### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
