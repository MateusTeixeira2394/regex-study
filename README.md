# Regular Expression (RegEx)
Repository to save regex teachings

## 1. Classes
### 1.1 Find any number

This class is for finding any number.

Syntax:

```
\d
[0-9]
```
Ex:

<p>Mateus<span style="background-color:#2497CD">123</span></p>

### 1.2 Find any word

This class is for finding any alphabet character.

Syntax:
```
\w
[A-Za-z0-9_]
```

Ex:
<p><span style="background-color:#2497CD">Mateus</span>123</p>

### 1.3 Find any white space

This class is for finding any white space character.

Syntax:
```
\s
[\t\r\n\f]
```

Ex:

Mateus<span style="background-color:#2497CD"> </span>is<span style="background-color:#2497CD"> </span>cool!

### 1.4 Any character
This class is for finding any character even a special one.

Syntax:
```
.
```

Ex:

<span style="background-color:#2497CD">Mateus is cool!</span>

### 1.5 Custom a class

You can inform which elements you want to find, classifying it like this:

Syntax:
```
[so!]
```

Ex:
Mateu<span style="background-color:#2497CD">s</span> i<span style="background-color:#2497CD">s</span> c<span style="background-color:#2497CD">oo</span>l<span style="background-color:#2497CD">!</span>

### 1.6 Summary:

```
[A-Z] - letter from A to Z
[123] - 1, 2 or 3
\d - all digits [0-9]
\s - whitespace [\t\r\n\f]
\w - wordchar [A-Za-z0-9_]
```
