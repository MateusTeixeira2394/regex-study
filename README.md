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

![Picture 1.1](/images/picture11.jpg)

### 1.2. Find any word

This class is for finding any alphabet character.

Syntax:
```
\w is equal to [A-Za-z0-9_]
```

Ex:

![Picture 1.2](/images/picture12.jpg)

### 1.3. Find any white space

This class is for finding any white space character.

Syntax:
```
\s is equal to [\t\r\n\f]
```

Ex:

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
[so!]
```

Ex:

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



