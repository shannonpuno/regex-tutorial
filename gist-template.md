# Regex Tutorial: Matching Email

This gist describes what a regular expression or regex is and how one would use it. Regex contains a series of special characters that define a search pattern. It is commonly used for search, manipulating and validating text. Regex is a useful and flexible tool, for instance, extracting data from text, verifying the format of user input, searching for patterns in datasets. Regular expressions are an essential tool for users to work with text data. 

## Summary

This tutorial will breakdown the components of regex, which can be used to match email address by defining a pattern that matches the format of an email address. Usages for this type of code can be to validate that the user enters a valid email address. 

Here is an example of the code snippet:
Matching an Email – 
```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```

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

### Anchors
Anchors contain a specific special character that indicates what is the beginning and the end of the regular expression. 

So in our "Matching an Email" regex, the string starts with ```^``` and ends with ```$ ```. 
```/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/```

The anchors ensure that the regex pattern matches the whole string rather than just a portion of it.  For instance, to validate an email address it must start and match the given parameters:
```^([a-z0-9_\.-]+)```

As well as, end and match these parameters:
```([a-z\.]{2,6})$```
If these parameters are not met then the email address will not match.

### Quantifiers
Quantifiers specifies how many times a certain character or group of characters that regex is looking for to match. 

Looking at our example code:
```{2,6}``` 
The use of the curly brackets means it matches the pattern from a minimum of 2 times to a maximum of 6 number of times. Therefore regex looks to match the string pattern before this quantifier a minimum and maximum of those times. 

```[a-z\.]````

This means that within this bracket expression, regex will match any string that includes any lowercase letters bettween a-z. 

### OR Operator
The matching email code does not contain any OR operators. However, OR operators are the pipe characters ```|```. The pipe character means that it can match either one pattern or the other. 

For instance, 2|3 , would indicate the string that can contain either 2 or 3.

### Character Classes
Character classes defines a set of characters, which can occur in an input string to fulfill a match. 
```\d``` 
In the matching email code this means it will match a single lowercase letter character from a to z. 

### Flags
Flags are not present in the matching email code. However, flags are placed at the end of a reggex, after the second slash. They define additional functionality or the limits of the regex. 
Flag examples are 
```g``` , ```i``` , ```m```. 

### Grouping and Capturing
Grouping constructs determine that each part of a string is matched before moving on to the next part. 
In the email code
```([a-z0-9_\.-]+)``` This first part has to be fulfilled before matching ```([\da-z\.-]+)```. 

A category of Grouping constructs is Capturing. Where they capture the matched character sequences to be able to be re-used. 

### Bracket Expressions
Bracket expressions indicate anything inside the ```[]``` represents a range of characters that we want to match. 
### Greedy and Lazy Match
The matching email code doesn't contain any greedy or lazy matches. 

### Boundaries
Boundaries are used to match specfic positions within a string. For example as mentioned above, Anchors would be part of boundaries. 

### Back-references
A back reference is a reference to a previously captured group in the regex. It allows a pattern to match that would be repeated later in the string, based on a previous. 

### Look-ahead and Look-behind
Look-ahead and Look-behind in regex means that it has to match based on the context of the surrounding text, without including the context itself in the match. 

Look-ahead are used to match a pattern that is followed by a specific sequence of characters without including the sequence in the match. 

Look-behind are used to match a pattern that is before the sequence of characters without including the sequence in the match. 
## Author

Created By: Shannon Puno
Github link: https://github.com/shannonpuno

