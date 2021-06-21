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
       * [Creating Lists](#creating-lists)
       * [Modifying Lists](#modifying-lists)
       * [Rearranging Lists](#rearranging-lists)
     * [Dictionaries](#dictionaries)
       * [Creating Dictionaries](#creating-dictionaries)
       * [Modifying Dictionaries](#modifying-dictionaries)
       * [Reviewing Dictionaries](#reviewing-dictionaries)
     * [Tuples](#tuples)
       * [Tuples Immutability](#tuples-immutability)
     * [Sets](#sets)
     * [Booleans](#booleans)   
   * [Comparison Operators](#comparison-operators)

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
 
####### Float Formatting

Float formatting allows you to adjust the precision of a floating point number and follows {value:width.precision f}. A width greater than 1 increases whitespace.


```python
result = 100/777
#0.1287001287001287

print("The result was {r:1.3f}".format(r = result))
```
 ##### f-strings
 
 ```python
 
 name = "Rikki"
 
 print(f"Hello, my name is {name}")
 #Hello, my name is Rikki
 
 age = 25
 
 print(f"{Rikki} is {age} years old.")
 ```
 
 #### Data Structures
 
 ##### Lists
 
Lists are ordered sequences that can be used to hold a variety of objects.They use [] and commas to seperate objects in the list e.g. [1,2,3,4,5]. Lists also support indexing and slicing, can be nested and have a variety of useful methods.
 
###### Creating Lists

 ```python
 
 my_list = [1,2,3]
 
 my_list2 = ["String",102,25,6]
 
 len(my_list)
 #3
 
 my_list[0]
 #1
 
 my_list[1:0]
 #[2,3]
 ```
 
 ###### Modifying Lists
 
 ```python
 another_list = [4,5]
 
 new_list = my_list + another_list
 #[1,2,3,4,5]
 
 new_list[0] = "ONE"
 
 new_list
 #["ONE",2,3,4,5]
 
 new_list.append(6)
 #["ONE",2,3,4,5,6]
 
 popped_iten = new_list.pop()
 #6
 
 new_list
 #["ONE",2,3,4,5]
 
 new_pop = new_list.pop(0)
 #"ONE"
 ```
 ###### Rearranging Lists
 
 ```python
 new_list
 #[2,3,4,5]

 new_list = ["a","e","x,"b","c"]
 num_list = [4,1,8,3]
 
 new_list.sort()
 #["a","b","c,"e","x"]
 
 num_list.sort()
 sorted_list = num_list
 #[1,3,4,8]
 
 num_list.reverse()
 #[8,4,3,1]
```

##### Dictionaries

Dictionaries are unordered mappings for storing objects, as such they cannot be sorted. They use key-value pairs to grab objects without needing to know an index location. Dictionaires use curly braces and colons to signify the keys and their associated values.{"key1":"value1","key2":"value2"}. 


###### Creating Dictionaries

```python

my_dict = {"key1":"value1","key2":"value2"}

my_dict
#{"key1":"value1","key2":"value2"}

my_dict["key1"]
#"value2"

prices_lookup = {"apple":1.99,"oranges":1.50,"milk":2.50}
prices_lookup["apple"]
#1.99

d = {"k1":123,"k2":[9,8,7],"k3":{"inside_key":100}}

d["k2]
#[9,8,7]

d["k2][2]
#7

d["k3"]
#{"inside_key":100}

d["k3"]["inside_key]
#100

d= {"key1":["a","b","c"]}

my_list = d["key1"]

letter = my_list[2]
letter.upper()
#C

# Can do all operations in one step
d["key1"][2].upper()
```

###### Modifying Dictionaries

```python
d = {"k1":100,"k2":200}
d["k3"] = 300
#{"k1":100,"k2":200,"k3":300}

d["k1] = "New Value"
#{"k1":"New Value,"k2":200,"k3":300}
```

###### Reviewing Dictionaries

```python
d = {"k1":100,"k2":200}

d.keys()
#["k1","k2"]

d.values()
#[100,200]

d.items()

[("k1",100),("k2,200)]
```

##### Tuples

Tuples are very similar to lists. However they are immutible, therefore once inside a tuple it cannot be reassigned. Tuples use parenthesis: (1,2,3).

```python

t = (1,2,3)
type(t)
#tuple

len(t)
#3

t = ("one", 2, 3)

t[0]
#"one"

t[-1]
#3

t = ("a","a",b")
t.count("a")
#count

'''Returns first occurance of "a"'''
t.index("a")
#0

t.index("b")
#2
```

###### Tuples Immutability

```python

my_list = [1,2,3]
my_list[0] = "NEW"
#["NEW",2,3]

t = (1,2,3)
t[0] = "New"
#TypeError
```

##### Sets

Sets are unordered collections of unique elements. There can only be one representation of the same object.

```python

my_set = set()

my_set.add(1)
#{1}

my_set.add(2)
#{1,2}

my_set.add(2)
#{1,2}

my_list = [1,2,2,1,2,3,4,4,4,5,3,2,1,2]
set(mylist)
#{1,2,3,4,5}
'''sets are not ordered'''
```

##### Booleans

Booleans are True or False operators. 


```python

1 > 2
#False

1 == 1
#True

'''None can be used as a placeholder'''
b = None
type(b)
#None
```

#### Comparison Operators
