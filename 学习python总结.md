## 学习python总结

### 1.variables

(1). variable definition

```python
a = 1

# This is called a "chained assignment". It assigns the value 2 to variables "a" and "b".
a = b = 2
print("a = " + str(a))
print("b = " + str(b))
```

(2)variable types

All data in a Python program is represented by objects or by relations between objects. Every object has an **identity, a type, and a value**. An object’s identity never changes once it has been created; you may think of it as the object’s address in memory.

```python
number = 9
print(type(number))   # Print type of variable "number"
```

(3)type conversion

```python
int(), float(),str()
```

(4)arithmetic operators

Just as in any other programming language, the addition ( + ), subtraction ( - ), multiplication ( * ), and division ( / ) operators can be used with numbers. In addition, Python has the power ( ** ), modulo ( % ), and floor division ( // ) operators.

(5)assignment

+= , -=

(6)boolean operators

==, is

(7)comparison operators

```python
one = 1
two = 2
three = 3
print(f"one < two < three: {one < two < three}")
is_true = one < three > two     # insert any operator rendering the expression true. There are several options.
print(f"one is smaller than three, which is greater than two: {is_true}")
```

### 2.Strings

(1)concatenation

```
hello = "Hello"
world = 'World'
hello_world = hello + " " + world
```

(2)string multiplication

```python
not_yet_food = "cous"
food = not_yet_food * 2
print(food)
```

(3)String indexing

```python
python = "Python"
print(("h" + python[4]) * 3)     # Note: string indexing starts with 0
p_letter = python[0]
print(p_letter)
print(python[-1], python[-2])    #
```

(4)String slicing

```python
# Note that the symbol with the index ind1 will be included, while the symbol with the index ind2 – won't.
str[start:end] # items start through end-1
str[start:]    # items start through the rest of the array
str[:end]      # items from the beginning through end-1
str[:]         # a copy of the whole array
```

(5)**in** operater

```python
ice_cream = "ice cream"
print("cream" in ice_cream)    # Print boolean result directly
```

(6)len()

(7)

```python
print("\"\"\"")
```

(8)basic stringmethod: str.upper(); str.lower()

(9)String formatting

```python
name = "John"
# Note: %s is inside the string, % is after the string.
print("Hello, PyCharm! My name is %s!" % name)
print("I'm %d years old" % 24)
```

str.format()有待探索

(10)F-String

```python
name = "yuanlaihe"
age = 24
print(f"Hello, My name is {name} and I'm {24} years old.")
```


### 3.Data structure

(1) introduction
Lists might contain items of different types, but usually all the items in a list are of the same type. Like strings, lists can be indexed and sliced (see Lesson 3). All slice operations return a new list containing the requested elements.

```python
lst = [item1, item2]
```
(2)list operations
Unlike strings, lists are a mutable type, i.e., it is possible to change their content using lst[index] = new_item.
list[1] = newValue
list.append()

(3)list items
```python
animals = ["elephant", "lion", "tiger", "giraffe", "monkey", "dog"]  # Create a new list
print(animals)

animals[1:3] = ["cat"]    # Replace 2 items -- "lion" and "tiger" with one item -- "cat"
print(animals)

animals[1:3] = []     # Remove 2 items -- "cat" and "giraffe" from the list
print(animals)

animals[-2:] = ["elephant", "elephant"]
print(animals)
```

(4)Nested Lists
```python
my_list = [[1, 2, 3], [4, 5, 6], [7, 8, 9], 10]
print(my_list[2][2])
print(my_list[3])
```

(5)Tuples
They are almost identical to lists. The only significant difference between tuples and lists is that tuples are immutable: you cannot add, replace, or delete elements in a tuple.

```python
empty = ()
singleton = 'hello',    # <-- note the trailing comma
len(empty) # 0
len(singleton) # 1 ， ('hello',)
```

(6)join method, should be iterable objects
```python
string_ = 'abcde'  # a string iterable
tuple_ = ('aa', 'bb', 'cc')  # a tuple iterable
list_ = ['Python', 'programming language']  # a list iterable

print(' + '.join(string_))  # join with the ' + ' separator
print(' = '.join(tuple_))  # join with the ' = ' separator

sep = ' is a '
print(sep.join(list_))  # join with the ' is a ' separator

#a + b + c + d + e
#aa = bb = cc
#Python is a programming language
```

(7)dictionaries

A dictionary is similar to a list, except that you access its values by looking up a key instead of an index

A key can be any immutable type. Strings and numbers can always be keys. Tuples can be used as keys if they contain only immutable objects. You can’t use lists as keys.

Think of a dictionary as a set of key: value pairs, with the requirement that the keys are unique within one dictionary

```python
phone_book = {"John": 123, "Jane": 234, "Gerard": 345}
print(phone_book)
# Add a new item to the dictionary.
phone_book["Jill"] = 345
print(phone_book)

# Remove a key-value pair from phone_book.
del phone_book["John"]

#A dictionary can also be created with the dict constructor:
a = dict(one=1, two=2, three=3)
b = {'one': 1, 'two': 2, 'three': 3}
c = dict([('two', 2), ('one', 1), ('three', 3)])
print(a == b == c)
```

(8)dict.keys(), dict.values(), and dict.items()

(9)In keyword

```python
grocery_dict = {"fish": 1, "tomato": 6, "apples": 3}   # create new dictionary

print(6 in grocery_dict.values())
print("basil" in grocery_dict.keys())
```



### 4.Condition expressions

(1)boolean operators

```python
print(name == "John" or name == "Jane")
print(not name == "John" and age == 17)
print(not False)
```

(2)boolean operator order

Boolean operators are not evaluated from left to right. There's an order of operations for boolean operators: not is evaluated first, and is evaluated next, and or is evaluated last.

```python
name = "John"
age = 17
print(name == "John" or not age > 17)
print(name == "John" and not age == 17)
print(name == "John" or name == "Jane" and 25 > age >= 16)
```

(3)if statement

A code block starts with indentation and ends with the first unindented line. The amount of indentation must be consistent throughout the block. Generally, four whitespaces or single tabs are used for indentation. Incorrect indentation will result in IndentationError.

```python
if value > 1000: 
    print("It's a large number!")  # Indented block
    a += 1                         # Indented block
    
print("Outside the block!")        
```

```python
if name == "John":
    print(True)
else:
    print(False)
```

(4)single line if-else statement

```python
from random import random  # Importing a pseudo-random number generator module
my_random_number = random() * 100
print(my_random_number) if my_random_number > 50 else print("Too small!")
```

### 5. Loops

(1)for loop

```python
primes = [2, 3, 5, 7]   # Create new list
for prime in primes:
    print(prime)
```

(2)loop over a string

```python
hello_world = "Hello, World!"
for character in hello_world:    # Print each character from hello_world
    print(character)
```

(3)list comprehension

```python
my_list = [i for i in range(5))]
```

(4)nested list comprehension

```python
string = '0123456789'
matrix = [[i for i in string] for j in range(10)]
for row in matrix:
    print(row)
```

(5)while loop

```python
while number < 10:
    square = number ** 2
    print(square)
    number += 1
```

(6)else with loops

Python also allows loop statements to have an else clause. It is executed when the loop terminates through exhaustion of the iterable (with for) or when the condition becomes False (with while), but not when the loop is terminated by a break statement.

```python
for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(n, 'equals', x, '*', n//x)
            break
    else:
        # loop fell through without finding a factor
        print(n, 'is a prime number')
```

(7)continue keyword

### 6.Functions

(1)Function keyword argument

```python
def cat(food, state='still hungry', action='meow', breed='Siamese'):
    print(f"-- This cat wouldn't {action}", end=' ')
    print(f"if you gave it {food}")
    print(f"-- Lovely fur, the {breed}")
    print(f"-- It's {state}!")
cat('chicken')                     # 1 positional argument
cat(food='chicken')                # 1 keyword argument
cat(food='fish', action='bite')    # 2 keyword arguments
cat(action='bite', food='fish')    # 2 keyword arguments
cat('beef', 'happy', 'hiss')       # 3 positional arguments
cat('a hug', state='purrring')     # 1 positional, 1 keyword
```

(2)Args and kwargs

```python
def random_dialogue(place, *args, **kwargs):
    print("-- Do you know how to get to the", place, "?")
    print("-- I'm sorry, I am not from here, no idea about the", place)
    for arg in args:
        print(arg)
    print("-" * 40)
    for kw in kwargs:
        print(kw, ":", kwargs[kw])
    print('\n')


random_dialogue("Library", "Do you at least have a cigar, sir?",  # Call 1
                "Sure, help yourself.",
                lost_person="old banker",
                other_guy="street clown",
                scene="in a park")

dic = {"lost_person": "old banker", "other_guy": "street_clown", "scene": "in a park"}
lst = ["Do you at least have a cigar, sir?", "Sure, help yourself."]
random_dialogue("Library", *lst, **dic)  # Call 2 - the exact same output
```

### 7. Classes and objects

(1)self keyword 最好都写上

(2)`__init__(self)`

```python
class Car:
    def __init__(self, color, brand):
        self.color = color
        self.brand = brand
```

(3)str()主要用来为终端用户输出一些信息，而repr()主要用来调试；同时后者的目标是为了消除一些歧义（例如浮点数的精度问题），前者主要为了可读。

```python
In [17]: import datetime
In [18]: n = datetime.datetime.now()
In [19]: print(str(n)
    ...: )
2020-01-16 09:22:13.361995

In [20]: repr(n)
Out[20]: 'datetime.datetime(2020, 1, 16, 9, 22, 13, 361995)'
```

(4)类`__init()__`之外的变量这个类的所有实例对象都共享

```python
class Cat:

    species = "Felis catus"  
    
    def __init__(self, breed, name):
        self.breed = breed  
        self.name = name

cleo = Cat('mix', 'Cleo')
furry = Cat('bengal', 'Furry')

print(cleo.name)
print(cleo.species)
print(furry.name)
print(furry.species)

"""
Cleo
Felis catus
Furry
Felis catus
"""
```

### 8.Modules and packages

(1)自定义的module

```python
my_module.py
""" documentation string for module my_module
This module contains hello_world function
"""
def hello_world(name):
    print(f"Hello, World! My name is {name}")
```

```python
import my_module

my_module.hello_world("John")
```

(2)built-in module

```python
import sys
import datetime

print(sys.path)
print(datetime.datetime.today())
```

(3)from import

One form of the import statement imports names from a module directly. This way, you can use the imported name without the module_name prefix. For example:

```python
from calculator import Add

calc = Add()    # name `Add` used directly without prefix `calculator`
from calculator import *

# There is even an option to import all names that a module defines
calc = Multiply()
```

This imports all names except those beginning with an underscore _. In most cases, Python programmers do not use this, since it introduces an unknown set of names into the interpreter, possibly hiding some things you have already defined.

(4)package

```python
import functions.goodbye as bye
import functions.greeting.hello
from classes import calculator
import functions.greeting.official as official

print(functions.greeting.hello.hello('Susan'))
print(bye.good_bye('Alex'))
print(official.hello('Sam'))
```

(5)excuting modules as scripts

Python模块是包含可执行语句以及函数或类定义的文件。

When you run a module **directly** (that is, not by importing it into another one), the code in the module will be executed, just as if you imported it, but with __name__ set to *"__main__"*.

```python
import some_module

print(f"main_program __name__ is: {__name__}")

if __name__ == "__main__":
   print("main_program executed directly")
else:
   print("main_program executed when imported")
```

### 9. File input/output

(1)open file

It is good practice to use the with keyword when dealing with file objects. The advantage is that the file is properly closed after the code suite finishes.

```python
with open('input.txt', 'r') as my_file:
    # Some action performed with the file, the read() method explained later.
    print(my_file.read(), '\n')
with open('input1.txt', 'r') as file:
    print(file.read())
outfile = open('outfile.txt', 'w')  # Opening the file in write mode (using `w` argument)
outfile.write('Hello World')  # Writing to the file, the write() method is explained later.
outfile.close()
```

(2)read file

To read a file’s contents, you can call f.read(size), which reads some quantity of data and returns it as a string. When size is omitted or negative, the entire contents of the file will be read and returned.

***Note**: there will be a problem if the file is twice as large as your machine’s memory.*

For reading lines from a file, you can loop over the file object. This is memory efficient, fast, and makes the code simple:

```python
with open("input.txt", "r") as f:
    for line in f:
        print(line)
```

(2)read all lines

```python
# 下面的两个等价，而且with 里的是全局变量
# 1
with open("input.txt", "r") as infile:
   lines_list = []
   for line in infile:
       lines_list.append(line)
# 2
with open("input.txt", "r") as infile:
    lines_list = infile.readlines()

if __name__ == "__main__":
    print(lines_list)
```

(3)write files

Another file object method, f.write(string), writes the contents of a *string* to the file, returning the number of characters written.

```python
zoo = ["lion", "elephant", "monkey"]
number = 15

with open("output.txt", 'a') as f:
    f.write('\n' + ' and '.join(zoo)) # 在新的一行添加
    f.write('\n' + str(number)) # 在新的一行添加
```







