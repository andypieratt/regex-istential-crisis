# regex-istential-crisis

This tutorial will help guide you through a few of the key elements within a regular expression. This example will primarily focus on an email string and how we break that apart into sections using a regex. The concept of regular expressions can be a bit vague and confusing, so this tutorial aims to consoldiate some of that information and relay it in a transparent and digestible form. Hope you enjoy it, thank you!

## Summary:

The regular expression or regex, that I will be covering in this tutorial is matching an email. I will explain each of the elements that are included in this regex, as well as, what they represent and their functionality within the expression. We will cover all the elements in depth so don't be alarmed on the initial glance of our code example!

Here is the email regex code snippet that I will be dissecting:

- `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

Now let's break it all down, so we can understand what this expression actually means.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)

## Regex Components:

First and foremost, a regex must be wrapped with `/` characters because it signifys what the string contains and sets the foundation for us to construct our regex. You can see that in our case, our regex begins with `/` and also ends with `/`.

### Anchors:

Within our email code snippet example, the "anchor(s)" that we use is the `^` that follows the first `/` and the `$` that precedes the ending `/`.

Anchors are important to regular expressions because they signify what the string is able to contain and what we are attempting to locate or search for. Depending on the anchor being used, it will either represent a string that begins with those specified characters (`^`) and/or a string that ends in those characters (`$`).

### Quantifiers:

Quantifiers are a very interesting element in regex because they basically set the limit or ammount of times that the string matches in your expression.

In our example, the quantifiers that we have are the following:

- `+` and `{}`

In our case, the `+` quantifier essentially menas that the prior elements of the string that we specified, must match the pattern one or more times. So, at least one of the following "acceptance" criteria that we specified in those `[]` must match the pattern.

Then we also have those `{}` quantifiers that, in our case, had the values `{2,6}` passed into it. This quantifier is specifying the minimum (2) and the maximum (6) ammount of timmes the pattern must match. With the `{}` quantifier you can also throw in just one value like `{2}` and this means that the pattern must match "exactly" this many times. We can also throw in a value followed by a comma with no second value like `{2, }` and this means that the pattern must "at least" match this ammount of times.

### Character Classes:

Character classes help define specific sets of characters that are included in the string and would qualify for our "match pattern" parameters that we set up with the quatifiers.

In our example, the character classes that we have are the following:

- `.` in the `\.([a-z\.]{2,6})$/` section and `\d` in the `[\da-z\.-]` section.

The first character class that we see is the `.`, which is used quite a few times in our regex within the bracket expressions following a `\`. The `\` is considered a "character escape" and it loses much of its purpose when it's nested within a bracket expression. But overall, the `.` character class means that whatever character or values it precedes, matches any character except the "newline" character which is `\n`(responsible for creating a new line. The period in our example represents some sort of break that we are expecting after certain requirements are met. We are expecting some sort of ".com" or ".org" and so on after the section `@([\da-z\.-]+)` is fulfilled

The main, functioning character class that we have in our regex is `\d` and this essentially means that it matches any Arabic numerical digit. So, and numeric values between `[0-9]`. In our example `[\da-z\.-]`, the `\d` represents any numeric value and "a-z".

### Grouping and Capturing:

Grouping and/or capturing is a way to seperate certain sections or aspects of your expression, especially if yoy want to check for different values or characters throughout different sections of the string.

In our example, we use parentheses (`()`) to seperate our sections.

The first set of parens that we see are beforwe the `@` symbol in our email string so the entire section of `([a-z0-9_\.-]+)` is checking for and a capturing different values than the half that follows the `@` symbol being `([\da-z\.-]+)\.([a-z\.]{2,6})` which is checking for most likely some sort of domain like "@gmail.com" or "@thecoolestwebsite-ever.org".

Grouping and capturing is extremely helpful and useful because it really cleans up the expression and allows us to search for different aspects dependent upon what we are trying to create. Like a password may need different sections, or a username, or in our case, an email address.

### Bracket Expressions:

Within our email code snippet example, the "bracket expressions" are the following:

- `[a-z0-9_\.-]`
- `[\da-z\.-]`
- `[a-z\.]`

Bracket expressions are basically the backbone of our regex because they signify the types of characters or values that we want to include within our string.

In our example, the `[a-z]` portion of the expression menas that the string contains only lowercase characters between a-z in the alphabet. The bracket expressions are case-sensitive so this means if we wanted to include uppercase characters, we would have to include `[A-Z]` somewhere within the expression to include thos uppercase values.

The next section of our bracket expression is `[0-9]` which signifies that our string can contain any numeric value between 0-9.

The final piece of our bracket expressions is the special characters that we want to include, which are very much prevalent, especially in the case of emails. In our example, we have `[.]`, `[_]`, and `[-]`. So these values mean that we can have an underscore(`[_]`), a period(`[.]`), or hyphen(`[-]`) within our email string.

## Author:

Andrew Pieratt

Full-Stack Coding Bootcamp Student at the University of Denver

If you have any questions or want to connect, please use one (or both) of the links below!

- Email: pieratt.aw@gmail.com
- GitHub: https://github.com/andypieratt
