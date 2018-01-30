# Haskell Notes
## Introduction
Haskell is a purely functional programming language.In purely functional programming you don't tell the computer what to do as such but rather you tell it what stuff is.So in purely functional languages, a function has no side-effects. The only thing a function can do is calculate something and return it as a result.

**Referential transparency** If a function is called twice with the same parameters, it's guaranteed to return the same result.

#### Haskell is lazy
That means that unless specifically told otherwise, Haskell won't execute functions and calculate things until it's really forced to show you a result. That goes well with referential transparency and it allows you to think of programs as a series of transformations on data.

Say you have an immutable list of numbers `xs = [1,2,3,4,5,6,7,8]` and a function `doubleMe`. In Java `doubleMe(doubleMe(doubleMe(xs)))` will first multiply each number by 2 and will return a new list then again new list. But, in Haskell each number is multiplied one by one. So, innermost `doubleMe` will multiple 1 by 2 and then second `doubleMe` will multiply 2 by 2 and then outermost `doubleMe` will multiply 4 by 2.

Haskell is statically typed. When you compile your program, the compiler knows which piece of code is a number, which is a string and so on. 

If a function takes two parameters, we can also call it as an infix function by surrounding it with backticks.

#### Baby's first functions

```haskell
doubleMe x = x + x 
```

The difference between Haskell's if statement and if statements in imperative languages is that the else part is mandatory in Haskell.
in Haskell every expression and function must return something

the `'` at the end of the function name. That apostrophe doesn't have any special meaning in Haskell's syntax. It's a valid character to use in a function name. We usually use ' to either denote a strict version of a function (one that isn't lazy) or a slightly modified version of a function or a variable.

functions can't begin with uppercase letters. 

When a function doesn't take any parameters, we usually say it's a definition 

#### An intro to lists
In Haskell, lists are a homogenous data structure. 
