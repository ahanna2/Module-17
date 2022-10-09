<!-- @format -->

# Module 17 Regex

The module 17 challenge summary is shown below.

## Summary

The specific text string known as a regular expression (Regex or Regexp) is used to provide a search pattern. Regular expressions can be used in code or search engines to discover certain character patterns inside a text. as shown here: `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

## Regex Components

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries] (### Bondaries)
- [Back-references] (### Back-references)
- [Look-ahead-and-Look-behind] (### Look-ahead and Look-behind)

## Regex Components

### Anchors

-/ Regex starts - To locate the anchors, do this at the beginning of the string every time. -( combines many "tokens" to form a capture group. This may be used to get a backreference or substring. -https This denotes a string subexpression that has to be matched. "s"

? This Greedy quantifier simply indicates if the previous character (s), either http or https, occurred 0 or 1 once. Although I'm not certain, I believe it removes the's' from http.

\/\/ escaped character

) Ends the capture grouped.

? Greedy quaintifier indicating the entire previous section wrapped in () is optional.

( Begins captured group.

) Ends captured group.

[ Begins bracket list.

] Ends bracket list.

/d A metacharacter indicating any one digit character (0-9)

a-z Indicates lower case letters between a-z.

\. Escape sequence denoting the character.

- Indicates - character

* Because its outside the brackets the Greedy quantifier is denoting that the previous bracket list characters, may occur one or more times.

] Ends bracket list. {2,6} Occurence indicator denoting the previous bracket list characters may occur from 2 to 6 times.

/ Escapes regex to match the character /

/ Escapes regex to denote a regular / character

\w Is a character class indicating any dingle Word Characters. Those are any characters including a-z, A-Z, 0-9, and \_.

. Escape sequence denoting the character.

- Indicates - character

* The Greedy quantifier denoting that the previous bracket list characters may occur zero or more times
  ) Ends captured group.

* Greedy quantifier indicating that the entire previous captured group may occur zero or more times.

? Greedy quantifier indicating previous / character may have 0 or 1 occurrences.

$ Position acnhoring that ends the string.

/ Ends Regex.

### Quantifiers

Quantifiers let the regex engine know that it needs to match the character or expression's quantity upon that order to match the character or expression. Both the greedy and the lazy varieties of quantifiers have the same definition.

- and \*? meets 0 time or more times.

* and +? Matches once or Many times.
  ? and ?? matches 0 or 1 time.
  {n,} and {n,}? at least n times of matches.
  {n} and {n}? precisely n times match.
  {n,m} and {n,m}? Matches from n to m times.

Examples:

https? `?` Matches 'https', 'http'.
[\da-z\.-]+ `+` it matches a single digit, group of letters (a-z), dot (.) or hyphen (-) 1 or more often
[a-z\.]{2,6} `{2,6}` it matches 2 to 6 copies of the sequence [a-z\.]
[\/\w \.-]_ `_` it matches '/', '.', '-', 'www', '//'

### Character Classes

Character classes make ensuring that a specific character sequence corresponds to a larger set of characters.

[a-z] Matching lowercase alphabetic characters from a to z
\w Matching a single word
\d Matching a single character that is a digit 0 to 9
. Matching any character

### Flags

The way that an expression is evaluated is modified by expression flags. The expression's forward slash that closes it is followed by flags.

### Grouping and Capturing

Expressions can be grouped to help us stay more organized and make it simpler to identify the characters that belong to a certain group. This is used with the "()" parentheses.

(https?:\/\/) This group allows the URL code to being with "http://", "https://" or none.
([\da-z\.-]+) This group is the domain name. It matches one or more numbers, letters, dots or hypens. finishing it with a "+" to link it to the line.
([a-z\.]{2,6}) Withe the + connecting the group together, this matches 2-6 copies of the sequences "[a-z\.]"
([\/\w \.-]_) This group is is being matched as many times, because of "_" in the end.

### Bracket Expressions

Expressions inside brackets ([]) are known as bracket expressions. The following Bracket Expressions are included in the aforementioned example.

[a-z\.]
[\da-z\.-]
[\/\w \.-]

### Greedy and Lazy Match

lazy and greedy You may match the Greedy with the Lazy using quantifiers. Being the longest is "Greedy." being the shortest, "lazy."

([\da-z\.-]+) Because it permits character matching once up to an unlimited number of times, the "+" operator is greedy.

### Bondaries

Most regex languages define a word boundary as a place between /w and /w (non-word char) or at the start or end of a string if it contains a word character ([0-9A-Za-z_]). Therefore, it would match before the 1 or after the 2 in the string "-12." It's not a word character, the dash.

### Back-references

Backreferences point to a captured group that was previously used in the same regular expression, for instance, you may use backreferences as a basic example. A pattern that extracts just one word from the match might be used.

### Look-ahead and Look-behind

Lookbehind. asserts that foo is the value that comes before the present location in the string. (?!foo) Negative Lookahead. Declares that the character that follows the current location in the string is not the character foo.

### Author

Github link: git@github.com:ahanna2/Module-17.git
Email: alanjalil@yahoo.com
