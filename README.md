# Regex Tutorial, email 

Today, you'll have the opportuniy to better understand regex, regular expressions. Throughout this passage, you'll have regex simplified and explained in a manner most can understand.
## Summary

We'll be using this example of regex for this tutorial: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, that is used to go through a set of data to match strings that would in turn, be a valid email address. We'll be discussing certain fundamental aspects about anchors, quantifiers, grouping constructs, bracket expressions, cahracter classes, the OR operator, flags, and character escapes.

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

Anchors are used to identify where the matching should occur in a string, `^` is used to identify that the match should occur at the start, while `$` is used to identify that the match should occur at the end.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
 &nbsp; &#8593; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp;&emsp; &emsp; &emsp; &emsp; &emsp; &nbsp; &#8593;

### Quantifiers

#### Exact Count

A number in curly braces `{n}` is the simplest quantifier. When you append it to a character or character class, it specifies how many characters or character classes you want to match.

#### The Range

The range matches a character or character class from n to m times, `{n,m}`

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
 &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp; &emsp;&emsp; &emsp; &emsp; &emsp; &emsp; &nbsp; &#8593;
 
 #### Shorthands

#### `+`
The quantifier `+` means one or more. It is the same as `{1,}`.
  
`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
&emsp; &emsp; &emsp; &emsp; &emsp; &nbsp; &nbsp; &#8593; &emsp; &#8593; &emsp; &emsp; &emsp; &nbsp; &#8593;

#### `?`
The quantifier `?` means zero or one.`{0,1}`.


#### `*`
The quantifier `*` means zero or more.`{0,}`.

### Grouping Constructs

By placing part of a regular expression inside round brackets or parentheses, you can group that part of the regular expression together. This allows you to apply a quantifier to the entire group or to restrict alternation to part of the regex. Only parentheses can be used for grouping. Square brackets define a character class, and curly braces are used by a quantifier with specific limits.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
&emsp; &#8593; &emsp; &emsp; &emsp; &emsp; &nbsp; &#8593; &nbsp; &#8593; &emsp; &emsp; &emsp; &nbsp; &#8593; &emsp; &#8593; &emsp; &emsp; &emsp; &emsp; &#8593;

### Bracket Expressions

A bracket expression is a list of characters enclosed by `[` and `]`. It matches any single character in that list. If the first character of the list is the caret '^', then it matches any character not in the list, and it is unspecified whether it matches an encoding error. 

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
&emsp; &nbsp; &#8593; &emsp; &emsp; &emsp; &nbsp; &#8593; &nbsp; &nbsp; &nbsp; &#8593; &emsp; &emsp; &nbsp; &nbsp; &#8593; &nbsp; &nbsp; &nbsp; &#8593; &emsp; &nbsp; &nbsp; &#8593;

### Character Classes

`.`:

`\d`: Matches any digit (Arabic numeral). Equivalent to [0-9].

`\D`: Matches any character that is not a digit. Equivalent to [^0-9].

`w`: Matches any alphanumeric character from the basic Latin alphabet, including the underscore. Equivalent to [A-Za-z0-9_].

`W`: Matches any character that is not a word character from the basic Latin alphabet. Equivalent to [^A-Za-z0-9_].

`s`: Matches a single white space character, including space, tab, form feed, line feed, and other Unicode spaces.

`S`: Matches a single character other than white space.

`t`: Matches a horizontal tab.

`r`: Matches a carriage return.

`n`: Matches a linefeed.

`v`: Matches a vertical tab.

`f`: Matches a form-feed.

`[\b]`: Matches a backspace.

`0`: Matches a NUL character. Do not follow this with another digit.

`cX`: Matches a control character using caret notation, where 'X' is a letter from A–Z

### The OR Operator

The OR operator is a `|` symbol, it can be used like `t|T` matching lower 't' and capital 'T' would be the outcome.

### Flags

`d`: Generate indices for substring matches.

`g`: Global search.

`i`: Case-insensitive search.

`m`: Multi-line search.

`s`: Allows . to match newline characters.

`u`: "unicode"; treat a pattern as a sequence of unicode code points.

`y`:	Perform a "sticky" search that matches starting at the current position in the target string.

### Character Escapes

If you need to use any special character, let's say you need to find "*" for instance, you must escape it by putting a backslash in front of it. For instance, to search for 'a' followed by '*', followed by 'b', you'd use `/a\*b/` — the backslash escapes the '*', making it literal instead of special.

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` <br>
&emsp; &emsp; &emsp; &nbsp; &nbsp; &nbsp; &#8593; &emsp; &emsp; &nbsp; &nbsp; &#8593; &emsp; &#8593; &emsp; &emsp; &#8593; &emsp; &emsp; &#8593;

## Author

Im an aspiring software engineer currently enrolled in a UCLA bootcamp attendee with a passion to learn. A great tool when coding is regex, to get pin point validtation. Check out my github at https://github.com/marsmeshed
