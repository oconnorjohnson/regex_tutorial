# regex_tutorial
A breakdown of the regular expressions (regex) used to match Hex color values.  

## Summary 
This tutorial breaks down the definition of sequenced special characters which serve to verify a search term. A regular expression, or regex, is a series of characters that define a specific search pattern. Within code, regex expressions search for patterns with a string or search to replace character(s) within a string as well as serve to validate input data. Hex Values are one of multiple methods of denoting color within code. Within Hex Color code, both the standard hex triplet as well as a shorter hex format are acceptable. 

```/^#?([a-f0-9]{6}|[a-f0-9]{3})$/```

## Regex Components

### Anchors

```/^```#?([a-f0-9]{6}|[a-f0-9]{3})```$/```

The anchors are the first element that will be dissected. The components that are highlighted are what we refer to as anchors, as can be seen in the highlighted section of our regular expression. At the beginning and end of a string or expression, anchors are employed. In this instance, ```/``` and ```$/``` denote the start and finish of our expression, respectively.

### Quantifiers 

/^#```?```([a-f0-9]```{6}```|[a-f0-9]```{3}```)$/

Quantifiers will be covered next. Quantifiers are used to specify the expected number of characters. Quantifiers define the minimum number of occurrences of a character, group, or character class required in the input for a match to be found. Quantifiers will try to match as many characters as they can by default because they are greedy. Regular expressions that contain the characters ",+,?," are regarded as quantifiers. The ```?``` tells the expression if it should match 0 or 1 times. Because there are two different types of formats, as was described in the overview above, we will use the or operator to indicate which format we are utilizing. The numbers ```{6}``` (Hex Triplet Format) and ```{3}``` (Shorthand Hex Format) in our Hex Value regular expression denote that the length of the component preceding these quantifiers should be 6 for ```{6}``` and 3 for ```{3}```.

Hex Triplet Formats Include: #000000, #FFFFFFF, #1188BB

Shorthand Hex Format: #000, #FFF, #18B (the hex triplet format would just double each character: #18B -> #1188BB)

### OR Operator 

/^#?([a-f0-9]{6}```|```[a-f0-9]{3})$/

The "or" operator is the next element we'll talk about. The | element in a regular expression defines the "or" operator. It is possible for either of the components, which we are separating with the ```|```, according to the or operator. ([a-f0-9]6```|```[a-f0-9]3]) is the hex value regular expression we have. Note how these 2 elements are separated by the or operator. As a result, our hex value may either be 3 or 6 characters.

### Character Classes 

/^#?(```[a-f0-9]```{6}|```[a-f0-9]```{3})$/

We'll talk about character classes next. Character classes are elements of our regular expression that specify the kinds of characters we should anticipate. Our character classes in this example are enclosed in brackets []. For our example, we have two character classes that look for the identical values: ```[a-f0-9]``` and ```[a-f0-9]```. What the characters are looking for within these character classes will be broken out. ```A-F``` looks for letters, while ```0-9``` looks for digits 0 to 9.

### Bracket Expressions 

/^#?```([a-f0-9]{6}|[a-f0-9]{3})```$/

In our regular expression, bracket expressions denote the start of a character class or quantifier statement. In our example, we define our bracket expressions using parenthesis.

### Greedy and Lazy Match 

/^#```?```([a-f0-9]{6}|[a-f0-9]{3})$/

Finally, we'll talk about greedy and lazy matches. An element is attempted to match as many times as possible in a greedy match. A lazy match, on the other hand, seeks to match an element as little as possible. In our case, the ```?``` stands for a lazy quantifier. Due to the fact that it forces the regular expression engine to match the fewest possible occurrences, this is known as a lazy quantifier. Simply by inserting a ```?```, we can transform this idle match into a greedy one.

