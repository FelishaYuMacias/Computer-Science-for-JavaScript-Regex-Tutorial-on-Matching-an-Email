# Computer Science for JavaScript: Regex Tutorial on Matching an Email
Module 17 Challenge

Let's talk regex! 

Regex is short for regular expression. A regular expression is a series of special characters that define a search pattern within a string and helps us search for more dynamic and encompassing data than a simple direct match.

## Summary

The example we are covering is used to match or validate email addresses. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [Conclusion](#conclusion) 

## Regex Components

### Anchors
Anchors are used to assert the position the characters have to be within the string. Usually either the beginning or end.

The anchors used in this expression are `^` and `$`. 

The `^`is the beginning anchor and signifies that the string we are verifying should begin with the characters that come after the anchor.

The `$` is the end anchor and signifies that the string we are verifying should end with the characters that came before the anchor.

So, if we are matching an email, we want to verify that the email starts with a string matching `([a-z0-9_\.-]+)` and ends with a string matching `([a-z\.]{2,6})`.


### Quantifiers
Quantifiers tell us how many characters or expressions to match. The ones used in our example are the `+` which signifies that at least one of the previously listed characters must be included and `{n, m}` which signifies that we need from *n* to *m* number of characters. 

For verifying an email address, we have, `[a-z0-9_\.-]+` which means we need at least one letter, number, period or hyphen. The letters are case sensitive.

Also `[\da-z\.-]+` means we need at least one letter, a period or a hyphen. The letters are case sensitive.

Lastly `[a-z\.]{2,6}` means we need between 2 and 6 characters that can include any letter or a period. The letters are case sensitive.


### Grouping Constructs
Grouping constructs separate sections of the string so that each section can be compared independently. This also allows for the matching of repeated sections and adding quantifiers to a section (see above section for more information on quantifiers). Constructs are grouped using parentheses `()`. 

There are 3 groups in our example.
`([a-z0-9_\.-]+)`
`([\da-z\.-]+)`
`([a-z\.]{2,6})`


### Bracket Expressions
Square brackets [] are used to represent the range of characters we can accept. This is called a bracket expression. 

In our matching email example, the following bracket expressions are used:
* `[a-z0-9_\.-]`- This means that we can accept any combination of uppercase letters, lowercase letters, numbers 0-9, periods, underscores, and hyphens. It is case sensitive so "Felisha" would not match "felisha".
* `[\da-z\.-]` - This means we can accept any combination of digits (this is the same as listing `[0-9]`), uppercase letters, lowercase letters, periods and hyphens. It too is case sensitive. 
* `[a-z\.]` - This means we can accept any combination of lowercase and uppercase letters. This is also case sensitive.


### Character Classes
A character class defines a set of characters. By using character classes, we do not have to list all possible options that we want to match. Our example uses the character class `\d` to mean "digit" or all numbers from 0 to 9. It also uses `[a-z]` meaning all letters from a to z and `[0-9]`all numbers from 0 to 9. Notice that `\d` and `[0-9]` are the same.


### Conclusion
Our expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` means to have a valid email we need:

* At least one character that can be a number, letter (case sensitive), period or hyphen  

* Followed by the @ sign

* Followed by at least one character that can be a number, letter (case sensitive), period or hyphen 

* Followed by a period (.)

* Finished with between 2 and 6 characters that can be letters (case sensitive) or a period (.)


## Author

Hi! My name is Felisha Yu-Macias. I am a former banker turned coder.

Here is a link to the gist: https://gist.github.com/FelishaYuMacias/93e02ae2a41e9be4e83a2dd143cfe9b5

Please check out my GitHub:https://github.com/FelishaYuMacias

