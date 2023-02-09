# Regex-Tutorial

## What is Regex?
***

A regular expression, commonly referred to as "`regex`"  or "regexp," is a sequence of characters that define a search pattern. It is mainly used to search, match, and manipulate text or strings.

## Summary
***

`Regex` is a powerful tool for text processing. It is widely used in many programming languages such as Java, Python, and more. In `regex`, a pattern is described using a special syntax that includes a set of symbols and special characters. These patterns can then be used to search for and match patterns in strings.

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
***
In regular expressions, "anchors" are special characters that match a position in the input string, rather than a character. There are two common anchors used in matching email addresses: The "^" anchor matches the start of a line, while the "$" anchor matches the end of a line. These anchors are often used together in a regex pattern to  ensure that the entire input string is matched, rather than just a substring.

For example, if you wanted to match a valid email address using regex, you could use the following:

```
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```
This pattern uses the "^" snd the "$" anchors to ensure that the entire input string matches the pattern of an email address.

### Quantifiers
***
Quantifiers can be used in regular expressions to specify the number of times a character or group of characters should be repeated when matching an email address.

The following is an example of a regular expression that uses quantifiers to mtch a valid email adress:

```
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```

In this pattern, the `+` quantifier is used after the 
 ` [a-zA-Z0-9._%+-] ` character group to match one or more occurances of characters that can appear in the username
part of the email address. The `{2,}` quantifier is used after the `[a-zA-Z]` character group to match two or more characters that must appear in the top-level domain of the email adress. 


### Grouping Constructs
***
In regular expressions, grouping constructs allow you to group together multiple characters or character sets into a single unit. This can be useful when you want to apply a quantifier to a group of characters, or when you want to capture a match as a single unit for later reference.

There are two types of grouping constructs in regular expressions. Non capturing group and capturing groups.

Non capturing group is defined using parentheses `()` and allows tou to group together characters for the purpose of applying a quatifier, qithout capturinfthe match as a single unit. For example:
```
(?:[a-zA-Z0-9._%+-])
```

The `?:` at the begining of the group specifies that it is a non-capturing group. This gorup matches one or morre occurences of the characters that can appear in the username part of an email address. 

A capturing group is defined using parentheses `()` and allows you to group together characters and capture the match as a single unit. Captured matches can be later referenced in a replacement string, or used to extract information from a string.
For example: 
```
^([a-za-z0-9._%+-]+)@([a-zA-Z0-9.-]+)
```

The following pattern uses `capturing groups` to capture the username and domain name parts of an email address. The first capturing group `( [a-zA-Z0-9._%+-]+)` captures the username, and the second capturing group `( [a-zA-Z0-9.-]+)` captures the domain name.

The follwoing is an example of a complete regular expression that uses both non-capturing and capturing groups to match a valid email address:

```
^([a-zA-Z0-9._%+-]+)@([a-zA-Z09._-]+)\.([a-zA-Z]{2,})$
```

This pattern use a capturing group to match the username, domain name, and top-level domain of an email address. The non-capturing group `(?:@)` is used to match the "@" symbol, and capturing group `([a-zA-Z]{2,})` is used to match the top-level domain.

### Bracket Expressions
***
In regular expressions, brackets `[]` are used to define a character set, which is a group of characters that you want to match. The regular expression engine will match any single character from the set, so if you want to match more than one character, you needs to use a qualifier.

For example, in an email address, the characters allowed in the username part of an email address are typically limited to letters, numbers, dots, underscores, percent signs, plus signs and hyphens. To match these characters in a regular expression, you can use a character set:
```
[1-zA-Z0-9._%+-]+
```

This pattern matches one or more occurences of characters that can appear in the username part o the email address. The `+` quantifier is used to match one or more characters, and the character set `[a-zA-Z0-9._%+-]` is used to define the set of allowed characters.

Here's an example of a complete regular expression that uses character sets to match a valid email address:

```
^[a-zA-Z0-9._%+-]+@[a-zA-Z0-9.-]+\.[a-zA-Z]{2,}$
```
In this pattern, two character sets are used: `[a-zA-Z0-9._%+-]+` is used to match the domain name part of the email address.
The `{2,}` quantifier is used after the `[a-zA-Z]` character set to match two or more characters that must appear in the top-level domain of the email address.

### Character Classes
***
### The OR Operator
***
### Flags
***
### Character Escapes
***
## Author
***
A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)