The "thread" function in "main.py" seeks to implement the basic behaviour of the Lisp
threading macro in Python. The function takes a value as the initial parameter and then
passes the value to a series of unary functions that transform the value.

The "thread" function also allows you to use prefix mathematical notation functions, with
the passed value acting as the initial parameter.

# Examples of Usage

```python
thread(100, lambda x: x / 2.25, (round, 2))
# result: returns 44.44

thread('MAKE THIS LOWER CASE', lambda x: x.lower(), print)
# result: prints string 'make this lower case'

thread(100,
       ('/', 2, 6, 8),
       ('+', 100.55),
       (round, 4),
       print)
# result: prints 101.5917
```
