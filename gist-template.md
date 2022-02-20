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
With a “character class”, also called “character set”, you can tell the regex engine to match only one out of several characters. Simply place the characters you want to match between square brackets.
* ^	Matches the starting position within the string. In line-based tools, it matches the starting position of any line.
* ( )	Defines a marked subexpression. The string matched within the parentheses can be recalled later (see the next entry, \n). A marked subexpression is also called a block or capturing group.
* [ ]	A bracket expression. Matches a single character that is contained within the brackets. For example, [abc] matches "a", "b", or "c". [a-z] specifies a range which matches any lowercase letter from "a" to "z". These forms can be mixed: [abcx-z] matches "a", "b", "c", "x", "y", or "z", as does [a-cx-z].
The - character is treated as a literal character if it is the last or the first (after the ^, if present) character within the brackets: [abc-], [-abc]. Note that backslash escapes are not allowed. The ] character can be included in a bracket expression if it is the first (after the ^) character: []abc].
* $	Matches the ending position of the string or the position just before a string-ending newline. In line-based tools, it matches the ending position of any line.
* +	Matches the preceding element one or more times. For example, ab+c matches "abc", "abbc", "abbbc", and so on, but not "ac".
* \d or [0-9] matches character from 0-9.
* [a-z]	Match any lowercase character from a to z.
* {2,6} The preceding element or subexpression must occur between 2 and 6 times, inclusive.

### Flags
A flag is an optional parameter to a regex that modifies its behavior of searching. A flag changes the default searching behaviour of a regular expression. It makes a regex search in a different way. A flag is denoted using a single lowercase alphabetic character.

### Grouping and Capturing

### Bracket Expressions
A bracket expression is either a matching list expression or a non-matching list expression. It consists of one or more expressions: ordinary characters, collating elements, collating symbols, equivalence classes, character classes, or range expressions. The <right-square-bracket> ( ']' ) shall lose its special meaning and represent itself in a bracket expression if it occurs first in the list (after an initial <circumflex> ( '^' ), if any). Otherwise, it shall terminate the bracket expression, unless it appears in a collating symbol (such as "[.].]" ) or is the ending <right-square-bracket> for a collating symbol, equivalence class, or character class. The special characters '.', '*', '[', and '\\' ( <period>, <asterisk>, <left-square-bracket>, and <backslash>, respectively) shall lose their special meaning within a bracket expression.
The character sequences "[.", "[=", and "[:" ( <left-square-bracket> followed by a <period>, <equals-sign>, or <colon>) shall be special inside a bracket expression and are used to delimit collating symbols, equivalence class expressions, and character class expressions. These symbols shall be followed by a valid expression and the matching terminating sequence ".]", "=]", or ":]", as described in the following items.

### Greedy and Lazy Match
Expand the match as far as possible through the text.
These are some examples of Greedy and Lazy Matching. * + {} - These characters can be used as a quantifier for Greedy or Lazy match.

### Boundaries
A word boundary, in most regex dialects, is a position between \w and \W (non-word char), or at the beginning or end of a string if it begins or ends (respectively) with a word character ( [0-9A-Za-z_] ). So, in the string "-12" , it would match before the 1 or after the 2.

### Back-references
Backreferences match the same text as previously matched by a capturing group. Suppose you want to match a pair of opening and closing HTML tags, and the text in between. By putting the opening tag into a backreference, we can reuse the name of the tag for the closing tag. 

### Look-ahead and Look-behind

Lookahead is used as an assertion in Python regular expressions to determine success or failure whether the pattern is ahead i.e to the right of the parser's current position. They don't match anything. Hence, they are called as zero-width assertions.

Lookbehind, which is used to match a phrase that is preceded by a user specified text. Positive lookbehind is syntaxed like (? <=a)something which can be used along with any regex parameter. The above phrase matches any "something" word that is preceded by an "a" word.

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
