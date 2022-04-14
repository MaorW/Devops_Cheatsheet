# Python commands & Practice

### Link for a free courses: [Link1](https://campus.gov.il/course/course-v1-cs-gov-cs-selfpy101/)

### For documentation press [here](https://docs.python.org/3/)

### For a style guide press [here](https://www.python.org/dev/peps/pep-0008/)

### For The Python Standard Library press [here](https://docs.python.org/3/library/index.html)

### For python's build-in functions press [here](https://docs.python.org/3/library/functions.html) 

### For python's build-in types press [here](https://docs.python.org/3/library/stdtypes.html) 

### For python's format documentation press [here](https://pyformat.info/) 

### For Dictionary view objects info press [here](https://docs.python.org/2/library/stdtypes.html#dictionary-view-objects) 

### Data types and variables
```
x = 5 # Integer

fairy_tale = "The Ugly Duckling"    # String - Immutable

swan_height = 90.7                   # Float

the_sun_will_rise_tomorrow = True   # Boolean

```

### Name conventions
```
current_book_sales = 5000   # Regular variables example - Meaningful expressions!

PI = 3.14                   # Constant variable example

```

### Getting input from user

```
## Getting integer input ##
num_of_breaks = int(input('Enter digits : ')) # Casting to integer

## Getting string input ##
num_of_breaks = str(input('Put a value : ')) # Casting to string
```

### Common functions
```
## Range
# The basic range() function
range(stop)

# The function range() with more parameters
range(start, stop[, step])

```

### Getting variable's type
```
type(x) # Getting the type of a variable
```

### String practice (immutable) - Basics

```
>>> '"All in!", she said happily.'
'"All in!", she said happily.'

>>> "Don't do it. You will lose the poker game."
"Don't do it. You will lose the poker game."

>>> print("\"Play with me\", she said.\"It will be SO hilarious when you will lose!\"")
"Play with me", she said." It will be SO hilarious when you will lose!"

\n = New line
\t = New tab

>>> print("Hey\nStarting a new line!")
'Hey
Starting a new line!'

>>> print("Creating four spaces…\tDone!")
'Creating four spaces…    Done!'

# How to reverse a String in Python
>>> word = "Hello"  
>>> word[::-1] 
'olleH'

```

### String practice - Slicing
```
>>> card_str = "Joker"
>>> card_str[0]
'J'
>>> card_str[2]
'k'
>>> card_str[4]
'r'

>>> card_str[-1]
'r'
>>> card_str[-3]
'k'
>>> card_str[-5]
'J'

>>> card_str[0:2]
'Jo'
>>> card_str[2:5]
'ker'
>>> card_str[1:-1]
'oke'

# Slicing with step: string[START:STOP:STEP]
>>> card_str[0:5:2]
'Jkr'

# Strings slicing: string[START:STOP]
>>> hobby = "Gaming"
>>> hobby[2:5]
'min'

```

### Objects and methods practice 
```
# object.method_name(parameter1, parameter2...)
>>> "print me in UPPERCASE".upper()
'PRINT ME IN UPPERCASE'
>>> "234".zfill(5)
'00234'

# Showing available methods by types with the dir() function
>>> dir(str)
['__add__', '__class__', '__contains__', '__delattr__', '__dir__', '__doc__', '__eq__', '__format__', '__ge__', '__getattribute__', '__getitem__', '__getnewargs__', '__gt__', '__hash__', '__init__', '__init_subclass__', '__iter__', '__le__', '__len__', '__lt__', '__mod__', '__mul__', '__ne__', '__new__', '__reduce__', '__reduce_ex__', '__repr__', '__rmod__', '__rmul__', '__setattr__', '__sizeof__', '__str__', '__subclasshook__', 'capitalize', 'casefold', 'center', 'count', 'encode', 'endswith', 'expandtabs', 'find', 'format', 'format_map', 'index', 'isalnum', 'isalpha', 'isdecimal', 'isdigit', 'isidentifier', 'islower', 'isnumeric', 'isprintable', 'isspace', 'istitle', 'isupper', 'join', 'ljust', 'lower', 'lstrip', 'maketrans', 'partition', 'replace', 'rfind', 'rindex', 'rjust', 'rpartition', 'rsplit', 'rstrip', 'split', 'splitlines', 'startswith', 'strip', 'swapcase', 'title', 'translate', 'upper', 'zfill']

```

### if elif else
```
if 3 < 4:
    print("Three is less than four")
Three is less than four


choice = int(input())
if choice == 1:
    print("You've chosen one")
elif choice == 2:
    print("You've chosen two")
elif choice == 3:
    print("You've chosen three")
else:
    print("You've chosen something else")


if (months_passed == 18) and (location_moon == location_sun):
    print("Eclipse!")
else:
    print("Just a regular day…")

```

### Function - Practice
#### Function - Basics
```
def function(parameter)
    print(does_something)

function(argument)


# Example_01
def my_first_function():
    print("This is my first function in Python!")

my_first_function() # This is my first function in Python!

# Example_02
def square(number):
    print(number ** 2)

square(3) # 9


# Example_03 -- Function is an object
def square(number):
    print(number ** 2)

print(square) # function square at 0x7dfe68d92488>

```
#### Function - scope
```
# Global vs Local
global_var = "I'm global"

def f():
  local_var = "I'm local"

# Error example
>>> def water():
...     fish_view = "I can only live within the water scope!"
...     print(fish_view)
...
>>> water()
I can only live within the water scope!
>>> print(fish_view) # Error message

# Global statement
global global_value

```

#### Function - return
```
>>> def add(num1, num2):
... return num1 + num2

>>> sum = add(15, 20)
>>> print(sum)
35

# By default, if there is'nt return value, the function returns "None"

# Return more then one arguments

def sum_and_avg(a, b):
   sum_num = a + b
   avg_num = (a + b) / 2
    return sum_num, avg_num

>>> x, y = sum_and_avg(3, 6)
>>> x
9
>>> y
4.5

# Default arguments
def multiply(base=4, multiplier=5):
    print(base * multiplier)

>>> multiply()
20


def show_date(day ,month, year=2017):
    print("Today is ",day,"/",month,"/",year)

show_date(day=15,month=12)


```

#### Function - Documentation
```
# How docstring looks like
def func():
  """This function does nothing for now, but I still document it.
   Really, documentation is very important!"""
   <your code here>

# Full documentation example
def power(base, exponent):
   """Calculates a number raised to a power.
   :param base: base value
   :param exponent: exponent value
   :type base: int
   :type exponent: int
   :return: The result of raising base to the power exponent
   :rtype: int
   """
   return base ** exponent

```

#### Function - main
```
def main():
    <your code here>

if __name__ == "__main__":
    main()

# 'if __name__ == "__main__":'  means to use this function only when executing the main func (Not when import)
```

### List - Practice (Mutable & Dynamic)
```
my_list = [int_obj, string_oboj, bool_obj, ...]

# Create List
empty_list = []
empty_list = list()
fibo_list = [1, 1, 2, 3, 5, 8, 13, 21]
crazy_list = [2, "The Big Bang Theory!", True, 4.6]

# Indexing list
>>> crazy_list
[2, "The Big Bang Theory!", True, 4.6]

>>> crazy_list[0]
2
>>> crazy_list[1]
'The Big Bang Theory!'

# List in list
>>> unique = [["a", "list"], ["of", "lists"]]
>>> unique
[['a', 'list'], ['of', 'lists']]

# List - Indexing
>>> chemical_elements = ["hydrogen", "helium", "lithium", "beryllium"]
>>> chemical_elements[3]
beryllium
>>> chemical_elements[-1]
beryllium
>>> chemical_elements[1:3]
['helium', 'lithium']


# List in list - Indexing
>>> unique[1]
['of', 'lists']
>>> unique[1][0]
'of'
>>> unique[0][1]
'list'

# obj concatenation
>>> chemical_elements = ["hydrogen", "helium", "lithium", "beryllium"]

>>> chemical_elements * 2
['hydrogen', 'helium', 'lithium', 'beryllium', 'hydrogen', 'helium', 'lithium', 'beryllium']

>>> chemical_elements + "boron" # TypeError (Not "str")
>>> chemical_elements += ["boron"]
>>> chemical_elements.append("boron")
['hydrogen', 'helium', 'lithium', 'beryllium', ‘boron']

# obj change
>>> solar_system
["Mercury", "Venus", "Earth", "Mars", "Jupiter", "Saturn", "Uranus", "Neptune"]

>>> solar_system[9] = "Sun" # IndexError
>>> solar_system[8] = "De Novo"
>>> solar_system
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'De Novo']

# obj deletion
>>> solar_system
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'De Novo']

>>> solar_system.remove("De Novo")
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune']

# Is_obj_exists check (obj "in" list)
>>> solar_system
['Mercury', 'Venus', 'Earth', 'Mars', 'Jupiter', 'Saturn', 'Uranus', 'Neptune', 'Sun']
>>> "Earth" in solar_system
True
>>> "Pluto" in solar_system
False

# list's values set to variables
>>> cool_trick = [1, 2, 3]
>>> a, b, c = cool_trick
>>> a
1
>>> c
3

# lenght func
>>> chemical_elements = ["hydrogen", "helium", "lithium", "beryllium"]
>>> len(chemical_elements)
4

# How to Remove Duplicates From a Python List
>>> mylist = ["a", "b", "a", "c", "c"]
>>> mylist = list(dict.fromkeys(mylist))
>>> mylist
['a', 'b', 'c']

```

#### List - Common functions
```
>>> temperatures = [-180, 800, -10, 60, -100, -180, 880, -400]
# reverse
>>> temperatures.reverse()
>>> temperatures
[-400, 880, -180, -100, 60, -10, 800, -180]

# sort
>>> temperatures.sort()
>>> temperatures
[-400, -180, -180, -100, -10, 60, 800, 880]

# count
>>> temperatures.count(-180)
2

# index
>>> temperatures.index(-100)
3

# max(list)
>>> max(temperatures)
880

# min(list)
>>> min(temperatures)
-400

# sum(list)
>>> sum(temperatures)
870

# sorted(list)
>>> sorted(temperatures)
[-400, -180, -180, -100, -10, 60, 800, 880]

# Sorted func with a key value
>>> my_list = ["A", "c", "b", "x", "Z", "i", "G", "J"]  
>>> sorted(my_list)
['A', 'G', 'J', 'Z', 'b', 'c', 'i', 'x']
>>> sorted(my_list, key=str.lower)
['A', 'b', 'c', 'G', 'i', 'J', 'x', 'Z']

>>> products = [('milk', '5.5'), ('candy', '2.5'), ('bread', '9.0')]
>>> print(sorted(products, key=lambda x: x[1],  reverse=True))
[('bread', '9.0'), ('milk', '5.5'), ('candy', '2.5')]

# Join - Print list as a string
print("Your pruduct list is: " + ",".join(products_list))

```

### Loops - Practice
#### While loops
```
# While loop template
while <condition>:
    <do something>


# Normal 'while' loop
>>> i = 0
>>> while i < 5:
. . .    print(i)
. . .    i += 1
. . .
1
2
3
4

# Infinit 'while' loop
while True:
    Pass   # <Keep on working!>


```

#### For loops
```
# For loop template
for <var> in <sequence>:
  <do something>

# Normal for loop
## exaple01
>>> animals = ["Grizzly Bear", "Siberian Husky", "Reindeer"]
for animal in animals:
  print(animal)

Grizzly Bear
Siberian Husky
Reindeer

## exaple02
>>> animal_sounds = [["bear", "roar"], ["dog", "bark"], ["deer", "bellow"]]
>>> for item in animal_sounds:
...     print("The sound a " + item[0] + " makes:\t" + item[1])
...
The sound a bear makes: roar
The sound a dog makes: bark
The sound a deer makes: bellow

## exaple03
>>> for num in range(5):
... print(num)
...
0
1
2
3
4

```

#### Loops - Flow control
```
# Break
while i < 10:
   i += 1
   if i % 2 == 0:
      break
   print(i)
1

# Continue
while i < 10:
   i += 1
   if i % 2 == 0:
      continue
   print(i)
1
3
5
7
9

```

### Advanced variable types
#### Tuple - Immutable 
```
## You can only access its content
>>> salad_ingredients[2] = "spinach" # TypeError
```
#### Best practice for data protection (Cannot be changed) and for law memory usage (Only necessary ram usage). Use it if the data per placement is important!

##### Tuple  - Create new tuple
```
>>> my_first_tuple =()
>>> one_value_tuple = (20,)
>>> friendly_tuple = (2.5, 3, "banana")
>>> sophisticated_tuple = 2, "tomato"

```

##### Tuple common actions
```
>>> milk_info = ("lactose", "11/08/2022", "dairy cows", "135.6 liters", 300)
>>> len(milk_info)
5

>>> milk_info[0]
'lactose'

>>> milk_info[2:]
('dairy cows', '135.6 liters', 300)

>>> str(milk_info[4])+ " "+ milk_info[2]
'300 dairy cows'

>>>for infoin milk_info:
... print("-- " + str(info) + " --")
...
-- lactose --
-- 11/08/2022 --
-- dairy cows --
-- 135.6 liters --
-- 300 --

```

##### Tuple - Special uses
```
## tuple assignment
>>> (food, type, calories) = ("bread", "whole wheat", 80)
>>> food
'bread'
>>> calories
80

# Basic formatting - old style 
## formatting - Sting (%s)
>>> fruit = "grapes"
>>> drink = "wine"

>>> "The basket contains %s and %s." % (fruit, drink)
The basket contains grapes and wine.

## formatting - int (%d)
>>> bottles_num, drink = 3, "wine"

>>> "The basket contains %d bottles of %s." % (bottles_num, drink)
The basket contains 3 bottles of wine.

## formatting - Hybrition of types
>>> basket_content = 3, "wine"
>>> "The basket contains %d bottles of %s." % basket_content
The basket contains 3 bottles of wine.


# Basic formatting - new style

## .format()
## formatting - Sting
>>> fruit = "grapes"
>>> drink = "wine"

>>> "The basket contains {} and {}.".format(fruit, drink)
>>> f"The basket contains {fruit} and {drink}."
The basket contains grapes and wine.

## formatting - int
>>> bottles_num, drink = 3, "wine"

>>> "The basket contains {} bottles of {}.".format(bottles_num, drink)
>>> "The basket contains {0} bottles of {1}.".format(bottles_num, drink)
The basket contains 3 bottles of wine.

>>> a = 5
>>> b = 10
>>> 
>>> f'Five plus ten is {a + b} and not {2 * (a + b)}.'
Five plus ten is 15 and not 30.

## formatting - Hybrition of types
>>> basket_content = 3, "wine"
>>> "The basket contains {} bottles of {}.".format(*basket_content) # Emphasis on an asterisk
>>> f'The basket contains {basket_content[0]} bottles of {basket_content[1]}.'
The basket contains 3 bottles of wine.

```

#### Dictionary(Dict) - Mutable
##### Dictionary(Dict) - Practice

```
# Create new dict
>>> new_dict = {}
>>> another_dict = dict()
>>> type(new_dict)
<class 'dict'>
>>> new_dict
{}

# Set key & value
## key: value
>>> keyboard_shortcuts = {"Copy": "Ctrl + C", "Paste": "Ctrl + V", "Undo": "Ctrl + Z"}
>>> keyboard_shortcuts
{'Copy': 'Ctrl + C', 'Paste': 'Ctrl + V', 'Undo': 'Ctrl + Z'}

# How to access key's value
## dict[key]
>>> keyboard_shortcuts['Copy'] 
'Ctrl + C'

# How to avoid from 'KeyError' message for unexisting key(For example)
>>> if "Cut" in keyboard_shortcuts:
... # <do something>
>>> keyboard_shortcuts['Cut'] 
>>>

# insert new key & value to dict
## dict[key] = value
>>> keyboard_shortcuts
{'Copy': 'Ctrl + C', 'Paste': 'Ctrl + V', 'Undo': 'Ctrl + Z'} >>> keyboard_shortcuts["Cut"] = "Ctrl + X"
>>> keyboard_shortcuts
{'Copy': 'Ctrl + C', 'Paste': 'Ctrl + V', 'Undo': 'Ctrl + Z', 'Cut': 'Ctrl + X'}

# Update key's value
>>> keyboard_shortcuts["Copy"] = "Ctrl + Insert"
>>> keyboard_shortcuts                          
{'Copy': 'Ctrl + Insert', 'Paste': 'Ctrl + V', 'Undo': 'Ctrl + Z'}

# Delete key & value
>>> keyboard_info = {"Company": "Logitech", "Number of keys": 101, "Are emoji included?": True, "Language": "Hebrew"}
>>> keyboard_info
{'Company': 'Logitech', 'Number of keys': 101, 'Are emoji included?': True, 'Language': 'Hebrew'}

## Option1 -- del
>>> del keyboard_info["Number of keys"]
>>> keyboard_info
{'Company': 'Logitech', 'Are emoji included?': True, 'Language': 'Hebrew'}

## Option2 -- pop()
>>> keyboard_info.pop("Company") 
'Logitech'
>>> keyboard_info
{'Number of keys': 101, 'Are emoji included?': True, 'Language': 'Hebrew'}

# View objects methods
## Show keys only - keys() method
>>> keyboard_info
{'Are emoji included?': True, 'Language': 'Hebrew'}
>>> keyboard_info.keys()
dict_keys(['Are emoji included?', 'Language'])

## Show values only - values() - method
>>> keyboard_info
{'Are emoji included?': True, 'Language': 'Hebrew'}
>>> keyboard_info.values()
dict_values([True, 'Hebrew'])

## Show pairs - Key & value - items() method
>>> keyboard_info.items()
dict_items([('Are emoji included?', True), ('Language', 'Hebrew')])

```

### Working with files - txt files
#### Working with files - Read files
```
# Open file
## file_object = open(file, mode) # mode = r/w/rw
>>> spells_input_file = open(r"c:\harry_potter\spells.txt","r") # r"" -- Avoid special marks like "\t"

# close()
>>> spells_input_file = open(r"c:\harry_potter\spells.txt", "r")
>>> # do something with the file
>>> spells_input_file.close()

# With statement - Alternative for close() func
>>> with open(r"c:\harry_potter\spells.txt", "r") as spells_input_file:
>>>    # do something with the file


# Reading a file - all the lines - best practice - for small files only
## read() 
>>> spells_input_file = open("c:\harry_potter\spells.txt", "r")
>>> spells = spells_input_file.read()
>>> spells
"Avada Kedavra: Death\nAberto: Opens objects\nLumos: Creates light from the wand's tip\nObliviate: Erases memories\n"

>>> print(spells)
Avada Kedavra: Death
Aberto: Opens objects
Lumos: Creates light from the wand's tip
Obliviate: Erases memories

## readlines() - return list of the file's content
>>> lines = spells_input_file.readlines()
>>> lines
['Avada Kedavra: Death\n', 'Aberto: Opens objects\n', 'Lumos: Creates light from the wand's tip\n', 'Obliviate: Erases memories']


# Reading a file - line by line - best practice - for medium/big files
## Reading files with for loop 
>>> spells_input_file = open("c:\harry_potter\spells.txt", "r")
>>> for line in spells_input_file
... print(line, end="")
...
Avada Kedavra: Death
Aberto: Opens objects
Lumos: Creates light from the wand's tip
Obliviate: Erases memories

## readline()
>>> line = spells_input_file.readline()
>>> print(line)
Avada Kedavra: Death
>>> line = spells_input_file.readline()
>>> print(line)
Aberto: Opens objects
>>> line = spells_input_file.readline()
>>> print(line)
Lumos: Creates light from the wand’s tip
>>> line = spells_input_file.readline()
>>> print(line)
Obliviate: Erases memories


```

#### Working with files - Write in files
```
# Create new file or Overrite file's content
chat_input_file = open("chat.txt", "w")

## Write func
chat_input_file = open("chat.txt", "w")
chat_input_file.write("Me: Why chat, when you can use an owl?")
chat_input_file.close()


```