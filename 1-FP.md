
# Functional programming

Certainly, one of the first hurdles, if not the first, is the paradigm of programming Haskell embraces: **Functional programming** at its core means building programs by uniquely applying functions to arguments. A python user, for example, has the *for* and *while* constructs and cannot live without them. In contrast, functional programming encourages to use the **recursion**.

To illustrate both those sides, consider how differently this simple task is faced: for a list of numbers, write a function that returns the sum of its elements. A python user, for example, finds natural to write this
```python
# There is a variable initialized as 0
# which is incremented at every step of
# of a for-loop. 
def sum(xs):
  s = 0
  for x in xs:
    s = s+x
  return s
```
On the other hand, a functional programmer loves recursion. It's a strict position: functional application and recursion are the *right* manner for doing things.
```haskell
-- Something mathematical here.
sum [] = 0
sum (x:xs) = x + sum xs
```
A *seasoned* functional programmer seeks brevity, too.
```haskell
-- A point-free definition here.
sum = foldl (+) 0 
```

## A quick glance at Haskell

In Haskell, things have **types**, that is *labels* attached to objects that convey their nature. For instance, ```1``` is an ```integer```, ```"hello"``` is a ```string```, the process that takes a natural number and returns it successor is a ```function from natural numbers to natural numbers```. It's better to have some notation for that: we write
```haskell
x :: T
```
to mean that the thing ```x``` has type ```T```. As we said earlier, functions have the type of functions, so that we write
```haskell
f :: X -> Y
```
to say that ```f``` is a function that takes inputs of type ```X``` and outputs things having type ```Y```.

