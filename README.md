# Regular Expression (RegEx)
Repository to save regex teachings

## 1. Classes
### 1.1. Find any number

This class is for finding any number.

Syntax:

```
\d is equal to [0-9]
```
Ex:

```
\d
```

![Picture 1.1](/images/picture11.jpg)

### 1.2. Find any word

This class is for finding any alphabet character.

Syntax:
```
\w is equal to [A-Za-z0-9_]
```

Ex:

```
\w
```

![Picture 1.2](/images/picture12.jpg)

### 1.3. Find any white space

This class is for finding any white space character.

Syntax:
```
\s is equal to [\t\r\n\f]
```

Ex:

```
\s
```

![Picture 1.3](/images/picture13.jpg)

### 1.4. Any character
This class is for finding any character even a special one.

Syntax:
```
.
```

Ex:

![Picture 1.4](/images/picture14.jpg)

### 1.5. Custom a class

You can inform which elements you want to find, classifying it like this:

Syntax:
```
[abc123...]
```

Ex:

```
[so!]
```

![Picture 1.5](/images/picture15.jpg)

### 1.6 Summary of classes

```
[A-Z] - letter from A to Z
[123] - 1, 2 or 3
\d - all digits [0-9]
\s - whitespace [\t\r\n\f]
\w - wordchar [A-Za-z0-9_]
```

## 2. Quantifiers

### 2.1. Inform the repetition quantity

Inform how many times the same characters type must be find together.

Syntax:
```
{the number of repetition}
```

Ex:

```
\d{3}
```

![Picture 2.1](/images/picture21.jpg)

### 2.2. Minimum and Maximum

Inform the minimum and the maximum times that the same characters type must be find together.

Syntax:

```
{min quantity, max quantity}
```

Ex:

```
\w{2,3}
```

![Picture 2.2](/images/picture22.jpg)

### 2.3. Minimum until infinity

Inform the minimum until infinity times that the same characters type must be find together.

Syntax:

```
{min quantity,}
+ is equal to {1,}
* is equal to {0,}
```

Ex:
```
{3,}
```

![Picture 2.3](/images/picture23.jpg)

### 2.4. Conditional

Inform if the character type is optional.

Syntax:

```
? is equal to {0,1}
```

Ex:

```
Mateus\s? or Mateus\s{0,1}
```

![Picture 2.4](/images/picture24.jpg)

### 2.5. Summary of quantifiers

```
{n} - exactly n times
{n,} - at least n times
{n,m} - at least n until m times
? - zero or once
+ - once or more times
* - zero or more times
```

## 3. Anchors

### 3.1. Word Boundary

To inform the word limits. On the other hand, it informs where the word begins and ends.

Syntax:

```
\b
```

Ex:

```
\b\w{2}\b
```

![Picture 3.1](/images/picture31.jpg)

### 3.2. Anchor of begin and end

To inform how the sentence have to begin and end. Besides that, no other character have to be before or after the finding sentence.

Syntax:

```
^Some sentence$
```

Ex:

```
^M.*!$
```

![Picture 3.2](/images/picture32.jpg)

### 3.3. Non Word Boundary

in opposite to word-boundary, this class inform if the character have to be followed by another character or not.

Syntax:

```
\Bchar\B
```

Ex:

```
\Bs\B
```

![Picture 3.3](/images/picture33.jpg)

### 3.4. Summary of anchors

```
\b - word boundary
\B - non word boundary
^ - begin of the target
$ - end of the target
```

## 4. Groups

You can split your regex code in groups to separate logic function, turning it more understandable when the regex code is too long, making it more flexible to add or remove code blocks and avoid repetitions, due to you can reuse any group.

### 4.1. Group syntax

Just put a piece of code between "(" and ")" to make a group. Thus, this piece of code become independent. 

Syntax:

```
(part of code)(another part of code)
```

Ex:

```
(\(\d{2}\)\s?)(\d{4,5}-?)(\d{4})
```
This regex code is used to get telephone number. So:

- The first group is a logic to get the local code that is a two digits between "()";
- The second group is a logic to get the first part of the telephone;
- The third one is a logic to get the second part of the telephone;


![Picture 4.1](/images/picture41.jpg)


### 4.1 Optional groups

You can select any piece of code and put it into a group. Besides that, you can use any quantifier expression on it. Thus, we use the expression "?" to turn this piece of code optional.

Ex:

```
([0123]\d)\s+(de\s+)?([a-zç]{4,10})\s+(de\s+)?([12]\d{3})
```

notice that the sentence part "de" with space is optional.

![Picture 4.2](/images/picture42.jpg)

### 4.2 Backreference

To avoid repetition you can reuse the same group, using the syntax \1, for instance, in which the number after the "\" represents the sequence of the group that will be reused. You can see more in the example below.

Syntax:

```

(group1) some text (group2) more some text (group3)
\number of the sequence of the group

```

Ex:

```
<(h1|h3).+?>.*<\/\1>
```

![Picture 4.3](/images/picture43.jpg)

Notice that instead of use the group (<h1|h3>) one more time, you can just use the syntax \1 to inform that the group 1 will be used again.

## 5. Greedy Expressions

The regex is a greedy partern that means it will get more characters as possible until find the some stop character.

Ex:

```
<h1.+>
```

![Picture 5.1](/images/picture5.jpg)

When use the expression "_<h1.+>_" the regex selected all the sentence until the last "_>_" because he is greedy by default. 

So, to inform to regex that he must stop to the first stop character, you have to use the syntax "_?_" before the stop character, like the example bellow:

Ex:

```
<h1.+?>
```

![Picture 5.2](/images/picture52.jpg)
