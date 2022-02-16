# Regex Tutorial

A regex, which is short for regular expression, is a sequence of characters that defines a specific search pattern. When included in code or search algorithms, regular expressions can be used to find certain patterns of characters within a string, or to find and replace a character or sequence of characters within a string. They are also frequently used to validate input.
Email validation and passwords are a few areas of strings where Regex is widely used to define the constraints. Regular Expressions are provided under java.



## Summary

A regular expression can be a single character, or a more complicated pattern.

Regular expressions can be used to perform all types of text search and text replace operations.

For example, the following regular expression can be used to verify that user input is a valid email address:

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

Each component of this regex has a unique responsibility to make sure that a user enters an email address that begins with an unspecified number of characters preceding the @ symbol, followed by a domain.

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
* Matching Fixed Strings
* Matching Special Characters
* Matching Character Sets
* Specifying Groups and Fields
* Evaluating Occurrences
* Specifying Location
* Specifying Alternatives
* Matching Information from a Table
* Capturing Multiple Lines
* Managing the Scope of Analysis

### Anchors
Anchors are a bit strange in the world of regex; they don't match any characters. What they do is ensure that a regex matches a string at a specific place: the beginning or end of the string or end of a line, or on a word or non-word boundary.
Anchors provide a way to limit how a regex matches a particular string by telling the regex engine where matches can begin and where they can end.

### Quantifiers
Specifies how many instances of a group, character, or character class must be in the input for a match to be found.
These are some examples of Quantifiers /X./; // matches any character /X*/; // Matches zero or several repetitions of letter X, is short for {0,} /X+-/; // matches one or more repetitions of letter X, is short for {1,} /X?/; // finds no or exactly one letter X, is short for is short for {0,1}. // d{3}; // matches three digits. {} describes the order of the preceding liberal // d{1,4} ; // means d must occur at least once and at a maximum of four

### OR Operator
Splits the text with a bar and matches everything to the left or right of the bar. If you want to limit the reach of it you need parenthesis, mostly used with booleans.
These are some examples of OR Operators

(some truthy expression) || expr expr1 || expr2

### Character Classes

### Flags
A flag is an optional parameter to a regex that modifies its behavior of searching. A flag changes the default searching behaviour of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character.

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
