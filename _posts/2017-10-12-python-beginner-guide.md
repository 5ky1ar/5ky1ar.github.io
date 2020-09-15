---
title: Python Beginner Guide
layout: post
category: python, coding, tutorial
date: 2017-10-12
---

<p style="text-align:center;"><img src="https://i.imgur.com/dPCbOJ6.png" alt="Python Logo"></p>

---

# Introduction
Python is a interpreted, object-oriented, high-level programming language.  
Python was created by Guido van Rossum and officially released in the year 1991.  
This language is still quite new and is one of the easier languages to learn.  
Another really great thing about python is that unlike many programming languages, it does NOT require a semi-colon(";") at the end of every line.

Despite what most people think you can use Python for alot of different things. For example, you can write python scripts or programs that interact with other computers.  
You can use python to make interactive webpages, and python is even used for well known programs and games.

The reason i created this guide is because the current guides in this subforum are either to limited or outdated.  
In this tutorial i am going to show you the basics of python, and hopefully intrigue you in this amazing language.  

# Getting Started
First of all, if you are going to be using python, you have to install the interpreter first.  
You can download it from the official python website [here](https://www.python.org/downloads/).  
I recommend you download and install Python, since Python 2.7.11 is outdated.  

If you want to write your own Python programs, you need to use an IDE (**I**ntegrated **D**evelopment **E**nvironment)  
There are a lot of different IDE's for python, personally i prefer PyCharm.

If you are not yet familiar with python, i recommend you use JetBrains PyCharm Edu, which you can download for free [here](https://www.jetbrains.com/pycharm-edu/download/).  
This version of PyCharm offers you a diversity of tutorials, aswell as extra help features.

If you are familiar with python already, i recommend you use JetBrains Pycharm Community Edition, which you can download for free [here](https://www.jetbrains.com/pycharm/download).  
This version of PyCharm offers you alot more plugins and features.

In python you can add a comment to your code using the hash symbol ('#').  
Example:
```python
#This is a comment!
```

If you wish to have multiple lines of comments, you can enclose the lines of comments using the double quote symbol 3 times.  
Example:
```python
"""
These
Are
Multiple
Lines
Of
Comments
"""
```

Comments will always be ignored by the interpreter and are usually used to add some notes to a part of the code.

# Variables
In python, variables are what you use to store values.  
The three most important variables in python are:  

## Integer
An integer (int) is a variable where you can store a number that can be written without a fractional component.  
Example:
```python
a = 100.42
b = -50.99
c = 0.000
```

## String
An string is a variable where you can store characters if you enclose them in quotes.  
Python treats single quotes the same as double quotes.  
Example:  
```python
a = "Hello"
b = "World"
c = "!"
```

# Operators
Python has a lot of different operators, such as *mathematicial operators* and *comparison(logical) operators*.  

## +
This operator adds the value's on both sides of the operator.  
Example:  
```python
a + b = 20
```

## -
This operator substracts the value on the right side of the operator from the value on the left side of the operator.  
Example:  
```python
a - b = 10
```

## *
This operator multiplies the values of on both sides of the operator.  
Example:  
```python
a * b = 100
```

## /
This operator divides the value on the right side of the operator by the value on the left side of the operator.  
Example:  
```python
a / b = 1
```

## %
This operator divides the value on the right side of the operator by the value on the left side of the operator and returns the remainder.  
Example:  
```python
a % b = 0
```

Here is a list of some of the *comparison operators* python uses.  
These are the operators you will be using when you are working with while statements and for loops etc.  

## ==
If the value of both operands are equal, then the condition becomes true.  
Example:  
```python
if a == b:
    print("a is equal to b")
```

## !=
If the value of both operands are not equal, then the condition becomes true.  
Example:  
```python
if a != b:
    print("a is not equal to b")
```

## >
If the value of the left operand is greater then the value of the right operand, then the condition becomes true.   
Example:   
```python
if a > b:
    print("a is bigger then b")
```

## <
If the value of the left operand is less then the value of the right operand, then the condition becomes true.  
Example:  
```python
if a < b:
    print("a is smaller then b")
```

## >=
If the value of the left operand is equal to or bigger then the value of the right operand, then the condition becomes true.  
Example:  
```python
if a >= b:
    print("a is equal or bigger then b")
```

## <=
If the value of the left operand is equal or less then the value of the right operand, then the condition becomes true.  
Example:  
```python
if a <= b:
    print("a is equal or smaller then b")
```

# Logical Statements
Logical statements are *also known as if/else statements*.  
They are statements that check whether the conditions are true or false.  
In these statements we are going to use the comparison operators we just discussed.  

A common mistake i made when i started out with Python was forgetting to add the ':' after the If statement line.  
Don't forget to add this, if you don't the statement won't work and you will get an _error_.  

Example:  
```python
a = 10
b = 10

if a == b:
    print("a is equal to b")
else:
    print("a is not equal to b")
```

If you run this code it will print "a is equal to b", because both variables are 10.

Example of a slightly more complicated if statement:  
```python
a = 10
b = 10
c = 20
isittrue = True

if a == c:
    isittrue = True
elif a == b:
    isittrue = True
else:
    print("A is not equal to b or c")
    isittrue = False

if a == b or a == c:
    isittrue = True
else:
    print("A is not equal to b or c")
    isittrue = False

if a == b and isittrue == True:
    c = c - b
    print(c)
```

The first If statement checks if a is equal to c or if a is equal to b. Since a is equal to b, the variable isittrue will be set to True.  
While this is a correct code, programmers are lazy people and always strive to make their code as short as possible.  
That's why the second If statement checks exactly the same as the first if statement, but uses the or operator instead.  
This way the or operator saves 2 lines of code, which in this case shouldn't matter alot, but if you are coding a big program, efficient coding will save you alot of time.

The third If statement checks if a is equal to b and if the variable isittrue is set on True.  
If this is both the case (which it is), c will be set to be c - b.  
Basicly what happens is the variable c is now 20 - 10.  
After that the print statement will show 10 as the new value of the variable c.  

# Lists
Lists are a very important part of python.  
A list is a variable that holds multiple values. A list in Python is similar to an array in Java.  
You can declare a list the same as any other variable, except that it needs to be enclosed with brackets ("[]") and seperated with commas(",").  

It's very important to remember that lists work with positions.  
The first position is always 0, NOT 1  

Example:  
```python
list = ["One", "Two", "Three"]
print (list)
print(list[0])
print(list[1])
print(list[2])
```

When you run this code, you will get this output:  
```python
["One", "Two", "Three"]
One
Two
Three
```

You might wonder what just happened, well:  
Print (list) tells python to print everything that is in the list, which is why the commas and brackets get printed aswell.  
Print (list[0] tells python to print the first variable in the variables list.  
Print (list[1] tells python to print the second variable in the variables list.  
Print (list[2] tells python to print the third variable in the variables list.  

You might wonder why or how this could be usefull. I will get back to that later in this guide.  

# Loops
In Python there are several kinds of loops.  
Right now we will discuss the two most important ones.  

## While Loop
This is one of the easiest and most basic loops of python. What a while loop does, is perfor a series of events as long as something is in a certain condition.  
With the while loop you also need to add the colon sign after the line (':')  

Example:  
```python
a = 5

while a > 0:
    print (a)
    a = a - 1
print("We are out of the loop!")
```

As you can see first we declare a variable, and then the while loop checks if the variable is bigger then 0.  
This while loop will keep running the events within it until a is equal to 0.  
So your output will be:  
```python
5
4
3
2
1
We are out of the loop!
```

You can use all comparison operators in a while loop to get the result you want.  

## For Loop
The for loop is slightly more complex then the while loop, but it's still perfectly understandable.  
The for loop executes a sequence of statements multiple times.  
With the while loop you also need to add the colon sign after the line (':')  

Let me explain this loop with an example.  
```python
for x in range(5):
    print (x)
```

If you run this code your output will be:  
```python
0
1
2
3
4
```

The for loop goes through every item in a list before it can exit the loop.  
In this example "x" is a variable. It does not have a set value, because it's used to run the for loop.  

In simple terms: for x in a list with a range of 5, print x

Now you might be wondering, why does it stop at 4, when we said range 5?  
You have to remember, that a for loop works with lists, and as mentioned before, the first position of a list is 0.  

# Functions
Functions are very important when you are coding a program or script.  
A function is in simple terms a specific piece of code.  
A function is very efficient when you need to run a function multiple times, for example in a loop.  

Here a simple example of a define:  
```python
def definitionname():
    print("This is my define.")
definitionname()
```

The "def" is how you start the definition. After that you put in a unique name for your definition. This can be anything you like.  
With the define you also need to add the colon sign after the line (':')  

If you want to run the code within the define, you can call it by typing the name of the function with parameters ("()")  
The output for the code above would be: This is my define.  

As mentioned before a function is especially efficient when you want to run the code in the function multiple times.

For example:  
```python
def multipletimes():
    print ("My very first define.")

for x in range(5):
    multipletimes()
```

When you run this code your output will be:  
```python
My very first define.
My very first define.
My very first define.
My very first define.
My very first define.
```

This is a very simple example, but you can already see how efficient it is.  
This way the print statement is executed 5 times, with only 4 lines of code.  
When you are coding a complex program or script defines will make your job a lot easier!  

# Modules
Modules are python programs that you can use.  
These mudules are scripts written by another person in order for you to be able to make a fairly complex script/program, without extensive knowledge about the functions you are using.  

To be able to use a module, you first have to import it. You can simply do this by typing 'import' and the Python module name.

For example:   
```python
import time
```

Time is a basic Python module that is included in the standard python package you downloaded at the start of this article.  
You are now able to use this module.  

A simple example of how you can use the time module:  
```python
import time
seconds = time.time()

print("number of seconds since 10:00am, January 1 1970:", seconds)
```

When you run this code the output will be something like:  
number of ticks since 10:00am, January 1 1970: 1457813005.3186388

You are probably thinking: How can i know every single module name and every statement within a module?  
The answer to that is simple. Google what you need! For example, if you want to make a running clock, you can google: Python clock.  

In the results you will most likely find a site such as stackoverflow. On this site it will probably tell you that in order for you to make a clock in python, you need to import the time module. 

# Global Variables
At last I want to explain what global variables are and what you can use them for.  
First of all, try to avoid global variables as much as possible! With big scripts it would get really messy really quick.  

That being said, a global variable is a normal variable, not unlike the normal variables we discussed earlier in this article.  
The difference between normal variables and global variables is that global variables are being used within loops and statements.  

For Example:  
```python
x = 10

def normalx():
    x = 5
normalx()

print (x)

def globalx():
    global x
    x = 20
globalx()

print (x)
```

In this example we declare the variable x as 10.  
Then we run the function normalx, and after the function has been ran we print x.  
Then we run the function globalx, and after the function has been ran we print x again.  

When you run this code your output will be:  
```python
10
20
```

The reason for this is that in the first define, x is not called as the global x.  
In the second define we do call x as global x, which is why the global x variable has been changed from 10 to 20.  

# Final Words
Congratulations! You have finished this python tutorial!  
Right now you know the basics of Python.  

Right now you are thinking: Hmm alright it was fun and all, but what do i do now with my knowledge?  
Simple! Practice with Python. You can code a variety of programs and scripts, from a logger to an email bomber to battlefield 2.  

Of course coding in python still requires some effort.  

Cheers guys, Happy programming! 🤝 


