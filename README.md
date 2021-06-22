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
     * [Chaining Comparison Operators/Logical Operators](#chaining-comparison-operatorslogical-operators)
   * [Python Statements](#python-statements)
     * [if, elif and else Statements](#if-elif-and-else-statements)
     * [for Loops](#for-loops)
       * [Iterating Through Lists](#iterating-through-lists)
       * [Iterating Through Strings](#iterating-through-strings)
       * [Tuple Unpacking](#tuple-unpacking)
       * [Iterating Through Dictionaries](#iterating-through-dictionaries)
     * [while Loops](#while-loops)
     * [break, continue and pass](#break-continue-and-pass)
       * [break](#break)
       * [continue](#continue)
       * [pass](#pass)
     * [Useful Operators](#useful-operators)
       * [range](#range)
       * [enumerate](#enumerate)
       * [zip](#zip)
       * [in](#in)
       * [Mathematical Functions](#mathematical-functions)
     * [List Comprehensions](#list-comprehensions)    
   * [Methods & Functions](#methods--functions)
     * [Methods](#methods)
     * [Functions](#functions)
       * [Default Values](#default-values)
       * [Functions WIth Logic](#functions-with-logic)
       * [Tuple Unpacking With Functions](#tuple-unpacking-with-functions)
       * [Interactions Between Functions](#interactions-between-functions)
       * [\*args and \**kwargs in Functions](#args-and--kwargs-in-functions)
       * [\*args](#args)  
       * [\**kwargs](kwargs#)
       * [\*args and \**kwargs](#args-and--kwargs)
     * [Lambda Expressions, Maps & Filter](#lambda-expressions-maps--filter)
        * [map](#map)
        * [filter](#filter) 
        * [Lambda Expressions](#lambda-expressions)
        * [Lambda Expressions With maps](#lambda-expressions-with-maps)
        * [Lambda Expressions With filters](#lambda-expressions-with-filters)

##### Methods


##### Lambda Expressions, Maps & Filter
###### map
###### filter
###### Lambda Expressions
###### Lambda Expressions With maps
###### Lambda Expressions With filters
#### Object Orientated Programming

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

| Operator | Description | Example|
| :--: | :--: | :--:|
| == | Returns true if values are equal  | (a==b) is not true|
| !=| Returns true is values are not equal | (a!=b) is true|
| >| Returns true is the value on the left is greater than the right| (2 > 1) is true |
| < | Returns true is the value on the left is less than the right | (2 < 1) is not true|
| >= | Returns true is the value on the left is greater or equal to the  right| (1 >= 2) is not true|
| <= | Returns true is the value on the left is less than or equal to the  right| (1 <= 2) is true|

```python

2 == 2
#True

"Hello" == "Bye"
#False
"Bye" == "bye"
#False

"2" == 2
#False

2.0 == 2
#True

3 != 3
#False

4 != 5
#True
```

##### Chaining Comparison Operators/Logical Operators

Logical operators (and/or/not) can be used to combine comparisons

```python
1 < 2 < 3
#True
1 < 2 and 2 < 3
#True

1 < 2 > 3
#False
1 < 2 and 2 > 3
#False

1 == 1 or 2 == 2
#True

100 == 1 or 2 == 2
#True

1 == 1
#True

not (1 == 1)
#False
'''Returns the opposite boolean'''

not 400 > 5000
True
```

#### Python Statements

##### if, elif and else Statements

When programming we sometimes only want certain sections of code to execute when a particular condition has been met. These can be done with the if,elif and else. Python uses colons and indentation (4 spaces).

```python
if some_condition:
    # execute some code
elif some_other_condition:
    # do something different
else:
    # do something else
```

An example can be found below:

```python

name = "Rikki"

if name == "Rikki":
    print("Hello Rikki!")
elif name == "Jocelyn":
    print("Hello Jocelyn")
else:
    print("What is your name?")
```

##### for Loops

for loops allow you to iterate over every element in an object. Such as an element in a list or character in a string.

###### Iterating Through Lists

```python
my_iterable = [1,2,3]

for item_name in my_iterable:
    print(item_name)
#1
#2
#3
```
Some examples can be seen below:

```python
my_list = [1,2,3,4,5,6,7,8,9,10]

for num in my_list:
    print(num)
#prints 1-10
for num in my_list:
    if num % 2 == 0:
        print(num)
#prints even numbers

list_sum = 0

for num in my_list:
    list_sum += num
    
print(list_sum)
#55
```

###### Iterating Through Strings

```python
for letter in "Hello World:
    print(letter)

#Prints each character in the string "Hello World"

for _ in "Hello World:
    print("Cool!")

#Prints Cool the same number of times there are character in the string "Hello World"
```

###### Tuple Unpacking


```python
tuple = (1,2,3)

for item in tup:
    print(item)
#Prints 1-3

my_list = [(1,2),(3,4),(5,6),(7,8)]
len(my_list)
#4

for item in my_list:
    print(item)
'''
(1,2)
(3,4)
(5,6)
(7,8)
'''

for (a,b) in my_list:
    print(a)
    print(b)
'''
1
2
3
4
5
6
7
8
'''

my_list = [(1,2,3),(4,5,6),(7,8,9)]

for a,b,c in my_list:
    print (b)
'''
2
5
8
'''
```

###### Iterating Through Dictionaries

```python
d = {"k1":1,"k2":2,"k3":3}
for item in d:
    print (item)
'''
k1
k2
k3
'''

for item in d.items():
    print (item)
'''
("k1",1)
("k2",2)
("k3",3)

for key,value in d.items():
    print (value)
'''
1
2
3
'''  
```

##### while Loops

while loops continue to execute a block of code *while* a condition remains *True*.

```python
while some_boolean_codition:
    #do something
else:
    #do something else
```

Some more examples can be seen below:

```python
x = 0

while x < 5:
   print(f"The current value of x is {x}")
   x += 1
else:
    print("X is not less than 5")
'''
The current value of x is 0
The current value of x is 1
The current value of x is 2
The current value of x is 3
The current value of x is 4
X is not less than 5
'''
```

##### break, continue and pass

The break, continue and pass keywords add additional functionality for loop use cases

* break: Breaks out of the current closest enclosing loop.
* continue: Goes to the top of the closest enclosing loop.
* pass: Does nothing.

###### break

```python
for letter in my_string:
    if letter == "i":
        break
    print(letter)
#R

x = 0

while x < 5:
    if x == 2:
    break
    print(x)
    x += 1
    
'''
0
1
'''
```

###### continue

```python

my_string = "Rikki"

for letter in my_string:
    if letter == "i":
        continue
    print(letter)
'''
R
k
k
'''
```

###### pass
```python

x = [1,2,3]

for item in x:
    #Any typical comment
# Results in an "EOF while parsing error"

for item in x:
    pass
# Runs without an error
```

##### Useful Operators

###### range

```python

for num in range (10):
    print(num)
#prints 0-9

for num in range (3,10):
    print(num)
#prints 3-9

for num in range (0,11),2:
    print(num)
#prints even numbers from 0-10

my_list = list(range(0,11,2))
#my_list contains even numbers from 0-10
```
###### enumerate

```python
index_count = 0

for letter in "abcde":
    print(f"At index {index_count} the letter is {letter}"
    index_count += 1

index_count = 0
word = "abcde"

for letter in word:
    print(word[index_count])
    index_count += 1
'''
a
b
c
d
e
'''

for item in enumerate(word):
    print(item)
'''
(0,"a")
(1,"b")
(2,"c")
(3,"d")
(4,"e")
'''
for index,letter in enumerate(word):
    print(index)
    print(letter)
    print("\n")
'''
0
a

1
b

2
c

3
d

4
e
```

###### zip


```python

my_list1 = [1,2,3]
my_list2 = ["a","b","c"]

for item in zip(my_list1,my_list2):
    print(item)
'''
(1, "a")
(2, "b")
(3, "c")
'''

my_list3 = [100,200,300]

for item in zip(my_list1,my_list2,my_list3):
    print(item)
'''
(1, "a", 100)
(2, "b", 200)
(3, "c", 300)
'''

my_list1 = [1,2,3,4,5,6]
for item in zip(my_list1,my_list2,my_list3):
    print(item)
'''
(1, "a", 100)
(2, "b", 200)
(3, "c", 300)
'''
#Zips to the length of the shortest list

list(zip(my_list1,my_list2)
#[(1, "a"),(2, "b"),(3, "c")]
```

###### in

```python

"x" in [1,2,3]
False

"x" in ["x","y","z"]
#True

"a" in "a world"
#True

"mykey" in {"mykey1":345,"mykey2":678}
#True

d = {"mykey1":345,"mykey2":678}

345 in d.values()
#True

345 in d.keys()
#True
```

###### Mathematical Functions

```python
my_list [10,20,30,40,500]

min(my_list)
#10

max(my_List)
#100
```

Other libraries can be imported:

```
from random import shuffle

my_list = [1,2,3,4,5,6,7,8,9,10]
shuffle(my_list)

my_list
#[3,1,2,6,5,4,8,10,9,7]

from random import randint

randint(0,100)
#79

randint(0,100)
#99

my_num = rand(0,10)
```

###### input

```python
result = input("Enter a number")
#Always accepts results as a string

float(result)
int(result)

result = int(input("Enter a number"))
```

##### List Comprehensions

A unique way to quickly create lists. If a list is being created with a loop statement and *append()*, list comprehensions are a good alternative.

```python

my_string = "hello"

my_list = []

for letter in my_string:
    my_list.append(letter)

my_list
#["h","e","l","l","0"]

my_list = [letter for letter in my_string]

my_list = [x for x in "word"]
#["w","o","r","d"]

my_list = [num for num in range(0,11)]
#[0,1,2,3,4,5,6,7,8,9,10]

my_list = [num**2 for num in range(0,11)]
#[0,1,4,9,16,25,36,49,64,81,100]

my_list = [x for x in range(0,11) if x%2 == 0]
#[0,2,4,6,8,10]

celcius = [0,10,20,34.5]

fahrenheit = [( (9/5)*temp + 32) for temp in celcius]

fahrenheit
#[32.0,50.0,68.0,94.1]
```
#### Methods & Functions

##### Methods

Methods are built into objects

```python
my_list = [1,2,3]

my_list.append(4)

my_list.pop()

my_list
```
You can often create the object place a "." and then press tab to see all available methods. Another way is to use the built in help function.

```python
my_list = [1,2,3]

help(my_list)

help(my_list.insert) 
```

##### Functions

Functions allow blocks of code to be executed without needing to rewrite it and can be defined using the *def* keyword.

```python
def name_of_function(name):
    '''
    Docstring explaining function
    '''
    print(f"Hello {name}")

name_of_function("Rikki")
#Hello Rikki
```

Typically the return keyword is used to send back the result of the function instead of printing it out. This allows the output of the function to be assigned to a new variable.

```python
def add_function(num1,num2):
    return num1 + num2
    
result = add_function(1,2)
print(result)
#3
```

###### Default Values

```python

def say_hello(name = "Default"):
    print(f"Hello {name}")
    
say_hello()
#Hello Default
```

###### Functions With Logic


```python
def even_check(number):
    return number % 2 == 0

even_check(10)
#True

even_check(21)
#false

def check_even_list(num_list):
    '''
    Return true if any number is even inside a list
    '''
    for number in num_list:
        if number % 2 == 0:
            return True
        else:
            pass
    return False

check_even_list([1,3,5)]
#False
check_even_list([2,4,5])
#True
```


```python
def check_even_list(num_list):
    '''
    Returns even numbers in a list
    '''
    even_numbers = []
    
    for number in num_list:
        if number % 2 == 0:
            even_numbers.append(number)
        else:
            pass
    return even_numbers
```

###### Tuple Unpacking With Functions

```python
stock_prices = [("Apple",200),("Google",400),("Microsoft",100)]

for stock,price in stock_prices:
    print(price + (0.1*price))
'''
220.0
440.0
110.0
'''

work_hours = [("Abby",40),("Billy",45),("Cassie",39)]

def employee_check(work_hours):
    current_max = 0
    employee_of_month = ""
    
    for employee,hours in work_hours:
        if hours > current_max:
            current_max = hours
            employee_of_month = employee
        else:
            pass
    return (employee_of_month,current_max)
    
name,hours = emmployee_check(work_hours)

name
#Billy

hours
#45
```

###### Interactions Between Functions

Typically outputs from one function are used as an input for another. Functions were used to design the game 3 cup monte which can be found [here](functions/interactions_between_functions)

###### \*args and \** kwargs in Functions

\*args and \** kwargs stand for arguments and keyword arguments and are used when passing an arbitrary number of arguments into a function.

###### \*args

Return a tuple

```python

def my_func(a,b):
    #Returns 5% of the sum of a and b
    
    return sum((a,b)) * 0.05

my_func(40,60)
#5
#Only takes 2 argumnets

def my_func(*args):
    return sum(args) * 0.05

my_func(40,60,40,20,50,70,80)
```
args is an arbitrary word and does not have to be used. However, it is convention but determining factor is the star.

###### \**kwargs

return a dictionary

```python

def my_func(**kwargs):
    if "fruit" in kwargs:
        print(f"My fruit of choice is {kwargs['fruit']}")
    else:
        print("I did not find any fruit here")
        
my_func(fruit = "apple",veggie = "lettuce")
My fruit of choice is apple
```

kargs is an arbitrary word and does not have to be used. However, it is convention but determining factor is the double star.

###### *\*args and \** kwargs

```python
def my_func(*args,**kwargs):
    print(f"I would like {args[0]} {kwargs['food']}")

my_func(10,20,30,fruit = "orange", food = "eggs", animal = "dog")
#I would like 10 eggs
```


#### Lambda Expressions, Maps & Filter

##### map

Applies a function to each element in an iterable e.g list

```python

def square(num):
     return num**2

my_nums = [1,2,3,4,5]

for item in map(square,ny_nums):
    print(item)
'''
1
4
9
16
25
'''

new_list =list(map(square,my_nums))
new_list
#[1, 4, 9, 16, 25]
```

```python

def splicer(my_string):
    if len(my_string) % 2 == 0:
        return "EVEN"
    else:
        return my_string[0]
        
names = ["Rikki","George", "James"]

new_list = list(map(splicer,names))

print(new_list)
#['R', 'EVEN', 'J']
```

##### filter

Filter by a function that returns either true or false

```python

def check_even(num):
    return num % 2 == 0

my_nums = [1,2,3,4,5,6]

new_list = list(filter(check_even,my_nums))
#[2,4,6]
```

##### Lambda Expressions

```python

square = lambda num: num ** 2

square(5)
#25
```

##### Lambda Expressions With maps
```python
my_nums = [1,2,3,4,5]
new_list = list(map(lambda num: num**2, my_nums))
new_list
#[1, 4, 9, 16, 25]

names = ["Rikki","George", "James"]
new_list = list(map(lambda name:name[0],names))
#["R","G","J"]
new_list = list(map(lambda name:name[::-1],names))
#["ikkiR","egroeG","semaJ"]
```

##### Lambda Expressions With filters

```python
my_nums = [1,2,3,4,5]
new_list = list(filter(lambda num: num % 2 == 0, my_nums))
[2,4]
```

#### Object Orientated Programming
