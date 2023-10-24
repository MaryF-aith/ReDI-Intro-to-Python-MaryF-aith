
# Lists and Dictionaries


![python gif](https://media.giphy.com/media/KAq5w47R9rmTuvWOWa/giphy.gif)

## Pre Requisites

None for today!

---

## Class Curriculum

| Section content                             | Expected time (mins) | Pre - Requirements |
| ------------------------------------------- | -------------------- | ------------------ |
| Check-in and questions from last class      | 5 minutes            | ❌                 |
| Lesson Goals                                | 5 minutes            | ❌                 |
| Python Overview                             | 15 minutes           | ❌                 |
| List, Dictionary, Boolean, Conditions       | 45-60 minutes        | ❌                 |
| Break                                       | 10 minutes           | ❌                 |
| Break out , pair-programming                | 15-30 minutes        | ❌                 |
| Check-out                                   | 5 minutes            | ❌                 |

<!--## 1. Recap
→ Data Types we have learned about so far are Strings, Numbers, Booleans, Lists and Dictionaries


```python
# Strings
"Hello World" # 'Hello World' (double or single quotation marks)
# Numbers
1
1.5
# Booleans
True
False
# Lists
[1, 2, 3]
['Hello', 'World']
# Dictionaries
{'name': 'John', 'age': 30}
```

→ we usually store data in variables through the use of the = operator (therefore called assignment operator) -->

```python
# Assign a value to a variable
name = 'John'
# Print the value of the variable
print(name)
# Print the type of the variable
print(type(name))
```



## 2. Goal for today

→ Get more comfortable with Python basics.

→ If-else statements

<!-- ## 3. Exercises 

Go to this [link](https://github.com/hannah-eichelsdoerfer/python_practice) to get todays exercises - clone the repository.

1. Open the folder called "Exercises" and start working on the challenges in the `strings.py` file.
2. Continue working on the challenges in the `lists.py` file.
3. Move on to working on the challenges in the `dictionaries.py` file. -->

#### List
Lists are one of the more complex Python data types. Lists hold other data types like strings, integers, floats, and even lists. Each list item has an index, like strings. The index starts from 0. Just as with strings, the `len` function also gives you the length of a list. Also like strings, you can slice a list, which means to get some part of the overall list. Here are some examples to illustrate this:

 ```python
  x = ["apple", "banana", "cherry"]
  print(x)
  #thislist = list(("apple", "banana", "cherry")) # note the double round-brackets
  #print(thislist)
  print(type(x))

  x[0] #first item of the list

  mylist=list(('apple','banana',"cherry"))
  mylist

  type(mylist)
  ```


  ```python
  l1 = [1, 5, 0, 4]  # create a list
  print(l1)
  l1.sort()          # sort the list
  print(l1)
  l1.append('a')     # add an element
  print(l1)
  del l1[2]          # remove an element
  print(l1)
  print(len(l1))     # length of the list
  print('The first element is', l1[1])
  empty_list = []    # create an empty list
  print(len(empty_list))
  # create a list from range: [0-10)
  l2 = list(range(10))
  print(l2)
  # create a list from range: [5-10)
  l3 = list(range(5, 10))
  print(l3)
  ```

  ```python
  #Copy a list
  original_list = list(range(1, 6))
  print(original_list)
  new_list = original_list.copy()
  new_list[2] = 128
  print(original_list)
  print(new_list)
  ```

  ```python
  original_list = list(range(1, 6))
  print(original_list)
  new_list = original_list
  new_list[2] = 128
  print(original_list)
  print(new_list)
  ```

  ```python
# creating some lists 
fruits = ['apple','banana','orange']
stuff = [12, 'asdf', 123.013, [1,2,3]]

# here's the indexing 
fruits = ['apple','banana','orange']
#            0        1        2
# like strings, lists can also use negative indexing
fruits = ['apple','banana','orange']
#           -3       -2        -1
# get the length of the list
print(len(fruits))
# outputs: 3# slice a list
print(fruits[:2])
# outputs: ['apple', 'banana']
print(fruits[1:3])
# outputs: ['banana', 'orange']
  ```
#### Dictionary

  Dictionaries are a Python data structure. While lists allow you to create ordered collections of values, dictionaries allow you to create collections of key / value pairs. An analogy for a dictionary is a telephone book: you can look up a telephone number (value) by a person's name (key).

  Here are some dictionary examples:

  ```python
  x = {"name" : "John", "age" : 36}
  print(x)
  
  x["name"]

  x["age"]

  print(x.get('age'))

  # update value
  x['age'] = 27
  print(x)

  # add item
  x['gender'] = 'Male'
  print(x)
```

  ```py
  empty_dict = dict()
  dog = { 'name': 'Roger' }
  # assign the value: 8 to the key: 'age'
  dog['age'] = 8
  # the dog dictionary now looks like: { 'name': 'Roger', 'age': 8 }

  # access a value by a key
  dog['name']
  # outputs: 'Roger'
  ```

  Dictionaries also contain the `.keys()`, `.values()`, and `.items()` methods which return iterables (like lists) of these values:

  ```py
  list(dog.keys())
  # outputs: ['name', 'age']
  list(dog.values())
  # outputs: ['Roger', 8]
  list(dog.items())
  # outputs: [('name', 'Roger'), ('age', 8)]
  ```

    
#### Boolean


  Booleans may only be one of two values: `True` or `False`. These are like on-off switches, where True is on and False is off. These states are mutually exclusive -- a condition can only be either `True` or `False` but not both. You can use the `not` keyword to "flip the switch" of the boolean value.


  ```python
  #Boolean
  x = True
  type(x)
  ```
  ```py
  val1 = True
  val2 = not True
  print(val2)
  # outputs: False
  ```

  - What does the `==` symbol mean? What about `!=`?

  `==` is "equals", `!=` is "does not equal".

  - `==`: equality operator: compares two values and returns True if they're equivalent or False if they are not
  - `!=`: inequality operator: opposite of equality, returns True if two values are not equivalent and False if they are

  - What is the difference between `=` and `==`?

  `=` is for assigning some value to a variable, while `==` is for testing for equality between the two sides.

  - `>`: greater than operator: returns True if the left side is greater than the right side and False if not
  - `<`: less than operator: returns True if the left side is less than the right side and False if not



## Extra resources and references from class

- [Python playground](https://trinket.io/python/f7ad7f9864)
- [Silent Teacher exercise from class](https://hourofcode.com/toxicodepython)
- [Python foundation docs](https://www.python.org/doc/essays/blurb/)
- [Python - Tyr it yourself](https://www.w3schools.com/python/)
- [List of some open source Python projects](https://data-flair.training/blogs/python-open-source-projects/)