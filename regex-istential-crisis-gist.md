# regex-istential-crisis

Introductory paragraph (replace this with your text)

## Summary

The regular expression or regex, that I will be covering in this tutorial is matching an email. I will explain each of the elements that are included in this regex, as well as, what they represent and their functionality within the expression.

Here is the email regex code snippet that I will be dissecting:

- `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

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

First and foremost, a regex must be wrapped with `/` characters because it signifys what the string contains and sets the foundation for us to construct our regex. You can see that in our case, our regex begins with `/` and also ends with `/`.

### Anchors

Within our email code snippet example, the "anchor(s)" that we use is the `^` that follows the first `/` and the `$` that precedes the ending `/`.

Anchors are important to regular expressions because they signify what the string is able to contain and what we are attempting to locate or search for. Depending on the anchor being used, it will either represent a string that begins with those specified characters (`^`) and/or a string that ends in those characters (`$`).

### Quantifiers

Quantifiers are a very interesting element in regex because they basically set the limit or ammount of times that the string matches in your expression.

In our example, the quantifiers that we have are the following:

- `+` and `{}`

In our case, the `+` quantifier essentially menas that the prior elements of the string that we specified, must match the pattern one or more times. So, at least one of the following "acceptance" criteria that we specified in those `[]` must match the pattern.

Then we also have those `{}` quantifiers that, in our case, had the values `{2,6}` passed into it. This quantifier is specifying the minimum (2) and the maximum (6) ammount of timmes the pattern must match. With the `{}` quantifier you can also throw in just one value like `{2}` and this means that the pattern must match "exactly" this many times. We can also throw in a value followed by a comma with no second value like `{2, }` and this means that the pattern must "at least" match this ammount of times.

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

Within our email code snippet example, the "bracket expressions" are the following:

- `[a-z0-9_\.-]`
- `[\da-z\.-]`
- `[a-z\.]`

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

Andrew Pieratt

Full-Stack Coding Bootcamp Student at the University of Denver

If you have any questions or want to connect, please use one (or both) of the links below!

- Email: pieratt.aw@gmail.com
- GitHub: https://github.com/andypieratt
