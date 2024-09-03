# Beyond the Basic Stuff with Python

Beyond the basics covers topics such as

- Dealing with errors
- Code Formatting with Black
- Choosing Understandable Names
- How to find Code Smells
- Writing Pythonic Code
- Common Gotchas
- Oddities with Python
- How to write functions effectively
- OOP

## Dealing with Errors

- tracebacks or stack traces detail where errors happened
- They don't always point to the exact line but they do give a general area

```python
def a():
  b()
def b():
  c()
def c():
  4/0


a()
```

- this would lead to

```python
Traceback (most recent call last):
  File "abcTraceback.py", line 9, in <module>
    a() # Call a().
  File "abcTraceback.py", line 2, in a
    b() # Call b().
  File "abcTraceback.py", line 6, in b
    c() # Call c().
  File "abcTraceback.py", line 7 in c
    4/0 # This will cause a zero divide error.
  ZeroDividionError: division by zero
```

- The first two lines are the frame summary and they show the information inside a frame object
- the local variable data and where in the code to return after the fuction call are stored in the frame object

## Code Smells

- source code pattern that signals potential bugs
- Common Code smells
  - Duplicate Code
  - Magic Numbers
  - Dead Code / Commented-out code
  - print statements used for debugging
  - Classes that should have been functions
  - List comprehensions inside List comprehensions

## Programming Jargon

- Literal: text in source code for a fixed typed out value. `2` or `Josh`
- Mutable: If you can change the objects value.

```python
data = {}
data["id"] = 1
```

- Immutable: You cannot change the value. Strings or primative types. a 1 will always be a 1.
- Containers: object of any data type that can house multiple types
- Sequence: object of any container data type that is ordered
- mapping: object of key / value pairs
- Callable: any object that implements `__call__`
- Funtions are first class objects meaning you can assign them attributes just like a class or any other object
- Statement / Expressions: Statement does not evaluate to a value. Expressions evaluates to a single value

## Pythonic Code

- use dictionaries instead of multiple if statements or switch statements
- Choose Ternary only when its simple conditions otherwise write out the if / else conditions
