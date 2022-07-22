# regex_tutorial
A breakdown of the regular expressions (regex) used to match Hex color values.  

## Summary 
This tutorial breaks down the definition of sequenced special characters which serve to verify a search term. A regular expression, or regex, is a series of characters that define a specific search pattern. Within code, regex expressions search for patterns with a string or search to replace character(s) within a string as well as serve to validate input data. Hex Values are one of multiple methods of denoting color within code. Within Hex Color code, both the standard hex triplet as well as a shorter hex format are acceptable. 

/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Regex Components
### Anchors
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
The anchors are the first element that will be dissected. The components that are highlighted are what we refer to as anchors, as can be seen in the highlighted section of our regular expression. At the beginning and end of a string or expression, anchors are employed. In this instance, / and $/ denote the start and finish of our expression, respectively.

### Quantifiers 
<mark>/^</mark>#?([a-f0-9]{6}|[a-f0-9]{3})$/
### OR Operator 
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
### Character Classes 
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
### Bracket Expressions 
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
### Greedy and Lazy Match 
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/

## Author 
