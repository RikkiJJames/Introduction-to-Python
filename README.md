# Introduction-to-Python
 An introductory guide into Python

 ## Contents

 * [Section 1 - Objects & Data Structures](#section-1---objects--data-structures)
   * [Numbers](#numbers)
   * [Variables](#variables)
     * [Datatypes](#datatypes)
     * [Declaring Variables](#declaring-variables)
     * [Variable Scope](#variable-scope)


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
