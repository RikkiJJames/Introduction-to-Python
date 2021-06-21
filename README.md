# Introduction-to-Python
 An introductory guide into Python

 ## Contents

 * [Section 1 - Objects & Data Structures](#section-1---objects--data-structures)
   * [Numbers](#numbers)
   * [Variables](#variables)
   * [Strings](#strings)
     * [Indexing](#indexing)
     * [Slicing](#slicing)
     * [String Properties & Methods](#string-properties--methods)
     * [String Formatting For Printing](string-formatting-for-printing)
     * [.format method](#format-method)
     * [Float Formatting](#float-formatting)
     * [f-strings](#f-strings)
   * [Data Structures](#data-structures)
     * [Lists](#lists)  
     * [Declaring Variables](#declaring-variables)
     * [Variable Scope](#variable-scope)

###### .format method
###### Float Formatting
 #### f-strings
 #### Data Structures
 ##### Lists

 ### Section 1 - Objects & Data Structures

 #### Numbers
 
 Python can be used as a simple calculator by inputing the desired calculation  
 
  ```python
  2+1 
  #3

  2.0-1
  #1.0

  2*2
  #4

  3/2
  #1.5
 ```
 
 The modulus operator can also be used to obtain the remainder
 
 ```python
 
 7 % 4
 #3
 
 50 % 5
 #0
 ```
 
 You can also do calculations to calculate powers
 
 ```python
 
 2 ** 3
 #8
 
 3**2
 #9
 
 ```
 
 The basic order of operations follows Bidmas/Bodmas. However brackets can be used to set the order of operations
 
 ```python
 2 + 10 * 10 + 3
#105

(2 + 10) * (10 + 3)
#156
 ```
 
 #### Variables
 
 Numbers as well as many other datatypes can be assigned to a variable to reference them easily. However, there are some rules for variable names.
 
 * They cannot begin with a number
 * There cannot be any spaces (underscores can be used instead)
 * It cannot use any of these symbols '''.<>/?|/()!@#$%^&*~-+
 * It's generally considered best practice for names to be lowercase
 * Words that have special meaning in Python should be avoided
 
  ```python
 
 my_pets = 2

 ```
 
 Python uses *Dynamic Typing* which means that variables can be reassigned to different data types.
 
 ```python
 
 my_pets = 2
 
 my_age = ["Flapjack", "Zuko"]
 ```
 
 There are pro's and cons for dynamic typing
 
 Pro's
 * Easy to work with
 * Faster Development Time

Con's
* May result in unexpected bugs
* Need to be aware of *type()*


```python

a = 10

type(a)
#int

a = 30.1
type(a)
#float
```

#### Strings

Strings are sequences of characters using either single quotes or double quotes:

```python

print('hello')
print("world")

print("hello \nworld")
#hello
#world

print("hello \tworld")
#hello    world
```

##### Indexing

Because strings are ordered sequences, indexing and slicing can be used to grab sub-sections of the string.


 | Character | h | e | l | l | o |
 | :-: | :-: | :-: | :-: | :-: | :-: |
 | Index | 0 | 1 | 2 | 3 | 4 |
 | Reverse Index | 0 | -4 | -3 | -2 | -1 |

```python

my_name = "Rikki"

my_name[0]
#R

my_name[-1]
#i
```

##### Slicing

Slicing grabs a subsection of multiple characters of a string and has the following syntax *[start:stop:step]*.

* start is the index the slice starts
* stop is the index you will go up to (but not include)
* step is the size of each "jump"

```python

my_name = "Rikki"

my_name[1:]
#ikki

my_name[:3]
#Rik

my_name[1:4]
#ikk

my_name[::2]
#Rki

my_name[::-1]
#ikkiR
#Reverses the string
```

##### String Properties & Methods

Strings in Python are immutable. Therefore indexing cannot be used to change individual elements of a string

To reassign a string, a new one must be created. Concatenation can also be used to make a change to the string.

```python

name = "Vikki"

last_letters = name[1:]
#"ikki"
"R" + last_letters
#"Rikki"
```

The multiplication sign can also be used to carry out multiple concatenations

```python

letter = "z"
letter * 10 
#zzzzzzzzzz
```

Be aware when concatenating a number with a string


``` python

2 +3 
#5

"2" + "3"
#"23"
```

There are various built in string methods. Some methods act "in-place" and do not affect the actual variable and would need to be reassigned e.g x = x.upper().

| Method name | Description | Example | Place |
| :--: | :--: | :--: | :--: |
|.len(x) | prints length of string | 11 | in-place |
|.upper()| makes entire string upper case | "HELLO WORLD" | in-place |
|.lower() | makes entire string lower case | "hello world" | in-place |
|.split() or .split("r")| creates a list from a string | ["Hello", "World"] / ["Hello Wo", "ld"] | in-place |

Examples on how to use each function can be found [here](Strings/String_Methods)


##### String Formatting For Printing

The are times when you want to insert a variable into a string to print also known as string interpolation, for example:

```python

my_name = "Rikki"

print("Hello " + my_name)
#Hello Rikki
```

However, there are many methods to do this, mainly the .format() method and f-strings (formatted string literals).

###### .format method

```python

print("This is a string {}".format("INSERTED"))
#This is a string INSERTED

print("The {} {} {}".format("red","big","house"))
#"The red big house

print("The {1} {0} {2}".format("red","big","house"))
#The big red house

print("The {0} {0} {0}".format("red","big","house"))
#The red red red

print("The {b} {r} {h}".format(r = "red",b = "big",h = "house"))
#The big red house
```
 
###### Float Formatting

Float formatting allows you to adjust the precision of a floating point number and follows {value:width.precision f}. A width greater than 1 increases whitespace.


```python
result = 100/777
#0.1287001287001287

print("The result was {r:1.3f}".format(r = result))
```
 #### f-strings
 
 ```python
 
 name = "Rikki"
 
 print(f"Hello, my name is {name}")
 #Hello, my name is Rikki
 
 age = 25
 
 print(f"{Rikki} is {age} years old.")
 ```
 
 #### Data Structures
 
 ##### Lists
