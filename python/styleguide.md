# Style Guide

Python provides a [Style Guide](https://www.python.org/dev/peps/pep-0008/#code-lay-out) which details all the requirements and recommendations for writting Python code.

The creator of Python, Guido van Rossum, noted: 

    "code is read more often than it is written, so readability counts" 
    
Python is one of the few languages that has an official style guide. This is due to the fact that there is tons of Python code out there and the core of the language is readability. 

I describe just the basics of this style below. As you continue to produce Python code, I recommend familiarizing yourself with the official style guide (PEP-8) to help your fellow researchers, scientists, and engineers in reading your code! 


Tim Peters, a long time "Pythoneer" channeled the guiding principles for Python's design into 19 recorded aphorisms. 

```python
import this 
```
    The Zen of Python, by Tim Peters

    Beautiful is better than ugly.
    Explicit is better than implicit.
    Simple is better than complex.
    Complex is better than complicated.
    Flat is better than nested.
    Sparse is better than dense.
    Readability counts.
    Special cases aren't special enough to break the rules.
    Although practicality beats purity.
    Errors should never pass silently.
    Unless explicitly silenced.
    In the face of ambiguity, refuse the temptation to guess.
    There should be one-- and preferably only one --obvious way to do it.
    Although that way may not be obvious at first unless you're Dutch.
    Now is better than never.
    Although never is often better than *right* now.
    If the implementation is hard to explain, it's a bad idea.
    If the implementation is easy to explain, it may be a good idea.
    Namespaces are one honking great idea -- let's do more of those!

## Indentation

For many languages, the indentation of the code is for asthetic purposes only, however with Python the indentation is highly important. 
Python uses indentation to indicate blocks of code. 

### For Example:

```python
if patient_age < 18:
    print("Child")
else:
    print("Adult")
```  

Python will give you a Syntax error if you try to type the code in like this: 
```python
if patient_age < 18:
print("Child")
else:
print("Adult")
```

When you do indentations, it is recommended to use spaces. **Use 4 spaces per indentation level.**


## Comments
Commenting your code is helpful for your future reference, as well as for others reading your code. 

```python
# This is an example of a block comment. 
# It spans multiple lines. 
# Each line starts with a # and a single space. 

print("Above is a block comment") # this is an inline comment
```
