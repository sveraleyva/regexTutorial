# Regex: How a computer can match an email address

A regex, or regular expression, is a string of characters that describes a particular pattern of search. Regular expressions can be utilized in coding or searching programs to locate certain character patterns within a string, replace specific characters or sequences within a string, or to validate input. Regex can be used to match and identify specific patterns within a string. This is particularly useful for searching and extracting data from large amounts of text. It can also be used to modify text by replacing or removing specific characters or patterns within a string, and to validate input from users by checking if the input matches a specific pattern.

## Summary

In this tutorial, I'll walk you through this expression: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`, which is used to match email addresses. Email addresses follow a specific format (username@domain.top-level-domain). We can use a regular expression to make sure an input string matches their format. If the input string matches this pattern, the regex will return a successful match.

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

Each section that describes a component should include more than just one sentence explaining what it does. It should also include a code snippet of that particular component and some examples that meet the requirements of that component.

### Anchors

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` begins with the ^ and $ anchors, which respectively mark the start and end of the string being searched. This ensures that the entire string matches the expression, rather than just a portion of it. 

### Quantifiers

Quantifiers specify how many times a character or group of characters should be matched. In this case, the + quantifier is used to indicate that the preceding character class should be matched one or more times.

### OR Operator

The OR operator, represented by the | symbol, allows for multiple options to be matched. In this expression, however, there is no OR operator.

### Character Classes

Character classes match a range of characters or a specific type of character, respectively.

[a-z0-9_\.-] - Matches any lowercase letter, digit, underscore, dot or dash on the username.
[\da-z\.-] - Matches any digit, lowercase letter, dot or dash on the domain.
[a-z\.] - Matches any lowercase letter or dot on the top-level domain.

### Flags

Flags modify how the expression is evaluated. For example, /a+/i with the "i" flag would match words like "apple", "aloe", "ant", and "Alligator". The "i" flag tells the computer to ignore whether the letter "a" is uppercase or lowercase, so it will find both "ant" and "Alligator" in the list. This expression does not have any flags.

### Grouping and Capturing

Using parentheses in a regular expression lets you capture and group certain parts of the pattern, so you can use them again later on. For this regex, there are three groups that are captured: the username, the domain name, and the top-level domain.

### Bracket Expressions

Bracket expressions tell the computer to look for the character that is within the brackets.
For example, [A] will match any occurrence of "A" within the string. This expression establishes that the username can have lowercase letters, digits, underscores, dots, or hyphens. The domain name after the "@" symbol can have digits, lowercase letters, dots, and hyphens. The top-level domain after the last dot must have 2 to 6 lowercase letters or dots.

### Greedy and Lazy Match

Regex expressions are greedy by default, which means they will match the longest possible string that satisfies the pattern. A greedy match tries to match as much as it can, while a lazy match stops as soon as it can. In this expression, + and {2,6} are greedy.

### Boundaries

Boundaries, such as \b, allow for matches at the beginning or end of words, rather than within them. The ^ anchor at the beginning and $ anchor at the end ensure that the entire input

### Back-references

Back-references can be useful when trying to match complex patterns within a string. They allow for matches to be based on previously matched groups. This expression has no back-references.

### Look-ahead and Look-behind

Look-ahead and look-behind allow for matches to be based on the presence or absence of certain characters before or after the match. They are not present in this expression.

## Author

Samantha is a student at the Northwestern coding bootcamp. You can find her Github at https://github.com/sveraleyva.
