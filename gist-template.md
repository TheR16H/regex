# /regex/ URL decode tutorial ✅

Regular expressions is a powerful tool for text processing and pattern matching. it's  supported in many programming languages including (but not limited too) Python, JavaScript, and Java. Regex in short is patterns that describe sets of strings and can be used for tasks like data validation, text search and replace, and text parsing.

## Summary ✅

**Regular expressions** aka regex (or regexp), uses a sequence of characters to define a search pattern so it is looking for matching patterns in strings. When included in algorithms, they can find and replace a character or sequence of characters. This tutorial will explain the components that make up the component/parts of a regular expression. 

To explain the components of regular expressions (regex), I will be deconstructing the JavaScript expression below that would in theory be used to find matching URLs:

`/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/`

## Table of Contents ✅

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)
- [Author](#author)

## Regex Components

### Anchors ✅
in Regex you use Anchors to match the starting the end of a line. 
<br> in Regex `^` is usually at the beginning of the string 
<br> while `$` is usually on the back half to signify the end of the string.

### Quantifiers ✅
These are used to specify the number of times a character, group, or character class should occur in the input string. this is benefical because you can define how many times an element match should occur. The 6 most common Quantifiers are 
<br> `* (Zero or more)` - matches 0 or more occurrences.
<br> `+ (One or more)` - matches 1 or more occurrences.
<br> `? (Zero or one)` - matches 0 or 1 occurences.
<br> `{n} (Exactly n times)` - matches the exact number of occurrences of the preceding element.
<br> `{n,} (At least n times)` - matches the minimum number occurrences of specificed.
<br> `{n,m} (Between n and m)` - Matches between n and m occurences of the preceding element.
 * n = number and m = maximum

### Grouping Constructs✅
Group constructs are when you group up some quantifiers in a () the groups serves a specific purpose in capturing and matching different parts of a URL pattern. <br> `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/` <br>
in this string there are atleast 3 different groups
<br> 1. `(https?:\/\/)?` - this is the first group says the https: is optional (OR Operator)
<br> 2. `([\da-z\.-]+)` -this is the second group, its gonna grab all the letters, hypeons,spaces, numbers etc.
<br> 3. `([a-z\.]{2,6})` - this third group is matching the domain and restricting it to 2-6 characters.

### Bracket Expressions
[] in regular expressions, allow you to specify a set of characters that you want to match at a particular position in the input string. 

### Character Classes ✅
Character classes allows us to define specific sets of characters so we can identify the pattern in order to decode the string. Ill show my string `/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/` in the preceding string there are multiple different classes / pattern identifiers but ill highlight 3. <br> the first is `\d` , this is used to identify/match any digit from 0-9. <br> The Second is `\w`this one is used to identify/match any alphanumeric character or underscore or even spaces & periods. <br> The third and final class i'll highlight is `a-z\.` this class will match any lower case letter or periods. 

### The OR Operator ✅
OR Operators usually are in code to show if the things before it are optional in the matching process. <br> ``/^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/``  <br> Using my string above as an example `(https?:\/\/)? ` is the OR Operator that's being used (because you dont need https: to visit a website).

### Flags ✅
Flags are used to modify the behavior of the expression or how its processed. the most common ones are 
<br> `i` - this flag performs case insensitive matching (so it can match no matter if its captial or not).
<br> `g` - this flag is used to find ALL matches instead of stopping after locating the first one.
<br> `m` - this flag is used to treat the current line as multiple lines. 

### Character Escapes
Character escapes in regular expressions are special sequences that begin with a backslash `\` followed by a character. i'll describe 6. 
<br> `\d` - matches any number.
<br> `\w` - Matches any word character.
<br> `\s` - this matches any breaks / space  created (like when you hit the `tab` button).
<br> `\t` - this will match a tab character.
<br> `\n` - this matches a newline return character.
<br> `\r` - this matches carriage return characters.

## Author 
This tutorial was written by `Rashawn Hall` an aspiring full stack developer. you can find me on github at the following link to see a few of my past/future works https://github.com/TheR16H. 
